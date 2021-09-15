---
title: WeeklyTrigger.DaysOfWeek, propiedad
description: Para el scripting, obtiene o establece los días de la semana en los que se ejecuta la tarea.
ms.assetid: 79f279d4-d6d2-428b-bbed-226e4eaaefb6
keywords:
- Propiedad DaysOfWeek Programador de tareas
- Propiedad DaysOfWeek Programador de tareas objeto , WeeklyTrigger
- Objeto WeeklyTrigger Programador de tareas propiedad , DaysOfWeek
topic_type:
- apiref
api_name:
- WeeklyTrigger.DaysOfWeek
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7f0a27ef031e7baf46d2d3c0e33c23fb505c7ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474642"
---
# <a name="weeklytriggerdaysofweek-property"></a>WeeklyTrigger.DaysOfWeek, propiedad

Para el scripting, obtiene o establece los días de la semana en los que se ejecuta la tarea.

## <a name="syntax"></a>Sintaxis


```VB
WeeklyTrigger.DaysOfWeek As short
```



## <a name="property-value"></a>Valor de propiedad

Máscara bit a bit que indica los días de la semana en los que se ejecuta la tarea.

## <a name="remarks"></a>Observaciones

En la tabla siguiente se muestra la asignación de la máscara bit a bit utilizada por esta propiedad.



| Mes     | Valor hexadecimal | Valor decimal |
|-----------|-----------|---------------|
| Domingo    | 0X01      | 1             |
| Lunes    | 0x02      | 2             |
| Martes   | 0X04      | 4             |
| Miércoles | 0X08      | 8             |
| Jueves  | 0X10      | 16            |
| Viernes    | 0x20      | 32            |
| Sábado  | 0X40      | 64            |



 

Al leer o escribir su propio XML para una tarea, los días de la semana se especifican mediante el [**elemento DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) del esquema Programador de tareas trabajo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





