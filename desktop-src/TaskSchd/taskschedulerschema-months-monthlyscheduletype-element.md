---
title: Months (monthlyScheduleType) (Elemento)
description: Especifica los meses del año durante los que se ejecuta la tarea para una programación mensual.
ms.assetid: 71c9f7ac-01fc-4837-bccf-1869df2bc24e
keywords:
- Elementos Months Programador de tareas
topic_type:
- apiref
api_name:
- Months
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ed40fd2466f8962f839f39e7addd3b7e1bc33eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259103"
---
# <a name="months-monthlyscheduletype-element"></a>Months (monthlyScheduleType) (Elemento)

Especifica los meses del año durante los que se ejecuta la tarea para una programación mensual.

``` syntax
<xs:element name="Months"
    type="monthsType"
 />
```

El **elemento Months** se define mediante el tipo complejo [**monthlyScheduleType.**](taskschedulerschema-monthlyscheduletype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                    | Derivado de                                                                       | Descripción                               |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|-------------------------------------------|
| [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) | [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) | Especifica una programación mensual. <br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                            | Tipo | Descripción                                           |
|------------------------------------------------------------------------------------|------|-------------------------------------------------------|
| [**Abril (monthsType)**](taskschedulerschema-april-monthstype-element.md)         |      | Especifica que la tarea se ejecuta en abril.<br/>     |
| [**Agosto (monthsType)**](taskschedulerschema-august-monthstype-element.md)       |      | Especifica que la tarea se ejecuta en agosto.<br/>    |
| [**Diciembre (monthsType)**](taskschedulerschema-december-monthstype-element.md)   |      | Especifica que la tarea se ejecuta en diciembre.<br/>  |
| [**Febrero (monthsType)**](taskschedulerschema-february-monthstype-element.md)   |      | Especifica que la tarea se ejecuta en febrero.<br/>  |
| [**Enero (monthsType)**](taskschedulerschema-january-monthstype-element.md)     |      | Especifica que la tarea se ejecuta en enero.<br/>   |
| [**Julio (monthsType)**](taskschedulerschema-july-monthstype-element.md)           |      | Especifica que la tarea se ejecuta en julio.<br/>      |
| [**Junio (monthsType)**](taskschedulerschema-june-monthstype-element.md)           |      | Especifica que la tarea se ejecuta en junio.<br/>      |
| [**Marzo (monthsType)**](taskschedulerschema-march-monthstype-element.md)         |      | Especifica que la tarea se ejecuta en marzo.<br/>     |
| [**Mayo (monthsType)**](taskschedulerschema-may-monthstype-element.md)             |      | Especifica que la tarea se ejecuta en mayo.<br/>       |
| [**Noviembre (monthsType)**](taskschedulerschema-november-monthstype-element.md)   |      | Especifica que la tarea se ejecuta en noviembre.<br/>  |
| [**Octubre (monthsType)**](taskschedulerschema-october-monthstype-element.md)     |      | Especifica que la tarea se ejecuta en octubre.<br/>   |
| [**Septiembre (monthsType)**](taskschedulerschema-september-monthstype-element.md) |      | Especifica que la tarea se ejecuta en septiembre.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de scripts, los meses de la programación se especifican mediante la [**propiedad MonthlyTrigger.MonthsOfYear.**](monthlytrigger-monthsofyear.md)

Para el desarrollo de C++, los meses de la programación se especifican mediante la [**propiedad IMonthlyTrigger::MonthsOfYear.**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_monthsofyear)

## <a name="examples"></a>Ejemplos

El xml siguiente define un calendario mensual que inicia la tarea el día 1 y 15 de cada mes del año.


```XML
</ScheduleByMonth>
    <DaysOfMonth>
        <Day>1</Day>
        <Day>15</Day>
    </DaysOfMonth
    <Months>
        <January/>
        <February/>
        <March/>
        <April/>
        <May/>
        <June/>
        <July/>
        <August/>
        <September/>
        <October/>
        <November/>
        <December/>
    <Months>
</ScheduleByMonth>
```



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

 

 





