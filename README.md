[README.md](https://github.com/user-attachments/files/24460941/README.md)
# ReStep Footwear — Business Plan (Pakistan)
Option A: Auto-generate DOCX via GitHub Actions (45–55 pages, 30–35% visuals)

This repository includes:
- A Python generator (`generate_restep_docx.py`) that creates a 45–55 page DOCX report with embedded charts and visuals (targeting 30–35% visual content).
- A GitHub Actions workflow (`.github/workflows/generate-docx.yml`) to run the generator in CI, push the output to a branch `docx-report`, and upload the DOCX as an artifact.

## What you’ll get
- `ReStep_Footwear_Business_Plan_Pakistan_Final.docx` generated on demand.
- The DOCX will be automatically pushed to the `docx-report` branch.
- A downloadable artifact named `ReStepFootwearDOCX` in the Actions run.

---

## Quick Start (Option A)
1) Add files to your repo (commit to default branch):
- `requirements.txt`
- `generate_restep_docx.py`
- `.github/workflows/generate-docx.yml`

2) In GitHub:
- Go to your repository → Actions tab.
- Click the workflow named “Generate Business Report DOCX”.
- Click “Run workflow” to trigger (it uses `workflow_dispatch`, so you can run it manually).

3) After the run completes:
- Check the `docx-report` branch — the file `ReStep_Footwear_Business_Plan_Pakistan_Final.docx` will be added.
- Download the artifact `ReStepFootwearDOCX` from the run if you prefer direct download.

4) Optional:
- Open a Pull Request from `docx-report` into your main branch to merge the DOCX file and any changes.

---

## How it works
- The workflow installs Python 3.11 and dependencies from `requirements.txt`.
- It runs `generate_restep_docx.py` to produce the DOCX and several charts.
- It creates or updates the `docx-report` branch and commits the DOCX there.
- It uploads the DOCX as an Action artifact for easy download.

---

## Adjusting visuals and page count
- Visual density: ~30–35% is targeted via multiple figures and exhibits.
- Page count: ~45–55 pages (Word pagination may vary by system and font settings).
- To adjust:
  - Increase/decrease `FIG_SCALE` in the script to change figure size.
  - Add/remove figures (search for “Visual Exhibits” block in the script).
  - Edit paragraph text lengths to tune page count.

---

## Troubleshooting
- Workflow permissions: The workflow sets `permissions: contents: write` to allow branch updates.
- If the workflow fails to push:
  - Ensure Actions are enabled in repository settings.
  - Make sure branch protection doesn’t block pushes to `docx-report`.
- Dependencies:
  - The runner installs packages listed in `requirements.txt`. If a package version conflicts, try updating the versions.

---

## Files in this setup
- `requirements.txt`: Python package dependencies.
- `generate_restep_docx.py`: Generator script with charts and doc structure.
- `.github/workflows/generate-docx.yml`: GitHub Actions workflow to run the script and push output.

---

## License and usage
- Content and generator are provided for academic/business planning. Customize as needed.
- Replace assumed metrics with your real data to improve accuracy.
