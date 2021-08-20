---
title: Elemento DaysInterval (dailyScheduleType)
description: Especifica el intervalo entre los días de la programación.
ms.assetid: 495ea1c0-37eb-4b12-8241-bfc6489e33ed
keywords:
- Elemento DaysInterval Programador de tareas
topic_type:
- apiref
api_name:
- DaysInterval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e35df4f102801f7d52faeb384f9a1113e00abbf034026d19b5b7b6e7b4c90ed7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119621105"
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

El elemento se define mediante el [**tipo complejo dailyScheduleType.**](taskschedulerschema-dailyscheduletype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                | Derivado de                                                                   | Descripción                            |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|----------------------------------------|
| [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) | [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) | Especifica una programación diaria.<br/> |



## <a name="remarks"></a>Comentarios

Para el desarrollo de scripts, la propiedad [**DailyTrigger.DaysInterval**](dailytrigger-daysinterval.md) especifica el intervalo de días de un desencadenador diario.

Para el desarrollo de C++, la propiedad [**IDailyTrigger::D aysInterval**](/windows/desktop/api/taskschd/nf-taskschd-idailytrigger-get_daysinterval) especifica el intervalo de días de un desencadenador diario.

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



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





