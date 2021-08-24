---
title: MonthlyDOWTrigger.DaysOfWeek, propiedad
description: Para el scripting, obtiene o establece los días de la semana durante los que se ejecuta la tarea.
ms.assetid: dd9b2463-69a1-4e77-a8f7-26b186d3d02d
keywords:
- Propiedad DaysOfWeek Programador de tareas
- Propiedad DaysOfWeek Programador de tareas objeto , MonthlyDOWTrigger
- Objeto MonthlyDOWTrigger Programador de tareas propiedad , DaysOfWeek
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.DaysOfWeek
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b9abf5dcd33c92d402f8ed6047a2fd80a0d5905bae075110931cfb8f83aa10a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119517465"
---
# <a name="monthlydowtriggerdaysofweek-property"></a>MonthlyDOWTrigger.DaysOfWeek, propiedad

Para el scripting, obtiene o establece los días de la semana durante los que se ejecuta la tarea.

## <a name="syntax"></a>Syntax


```VB
MonthlyDOWTrigger.DaysOfWeek As short
```



## <a name="property-value"></a>Valor de propiedad

Máscara bit a bit que indica los días de la semana durante los que se ejecuta la tarea.

## <a name="remarks"></a>Comentarios

En la tabla siguiente se muestra la asignación de la máscara bit a bit utilizada por esta propiedad.



| Día de la semana | Valor hexadecimal | Valor decimal |
|-------------|-----------|---------------|
| Domingo      | 0x01      | 1             |
| Lunes      | 0x02      | 2             |
| Martes     | 0x04      | 4             |
| Miércoles   | 0x08      | 8             |
| Jueves    | 0x10      | 16            |
| Viernes      | 0x20      | 32            |
| Sábado    | 0x40      | 64            |



 

Al leer o escribir XML para una tarea, el elemento [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) especifica los días de la semana de un calendario mensual del día de la semana.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MonthlyDOWTrigger**](monthlydowtrigger.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





