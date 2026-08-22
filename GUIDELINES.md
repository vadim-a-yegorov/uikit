
## GUIDELINES

---

Every interactive element must satisfy the Interaction rules below before you consider it done for each screen. If a layer is not applicable to a given element, state "N/A because <reason>" explicitly.

INTERACTION (apply to every list row, card, node, cell, or widget):

Beginning professionals implement only the primary path and silently skip the rest. This document exists for professionals to make that skipping visible and non-optional.

1. Primary action — one default action.
2. Secondary actions — a right-click/context menu with every state-valid
   non-primary action, not just "Edit/Delete."
3. Manipulation — drag/resize/reorder affordances wherever the data model
   supports reordering, nesting, or transfer between collections. Invalid
   drop targets must reject the drag DURING the drag with a visible reason,
   not after release.
4. Disclosure — a hover tooltip (delayed trigger, not instant) that adds
   information beyond the visible label: state, constraints, or context.
5. Reversibility — undo, preview-before-DO, or explicit confirmation
   for any destructive or multi-record mutation.

Also define for every element: empty, loading, partial, error, and
no-permission states.

 - Interaction Layers

    Actionable elements in a control panel exist in five layers simultaneously. An element that only implements Layer 1 is a CRUD, not a control.

      | Layer | Question it answers | Minimum requirement |
        |---|---|---|
        | 1. Primary action | What does clicking/tapping do? | One unambiguous default action per element |
        | 2. Secondary actions | What else can be done to this element without navigating away? | A context (right-click / long-press) menu exposing every non-primary action applicable to the element's current state |
        | 3. Manipulation | Can the element's position, size, order, or grouping be changed directly? | Drag, resize, or reorder affordances wherever the underlying data model supports reordering/regrouping — not just "add/edit/delete" |
        | 4. Disclosure | How does the user learn what an element is/does without leaving their task? | Hover tooltip (or long-press-hold on touch) explaining meaning, constraints, and current state — not just the label repeated |
        | 5. Reversibility | What happens when the user acts wrongly, or wants to act experimentally? | Every destructive or structural action must be undoable, previewable, or confirmable before commit |

    A component that satisfies only Layers 1 is a **CRUD form**. A component that satisfies all five is a **control surface**. This kit is about building control surfaces.


- Checklist (per interactive element)

    Apply this checklist to every list row, card, node, cell, or panel widget before considering it shippable.

    - Primary click/tap action defined and reachable via keyboard.
    - Right-click / context-menu populated with all state-valid secondary actions (not "Delete" alone).
    - Drag affordance present if the element belongs to any orderable, nestable, or transferable collection (rows in a table, cards in a board, nodes in a tree, columns, panels).
    - Drop targets are visually and functionally distinguishable from non-drop zones, and invalid drop targets reject the drag *during* the drag, not after release.
    - Multi-select behavior defined (shift-range, ctrl/cmd-toggle) if the element belongs to a collection where bulk operations make sense.
    - Tooltip or inline disclosure defined, triggered on hover with a deliberate delay (not instant) and dismissible without a click.
    - Keyboard equivalent exists for every mouse-only gesture (drag-drop needs a keyboard reorder path; right-click needs a menu key or shift+F10-equivalent).
    - Undo/redo or explicit confirm-before-commit exists for any action that mutates more than one record or is not trivially reversible.
    - Empty, loading, partial, error, and "no permission" states are all defined for the element — not just the happy-path populated state.
    - Density-appropriate variant exists (see DENSITY AND DETAILNESS) — the same control must degrade gracefully at higher information density without losing any of the above behaviors.

- Anti-Patterns

    | Anti-Pattern | What | Why happens |
    |---|---|---|
    | CRUD-only surface | Add/Edit/Delete buttons, no drag, no right-click | Fastest to ship, matches tutorial-level examples |
    | Silent drag | Drag works but no visual drop-target feedback, no invalid-drop rejection | Feedback states are "extra" work with no PM ticket |
    | Tooltip-as-label | Tooltip repeats the visible label instead of adding information | Nobody defines *what* the tooltip should disclose |
    | Irreversible bulk action | Multi-select delete/move with no undo, no confirm | Undo requires state history design, deferred indefinitely |
    | Mouse-only interaction | Drag-drop or right-click with zero keyboard path | Accessibility treated as compliance checkbox, not core spec |
    | Density collapse | Compact/dense view removes the right-click menu or drag handle entirely instead of adapting its trigger | Dense layouts are designed visually first, behaviorally never |

