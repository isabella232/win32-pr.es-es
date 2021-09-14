---
title: MonthlyTrigger.MonthsOfYear, propiedad
description: Para el scripting, obtiene o establece los meses del año durante los que se ejecuta la tarea. | MonthlyTrigger.MonthsOfYear, propiedad
ms.assetid: cf26a815-7f4f-4b7a-8db8-a4bd9b77cf49
keywords:
- Propiedad MonthsOfYear Programador de tareas
- Propiedad MonthsOfYear Programador de tareas , objeto MonthlyTrigger
- Objeto MonthlyTrigger Programador de tareas propiedad , MonthsOfYear
topic_type:
- apiref
api_name:
- MonthlyTrigger.MonthsOfYear
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5683fb1c85e470ca7c82b069929de0351ea7cffe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170669"
---
# <a name="monthlytriggermonthsofyear-property"></a>MonthlyTrigger.MonthsOfYear, propiedad

Para el scripting, obtiene o establece los meses del año durante los que se ejecuta la tarea.

## <a name="syntax"></a>Sintaxis


```VB
MonthlyTrigger.MonthsOfYear As short
```



## <a name="property-value"></a>Valor de propiedad

Máscara bit a bit que indica los meses del año durante los que se ejecuta la tarea.

## <a name="remarks"></a>Observaciones

En la tabla siguiente se muestra la asignación de la máscara bit a bit que usa esta propiedad.



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



 

Al leer o escribir su propio XML para una tarea, los meses del año se especifican mediante el elemento [**Months**](taskschedulerschema-months-monthlyscheduletype-element.md) del Programador de tareas esquema.

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

 

 





