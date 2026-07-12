# kf-asset-tagger — Claude Code Instructions

## Workflow

**Edit locally → push to GitHub → user runs on Colab → check outputs → repeat.**

All notebook changes go through `/tmp/gen_notebook.py`. Never edit the `.ipynb` directly.
After changing `gen_notebook.py`, always run `python3 /tmp/gen_notebook.py` to regenerate the notebook.

## Before every code change

Always present this table BEFORE touching any file:

| # | Bug | Root cause | Fix |
|---|-----|-----------|-----|
| 1 | ... | ...       | ... |

Wait for the user to approve ("yes go ahead", "go ahead", "do it", etc.) before making changes.

## After every code change

After pushing to GitHub, always end with:

**Hit Run all on Colab:**
https://colab.research.google.com/github/innersmoke/kf-asset-tagger/blob/main/kf_asset_tagger.ipynb

(User clicks "Run anyway" on the warning dialog themselves — browser automation cannot dismiss it.)

## Key files

- `/tmp/gen_notebook.py` — master notebook generator
- `/Users/siva/Downloads/kf-asset-tagger/kf_asset_tagger.ipynb` — generated notebook (do not edit directly)
- GitHub: https://github.com/innersmoke/kf-asset-tagger
- Colab: https://colab.research.google.com/github/innersmoke/kf-asset-tagger/blob/main/kf_asset_tagger.ipynb

## Colab environment

- Runtime: T4 GPU (15.64 GB VRAM)
- Model: Qwen2-VL-2B-Instruct (float16)
- Browser automation can open the tab but cannot dismiss the "Leave site?" or "Run anyway" dialogs — always tell the user to click through manually
