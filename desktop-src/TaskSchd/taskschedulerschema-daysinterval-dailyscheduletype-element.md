---
title: Elemento DaysInterval (dailyScheduleType)
description: Especifica el intervalo entre los días de la programación.
ms.assetid: 495ea1c0-37eb-4b12-8241-bfc6489e33ed
keywords:
- Programador de tareas del elemento DaysInterval
topic_type:
- apiref
api_name:
- DaysInterval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 97b50581aa4825b31983a234a5eb47ff7b7b7e06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996035"
---
# <a name="daysinterval-dailyscheduletype-element"></a>Elemento DaysInterval (dailyScheduleType)

Especifica el intervalo entre los días de la programación.

``` syntax
<xs:element name="DaysInterval"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="unsignedInt"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="365"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

El elemento se define mediante el tipo complejo de [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                | Derivado de                                                                   | Descripción                            |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|----------------------------------------|
| [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) | [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) | Especifica una programación diaria.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de scripts, el intervalo de días para un desencadenador diario se especifica mediante la propiedad [**DailyTrigger. DaysInterval**](dailytrigger-daysinterval.md) .

En el desarrollo de C++, el intervalo de días para un desencadenador diario se especifica mediante la propiedad [**IDailyTrigger::D aysinterval**](/windows/desktop/api/taskschd/nf-taskschd-idailytrigger-get_daysinterval) .

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

 

 





