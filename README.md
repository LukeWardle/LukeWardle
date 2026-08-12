## Luke Wardle

Self-taught, working in Python. Data pipelines, PostgreSQL/PostGIS and geospatial data.
Heading for data engineering.

**[sentinel2-brownfield-stoke](https://github.com/LukeWardle/sentinel2-brownfield-stoke)**
is the one to look at — a Sentinel-2 satellite pipeline built to find unregistered
brownfield land in Stoke-on-Trent. Copernicus API ingest with token refresh, cloud
masking, coordinate reference transforms, spectral indices, connected-component
clustering, PostGIS storage with a migration-driven schema, 400+ tests, and CI running
against a live PostGIS container.

**[Live demo](https://sentinel2-brownfield-stoke-kmk6mryzgmmtv3ewewdan5.streamlit.app/)** —
deploys from a bare checkout with no database connection and no secrets. It sleeps when
idle, so give it a few seconds to wake.

It doesn't work, and the repository explains why. Registered brownfield land turns out to
be vegetated; the detector was looking for bare ground; zero of 352 known sites pass its
threshold. Establishing that meant retracting recall figures I'd been reporting for three
months, tracing the cause to a comparison I'd never made between two numbers recorded in
the same notebook, and correcting the record across six notebooks and the README. I'd
rather show that than a screenshot of something that runs.

I stopped there rather than scaling it. The supervised route was closed on an effect size
of about 0.03 SD between matched and unmatched candidates — there was no label to learn —
and a UK-wide version wasn't worth building on a method that fails at one council.

### The rest of it

**[ftse-portfolio-rebalancer](https://github.com/LukeWardle/ftse-portfolio-rebalancer)** —
ridge-regularised rebalancing under FCA position, sector and liquidity limits; κ reduced
from 2,862 to 62.7. An external review found a one-character error that invalidated the
headline result while all 21 tests passed. Diagnosed, fixed, re-verified, and I write the
failing test first now.

**[tfl-optimiser](https://github.com/LukeWardle/tfl-optimiser)** — a linear programme
allocating 15 buses across 25 routes covering 50 stations, solved with HiGHS. Uses LP
relaxation rather than integer programming, which is a documented trade-off rather than
an oversight.

**[week3-linear-solvers](https://github.com/LukeWardle/week3-linear-solvers)** and
**[week3-gaussian-implementation](https://github.com/LukeWardle/week3-gaussian-implementation)** —
a deliberate pair. One picks its own strategy from matrix shape and condition number; the
other implements the same mathematics by hand and benchmarks it against LAPACK. NumPy
wins, which is the argument for using NumPy.

Also here: Markowitz portfolio optimisation under no-shorting constraints, NHS
resource-allocation models, and two small vector CLI tools from the start of all this.

### Stack

Python · SQL · PostgreSQL/PostGIS · Docker and docker-compose · GitHub Actions ·
pytest · NumPy, SciPy, pandas, scikit-learn, matplotlib · rasterio, pyproj · Streamlit,
Folium

Everything above is self-directed project work from 2026. My degree is in History, not
computer science, and I'd rather you read the code than take my word for any of it.

Open to remote or hybrid work — based near Newcastle-under-Lyme, Staffordshire. Data
engineering is what I'm aiming at; also interested in data science and geospatial roles.
