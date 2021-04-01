---
title: Elemento ScheduleByDay (calendarTriggerType)
description: Especifica una programación diaria.
ms.assetid: 5a6097ce-a855-4b08-84c5-71f06343805e
keywords:
- Programador de tareas de desencadenador diario, elemento XML
- Programador de tareas del elemento ScheduleByDay
topic_type:
- apiref
api_name:
- ScheduleByDay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 614777ede63605dc7ed6936bda952c6071bda371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996882"
---
# <a name="schedulebyday-calendartriggertype-element"></a>Elemento ScheduleByDay (calendarTriggerType)

Especifica una programación diaria. Por ejemplo, la tarea comienza a las 8:00 A.M. todos los días, cada día, cada tres días, etc.

``` syntax
<xs:element name="ScheduleByDay"
    type="dailyScheduleType"
 />
```

El elemento **ScheduleByDay** se define mediante el tipo complejo de [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                             | Derivado de                                                                       | Descripción                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) | Especifica un desencadenador de día de la semana (DOW) diario, semanal, mensual o mensual.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                            | Tipo             | Descripción                                                         |
|------------------------------------------------------------------------------------|------------------|---------------------------------------------------------------------|
| [**DaysInterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) | **unsignedByte** | Especifica el intervalo entre los días de la programación.<br/> |



## <a name="remarks"></a>Observaciones

El elemento secundario enumerado anteriormente está definido por los tipos de elemento complejo [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) .

La hora del día en que se inicia la tarea se establece mediante el elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) .

Para el desarrollo de scripting, se especifica un desencadenador diario mediante el objeto [**DailyTrigger**](weeklytrigger.md) .

En el desarrollo de C++, se especifica un desencadenador diario mediante la interfaz [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger) .

## <a name="examples"></a>Ejemplos

En el código XML siguiente se define un desencadenador de calendario diario que inicia la tarea cada día.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T00:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByDay>
        <DaysInterval>1</DaysInterval>
    </ScheduleByDay>
</CalendarTrigger>
```



Para obtener un ejemplo completo del XML de una tarea que especifica una programación diaria, vea [ejemplo de desencadenador diario (XML)](daily-trigger-example--xml-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas elementos de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





