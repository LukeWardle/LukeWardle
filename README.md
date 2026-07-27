## Luke Wardle

Self-taught developer. Python, PostgreSQL/PostGIS, and data pipelines.

**[sentinel2-brownfield-stoke](https://github.com/LukeWardle/sentinel2-brownfield-stoke)** is the one to look at — a Sentinel-2 satellite pipeline built to find unregistered brownfield land in Stoke-on-Trent. Copernicus API ingest with token refresh, cloud masking, coordinate reference transforms, spectral analysis, spatial clustering, PostGIS storage with migration-driven schema, 400+ tests and CI.

It doesn't work, and the repository explains why. Registered brownfield land turns out to be vegetated; the detector was looking for bare ground; zero of 352 known sites pass its threshold. Establishing that meant retracting recall figures I'd been reporting for three months, tracing the cause to a comparison I'd never made between two numbers recorded in the same notebook, and correcting the record across six notebooks and the README. I'd rather show that than a screenshot of something that runs.

Open to remote or hybrid work — based near Newcastle-under-Lyme, Staffordshire.