- Done

    An interactive element is "done" only when every row in Section 2 has an explicit answer — including "N/A because X" — recorded in the component's spec, not left implicit. "It works when I click it" is not a definition of done.


VISUAL LANGUAGE:
- [DESIGN.md]. If that file is empty or missing values you need, stop and ask rather than choosing defaults.


REFERENCE, TEMPLATE, FRAMEWORK:

- Provenance model — three layers, three altitudes. Each layer supplies only what the
  layers below it lack. Tokens are the floor of Layer 0, not its ceiling.

  | Layer | Source | Supplies |
  |---|---|---|
  | 0 — Foundation | IBM Carbon v11 via `flutter_carbon` (fork, not dependency) | Token architecture, 4-theme system, shell anatomy, grid/spacing/motion math, 48-component primitive vocabulary, accessibility baseline |
  | 1 — Enterprise application model | SAP Fiori (Horizon) / Fundamental Styles | Floorplans, message handling as a system, object semantics, table personalization, variant management, value help |
  | 2 — Craft techniques | Flexport UX (Coyle et al.) | Data table technique, validation timing, form internationalization, operator-first patterns, standardization governance |

- Stacking rule. Layer 1 components are built from Layer 0 primitives + [DESIGN.md]
  tokens only. Layer 2 techniques are applied to Layer 0/1 components, never replace
  their structure. Where two layers cover the same capability, the lower layer wins
  unless an override is recorded here. Recorded overrides:
  - Table column customization is implemented only through the p13n dialog
    (Layer 1 absorbs the Layer 2 technique).

- Reuse hierarchy: adopt → map → extend → invent. Exhaust each step before moving to
  the next. Inventing what a reference already covers is a defect.

- Provenance halt conditions (in addition to the VISUAL LANGUAGE):
  - The output is Layer 0's surface with Layer 1/2 styling mixed in.
  - You cannot name what a reference adds beyond the layers below it.
  - You are about to invent something the coverage matrix marks as covered.

- Token boundary. Colors, themes, fonts, icon assets, spacing and density values live
  in [DESIGN.md]. This includes the token-vendor decision: Carbon theme set vs SAP
  Horizon theme set (via `@sap-theming/theming-base-content`, mapped
  quadrant-for-quadrant) — a wholesale per-build-target swap, never a blend within a
  surface. Components consume tokens; nothing in this section hardcodes a value.

- Coverage matrix — who covers what:

  | Capability | L0 Carbon | L1 SAP | L2 Flexport | Take from |
  |---|---|---|---|---|
  | Token architecture, themes, grid/spacing/motion | ✅ | ✅ equivalent | — | L0 |
  | Primitive components (button, input, modal, toast, tabs, tree…) | ✅ 48 | partial overlap | — | L0 |
  | App shell | ✅ structure | ✅ normative contents | — | L0 structure + L1 contents |
  | Floorplans (page-type compositions) | ✖ | ✅ | partial | L1 |
  | Message handling (field-linked) | ✖ notifications only | ✅ | partial | L1 system + L2 timing |
  | Object semantics (status, draft, lock) | ✖ | ✅ | — | L1 |
  | Table personalization, saved variants | ✖ | ✅ | technique-level | L1 |
  | Value help (coded-value pickers) | ✖ | ✅ | — | L1 |
  | Data table interaction technique | basic | partial | ✅ | L2 |
  | Validation timing, error copy | basic states | containers | ✅ | L2 |
  | Form internationalization | ✖ | ✖ | ✅ | L2 |
  | Operator-first product patterns | ✖ | partial | ✅ | L2 |

