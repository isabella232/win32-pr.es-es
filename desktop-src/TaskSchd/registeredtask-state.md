---
title: RegisteredTask.State, propiedad
description: Para el scripting, obtiene el estado operativo de la tarea registrada.
ms.assetid: 1acd4946-322f-4f24-b317-92be80e19de5
keywords:
- Estado de la propiedad Programador de tareas
- Propiedad State Programador de tareas , objeto RegisteredTask
- Objeto RegisteredTask Programador de tareas , propiedad State
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172957"
---
# <a name="registeredtaskstate-property"></a>RegisteredTask.State, propiedad

Para el scripting, obtiene el estado operativo de la tarea registrada.

## <a name="syntax"></a>Sintaxis


```VB
RegisteredTask.State As Integer
```



## <a name="property-value"></a>Valor de propiedad

Constante [**TASK \_ STATE**](/windows/desktop/api/taskschd/ne-taskschd-task_state) que define el estado operativo de la tarea.



| Value                                                                                                                                                                                                                                   | Significado                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_STATE_UNKNOWN"></span><span id="task_state_unknown"></span><dl> <dt>**TASK \_ STATE \_ UNKNOWN**</dt> <dt>0</dt> </dl>    | Se desconoce el estado de la tarea.<br/>                                                                                                      |
| <span id="TASK_STATE_DISABLED"></span><span id="task_state_disabled"></span><dl> <dt>**TASK \_ ESTADO \_ DESHABILITADO**</dt> <dt>1</dt> </dl> | La tarea está registrada, pero está deshabilitada y no hay ninguna instancia de la tarea en cola o en ejecución. La tarea no se puede ejecutar hasta que esté habilitada.<br/> |
| <span id="TASK_STATE_QUEUED"></span><span id="task_state_queued"></span><dl> <dt>**TASK \_ ESTADO \_ EN COLA**</dt> <dt>2</dt> </dl>       | Las instancias de la tarea se ponen en cola.<br/>                                                                                                      |
| <span id="TASK_STATE_READY"></span><span id="task_state_ready"></span><dl> <dt>**TASK \_ STATE \_ READY**</dt> <dt>3</dt> </dl>          | La tarea está lista para ejecutarse, pero no hay instancias en cola ni en ejecución.<br/>                                                              |
| <span id="TASK_STATE_RUNNING"></span><span id="task_state_running"></span><dl> <dt>**TASK \_ STATE \_ RUNNING**</dt> <dt>4</dt> </dl>    | Se están ejecutando una o varias instancias de la tarea.<br/>                                                                                         |



 

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

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





