# Weekly Class Time Table — Assignment 03

## Dataset Overview
A 10-column semantic HTML5 schedule representing the **B.Tech Computer Science Weekly Class Time Table (Monday – Friday)**[cite: 1]. It organizes daily periods, time slots, lecture subjects (`Train-X`, `Chemistry`, `Math-I`, `Electrical`, `ED`), 2-hour practical labs (`E.D lab`, `Chemistry Lab`, `Electrical Lab`), classroom/lab allocations, and weekly session hours[cite: 1].

## Semantic Table Structure
- `<caption>`: Provides an accessible title describing the B.Tech CSE Weekly Class Time Table dataset.
- `<thead>`: Contains a two-tier header structure grouping columns into *Schedule & Timing*, *Weekly Lectures & Labs*, and *Session Summary*.
- `<tbody>`: Houses all 6 daily periods along with a full-width lunch recess row.
- `<tfoot>`: Summarizes total daily sessions and overall weekly hours (`30 Hrs`).
- `scope` Attributes: Uses `scope="colgroup"` on grouped top headers, `scope="col"` on individual column headers, `scope="rowgroup"` on shift headers, and `scope="row"` on period and footer labels for screen-reader accessibility.

## Complex Cell Merging (`colspan` & `rowspan`)
- **`colspan` Usage:**
  - **Grouped Top Headers (`<thead>`):** Merged with `colspan="3"`, `colspan="5"`, and `colspan="2"` across the 10-column grid.
  - **Common Training Sessions (`<tbody>`):** Merged across all 5 weekdays (`colspan="5"`) for `9:00 - 10:00` and `10:00 - 11:00` `Train-X` blocks[cite: 1].
  - **Lunch Break Banner (`<tbody>`):** Spans the entire table width (`colspan="10"`).
  - **Summary Label (`<tfoot>`):** Merges the first 3 columns (`colspan="3"`) for the *Total Weekly Sessions* label.
- **`rowspan` Usage:**
  - **Shift Categories:** `Morning Shift` and `Afternoon Shift` each span 3 consecutive rows (`rowspan="3"`).
  - **2-Hour Laboratory Sessions:** `E.D lab` (Wednesday) and `Chemistry Lab` (Monday) each span 2 consecutive period rows (`rowspan="2"`)[cite: 1].

## CSS Custom Properties (`:root`)
All visual styling in `style.css` is controlled through `:root` variables:
- **Colors:** `--color-bg`, `--color-surface`, `--color-primary`, `--color-primary-sub`, `--color-footer-bg`, `--color-break-bg`, `--color-stripe`, `--color-hover`, `--color-border`, `--color-text`, `--color-text-light`, and `--color-text-muted`.
- **Spacing:** `--space-page`, `--space-cell`, and `--space-caption`.
- **Typography:** `--font-family`, `--font-size-base`, `--font-size-title`, `--font-size-caption`, and `--font-size-header`.

## How to View
1. Open `assignment-03/index.html` in any web browser or launch it via VS Code **Live Server**.