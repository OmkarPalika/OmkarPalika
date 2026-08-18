# Omkar Palika

I build things that check whether other things actually work. Usually that means a
benchmark, and usually the interesting result is that the number everyone trusts was
measuring something else.

Based in Visakhapatnam.

### pgvector filtered-recall lab

[pgvector-filtered-recall](https://github.com/OmkarPalika/pgvector-filtered-recall) —
what happens to pgvector's HNSW recall when you add a `WHERE` clause. 1M vectors,
PostgreSQL 17, 45 configurations, ground truth from an exact scan inside the same
database.

The finding: under a filter that correlates with the embedding, a tenant, a category,
a date range, pgvector can return **zero rows and report success**. No error, no
warning, 683ms. `iterative_scan` does not fix that case. A btree on the filter column
does, in 3.6ms.

Also in there: why `ef_search` is inert once iterative scan is on, where the planner
flips from HNSW to an exact plan and what moves that threshold, and what the official
mitigation costs under concurrency (2.2x memory, 3.3x throughput).

Reproducible with `docker compose up` and two commands. Four of my own claims died
during the run when I re-measured them; the retractions are in the commit history
rather than quietly edited out.

### Other public work

- [agentiqa](https://github.com/OmkarPalika/agentiqa) — can an AI agent actually
  complete a purchase on your store? Run one and find out.
- [filmcraft](https://github.com/OmkarPalika/filmcraft) — film production craft as a
  Claude Code plugin: coverage, shot lists, scheduling, budgets.
- [tooning](https://github.com/OmkarPalika/tooning) — semantic indexing for
  high-density LLM context over a codebase.
- [codemood](https://pypi.org/project/codemood/) — code analysis, on PyPI.

Unpublished so far, same theme: calibration error on reasoning benchmarks (ECE 0.263
down to 0.056), treating chain-of-thought confidence as a trajectory rather than a
final number and scoring it with signal temporal logic, and ARC-AGI evaluation runs.

### Currently

Junior Developer at National Compliance, Abu Dhabi, remote. B.Tech CSE from ANITS,
Visakhapatnam. Also running MSME 360 and Evergreen Equity Ecosystem, and mentoring on
Unstop and Topmate.

I take focused engagements on vector search in Postgres: recall audits, filter-plan
review, index and layout tuning. If your filtered vector queries are returning the
wrong rows and you cannot work out why, that is the thing I am best at.

**palikaomkar@gmail.com** · [omkarpalika.vercel.app](https://omkarpalika.vercel.app) ·
[LinkedIn](https://www.linkedin.com/in/omkar-palika/)
