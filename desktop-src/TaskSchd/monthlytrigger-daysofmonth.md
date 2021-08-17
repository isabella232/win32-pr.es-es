---
title: MonthlyTrigger.DaysOfMonth, propiedad
description: Para el scripting, obtiene o establece los días del mes durante los que se ejecuta la tarea.
ms.assetid: 4da80d0f-ae0c-4e56-b51b-6ee6ab309d7c
keywords:
- Propiedad DaysOfMonth Programador de tareas
- Propiedad DaysOfMonth Programador de tareas objeto , MonthlyTrigger
- Objeto MonthlyTrigger Programador de tareas propiedad , DaysOfMonth
topic_type:
- apiref
api_name:
- MonthlyTrigger.DaysOfMonth
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b256295b98105f79b144285d4aec77768f0648fc327be8be29d3f203586fe484
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139408"
---
# <a name="monthlytriggerdaysofmonth-property"></a>MonthlyTrigger.DaysOfMonth, propiedad

Para el scripting, obtiene o establece los días del mes durante los que se ejecuta la tarea.

## <a name="syntax"></a>Syntax


```VB
MonthlyTrigger.DaysOfMonth As long
```



## <a name="property-value"></a>Valor de propiedad

Máscara bit a bit que indica los días del mes durante los que se ejecuta la tarea.

## <a name="remarks"></a>Comentarios



| Día del mes. | Valor hexadecimal  | Valor decimal |
|--------------|------------|---------------|
| 1            | 0x01       | 1             |
| 2            | 0x02       | 2             |
| 3            | 0x04       | 4             |
| 4            | 0x08       | 8             |
| 5            | 0x10       | 16            |
| 6            | 0x20       | 32            |
| 7            | 0x40       | 64            |
| 8            | 0x80       | 128           |
| 9            | 0x100      | 256           |
| 10           | 0x200      | 512           |
| 11           | 0x400      | 1024          |
| 12           | 0x800      | 2048          |
| 13           | 0x1000     | 4096          |
| 14           | 0x2000     | 8192          |
| 15           | 0x4000     | 16384         |
| 16           | 0x8000     | 32 768         |
| 17           | 0x10000    | 65536         |
| 18           | 0x20000    | 131 072        |
| 19           | 0x40000    | 262 144        |
| 20           | 0x80000    | 524 288        |
| 21           | 0x100000   | 1 048 576       |
| 22           | 0x200000   | 2 097 152       |
| 23           | 0x400000   | 4 194 304       |
| 24           | 0x800000   | 8388608       |
| 25           | 0x1000000  | 16777216      |
| 26           | 0x2000000  | 33554432      |
| 27           | 0x4000000  | 67108864      |
| 28           | 0x8000000  | 134217728     |
| 29           | 0x10000000 | 268435456     |
| 30           | 0x20000000 | 536870912     |
| 31           | 0x40000000 | 1073741824    |
| Último         | 0x80000000 | 2147483648    |



 

Al leer o escribir su propio XML para una tarea, los días del mes se especifican mediante el [**elemento DaysOfMonth**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) del esquema Programador de tareas datos.

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
</dt> <dt>

[**MonthlyTrigger**](monthlytrigger.md)
</dt> </dl>

 

 





