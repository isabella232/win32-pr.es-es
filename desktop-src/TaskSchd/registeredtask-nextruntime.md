---
title: Propiedad RegisteredTask. NextRunTime
description: En el caso de scripting, obtiene la hora a la que se programa la próxima ejecución de la tarea registrada.
ms.assetid: f63298a8-c9fa-4fea-ad0b-2c8739aced19
keywords:
- Programador de tareas de la propiedad NextRunTime
- Programador de tareas de la propiedad NextRunTime, objeto RegisteredTask
- Programador de tareas de objeto RegisteredTask, propiedad NextRunTime
topic_type:
- apiref
api_name:
- RegisteredTask.NextRunTime
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94db26c023ddd2c146586fbc433548517a84f234
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803235"
---
# <a name="registeredtasknextruntime-property"></a>Propiedad RegisteredTask. NextRunTime

En el caso de scripting, obtiene la hora a la que se programa la próxima ejecución de la tarea registrada.

## <a name="syntax"></a>Sintaxis


```VB
RegisteredTask.NextRunTime As String
```



## <a name="property-value"></a>Valor de propiedad

La hora a la que se ha programado la próxima ejecución de la tarea registrada.

## <a name="remarks"></a>Observaciones

Si la tarea registrada contiene desencadenadores que se deshabilitan de forma individual, estos desencadenadores todavía afectarán a la siguiente hora de ejecución programada que se devuelva aunque estén deshabilitados.

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
</dt> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





