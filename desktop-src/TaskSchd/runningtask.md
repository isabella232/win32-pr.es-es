---
title: Objeto RunningTask
description: Objeto de scripting que proporciona los métodos para obtener información y controlar una tarea en ejecución.
ms.assetid: 335e69d8-affa-4845-a067-641184e0f7df
keywords:
- Objeto RunningTask Programador de tareas
- Programador de tareas de objeto RunningTask, descrito
topic_type:
- apiref
api_name:
- RunningTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 261be07f71d0d35f5d3140de1b39574b635a531e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534594"
---
# <a name="runningtask-object"></a>Objeto RunningTask

Objeto de scripting que proporciona los métodos para obtener información y controlar una tarea en ejecución.

## <a name="members"></a>Miembros

El objeto **RunningTask** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **RunningTask** tiene estos métodos.



| Método                                 | Descripción                                                           |
|:---------------------------------------|:----------------------------------------------------------------------|
| [**Actualizar**](runningtask-refresh.md) | Actualiza todas las variables de instancia local de la tarea.<br/> |
| [**Stop**](runningtask-stop.md)       | Detiene esta instancia de la tarea.<br/>                           |



 

### <a name="properties"></a>Propiedades

El objeto **RunningTask** tiene estas propiedades.



| Propiedad                                                      | Tipo de acceso          | Descripción                                                                         |
|:--------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [**CurrentAction**](runningtask-currentaction.md)<br/> | Solo lectura<br/> | Obtiene el nombre de la acción actual que está realizando la tarea en ejecución.<br/> |
| [**EnginePID**](runningtask-enginepid.md)<br/>         | Solo lectura<br/> | Obtiene el identificador de proceso del motor (proceso) que está ejecutando la tarea.<br/>  |
| [**Valor FileStream**](runningtask-instanceguid.md)<br/>   | Solo lectura<br/> | Obtiene el identificador GUID para esta instancia de la tarea.<br/>                  |
| [**Name**](runningtask-name.md)<br/>                   | Solo lectura<br/> | Obtiene el nombre de la tarea.<br/>                                               |
| [**Ruta**](runningtask-path.md)<br/>                   | Solo lectura<br/> | Obtiene la ruta de acceso donde se almacena la tarea.<br/>                               |
| [**State**](runningtask-state.md)<br/>                 | Solo lectura<br/> | Obtiene el estado de la tarea en ejecución. <br/>                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos Programador de tareas](task-scheduler-objects.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> <dt>

[**RunningTaskCollection**](runningtaskcollection.md)
</dt> <dt>

[**RegisteredTask. Run**](registeredtask-run.md)
</dt> <dt>

[**RegisteredTask.RunEx**](registeredtask-runex.md)
</dt> </dl>

 

 





