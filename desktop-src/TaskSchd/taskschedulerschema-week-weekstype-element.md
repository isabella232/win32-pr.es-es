---
title: Elemento Week (weeksType)
description: Especifica una semana específica del mes.
ms.assetid: 0cec07da-e9e7-43ef-9f54-48d00114ba1f
keywords:
- Elemento Week Programador de tareas
topic_type:
- apiref
api_name:
- Week
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0487aa07e1f1132c998b6cb2ba0f518a9db57ce2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474654"
---
# <a name="week-weekstype-element"></a>Elemento Week (weeksType)

Especifica una semana específica del mes.

``` syntax
<xs:element name="Week"
    type="weekType"
 />
```

El **tipo complejo weeksType** define el elemento [**Week.**](taskschedulerschema-weekstype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                                        | Derivado de                                                   | Descripción                                                           |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------------------------------------------|
| [**Weeks (monthlyDayOfWeekScheduleType)**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) | [**weeksType**](taskschedulerschema-weekstype-complextype.md) | Especifica las semanas del mes en que se ejecuta la tarea.<br/> |



## <a name="remarks"></a>Observaciones

Al especificar las semanas del mes, use los números 1 a 4 para las cuatro primeras semanas del mes o use la cadena "Last" para indicar esa última semana del mes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





