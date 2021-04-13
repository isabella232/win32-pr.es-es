---
title: Propiedad MonthlyDOWTrigger. WeeksOfMonth
description: En el caso de scripting, obtiene o establece las semanas del mes en las que se ejecuta la tarea.
ms.assetid: 62c3b654-622e-4a71-b77e-1b3fd5fb46b8
keywords:
- Programador de tareas de la propiedad WeeksOfMonth
- Programador de tareas de la propiedad WeeksOfMonth, objeto MonthlyDOWTrigger
- Programador de tareas de objeto MonthlyDOWTrigger, propiedad WeeksOfMonth
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.WeeksOfMonth
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7efea628e6eefdef07bdc50b9719a7c404f78bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489700"
---
# <a name="monthlydowtriggerweeksofmonth-property"></a>Propiedad MonthlyDOWTrigger. WeeksOfMonth

En el caso de scripting, obtiene o establece las semanas del mes en las que se ejecuta la tarea.

## <a name="syntax"></a>Sintaxis


```VB
MonthlyDOWTrigger.WeeksOfMonth As short
```



## <a name="property-value"></a>Valor de propiedad

Máscara bit a bit que indica los días de la semana en los que se ejecuta la tarea.

## <a name="remarks"></a>Observaciones

En la tabla siguiente se muestra la asignación de la máscara bit a bit utilizada por esta propiedad.



| Semana                     | Valor hexadecimal | Valor decimal |
|--------------------------|-----------|---------------|
| Primera semana del mes  | 0X01      | 1             |
| Segunda semana del mes | 0x02      | 2             |
| Tercera semana del mes  | 0X04      | 4             |
| Cuarta semana del mes | 0X08      | 8             |



 

Al leer o escribir XML para una tarea, los días de la semana de un calendario mensual de día de la semana se especifican mediante el elemento [**weeks**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) .

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

 

 





