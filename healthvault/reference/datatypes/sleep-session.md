---
uid: HV_11C52484-7F1A-11DB-AEAC-87D355D89593
title: Sleep session
---

# Sleep session

## Overview

Property|Value
---|---
id|11C52484-7F1A-11DB-AEAC-87D355D89593
name|Sleep session
immutable|False
singleton|False
allow-readonly|False
effective date XPath|No effective date XPath

## .NET reference
- [Microsoft.Health.ItemTypes.SleepJournalAM](https://docs.microsoft.com/dotnet/api/microsoft.health.itemtypes.sleepjournalam)
- [Microsoft.HealthVault.ItemTypes.SleepJournalAM](https://docs.microsoft.com/dotnet/api/microsoft.healthvault.itemtypes.sleepjournalam)

## Related data types

- [PAP session](xref:HV_9085CAD9-E866-4564-8A91-7AD8685D204D)
- [Sleep journal entry](xref:HV_031F5706-7F1A-11DB-AD56-7BD355D89593)

## Details
A morning sleep journal reflects back on the previous nights sleep. The data items were adapted from the NIH publication #06-5271, November 2005, "Your Guide to Healthy Sleep", ISBN 1-933236-05-1.

<a name='sleep-am'></a>

### Root element: sleep-am

Schema for a morning sleep journal.

A morning sleep journal reflects back on the previous nights sleep. The data items were adapted from the NIH publication #06-5271, November 2005, "Your Guide to Healthy Sleep", ISBN 1-933236-05-1.

### Element sequence

Name|Type|Min occurs|Max occurs|Summary|Remarks
---|---|---|---|---|---
when|[date-time](xref:HV_File_dates#date-time)|1|1|The date and time that the journal entry refers to.|
bed-time|[time](xref:HV_File_dates#time)|1|1|The time the person went to bed.|
wake-time|[time](xref:HV_File_dates#time)|1|1|The time the person woke up for a period of activity.|
sleep-minutes|[nonNegativeInt](xref:HV_3e730686-781f-4616-aa0d-817bba8eb141#nonNegativeInt)|1|1|The number of minutes slept.|
settling-minutes|[nonNegativeInt](xref:HV_3e730686-781f-4616-aa0d-817bba8eb141#nonNegativeInt)|1|1|The number of minutes it took to fall asleep.|
awakening|[Awakening](#Awakening)|0|unbounded|The time and duration of each the person awoke during the night.|
medications|[codable-value](xref:HV_3e730686-781f-4616-aa0d-817bba8eb141#codable-value)|0|1|A description of the medications taken before going to bed.|
wake-state|[wake-state](#wake-state)|1|1||
times-woken-up|[nonNegativeInt](xref:HV_3e730686-781f-4616-aa0d-817bba8eb141#nonNegativeInt)|0|1|The number of times the person woke up at night.|
average-resting-hr|[nonNegativeInt](xref:HV_3e730686-781f-4616-aa0d-817bba8eb141#nonNegativeInt)|0|1|The average resting heart rate of the person.|
calories-burned|[nonNegativeInt](xref:HV_3e730686-781f-4616-aa0d-817bba8eb141#nonNegativeInt)|0|1|The number of calories burned while sleeping.|
awake-minutes|[nonNegativeInt](xref:HV_3e730686-781f-4616-aa0d-817bba8eb141#nonNegativeInt)|0|1|The number of minutes that the person was awake during their sleep session.|
sleep-phase-summary-group|[SleepPhaseSummaryGroup](#SleepPhaseSummaryGroup)|0|1|A summary of the total amount of time the person spent in each sleep phase. For example, minutes spent in Light, Deep, or REM sleep.|

>[!div style="margin-left: 4px; border-left: 1px solid; padding-left: 5px;"]
>
> <a name='wake-state'></a>
>
> ### wake-state
>
> An evaluation of how the person felt when they got up in the morning.
>
> 1 = Wide awake, 2 = Awake but a little tired, 3 = Sleepy
>
> ### Restriction
>
> Base type: [int](xref:HV_1ed1cba6-9530-44a3-b7b5-e8219690ebcf#int)
>
> #### Restriction facets
>
> Restriction type|Value|Summary|Remarks
> ---|---|---|---
> minInclusive|1||
> maxInclusive|3||
>
>

>[!div style="margin-left: 4px; border-left: 1px solid; padding-left: 5px;"]
>
> <a name='Awakening'></a>
>
> ### Awakening
>
> A time and duration of an awakening during a period of sleep.
>
> An awakening covers those times during a sleep session in which the person awoke and then went back to sleep. For example, if a person wakes up during a night's sleep to use the restroom and then returns to sleep. It does not include awakenings that result in the person remaining awake for active periods.
>
> ### Element sequence
>
> Name|Type|Min occurs|Max occurs|Summary|Remarks
> ---|---|---|---|---|---
> when|[time](xref:HV_File_dates#time)|1|1|The time when the person awoke.|
> minutes|[nonNegativeInt](xref:HV_3e730686-781f-4616-aa0d-817bba8eb141#nonNegativeInt)|1|1|The duration the person stayed awake in minutes.|
>
>

>[!div style="margin-left: 4px; border-left: 1px solid; padding-left: 5px;"]
>
> <a name='SleepPhaseSummaryGroup'></a>
>
> ### SleepPhaseSummaryGroup
>
> A group of sleep phase minutes for this sleep event.
>
> ### Element sequence
>
> Name|Type|Min occurs|Max occurs|Summary|Remarks
> ---|---|---|---|---|---
> sleep-phase-summary|[SleepPhaseSummary](#SleepPhaseSummary)|1|unbounded|The sleep phase minutes definitions for this sleep event.|
>
>

>[!div style="margin-left: 4px; border-left: 1px solid; padding-left: 5px;"]
>
> <a name='SleepPhaseSummary'></a>
>
> ### SleepPhaseSummary
>
> A summary of the amount of time the person slept in each phase during this sleep event. Each element should represent the total amount of time the person spent in that phase during this sleep event.
>
> A sleep phase minutes summary is meant to cover the total sleep time that the user spent in each phase of sleep. For example, the amount of time they spent in deep, light, or rem sleep.
>
> ### Element sequence
>
> Name|Type|Min occurs|Max occurs|Summary|Remarks
> ---|---|---|---|---|---
> phase|[codable-value](xref:HV_3e730686-781f-4616-aa0d-817bba8eb141#codable-value)|1|1|The phase of sleep represented by this object. Example values could be light, deep, or REM sleep.|
> minutes|[nonNegativeInt](xref:HV_3e730686-781f-4616-aa0d-817bba8eb141#nonNegativeInt)|1|1|The amount of time that the person spent in this phase during this sleep event.|
>
>

## Example
[!code-xml[Example](../sample-xml/11C52484-7F1A-11DB-AEAC-87D355D89593.xml)]

## XSD schema
[![Download](/healthvault/images/download.png)Download](../xsd/sleepjournal-am.xsd)
[!code-xml[XSD schema](../xsd/sleepjournal-am.xsd)]
