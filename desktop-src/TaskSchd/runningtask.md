---
title: Objeto RunningTask
description: Objeto de scripting que proporciona los métodos para obtener información de una tarea en ejecución y controlarla.
ms.assetid: 335e69d8-affa-4845-a067-641184e0f7df
keywords:
- Objeto RunningTask Programador de tareas
- Objeto RunningTask Programador de tareas , descrito
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172806"
---
# <a name="runningtask-object"></a>Objeto RunningTask

Objeto de scripting que proporciona los métodos para obtener información de una tarea en ejecución y controlarla.

## <a name="members"></a>Members

El **objeto RunningTask** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto RunningTask** tiene estos métodos.



| Método                                 | Descripción                                                           |
|:---------------------------------------|:----------------------------------------------------------------------|
| [**Actualizar**](runningtask-refresh.md) | Actualiza todas las variables de instancia local de la tarea.<br/> |
| [**Stop**](runningtask-stop.md)       | Detiene esta instancia de la tarea.<br/>                           |



 

### <a name="properties"></a>Propiedades

El **objeto RunningTask** tiene estas propiedades.



| Propiedad                                                      | Tipo de acceso          | Descripción                                                                         |
|:--------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [**CurrentAction**](runningtask-currentaction.md)<br/> | Solo lectura<br/> | Obtiene el nombre de la acción actual que está realizando la tarea en ejecución.<br/> |
| [**EnginePID**](runningtask-enginepid.md)<br/>         | Solo lectura<br/> | Obtiene el identificador de proceso del motor (proceso) que ejecuta la tarea.<br/>  |
| [**InstanceGuid**](runningtask-instanceguid.md)<br/>   | Solo lectura<br/> | Obtiene el identificador GUID de esta instancia de la tarea.<br/>                  |
| [**Nombre**](runningtask-name.md)<br/>                   | Solo lectura<br/> | Obtiene el nombre de la tarea.<br/>                                               |
| [**Path**](runningtask-path.md)<br/>                   | Solo lectura<br/> | Obtiene la ruta de acceso a donde se almacena la tarea.<br/>                               |
| [**Estado**](runningtask-state.md)<br/>                 | Solo lectura<br/> | Obtiene el estado de la tarea en ejecución. <br/>                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas objetos](task-scheduler-objects.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> <dt>

[**RunningTaskCollection**](runningtaskcollection.md)
</dt> <dt>

[**RegisteredTask.Run**](registeredtask-run.md)
</dt> <dt>

[**RegisteredTask.RunEx**](registeredtask-runex.md)
</dt> </dl>

 

 





