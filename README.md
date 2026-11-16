# CloudJobs Open Datasets

Machine-readable datasets on the cloud computing job market, aggregated daily from
[CloudJobs](https://cloudjobs.io) — a live job board tracking cloud, DevOps, SRE,
and platform-engineering roles across AWS, Azure, GCP, Kubernetes, and adjacent stacks.

**~11,000 live job postings · ~550 hiring companies · salaries normalized to annual USD**

## Datasets

| File | Rows | Contents |
|------|------|----------|
| `data/cloudjobs-market-overview.csv` | 1 | Daily snapshot: total jobs, companies, median/avg salary, remote split |
| `data/cloudjobs-certifications.csv` | ~40 | Job count and average salary per certification (AWS, Azure, GCP, Kubernetes, CompTIA, CISSP…) |
| `data/cloudjobs-technologies.csv` | ~20 | Job count and average salary per technology |
| `data/cloudjobs-companies.csv` | ~550 | Per-company role counts, remote/hybrid/onsite mix, salary min/median/max |
| `data/cloudjobs-locations.csv` | ~2,000 | Role counts and average salary by location |
| `data/cloudjobs-jobs.csv` | ~11,000 | The full live postings feed: title, company, location, remote flag, salary range, technologies, certifications, posted date, canonical URL |

## Update cadence

Files are refreshed daily via GitHub Actions from the canonical endpoints:

```
https://cloudjobs.io/datasets/files/<dataset>.csv
https://cloudjobs.io/datasets/files/<dataset>.json
```

The same data is queryable interactively through the
[CloudJobs MCP server](https://cloudjobs.io/mcp) and documented at
[cloudjobs.io/datasets](https://cloudjobs.io/datasets) and
[cloudjobs.io/methodology](https://cloudjobs.io/methodology).

## License

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — use and redistribute
freely with attribution to **CloudJobs (https://cloudjobs.io)**.

## Citation

```bibtex
@misc{cloudjobs2026,
  author  = {CloudJobs},
  title   = {CloudJobs Open Datasets: Cloud Job Market Data},
  year    = {2026},
  url     = {https://cloudjobs.io/datasets}
}
```
