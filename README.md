# Omkar Palika

AI/ML and full-stack developer in Visakhapatnam. Building [MSME 360](https://github.com/OmkarPalika)
and Evergreen Equity Ecosystem, mentoring on Unstop and Topmate, currently a Junior
Developer at National Compliance.

The thread running through most of what I build: checking whether a number measures
what everyone assumes it measures. Calibration error on reasoning benchmarks, whether
an agent can actually finish the task, whether a database returns the right rows.

### Recent work

**[pgvector-filtered-recall](https://github.com/OmkarPalika/pgvector-filtered-recall)** —
what happens to pgvector's HNSW recall when you add a `WHERE` clause. 1M vectors,
PostgreSQL 17, 45 configurations, ground truth from an exact scan in the same database.

Under a filter that correlates with the embedding, a tenant, a category, a date range,
pgvector can return zero rows and report success. No error, no warning, 683ms.
`iterative_scan` does not fix that case; a btree on the filter column does, in 3.6ms.
Reproducible with `docker compose up` and two commands.

**[agentiqa](https://github.com/OmkarPalika/agentiqa)** — can an AI agent actually
complete a purchase on your store? Run one and find out.

**[filmcraft](https://github.com/OmkarPalika/filmcraft)** — film production craft as a
Claude Code plugin: coverage, shot lists, scheduling, budgets.

**[tooning](https://github.com/OmkarPalika/tooning)** — semantic indexing for
high-density LLM context over a codebase.

**[codemood](https://pypi.org/project/codemood/)** — code analysis, published on PyPI.

Not public yet, same theme: calibration error on reasoning benchmarks (ECE 0.263 down
to 0.056), scoring chain-of-thought confidence as a trajectory with signal temporal
logic rather than as a final number, and ARC-AGI evaluation runs.

### Background

B.Tech CSE from ANITS, Visakhapatnam. Java backend at Fulcrum GT, frontend at Oasis
Infobyte, now full-stack in Next.js at National Compliance. GeeksforGeeks Chapter Lead
then Campus Mantri: 10+ events, 2 hackathons, 250+ participants. Unstop Top Mentor,
top 10% with a 4.9 rating.

I write Momentum, a weekly newsletter on LinkedIn for students, founders and people
building things.

### Reach me

Open to full-time roles in AI/ML and full-stack engineering, and to focused consulting
on vector search in Postgres: recall audits, filter-plan review, index and layout
tuning.

**palikaomkar@gmail.com** · [omkarpalika.vercel.app](https://omkarpalika.vercel.app) ·
[LinkedIn](https://www.linkedin.com/in/omkar-palika/) ·
[Topmate](https://topmate.io/omkar_palika)
