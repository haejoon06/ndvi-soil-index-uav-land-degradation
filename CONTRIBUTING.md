# Contributing

Contributions that improve reproducibility, documentation, portability, or validation are welcome.

## Before opening a change

1. Do not commit raw UAV imagery, model checkpoints, generated tiles, credentials, or restricted metadata.
2. Keep scene-level train/validation/test separation intact.
3. Clearly distinguish pseudo-label agreement from independent field-ground-truth accuracy.
4. Record dependency or threshold changes that can affect reported results.
5. Add a concise explanation and verification evidence to the pull request.

## Notebook changes

- Make changes in `notebooks/Penelitian_V2_clean.ipynb`.
- Clear transient outputs before committing unless the output is necessary evidence.
- Keep the executed reference notebook unchanged unless a complete rerun has been performed.
- Export compact result tables to `results/` when results change.

## Suggested validation

- Confirm all notebook cells parse as valid Python/IPython.
- Check that the clean notebook contains no embedded credentials or machine-specific absolute paths.
- Verify reported metrics against the exported CSV files.
- Confirm the manuscript and README describe the same model configuration and limitations.

