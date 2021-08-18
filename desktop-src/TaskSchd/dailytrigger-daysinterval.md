---
title: DailyTrigger.DaysInterval, propiedad
description: Para el scripting, obtiene o establece el intervalo entre los días de la programación.
ms.assetid: 13e9f6fd-62ee-4b19-8b3d-a6808e146340
keywords:
- Propiedad DaysInterval Programador de tareas
- Propiedad DaysInterval Programador de tareas , objeto DailyTrigger
- Objeto DailyTrigger Programador de tareas , propiedad DaysInterval
topic_type:
- apiref
api_name:
- DailyTrigger.DaysInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4355e6c2a26b197224141018fa5a1d85e7d31e211ac47dc84a9e8c9ef3750fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139498"
---
# <a name="dailytriggerdaysinterval-property"></a>DailyTrigger.DaysInterval, propiedad

Para el scripting, obtiene o establece el intervalo entre los días de la programación.

## <a name="syntax"></a>Syntax


```VB
DailyTrigger.DaysInterval As short
```



## <a name="property-value"></a>Valor de propiedad

Intervalo entre los días de la programación.

## <a name="remarks"></a>Comentarios

Un intervalo de 1 genera una programación diaria. Un intervalo de 2 genera una programación cada dos días.

Al leer o escribir su propio XML para una tarea, el intervalo de una programación diaria se especifica mediante el elemento [**DaysInterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) del Programador de tareas esquema.

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

[**DailyTrigger**](dailytrigger.md)
</dt> </dl>

 

 





