# adx-sample-dataset-stormevents
This repository serve ADX sample datasets

# Datasets
## StormEvents CSV
- CSV file link
- ADX ingest command
```
.create table StormEvents (StartTime: datetime, EndTime: datetime, EpisodeId: int, EventId: int, State: string, EventType: string, InjuriesDirect: int, InjuriesIndirect: int, DeathsDirect: int, DeathsIndirect: int, DamageProperty: int, DamageCrops: int, Source: string, BeginLocation: string, EndLocation: string, BeginLat: real, BeginLon: real, EndLat: real, EndLon: real, EpisodeNarrative: string, EventNarrative: string, StormSummary: dynamic)

.ingest into table StormEvents 'https://kustosamplefiles.blob.core.windows.net/samplefiles/StormEvents.csv?sv=2019-12-12&ss=b&srt=o&sp=r&se=2022-09-05T02:23:52Z&st=2020-09-04T18:23:52Z&spr=https&sig=VrOfQMT1gUrHltJ8uhjYcCequEcfhjyyMX%2FSc3xsCy4%3D' with (ignoreFirstRecord=true)

```
- [ADX Ingest sample data into Azure Data Explorer](https://docs.microsoft.com/en-us/azure/data-explorer/ingest-sample-data)
- [NOAA Storm Events Dataset](https://www.ncdc.noaa.gov/stormevents/)
