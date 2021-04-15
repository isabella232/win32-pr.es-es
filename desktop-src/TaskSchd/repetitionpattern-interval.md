---
title: RepetitionPattern. Interval (propiedad)
description: En el caso de scripting, obtiene o establece la cantidad de tiempo entre cada reinicio de la tarea.
ms.assetid: c48bd304-21f3-435e-99f5-3b2da0078bb8
keywords:
- Propiedad Interval Programador de tareas
- Propiedad Interval Programador de tareas, objeto RepetitionPattern
- Programador de tareas de objeto RepetitionPattern, propiedad Interval
topic_type:
- apiref
api_name:
- RepetitionPattern.Interval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d62bb821f4c5e61d344e21fafa4ba1265c73470
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534600"
---
# <a name="repetitionpatterninterval-property"></a>RepetitionPattern. Interval (propiedad)

En el caso de scripting, obtiene o establece la cantidad de tiempo entre cada reinicio de la tarea.

## <a name="syntax"></a>Sintaxis


```VB
RepetitionPattern.Interval As String
```



## <a name="property-value"></a>Valor de propiedad

Cantidad de tiempo entre cada reinicio de la tarea. El formato de esta cadena es P <days> DT <hours> H <minutes> M <seconds> S (por ejemplo, "PT5M" es de 5 minutos, "PT1H" es 1 hora y "PT20M" es de 20 minutos). El tiempo máximo permitido es de 31 días y el tiempo mínimo permitido es 1 minuto.

## <a name="remarks"></a>Observaciones

Si especifica una duración de repetición para una tarea, también debe especificar el intervalo de repetición.

Al leer o escribir XML para una tarea, el intervalo de repetición se especifica en el elemento [**Interval**](taskschedulerschema-interval-repetitiontype-element.md) del esquema de programador de tareas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





