# CloudJobs Open Datasets

Machine-readable datasets on the cloud computing job market, aggregated from
[CloudJobs](https://cloudjobs.io) — a live job board tracking cloud, DevOps, SRE,
and platform-engineering roles across AWS, Azure, GCP, Kubernetes, and adjacent stacks.

**~11,000 live job postings · ~550 hiring companies · salaries normalized to annual USD**

## Datasets

| File | Rows | Contents |
|------|------|----------|
| `data/cloudjobs-market-overview.csv` | 1 | Point-in-time snapshot: total jobs, companies, median/avg salary, remote split |
| `data/cloudjobs-certifications.csv` | ~40 | Job count and average salary per certification (AWS, Azure, GCP, Kubernetes, CompTIA, CISSP…) |
| `data/cloudjobs-technologies.csv` | ~20 | Job count and average salary per technology |
| `data/cloudjobs-companies.csv` | ~550 | Per-company role counts, remote/hybrid/onsite mix, salary min/median/max |
| `data/cloudjobs-locations.csv` | ~2,000 | Role counts and average salary by location |
| `data/cloudjobs-jobs.csv` | ~11,000 | The full live postings feed: title, company, location, remote flag, salary range, technologies, certifications, posted date, canonical URL |

## Versions and update cadence

| Source | Changes? | Use it for |
|--------|----------|------------|
| **[Releases](https://github.com/johnmehler/cloudjobs-datasets/releases)** (`vYYYY.MM`) | **Never.** A new immutable snapshot is published on the 1st of every month. | Research, papers, reproducible analysis, citations |
| `data/` on `main` | Replaced by each monthly snapshot | Browsing the latest snapshot |
| Live feed: `https://cloudjobs.io/datasets/files/<dataset>.csv` (or `.json`) | Yes - reflects current listings and changes continuously | Dashboards, exploration, current data |

Snapshot assets have permanent URLs, e.g.
`https://github.com/johnmehler/cloudjobs-datasets/releases/download/v2026.11/cloudjobs-jobs.csv`.
Each snapshot is also published as a new version on
[Kaggle](https://www.kaggle.com/datasets/johnmehler/cloudjobs-cloud-job-market).
**Always cite the snapshot version you used.**

The same data is queryable interactively through the
[CloudJobs MCP server](https://cloudjobs.io/mcp) and documented at
[cloudjobs.io/datasets](https://cloudjobs.io/datasets) and
[cloudjobs.io/methodology](https://cloudjobs.io/methodology).

### Notes on the data

- Each snapshot is a point-in-time view of *open* roles, not a historical series; stitch monthly snapshots for trends.
- `certifications.csv` has an `in_catalog` column: `false` rows are raw free-text mentions in postings that do not match a certification CloudJobs tracks.
- Locations are as written by employers (semicolon-separated in the raw feed), not normalized to a gazetteer.
- Salaries are annualized USD and only present for postings that list a range.

## License

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — use and redistribute
freely with attribution to **CloudJobs (https://cloudjobs.io)**.

## Citation

Cite the version you used (replace `2026.11`):

```bibtex
@misc{cloudjobs2026,
  author  = {CloudJobs},
  title   = {CloudJobs Open Datasets: Cloud Job Market Data},
  version = {2026.11},
  year    = {2026},
  url     = {https://cloudjobs.io/datasets}
}
```
