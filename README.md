## Week 7: Testing, Refinement and End-to-End Validation

In Week 7 I tested the Week 6 dashboard, fixed the problems I found, and retested it. I kept the same dataset (the HealthConnect Rwanda database) and built on the Week 6 work.

### Files added (folder: `Week7`)

| File | Description |
|---|---|
| Analytics Testing and Refinement Report | Testing approach, KPI validation, issues, fixes, retests, updated insights and recommendations |
| Week 7 Project Summary | Short summary of what was tested, changed and still open |
| `HealthConnect_Week7_Testing_Record.xlsx` | Testing record, issue log and validated findings |
| Before and after screenshots | Evidence for each fix |
| Updated dashboard (`.pbix`) and PDF | Refined version of the Week 6 dashboard |

### How the testing was done

- Every main KPI was recalculated from the original CSV files and compared with the dashboard.
- Each page was checked for charts that should split by hospital, rankings that should be sorted, truncated values and blank categories.
- Slicers, drill-through, the tooltip and bookmarks were tested against known expected results.
- Key conclusions were rechecked across insurers, months and hospitals.

### Results

- The first round recorded 39 checks: 24 passed, 7 failed and 8 were not yet tested.
- Retesting found 2 more issues. After refinement, all checks passed. The cross-track test is still outstanding.
- Every KPI matched the source data. The failures were display and structure problems, not calculation errors.

### Main fixes

- Facility matrix and bed chart repeated the same totals for every hospital. Fixed by using the correct facility field.
- Bed utilization measure returned 100% for a blank row. Rewrote the measure.
- Department ranking was alphabetical. Sorted it by average satisfaction.
- Cards hid filtered values because of display units. Changed the units.
- Truncated revenue card, cut-off revenue trend and a meaningless total row were corrected.

### Validated findings

- Claim approval stays between 49.3% and 50.9% across all insurers.
- Emergency share stays between 30.1% and 36.5% in every month.
- Bill status does not match payments, and comments contradict ratings, so payment amounts and ratings are the reliable measures.
- Hospital satisfaction rankings rest on 72 to 102 records per hospital, so they should be read with caution.

### Limitations

The Week 6 dataset has no attendance or no-show field, so attendance findings could not be reassessed. Only 5,000 of 60,000 bills and diagnoses link to appointments.
