---
title: Elemento Day (daysOfMonthType)
description: Especifica un día del mes durante el que se ejecuta la tarea.
ms.assetid: b213df09-9301-4a51-b000-edfdafbe861e
keywords:
- Elemento Day Programador de tareas
topic_type:
- apiref
api_name:
- Day
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e8e06169d2b758264f181263a5cb717977a1602
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071034"
---
# <a name="day-daysofmonthtype-element"></a>Elemento Day (daysOfMonthType)

Especifica un día del mes durante el que se ejecuta la tarea.

``` syntax
<xs:element name="Day"
    type="dayOfMonthType"
 />
```

El **elemento Day** se define mediante el tipo complejo [**daysOfMonthType.**](taskschedulerschema-daysofmonthtype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                            | Derivado de                                                               | Descripción                                                            |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**DaysOfMonth**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [**daysOfMonthType**](taskschedulerschema-daysofmonthtype-complextype.md) | Especifica los días del mes durante los que se ejecuta la tarea.<br/> |



## <a name="examples"></a>Ejemplos

El xml siguiente define la parte de días de un calendario mensual que ejecuta la tarea el primer y el 15 día del mes.


```XML
<DaysOfMonth>
    <Day>1</Day>
    <Day>15</Day>
</DaysOfMonth>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





