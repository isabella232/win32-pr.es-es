---
title: Propiedad MonthlyDOWTrigger. MonthsOfYear
description: En el caso de scripting, obtiene o establece los meses del año en los que se ejecuta la tarea. | Propiedad MonthlyDOWTrigger. MonthsOfYear
ms.assetid: 4ab7ab43-9c9b-4cd3-be8f-1989b83e8cf3
keywords:
- Programador de tareas de la propiedad MonthsOfYear
- Programador de tareas de la propiedad MonthsOfYear, objeto MonthlyDOWTrigger
- Programador de tareas de objeto MonthlyDOWTrigger, propiedad MonthsOfYear
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.MonthsOfYear
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c345cd3de12d7dba3450f62bdb18bfdcee496b13
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914597"
---
# <a name="monthlydowtriggermonthsofyear-property"></a>Propiedad MonthlyDOWTrigger. MonthsOfYear

En el caso de scripting, obtiene o establece los meses del año en los que se ejecuta la tarea.

## <a name="syntax"></a>Sintaxis


```VB
MonthlyDOWTrigger.MonthsOfYear As short
```



## <a name="property-value"></a>Valor de propiedad

Máscara bit a bit que indica los meses del año en los que se ejecuta la tarea.

## <a name="remarks"></a>Observaciones

En la tabla siguiente se muestra la asignación de la máscara bit a bit utilizada por esta propiedad.



| Mes     | Valor hexadecimal | Valor decimal |
|-----------|-----------|---------------|
| January   | 0X01      | 1             |
| February  | 0x02      | 2             |
| Marzo     | 0X04      | 4             |
| April     | 0X08      | 8             |
| May       | 0X10      | 16            |
| Junio      | 0X20      | 32            |
| Julio      | 0x40      | 64            |
| Agosto    | 0X80      | 128           |
| Septiembre | 0X100     | 256           |
| Octubre   | 0X200     | 512           |
| Noviembre  | 0X400     | 1024          |
| Diciembre  | 0X800     | 2048          |



 

Al leer o escribir XML para una tarea, los meses del año de un calendario mensual de día de la semana se especifican mediante el elemento [**months**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) del esquema de programador de tareas.

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

 

 