- Foundation adoption (`flutter_carbon`):
  - No restyling outside the token layer. Behavior and accessibility fixes are allowed
    and recorded in the fork changelog.
  - Strip unused components; re-import from the pin if needed later.
  - Kept vocabulary: themes + token system (color/layering, type scale, spacing
    scale, motion); `CarbonUIShell` + `CarbonPageHeader`; breadcrumb, pagination,
    tree view, tabs; structured list, themed DataTable, contained list; modal family,
    side panel, tearsheet, popover, toggle tip, overflow menu; dropdown, combo box,
    multi-select, number input, toggle, file uploader, themed pickers; notifications,
    loading, skeletons.
  - The 12 upstream-omitted components stay omitted unless the build list below
    re-adds them as Layer 1 items.

- SAP-derived build list — components Carbon lacks. Each is a mapping, not an
  invention: spec source is the Fundamental Styles / Fiori element of the same name,
  primitives come from the fork, values come from [DESIGN.md](DESIGN.md). P0 = first operator
  console, P1 = first expansion.

  | # | Component | What it is | Fork basis | Priority |
  |---|---|---|---|---|
  | 1 | Shell Bar | Always-visible top bar: back nav, title, search, notifications, AI slot, product switcher, user menu | `CarbonUIShell` header | P0 |
  | 2 | Vertical Navigation | Grouped 2-level tree nav, icon-only collapsed mode | `CarbonUIShell` side + `CarbonTreeView` | P0 |
  | 3 | Dynamic Page | Header collapses on scroll; pinned summary; anchor bar | `CarbonPageHeader` + scroll behavior | P0 |
  | 4 | Object Page | One entity = one page: header facets, sections, anchor nav, global edit mode with Save/Cancel | composition | P0 |
  | 5 | Flexible Column Layout | list → detail → detail-detail; max 3 columns; defined ratios; per-column full-screen toggle | composition over shell | P1 |
  | 6 | Worklist / List Report floorplan | Filter bar + table + variant management + create action | composition | P0 |
  | 7 | Wizard | Stepped conditional flow, branching, per-step validation | composition | P1 |
  | 8 | Message Strip | Inline semantic message, dismissible | `CarbonNotification` inline | P0 |
  | 9 | Message Box | Modal confirmation with expandable details list | `CarbonModal` | P0 |
  | 10 | Message Page | Full-page error/empty with illustrated message slot | composition | P0 |
  | 11 | Message Popover | Field-linked validation message list, severity-segmented, click-to-focus field | `CarbonPopover` + `CarbonToggleTip` | P0 |
  | 12 | Message model | Messages as first-class objects with target-field references, separate from data state | pattern, not widget | P0 |
  | 13 | Object Status | Semantic state badge (positive/critical/negative/neutral/informative) | themed tag/chip | P0 |
  | 14 | Object Identifier | Title + stable key line; the entity identity block | composition | P0 |
  | 15 | Object Number | Number + unit, right-aligned, tabular numerals | text style rule | P0 |
  | 16 | Draft / Lock indicators | "Draft", "Locked by {user}", "Unsaved changes" badges with disclosure | tag + tooltip | P1 |
  | 17 | Responsive Table | Row-based, growing or paginated, row actions | themed DataTable + `CarbonPagination` | P0 |
  | 18 | Analytical (grid) Table | ALV-style: fixed header, column resize/reorder, grouping, aggregation rows | DataTable extended | P1 |
  | 19 | Tree Table | Hierarchy column + data columns; depth limits below | `CarbonTreeView` + grid fusion | P1 |
  | 20 | Personalization dialog (p13n) | Column show/hide/reorder, sort, filter as a standard dialog | `CarbonModal` + `CarbonSidePanel` | P0 |
  | 21 | Variant Management | Saved views per user per table; "Standard" default; dirty marker on modified view | `CarbonDropdown` + persistence | P1 |
  | 22 | Value Help Dialog | Searchable picker for coded values; tokenized output | `CarbonModal` + `CarbonMultiSelect` | P1 |
  | 23 | Multi-Input with tokens | Tokenized multi-value field fed by typing or value help | `CarbonMultiSelect` pattern | P1 |
  | 24 | Busy Indicator | Local (component) and global (shell) busy states | `CarbonLoading` | P0 |
  | 25 | Illustrated Message | Normative empty/error/no-permission compositions (page, panel, dialog slots) | composition | P0 |

