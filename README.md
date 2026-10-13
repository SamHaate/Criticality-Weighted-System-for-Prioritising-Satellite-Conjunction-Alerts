# Criticality-Weighted Prioritisation of Satellite Conjunction Alerts

Data snapshot for FIT5145 Assignment 3 (Monash University, Sameer Hate, 36783617). The project ranks satellite close-approach alerts by how critical the objects involved are (operational status and launch recency), rather than by distance alone. All data come from [CelesTrak](https://celestrak.org) and were downloaded on 13 October 2026. The data change every few hours, so these files are a fixed snapshot used to make the analysis reproducible.

**Files**
- `sc_0.csv` to `sc_9.csv`, `sc_A.csv` to `sc_Z.csv`: SATCAT records of on-orbit objects, one request per character in the object name. They overlap and are merged and de-duplicated by `NORAD_CAT_ID` in the R Markdown script.
- `satcat_onorbit.csv`: the merged result (35,280 objects), kept to check the merge.
- `satcat_active.csv`: SATCAT records for active payloads only (17,203 objects), used to show that 95% have no size (RCS) recorded.
- `iridium_next.tle`, `iridium33_debris.tle`, `cosmos2251_debris.tle`: two-line element sets for one congested orbital band (about 780 to 800 km), used for the SGP4 close-approach screening.
