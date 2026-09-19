# Dual-Layer Edge Intelligence for Secure Real-Time Medical IoT — Profiling Code

Supplementary code and execution logs supporting the resource-profiling
experiments reported in Section 5.2 (Table V) and Section 5.3 (Table VII)
of the manuscript, provided in response to Reviewer 1, Comment 4.

## Contents

- `AI_healthcare.ipynb` — Isolation Forest labeling and Healthcare AI
  (HGB) training pipeline on MIMIC-IV waveform data. Outputs preserved.
- `Combined_IDS_Pipeline.ipynb` — Security AI (soft-voting ensemble)
  training pipeline on CICIDS-2017. Outputs preserved.
- `Updated_code_file_with_improvement.ipynb` — Real hardware profiling
  run: downloads 194 real patient records from PhysioNet MIMIC-IV
  Waveform Database, trains all five candidate Healthcare AI classifiers,
  and measures throughput and per-sample latency under sustained
  inference. Executed on Google Colab (CPU runtime). Outputs preserved,
  corresponding to Table V in the manuscript.
- `screenshots/` — Execution logs showing the real MIMIC-IV data download
  (198 patient folders, 194 numeric files retrieved from PhysioNet) and
  the Colab runtime environment.
- `findings.pdf` — Summary report of the profiling results.

## Data source

MIMIC-IV Waveform Database v0.1.0, PhysioNet (open access, ODbL v1.0):
https://physionet.org/content/mimic4wdb/0.1.0/

## Note on resource metrics

CPU utilization, memory, and energy consumption were instrumented but
not reliably captured at this scale, since batch inference completed in
4–20 ms, faster than standard OS-level sampling resolution. This is
documented as a measurement limitation in Section 5.3 and Section 7.1
of the manuscript.
