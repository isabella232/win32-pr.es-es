---
title: Elemento ScheduleByDay (calendarTriggerType)
description: Especifica una programación diaria.
ms.assetid: 5a6097ce-a855-4b08-84c5-71f06343805e
keywords:
- desencadenador diario Programador de tareas elemento , XML
- Elemento ScheduleByDay Programador de tareas
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968684"
---
# <a name="schedulebyday-calendartriggertype-element"></a>Elemento ScheduleByDay (calendarTriggerType)

Especifica una programación diaria. Por ejemplo, la tarea se inicia a las 8:00 a. m. todos los días, cada dos días, cada tercer día, y así sucesivamente.

``` syntax
<xs:element name="ScheduleByDay"
    type="dailyScheduleType"
 />
```

El tipo complejo [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) define el elemento **ScheduleByDay.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                             | Derivado de                                                                       | Descripción                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) | Especifica un desencadenador diario, semanal, mensual o mensual del día de la semana (DOW).<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                            | Tipo             | Descripción                                                         |
|------------------------------------------------------------------------------------|------------------|---------------------------------------------------------------------|
| [**DaysInterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) | **unsignedByte** | Especifica el intervalo entre los días de la programación.<br/> |



## <a name="remarks"></a>Observaciones

Los tipos de elemento complejo [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) definen el elemento secundario enumerado anteriormente.

El elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) establece la hora del día en que se inicia la tarea.

Para el desarrollo de scripting, se especifica un desencadenador diario mediante el [**objeto DailyTrigger.**](weeklytrigger.md)

Para el desarrollo de C++, se especifica un desencadenador diario mediante la [**interfaz IDailyTrigger.**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)

## <a name="examples"></a>Ejemplos

El código XML siguiente define un desencadenador de calendario diario que inicia la tarea todos los días.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T00:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByDay>
        <DaysInterval>1</DaysInterval>
    </ScheduleByDay>
</CalendarTrigger>
```



Para obtener un ejemplo completo del XML de una tarea que especifica una programación diaria, vea Ejemplo de desencadenador [diario (XML).](daily-trigger-example--xml-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





