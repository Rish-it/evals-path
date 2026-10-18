# Evals Path

A borderless, two-tab learning tracker for applied AI and evaluation engineering. Includes an interactive resource audit and hiring-requirement matrix.

## Run locally

```sh
python3 -m http.server 8787
```

Open http://localhost:8787/. No build or package installation is needed.

## Curriculum

43 chapters, 9 sections, approximately 302 hours. The original 39 chapter IDs are unchanged; four production applied-AI chapters were appended. Resources were reviewed on 17 October 2026, and recommendations were applied on 18 October 2026.

- `index.html`: tracker with locally saved progress, chapter resources, scores, and JSON export/import.
- `curriculum.json`: readable copy of the curriculum embedded in the tracker.
- `audit.html`: 151-resource audit and hiring alignment.
- `AUDIT.md`: written analysis, methodology, role examples and limitations.
- `data/`: resource scores and job alignment CSVs.

The audit describes the original 39-chapter snapshot. New recommendations and replacement URLs are explicitly unrated in the tracker rather than inheriting scores from different resources. Hiring data is a dated snapshot, not a live job feed.

## Progress and moving from localhost

Progress stays in browser localStorage. Existing localhost completions remain intact. On the old tracker use **export progress**, then **import progress** on the deployed site. Import merges valid chapter completions into existing progress. The older **copy** JSON export is accepted too. Progress is not sent to GitHub.

## Validate

```sh
node scripts/check.cjs
```

Browser checks also cover completing/undoing chapters, two-tab navigation, syllabus filters, resource scores, legacy progress imports and mobile overflow.

## Deployment

GitHub Pages serves `main` from the repository root. `.nojekyll` keeps the site static. No secrets, credentials, personal progress, raw scraped job descriptions or downloaded transcripts are published.

A private source repository does not automatically make the Pages website private. Private-repository Pages availability depends on the GitHub account plan.
