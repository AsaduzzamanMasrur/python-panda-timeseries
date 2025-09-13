# python-panda-timeseries

Time Series with Pandas

Working with time-series data is an important part of data analysis.

Starting with v0.8, the pandas library has included a rich API for time-series manipulations.

The pandas time-series API includes:

Creating date ranges

From files

From scratch

Manipulations: Shift, resample, filter

Field accessors (e.g., hour of day)

Plotting

Time zones (localization and conversion)

Dual representations (point-in-time vs interval)

Example Using Tick Data

Sample trade ticks from 2011-11-01 to 2011-11-03 for a single security.

parse_dates: use a list or dict for flexible (possibly multi-column) date parsing.

resample: regularization and frequency conversion.

Compute a VWAP using resample.

Convenient indexing for time series data:

at_time (select a specific time of day)

between_time (select a time range)

fillna: handling missing data.

Simple plotting.

Lead / Lag

shift realigns values.

tshift manipulates index values.

Strategy example with lagged returns.

Volume and Percentages

Convert volume to percentage of daily volume.

Group by hour to compute average hourly volume.

Expanding windows of hourly means.

Compute deviations from hourly means.

Date Range Creation

pd.date_range: flexible date range creation.

Frequency constants:

D: Calendar day

B: Business day

M / MS: Month end / start

W-{MON, TUE...}: Week ending on chosen day

Q, QS, BQ, BQS: Quarter ends / starts

A, AS, BA, BAS: Year ends / starts

H, T, S: Hour, Minute, Second

L/ms, U: Millisecond, Microsecond

DatetimeIndex

Subclass of Index.

Useful for labeling Series / DataFrames.

Supports slicing, partial indexing, positional indexing.

Elements are boxed as Timestamp.

Internal representation: numpy.datetime64.

Multiple views: to_pydatetime, asobject, integer representation.

Resampling and Frequency Conversion

resample: downsample or upsample.

asfreq: change frequency without aggregation.

Options:

closed: left or right bin edge closed

label: left or right label

loffset: shift index labels

Time Zones

tz_localize: assign a timezone.

tz_convert: convert between timezones.

Naive vs localized timestamps.

Period Representation

Some time-series are better represented as intervals rather than points.

Period and PeriodIndex represent intervals.

Conversion between Period and Timestamp.

period_range to create ranges of periods.

Known bugs in older pandas versions (e.g., end time comparisons).
