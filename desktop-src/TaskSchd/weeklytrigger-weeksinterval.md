---
title: Propiedad WeeklyTrigger. WeeksInterval
description: En el caso de scripting, obtiene o establece el intervalo entre las semanas de la programación.
ms.assetid: 7992dee2-1725-4325-9fe9-eaff84fa5adc
keywords:
- Programador de tareas de la propiedad WeeksInterval
- Programador de tareas de la propiedad WeeksInterval, objeto WeeklyTrigger
- Programador de tareas de objeto WeeklyTrigger, propiedad WeeksInterval
topic_type:
- apiref
api_name:
- WeeklyTrigger.WeeksInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4668b68d0b3f83e096284db35df799a63eb677b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685876"
---
# <a name="weeklytriggerweeksinterval-property"></a>Propiedad WeeklyTrigger. WeeksInterval

En el caso de scripting, obtiene o establece el intervalo entre las semanas de la programación.

## <a name="syntax"></a>Sintaxis


```VB
WeeklyTrigger.WeeksInterval As short
```



## <a name="property-value"></a>Valor de propiedad

Intervalo entre las semanas de la programación.

## <a name="remarks"></a>Observaciones

Un intervalo de 1 genera una programación semanal. Un intervalo de 2 genera una programación de cada semana.

Al leer o escribir su propio XML para una tarea, el intervalo de una programación semanal se especifica mediante el elemento [**WeeksInterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) del esquema de programador de tareas.

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

 

 





