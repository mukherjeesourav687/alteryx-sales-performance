# Validation record

## Original Alteryx workflow

The enhanced cloud workflow completed successfully on 12 October 2026, job 4784772. All five outputs reported Success in the Jobs page.

Design previews reported zero warnings, errors and conversion errors. The Filter reported 50 accepted records and zero rejected records. Unique reported 50 unique records and zero duplicate records. The product summary generated five groups, the month summary five groups, and the regional summary four groups. Append Columns generated five product records from five target records and one grand-total source record.

## Independent reference outputs

The results/ CSVs were reproduced locally from exactly the five named monthly source files. They are reference calculations, not downloaded copies of the cloud job's output files. Their records and totals were compared with the Alteryx preview tables.

- Every summary reconciles to 253 units and 1,467,300 sales value.
- Product units match the original product quantity summary: Mouse 102, Keyboard 55, Headphones 53, Monitor 26, Laptop 17.
- Monthly values: January 268,600; February 277,650; March 366,700; April 272,950; May 281,400.
- Regional values: North 454,800; South 390,600; West 343,550; East 278,350.
- Product sales-value and unit shares sum to 100% within floating-point tolerance. CSV formatting and final floating-point digits may differ from Alteryx.

## Public workflow definition

The copied JSON was parsed, all node IDs were checked for uniqueness, and every connection endpoint was checked against the saved node IDs. The public definition contains 32 nodes and 25 connections. Workspace-specific input/output bindings and sampled metadata were removed. Calculation expressions and the processing graph are preserved.

The public copy has not been executed in a second workspace. It requires dataset and output reconnection. The source data are clean; synthetic invalid-input test cases and production testing have not been added.
