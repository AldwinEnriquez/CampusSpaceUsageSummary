# Campus Space Usage Summary

A small reproducible project that summarizes observed use of synthetic
campus study spaces. Given a CSV of study-space records, the analysis
script prints a short summary of capacity, occupancy, and the busiest
observed space.

## Data

The records are **synthetic teaching data** — they do not describe real
campus spaces or real usage. The tracked sample lives at:

    data/sample/campus_spaces.csv

## Repository structure
- `scripts/` — source code for the analysis.
- `data/sample/` — the tracked synthetic sample used by the script.
- `docs/` — project documentation, including the data dictionary.
- `outputs/` — generated results. This directory is gitignored and its
  contents are not committed.

## Requirements

- R 4.6.1 (the version this project was tested with).
- No additional R packages are required; the script uses base R only.

## How to run

Run the script from the **repository root**, passing the sample CSV as
its single argument:

    Rscript scripts/summarize_spaces.R data/sample/campus_spaces.csv

Running it from any other directory may cause the script to fail to
find the input file.

## Expected result

A successful run prints a summary containing, among other values:

- Rows: 12
- Total seats: 278
- Occupied seats: 214
- Available seats: 64
- Occupancy rate: 77.0%
- Busiest observed space: S103

## Outputs

The script prints its summary to the terminal. It does **not** write a
result file, so nothing is created under `outputs/` by a normal run.

## Notes

- Local scratch files (`local_notes.txt`, `analysis_run.log`) and R
  session files are intentionally not tracked.

