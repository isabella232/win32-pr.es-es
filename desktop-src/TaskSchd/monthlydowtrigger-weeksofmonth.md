---
title: MonthlyDOWTrigger.WeeksOfMonth, propiedad
description: Para el scripting, obtiene o establece las semanas del mes durante las que se ejecuta la tarea.
ms.assetid: 62c3b654-622e-4a71-b77e-1b3fd5fb46b8
keywords:
- Propiedad WeeksOfMonth Programador de tareas
- Propiedad WeeksOfMonth Programador de tareas objeto , MonthlyDOWTrigger
- Objeto MonthlyDOWTrigger Programador de tareas propiedad , WeeksOfMonth
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073423"
---
# <a name="monthlydowtriggerweeksofmonth-property"></a>MonthlyDOWTrigger.WeeksOfMonth, propiedad

Para el scripting, obtiene o establece las semanas del mes durante las que se ejecuta la tarea.

## <a name="syntax"></a>Sintaxis


```VB
MonthlyDOWTrigger.WeeksOfMonth As short
```



## <a name="property-value"></a>Valor de propiedad

Máscara bit a bit que indica los días de la semana durante los que se ejecuta la tarea.

## <a name="remarks"></a>Observaciones

En la tabla siguiente se muestra la asignación de la máscara bit a bit utilizada por esta propiedad.



| Semana                     | Valor hexadecimal | Valor decimal |
|--------------------------|-----------|---------------|
| Primera semana del mes  | 0X01      | 1             |
| Segunda semana del mes | 0x02      | 2             |
| Tercera semana del mes  | 0X04      | 4             |
| Cuarta semana del mes | 0X08      | 8             |



 

Al leer o escribir XML para una tarea, el elemento Weeks especifica los días de la semana de un calendario mensual del día [**de**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) la semana.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 





