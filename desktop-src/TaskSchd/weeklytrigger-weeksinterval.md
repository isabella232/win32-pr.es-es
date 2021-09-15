---
title: WeeklyTrigger.WeeksInterval, propiedad
description: Para el scripting, obtiene o establece el intervalo entre las semanas de la programación.
ms.assetid: 7992dee2-1725-4325-9fe9-eaff84fa5adc
keywords:
- Propiedades weeksInterval Programador de tareas
- Propiedad WeeksInterval Programador de tareas objeto , WeeklyTrigger
- Objeto WeeklyTrigger Programador de tareas propiedad , WeeksInterval
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474638"
---
# <a name="weeklytriggerweeksinterval-property"></a>WeeklyTrigger.WeeksInterval, propiedad

Para el scripting, obtiene o establece el intervalo entre las semanas de la programación.

## <a name="syntax"></a>Sintaxis


```VB
WeeklyTrigger.WeeksInterval As short
```



## <a name="property-value"></a>Valor de propiedad

Intervalo entre las semanas de la programación.

## <a name="remarks"></a>Observaciones

Un intervalo de 1 genera una programación semanal. Un intervalo de 2 genera una programación semanal cada dos semanas.

Al leer o escribir su propio XML para una tarea, el intervalo de una programación semanal se especifica mediante el [**elemento WeeksInterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) del esquema Programador de tareas trabajo.

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

 

 