- Flexport craft rules (Layer 2), applied to the components above:

  - Data:
    - Fixed header on every scrollable table.
    - Horizontal scroll only when column comparison is the primary task; otherwise
      resolve overflow through the on-demand tier (per DENSITY AND DETAILNESS).
    - Resizable columns, widths persisted per user per table.
    - Row style: line divisions at compact density; zebra optional at cozy; free-form
      forbidden on manipulation surfaces.
    - Footer summary: visible/total count plus aggregation of the filtered set where
      numeric.
    - Pagination for operator consoles (stable position, jump-to-page); growing
      ("load more") for casual-review lists. Decided once per entity.
    - Hover actions mirror the row's context menu exactly — hover is a shortcut,
      never the only path.
    - Inline editing follows the validation sequencing below and commits per-cell
      with undo.
    - Expandable rows are the on-demand tier mechanism.
    - Quick view = side panel peek, one level maximum.
    - Modal drill hard-capped at 2; the second level may only be a Message Box or
      Value Help, never another record form.
    - Row → details navigates to the entity's Object Page permalink.
    - Sort persisted per user per table (feeds Variant Management).
    - Filter bar on operator surfaces; per-column and searchable columns on
      analytical tables.
    - Alignment: text left, numbers right, dates left; headers follow their column's
      data; comparison columns use tabular numerals.
    - Row detail ledger (usually-unmentioned details, non-optional): hover state,
      selected state, focus ring, keyboard navigation, context menu, drag handle
      when orderable, inline-edit affordance, row-level error badge,
      permission-disabled action state, per-row loading skeleton, stale-data
      indicator.

  - Validation:
    - Default: validate on blur.
    - On focus: never show errors; helper text allowed.
    - As-you-type: forbidden except password strength and availability checks.
    - At character requirement: fixed-length formats only; forbidden for
      locale-variable formats (postal codes, phone numbers).
    - On pause: acceptable for async checks; show field-local busy state.
    - After a field's first error: re-validate on every change until valid; the error
      clears the moment the entry becomes valid.
    - On submit: invalid fields join the Message Popover list, focus moves to the
      first invalid field, a Message Strip summarizes the count.
    - Error copy = what is wrong + how to fix it. "Invalid value" alone is a defect.
    - Placement below the field; tooltips may duplicate, never replace.
    - Never clear a valid entry because a sibling field or the submit failed.

  - Form internationalization:
    - Country known → changing format: country selector first, fields reformat on
      selection.
    - Country unknown → generic unstructured inputs; do not fake structure.
    - State/Province/Region and postal code are optional globally.
    - Preferred when an address service exists: autocomplete first, then restructure
      to the country's format and pre-fill; user edits after.
    - Field structure communicates format only when the format is certain.
    - Layouts survive ~40% label-length growth without truncating Identifying or
      Operational fields.
    - Locale-driven forms are data-driven schemas; no hardcoded per-country layouts.

  - Operator-first product patterns:
    - Exception-first surfaces: lead with what needs attention, not everything that
      exists.
    - Every entity has a stable permalink, deep-linkable from notifications,
      messages, and other records.
    - User-defined reference fields (PO, SKU, tags): searchable, filterable,
      reportable — first-class, not a notes field.
    - A single explicit priority flag: searchable, filterable, reportable.
    - Watchlists replace offline notes.
    - Enter-once reuse across documents and forms; pre-fill rate is a measured
      quality metric.
    - Design each workflow for the chain of adjacent roles that touch it, not one
      primary persona with accommodations.
    - Three-view system for geospatial/temporal entities: map (where), list (pivot
      to action), object page (single source of truth). The list is the default
      working view.

- Context menu composition:
  - Order: primary action → state-valid verbs → transfer group (move/copy/assign) →
    inspect group (details, permalink, activity) → separator → danger group last.
  - State-invalid actions are hidden, except where visibility teaches the model —
    then disabled with a stated reason.
  - Right-click menu, overflow menu, and hover actions expose the identical set.
    Divergence is a defect.
  - Destructive entries carry the reversibility path in the label when non-obvious
    ("Delete — undo available").

