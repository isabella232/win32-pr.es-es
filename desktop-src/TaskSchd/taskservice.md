---
title: Objeto TaskService
description: En el caso de scripting, proporciona acceso al servicio Programador de tareas para administrar tareas registradas.
ms.assetid: 6ddd43dc-d027-4792-a53b-07fe4d4a3576
keywords:
- Objeto TaskService Programador de tareas
- Programador de tareas de objeto TaskService, descrito
topic_type:
- apiref
api_name:
- TaskService
- HighestVersion
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 762cd2445c3c6b720bba0f01ae48b787abc1fb38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492263"
---
# <a name="taskservice-object"></a>Objeto TaskService

En el caso de scripting, proporciona acceso al servicio Programador de tareas para administrar tareas registradas.

Se debe llamar al método [**TaskService. Connect**](taskservice-connect.md) antes de llamar a cualquiera de los otros métodos **TaskService** .

## <a name="members"></a>Miembros

El objeto **TaskService** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **TaskService** tiene estos métodos.



| Método                                                 | Descripción                                                                                                                                                                                                          |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Conectar**](taskservice-connect.md)                 | Se conecta a un equipo remoto y asocia todas las llamadas subsiguientes en esta interfaz a una sesión remota.<br/>                                                                                                 |
| [**GetFolder**](taskservice-getfolder.md)             | Obtiene la ruta de acceso a una carpeta de tareas registradas.<br/>                                                                                                                                                            |
| [**GetRunningTasks**](taskservice-getrunningtasks.md) | Obtiene una colección de tareas en ejecución.<br/>                                                                                                                                                                       |
| [**NewTask**](taskservice-newtask.md)                 | Devuelve un objeto de definición de tarea vacía que se rellenará con la configuración y las propiedades y, a continuación, se registrará mediante el método [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .<br/> |



 

### <a name="properties"></a>Propiedades

El objeto **TaskService** tiene estas propiedades.



| Propiedad                                                          | Descripción                                                                                                                 |
|:------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**Conectado**](taskservice-connected.md)<br/>             | Obtiene un valor booleano que indica si está conectado al servicio de Programador de tareas.<br/>                          |
| [**ConnectedDomain**](taskservice-connecteddomain.md)<br/> | Obtiene el nombre del dominio al que está conectado el equipo [**TargetServer**](taskservice-targetserver.md) .<br/> |
| [**ConnectedUser**](taskservice-connecteduser.md)<br/>     | Obtiene el nombre del usuario que está conectado al servicio de Programador de tareas.<br/>                                       |
| HighestVersion<br/>                                         | Obtiene la versión más alta de Programador de tareas que admite un equipo.<br/>                                             |
| [**TargetServer**](taskservice-targetserver.md)<br/>       | Obtiene el nombre del equipo que está ejecutando el servicio Programador de tareas al que está conectado el usuario.<br/>          |



 

## <a name="examples"></a>Ejemplos

Para obtener más información y código de ejemplo de este objeto de scripting, vea [ejemplo de desencadenador de tiempo (scripting)](time-trigger-example--scripting-.md), [ejemplo de desencadenador de eventos (scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), ejemplo de [desencadenador diario (](daily-trigger-example--scripting-.md)scripting), ejemplo de [desencadenador de registro (scripting](registration-trigger-example--scripting-.md)), [ejemplo de desencadenador semanal (scripting)](weekly-trigger-example--scripting-.md), [ejemplo de desencadenador de inicio de sesión (](logon-trigger-example--scripting-.md)scripting), [ejemplo de desencadenador de arranque (](boot-trigger-example--scripting-.md)scripting) o [visualización](displaying-task-names-and-state--scripting-.md)de

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

 

 





