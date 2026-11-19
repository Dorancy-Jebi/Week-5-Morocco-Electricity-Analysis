# Business Insights and Recommendations

**Analysis basis:** 52,416 observations across three zones, from January 1 through December 30, 2017. Values below are means or peaks of recorded per-reading values. The per-reading energy/power interpretation remains unconfirmed in the supplied files; values are not summed into kWh totals.

## Evidence-based findings

1. **Zone 1 records the highest average value.** Its mean is 32,344.97, compared with 21,042.51 for Zone 2 and 17,835.41 for Zone 3. Zone 1's mean is about 81.4% higher than Zone 3's.

2. **All three zones have an evening peak in the average hourly profile.** The highest hourly mean occurs at 20:00 for Zones 1, 2 and 3. The lowest mean hour is 06:00 for Zones 1 and 2 and 07:00 for Zone 3.

3. **High months differ by zone.** The highest monthly mean occurs in August for Zones 1 (36,435.19) and 2 (24,656.22), and July for Zone 3 (28,194.11). Zone 3's lowest monthly mean is in December (11,044.81).

4. **Weekly patterns are not identical across zones.** Weekend mean values are lower than weekday means in Zone 1 (31,516.56 vs 32,676.34) and Zone 2 (19,782.67 vs 21,546.45). Zone 3's weekend mean is slightly higher than its weekday mean (17,983.01 vs 17,776.37). Sunday is the lowest day for Zones 1 and 2; Zone 3 is comparatively steady across weekdays and weekends.

5. **Temperature shows the clearest environmental association at the 10-minute level.** Spearman rho is 0.433 for Zone 1, 0.379 for Zone 2 and 0.436 for Zone 3. Humidity associations are negative (-0.300, -0.309 and -0.212); wind-speed associations are weakly positive (0.107, 0.087 and 0.079).

6. **Aggregation changes the apparent association.** On 364 daily means, temperature rho is 0.724 for Zone 1, 0.394 for Zone 2 and 0.467 for Zone 3; daily humidity correlations are weaker (-0.108 to -0.129). The difference demonstrates sensitivity to timescale and possible seasonality; it does not establish a causal weather effect.

7. **High statistical flags are concentrated in Zone 3's summer evenings.** The global IQR rule flags 1,191 Zone 3 observations (2.27%), all above the upper fence; the flags occur in July-August and mostly 19:00-23:00. It also flags 7 Zone 2 observations and none in Zone 1. They should be investigated, not automatically removed.

8. **The recorded series is complete and regular within its observed window.** There are no missing cells, duplicates, parse failures, negative numeric readings, or missing ten-minute timestamps between 2017-01-01 00:00 and 2017-12-30 23:50. December 31 is absent.

## Actionable recommendations

1. **Plan staffing and capacity around the 20:00 peak.** Use zone-specific hourly profiles to schedule operational coverage and evaluate demand-response windows; avoid assuming the same weekend pattern applies in all zones.

2. **Prepare seasonal operating plans before July-August.** Zones 1 and 2 reach their highest monthly means in August, while Zone 3 peaks in July. Validate this timing against more years before setting long-term seasonal targets.

3. **Investigate Zone 3's July-August evening high readings.** Cross-check flagged intervals with meter quality, site operating calendars, weather and system events. Preserve them unless evidence confirms measurement errors.

4. **Evaluate temperature as a forecasting input, not as a causal lever.** Build a future forecast with time-based validation, relevant operational controls and out-of-time testing. Compare performance against a time-only baseline before operational use.

5. **Resolve unit and variable definitions with the data owner.** Confirm whether zone readings are interval kWh or a power level, and clarify `GeneralDiffuseFlows` / `DiffuseFlows` units and physical meaning before summing consumption or making environmental claims.

## Interpretation limits

This is one partial calendar year of observations. It cannot support year-over-year conclusions or establish stable seasonal patterns. The rank correlations may reflect autocorrelation, seasonal co-movement or other confounders; correlation is not causation. The supplied unit descriptions are not sufficient to assert interval-energy semantics.
