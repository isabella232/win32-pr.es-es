---
title: Elemento Day (daysOfMonthType)
description: Especifica un día del mes durante el que se ejecuta la tarea.
ms.assetid: b213df09-9301-4a51-b000-edfdafbe861e
keywords:
- Programador de tareas del elemento Day
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079100"
---
# <a name="day-daysofmonthtype-element"></a>Elemento Day (daysOfMonthType)

Especifica un día del mes durante el que se ejecuta la tarea.

``` syntax
<xs:element name="Day"
    type="dayOfMonthType"
 />
```

El elemento **Day** se define mediante el tipo complejo [**daysOfMonthType**](taskschedulerschema-daysofmonthtype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                            | Derivado de                                                               | Descripción                                                            |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**DaysOfMonth**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [**daysOfMonthType**](taskschedulerschema-daysofmonthtype-complextype.md) | Especifica los días del mes durante los que se ejecuta la tarea.<br/> |



## <a name="examples"></a>Ejemplos

El siguiente código XML define la parte correspondiente a los días de un calendario mensual que ejecuta la tarea el día 1 y el 15 del mes.


```XML
<DaysOfMonth>
    <Day>1</Day>
    <Day>15</Day>
</DaysOfMonth>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas elementos de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





