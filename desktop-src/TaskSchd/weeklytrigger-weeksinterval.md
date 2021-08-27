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
ms.openlocfilehash: 547ebc8617d625df3dd0e8dba167bb60682185dfb13897c49524d1894789c933
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080265"
---
# <a name="weeklytriggerweeksinterval-property"></a>WeeklyTrigger.WeeksInterval, propiedad

Para el scripting, obtiene o establece el intervalo entre las semanas de la programación.

## <a name="syntax"></a>Syntax


```VB
WeeklyTrigger.WeeksInterval As short
```



## <a name="property-value"></a>Valor de propiedad

Intervalo entre las semanas de la programación.

## <a name="remarks"></a>Comentarios

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

 

 