- Drag-and-drop foundations:
  - Drag handle on every orderable item; at compact density it may collapse to a
    row-start hover affordance, but the keyboard reorder path remains.
  - During the drag: valid targets highlight; invalid targets show a rejection
    cursor plus an inline reason naming the violated constraint ("Cannot nest under
    a child", "Target is read-only").
  - Auto-scroll containers when dragging near edges.
  - Multi-select drag moves the selection as one undo unit.
  - Touch: long-press initiates; identical validity feedback.

- Keyboard parity (in addition to the INTERACTION keyboard-equivalents):

  | Mouse gesture | Keyboard equivalent |
  |---|---|
  | Right-click | Menu key / Shift+F10 |
  | Drag & drop | Cut/paste (Ctrl+X/V) or modifier+arrow reorder |
  | Hover disclosure | Focus triggers the same disclosure |
  | Column/panel resize | Resize command on the focused splitter |
  | Row hover actions | Tab to row, then context menu |

- Undo:
  - Workspace-level command stack; bulk mutations are one undo unit.
  - Destructive single-record actions: toast with Undo window when restoration is
    cheap; Message Box confirmation when it is not.
  - Structural/layout changes: preview or instant undo — never confirmation dialogs
    for layout experimentation.

- State:

  | State | Standard pattern |
  |---|---|
  | Empty | Illustrated Message + the primary creation action in place; never a blank region |
  | Loading | Initial load: skeleton matching the final layout. Mutation: local Busy Indicator. Never spinners inside table cells — skeleton rows |
  | Partial | Last-good data + freshness timestamp + indicator naming the failed region + scoped retry; never blank the whole element over one failed source |
  | Error | Inline: Message Strip with retry. Full-surface: Message Page. Correlation ID when backend-bound |
  | No-permission | Navigation entries the user can never use: hidden. Actions on visible entities: disabled + tooltip naming the missing permission. Absence is explained, never silent |

- Density (in addition to the DENSITY & DETAILNESS):

  These are not to be a user-switch, but a permanent decision per screen.

  | Tier | Carbon mechanism | SAP name | Use |
  |---|---|---|---|
  | Compact | Data table compact/condensed sizes | Compact | Mouse+keyboard, continuous use |
  | Cozy | Data table default sizes | Cozy | Touch, accessibility preference, casual review |

  Row heights, paddings, and type sizes at each tier are [DESIGN.md](DESIGN.md) values.

- Tree-table depth limits:
  - Load expanded to level 1 only.
  - Soft cap: 3 simultaneously expanded levels per branch. Hard cap: 5.
  - Beyond the cap, hand off to the entity's Object Page — never deeper nesting.
  - Children lazy-load on expand, rendered as skeletons.
  - No tree tables on small/touch surfaces; use a drill-down list instead
    (Fiori guidance).
  - Per-entity cap overrides are recorded in that entity's spec with a reason.

- Collection:
  - Header checkbox selects the visible page, with an explicit "select all N"
    escalation.
  - Bulk action bar appears on selection and lists the affected count.
  - Pagination vs growing is decided once per entity and consistent on every surface
    showing that entity.

- Sources:

  | Source | Layer |
  |---|---|
  | IBM Carbon v11 / `pub.dev/packages/flutter_carbon` (Apache-2.0) | Layer 0 foundation, fork base |
  | SAP Fundamental Styles (`github.com/SAP/fundamental-styles`, Storybook) | Build-list component specs, reference HTML/ARIA contract |
  | `@sap-theming/theming-base-content` | Vendor-B tokens, Horizon themes, SAP icon fonts (via [DESIGN.md](DESIGN.md)) |
  | SAP Fiori guidelines (`experience.sap.com/fiori-design-web`) | Floorplans, message handling, object semantics, tree-table guidance |
  | Flexport UX — "Design better data tables" | Data table rules |
  | Flexport UX — "Forms Need Validation" | Validation sequencing |
  | Flexport UX — "Form Internationalization Techniques" | Form i18n |
  | Flexport UX — "Operating System for Global Trade"; andrewcoyle.com/flexport; Platform 2.0 launch post | Operator-first patterns, governance |

  Reuse as much as possbile of existing framework(s), invent as less as possible, STILL ALIGN WITH [DESIGN.md](DESIGN.md).

DENSITY AND DETAILNESS:
- Density (how much fits on screen) and detailness (how deep you can go
  per item) are separate decisions. Default posture for this product:
  deep, not wide — prefer nested/expandable disclosure over adding columns
  or requiring horizontal scroll.
- Set density once per application/workspace, never mixed between
  screens.
- Always-visible fields = Identifying + Operational only. Contextual and
  Diagnostic fields go in a one-click-reachable expanded/nested tier —
  never deleted from the UI, never requiring page navigation.
- This product's density/detailness decisions are recorded in
  [DESIGN.md](DESIGN.md). Read it before generating layout code.
  If it is not yet filled, ask me to fill it before proceeding rather than
  guessing.

- Two independent axes. Density and detailness are frequently conflated. Separate them explicitly.

  | Axis | Definition | Controls |
  |---|---|---|
  | Density | How many discrete data points/rows/cells are visible per unit of screen area at once | Row height, cell padding, font size, whether secondary metadata is inline or hidden |
  | Detailness | How much depth of information/action is available per single data point once you engage with it | Number of visible columns/fields, presence of nested rows, drill-in levels, action count exposed |

  An entity can be simultaneously high-density and low-detail (e.g., a compact list with only IDs) or low-density and high-detail (e.g., one expanded record card with 40 fields), work should default toward **high density AND high detail**.


- Density

  Answer these in order for each screen or entity.

  * **Input device**: Is the primary input mouse+keyboard, touch, or both? Touch requires larger hit targets; mouse+keyboard permits tighter packing. (SAP's own model ties density directly to input device — touch defaults to a looser mode, mouse/keyboard defaults to a tighter one.)
  * **Task frequency**: Is this screen used continuously for hours (operator console) or occasionally (settings page)? Continuous-use screens should default to the tightest density the input device allows.
  * **Row/record count at steady state**: If typical data volume exceeds ~30 visible rows, default to the tightest density; if it's consistently under ~10, density can relax without hurting scanability.
  * **Never mix densities in one hierarchy.** Set density once at the application or workspace root, not per-widget — mixed density inside a single view is a defect, not a style choice.
  * **Provide exactly one user override**, applied globally, persisted per user — not per screen. Users who need scanability choose loose; users who need throughput choose tight.


- Detailness

  Answer these per data entity, not per screen.

  * **Identify the entity's full field set** — every field that exists in the underlying data model for this entity, regardless of whether it will be shown.
  * **Classify each field**: Identifying (must always be visible), Operational (needed to decide an action), Contextual (useful but not decision-critical), Diagnostic (only needed when something is wrong).
  * **Always-visible tier** = Identifying + Operational fields only. This is what shows at rest, at any density.
  * **On-demand tier** = Contextual + Diagnostic fields. These must be reachable via a single interaction (expand row, hover disclosure, right-click "Details").
  * **Depth over breadth rule**: when a screen has more fields than fit at the chosen density, prefer adding a nested/expandable level (deeper) over adding another column that forces horizontal scroll or a wider viewport (wider).
  * **Every on-demand tier must still satisfy the full Interaction rules**.


- Density/detailness

  |  | Density | Detailness |  |
  |---|---|---|---|
  | Operator console (continuous use, mouse/keyboard, 100+ rows) | Tightest available | Always-visible = Identifying + Operational only; everything else on-demand, nested | Maximize throughput, minimize scroll, never sacrifice reachable depth |
  | Supervisor review panel (occasional, mixed input) | Medium | Always-visible = Identifying + Operational + top 1 Contextual field | Balance scan speed with enough context to avoid an extra click |
  | Configuration/settings panel (rare use) | Loosest acceptable | All relevant fields visible at once, minimal on-demand tier | Correctness and discoverability matter more than throughput here |

- Anti-patterns

  * Treating whitespace-heavy cards as the default for screens — that pattern belongs to observation surfaces, not manipulation surfaces.
  * Hiding operational fields behind a click to "look clean" — operational fields must always be visible regardless of density.

REFRENCES:

- [references/atlas.svg](references/interactions.svg)
- [references/interactions.svg](references/interactions.svg)

Before writing code for a new element, restate back to me:  \
(a) which of the 5 Interaction Contract layers apply and how,  \
(b) the density/detailness tier this element inherits,  \
(c) which fields are always-visible vs on-demand.

Tool use prioritzied:
- clarify
- create_task