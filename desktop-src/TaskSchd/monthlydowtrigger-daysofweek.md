---
title: MonthlyDOWTrigger. DaysOfWeek (propiedad)
description: En el caso de scripting, obtiene o establece los días de la semana en los que se ejecuta la tarea.
ms.assetid: dd9b2463-69a1-4e77-a8f7-26b186d3d02d
keywords:
- Propiedad DaysOfWeek Programador de tareas
- Propiedad DaysOfWeek Programador de tareas, objeto MonthlyDOWTrigger
- Programador de tareas de objeto MonthlyDOWTrigger, propiedad DaysOfWeek
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
ms.openlocfilehash: 15344650dabdec2bcbacf91397b37b97ce3f0772
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492310"
---
# <a name="monthlydowtriggerdaysofweek-property"></a>MonthlyDOWTrigger. DaysOfWeek (propiedad)

En el caso de scripting, obtiene o establece los días de la semana en los que se ejecuta la tarea.

## <a name="syntax"></a>Sintaxis


```VB
MonthlyDOWTrigger.DaysOfWeek As short
```



## <a name="property-value"></a>Valor de propiedad

Máscara bit a bit que indica los días de la semana en los que se ejecuta la tarea.

## <a name="remarks"></a>Observaciones

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



 

Al leer o escribir XML para una tarea, los días de la semana de un calendario mensual de día de la semana se especifican mediante el elemento [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MonthlyDOWTrigger**](monthlydowtrigger.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





