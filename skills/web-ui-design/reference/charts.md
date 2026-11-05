# Charts and data tables

Applies when a screen shows a chart, sparkline or data table. Rules in [rules.md](rules.md) still hold. A chart that fails a wrong-answer rule misleads and does not ship.

## Choose the form

- Exact values to look up or compare: a table. A trend or pattern: a chart. One or two numbers: large text with a context phrase, no chart wrapper.
- Time: line for a trend, vertical bars for discrete periods. Categories and rankings: bars sorted by value, horizontal when labels are long. Distribution: histogram with equal bin widths. Correlation: scatterplot, with transparency or jitter when points overlap.
- Part of a whole: sorted bars. A pie or donut only with 5 slices or fewer, sorted, direct-labelled.
- Value against a target: a bullet graph or progress bar, never a gauge. No 3D, no rainbow ramps. Sequential data gets one hue ramp.

## Wrong-answer rules

- A bar chart's value axis starts at 0. A line chart may start higher when the axis says so.
- Lines join ordered points only (time, steps). Unordered categories get bars or dots.
- One y-axis per chart. Two measures with different units become two stacked charts sharing the x-axis.
- Charts that sit side by side to be compared share axis ranges.
- Data marks (lines, bars, points) reach 3:1 against their background. A deliberately muted context series may sit lower while the series that carries the message passes.
- Two or more series differ by more than hue: direct label, marker shape or line style. Red against green never stands alone.
- A forecast or estimate looks different from measured data (dashed line, lighter fill, band).

## Density and focus

- More than 5 lines or 15 bars: small multiples, top N plus "Other", or one series in the accent with the rest in grey. Accent at most 10% of the marks.
- Label series directly when there are 5 or fewer. Beyond 5, use a legend.
- More than 8 category colors: group the small ones.
- Gridlines, axis lines and ticks are light grey, with no chart border or background fill. Text stays horizontal; a label that needs rotating means switching to horizontal bars.
- A sparkline shows its min, max or target. A KPI tile pairs the number with a delta and its comparison period.

## Words and access

- A chart in a report states its finding in the title ("Refunds rose 12% after the price change"). A dashboard tile names metric, unit and period.
- Axes carry units and the time grain. A defined metric ("active users") gets a one-line definition near the chart.
- Every chart has a text alternative: its type, the pattern, the main takeaway. A chart drawn on a canvas also has its data as a table, available on request.

## Tables

- Numbers and their headers are right-aligned; text and its headers are left-aligned; nothing is centered. A column has one decimal precision, units in the header, thousands separators, and `tabular-nums`.
- Rows are the things compared, columns the measures. Default sort is by a meaningful value, alphabetical only when people look up by name.
- Separate rows with space or one light rule, with no full grid. Zebra only on tables wide enough to lose the row. Totals are bold, set off by one light rule.
- Real `th` cells with `scope`. A cell colored by value also carries an icon or text.

Chart and table checks adapted from dataink by Ohad Dahan (MIT, github.com/oh-da/dataink), reworded.
