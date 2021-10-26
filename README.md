# adx-sample-dataset-stormevents
This repository serve ADX sample datasets

# Datasets
## StormEvents CSV
- CSV file link
- ADX ingest command
```
.create table StormEvents (StartTime: datetime, EndTime: datetime, EpisodeId: int, EventId: int, State: string, EventType: string, InjuriesDirect: int, InjuriesIndirect: int, DeathsDirect: int, DeathsIndirect: int, DamageProperty: int, DamageCrops: int, Source: string, BeginLocation: string, EndLocation: string, BeginLat: real, BeginLon: real, EndLat: real, EndLon: real, EpisodeNarrative: string, EventNarrative: string, StormSummary: dynamic)

.ingest into table StormEvents 'https://github.com/CloudBreadPaPa/adx-sample-dataset-stormevents/blob/main/dataset/StormEvents.csv?raw=true' with (ignoreFirstRecord=true)

StormEvents
| sort by StartTime desc
| take 10
```
- [ADX Ingest sample data into Azure Data Explorer](https://docs.microsoft.com/en-us/azure/data-explorer/ingest-sample-data)
- [NOAA Storm Events Dataset](https://www.ncdc.noaa.gov/stormevents/)
