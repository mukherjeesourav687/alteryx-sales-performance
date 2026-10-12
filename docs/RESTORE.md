# Restoring the Alteryx canvas

The JSON file in workflow/ uses the native canvas clipboard structure: nodes, connections, and workflowMode. It contains all 32 saved nodes (25 tools and 7 comments) and 25 connections.

Copy the entire JSON text, click an empty Standard-mode Designer Cloud canvas, and paste with Ctrl+V. Do not upload this file through the Library native-workflow importer. Dataset bindings, storage paths and sampled metadata from the owner's workspace are absent from the public copy.

## Input mapping

| Input tool | Month | CSV |
|---|---|---|
| 1 | January 2026 | data/sales_january.csv |
| 2 | February 2026 | data/sales_february.csv |
| 3 | March 2026 | data/sales_march.csv |
| 4 | April 2026 | data/sales_april.csv |
| 5 | May 2026 | data/sales_may.csv |

Tool numbers may be reassigned if pasting into a nonempty canvas, so prefer an empty workflow and match the month labels.

Upload the five CSVs to your workspace and select each corresponding dataset in its Input Data tool. Keep Union configured to match column names.

## Output mapping

- Invalid records: sales_invalid_records.csv
- Duplicate OrderID review: sales_duplicate_review.csv
- Product leaderboard and shares: product_performance.csv
- Month totals: monthly_performance.csv
- Region totals: regional_performance.csv

Choose a destination you own for each output. Create New preserves prior runs by appending an incremental filename when needed.

## Verification after reconnecting

The source has 50 records. All 50 pass the validation filter and are unique by OrderID. Product, monthly and regional outputs each total 253 units and 1,467,300 sales value. Each share column in the product output should sum to 100% within rounding tolerance.

The original connected workflow completed successfully. This public copy preserves its calculation and connection structure, but a run in a new workspace is pending your input/output reconnection.
