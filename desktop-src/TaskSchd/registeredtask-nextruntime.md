---
title: RegisteredTask.NextRunTime, propiedad
description: Para el scripting, obtiene la hora a la que se programa la siguiente ejecución de la tarea registrada.
ms.assetid: f63298a8-c9fa-4fea-ad0b-2c8739aced19
keywords:
- Propiedad NextRunTime Programador de tareas
- Propiedad NextRunTime Programador de tareas , objeto RegisteredTask
- Objeto RegisteredTask Programador de tareas propiedad , NextRunTime
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
ms.openlocfilehash: 850c0215555fd24b729b1d71acaff9fa7083c0f53289f28e4228b8e57ff40e52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060053"
---
# <a name="registeredtasknextruntime-property"></a>RegisteredTask.NextRunTime, propiedad

Para el scripting, obtiene la hora a la que se programa la siguiente ejecución de la tarea registrada.

## <a name="syntax"></a>Syntax


```VB
RegisteredTask.NextRunTime As String
```



## <a name="property-value"></a>Valor de propiedad

Hora a la que se programa la siguiente ejecución de la tarea registrada.

## <a name="remarks"></a>Comentarios

Si la tarea registrada contiene desencadenadores que están deshabilitados individualmente, estos desencadenadores seguirán afectando al siguiente tiempo de ejecución programado que se devuelve aunque estén deshabilitados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





