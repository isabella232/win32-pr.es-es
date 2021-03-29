---
title: Propiedad RegisteredTask. State
description: En el caso de scripting, obtiene el estado operativo de la tarea registrada.
ms.assetid: 1acd4946-322f-4f24-b317-92be80e19de5
keywords:
- Programador de tareas de propiedad de estado
- Propiedad State Programador de tareas, objeto RegisteredTask
- Programador de tareas de objeto RegisteredTask, propiedad State
topic_type:
- apiref
api_name:
- RegisteredTask.State
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47af082174bc6927a16760e87566f311ec9f4a14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492802"
---
# <a name="registeredtaskstate-property"></a>Propiedad RegisteredTask. State

En el caso de scripting, obtiene el estado operativo de la tarea registrada.

## <a name="syntax"></a>Sintaxis


```VB
RegisteredTask.State As Integer
```



## <a name="property-value"></a>Valor de propiedad

Constante [**de \_ Estado de tarea**](/windows/desktop/api/taskschd/ne-taskschd-task_state) que define el estado operativo de la tarea.



| Value                                                                                                                                                                                                                                   | Significado                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_STATE_UNKNOWN"></span><span id="task_state_unknown"></span><dl> <dt>**Tarea \_ de ESTADO \_ desconocido**</dt> <dt>0</dt> </dl>    | No se conoce el estado de la tarea.<br/>                                                                                                      |
| <span id="TASK_STATE_DISABLED"></span><span id="task_state_disabled"></span><dl> <dt>**Tarea \_ de ESTADO \_ deshabilitado**</dt> <dt>1</dt> </dl> | La tarea está registrada, pero está deshabilitada y ninguna instancia de la tarea está en cola o en ejecución. La tarea no se puede ejecutar hasta que se habilite.<br/> |
| <span id="TASK_STATE_QUEUED"></span><span id="task_state_queued"></span><dl> <dt>**Tarea \_ de ESTADO \_ en cola**</dt> <dt>2</dt> </dl>       | Las instancias de la tarea se ponen en cola.<br/>                                                                                                      |
| <span id="TASK_STATE_READY"></span><span id="task_state_ready"></span><dl> <dt>**Tarea \_ de ESTADO \_ preparado**</dt> <dt>3</dt> </dl>          | La tarea está lista para ejecutarse, pero no hay ninguna instancia en cola o en ejecución.<br/>                                                              |
| <span id="TASK_STATE_RUNNING"></span><span id="task_state_running"></span><dl> <dt>**Tarea \_ de Estado en \_ ejecución**</dt> <dt>4</dt> </dl>    | Se están ejecutando una o varias instancias de la tarea.<br/>                                                                                         |



 

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

 

 





