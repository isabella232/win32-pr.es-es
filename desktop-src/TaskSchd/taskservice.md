---
title: Objeto TaskService
description: Para el scripting, proporciona acceso al servicio Programador de tareas para administrar las tareas registradas.
ms.assetid: 6ddd43dc-d027-4792-a53b-07fe4d4a3576
keywords:
- Objeto TaskService Programador de tareas
- Objeto TaskService Programador de tareas , descrito
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968555"
---
# <a name="taskservice-object"></a>Objeto TaskService

Para el scripting, proporciona acceso al servicio Programador de tareas para administrar las tareas registradas.

Se [**debe llamar al Conectar TaskService.Conectar**](taskservice-connect.md) antes de llamar a cualquiera de los otros **métodos TaskService.**

## <a name="members"></a>Members

El **objeto TaskService** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto TaskService** tiene estos métodos.



| Método                                                 | Descripción                                                                                                                                                                                                          |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Conectar**](taskservice-connect.md)                 | Se conecta a un equipo remoto y asocia todas las llamadas posteriores en esta interfaz a una sesión remota.<br/>                                                                                                 |
| [**Getfolder**](taskservice-getfolder.md)             | Obtiene la ruta de acceso a una carpeta de tareas registradas.<br/>                                                                                                                                                            |
| [**GetRunningTasks**](taskservice-getrunningtasks.md) | Obtiene una colección de tareas en ejecución.<br/>                                                                                                                                                                       |
| [**NewTask**](taskservice-newtask.md)                 | Devuelve un objeto de definición de tarea vacío que se va a rellenar con valores y propiedades y, a continuación, se registra mediante el [**método TaskFolder.RegisterTaskDefinition.**](taskfolder-registertaskdefinition.md)<br/> |



 

### <a name="properties"></a>Propiedades

El **objeto TaskService** tiene estas propiedades.



| Propiedad                                                          | Descripción                                                                                                                 |
|:------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**Conectado**](taskservice-connected.md)<br/>             | Obtiene un valor booleano que indica si está conectado al servicio Programador de tareas trabajo.<br/>                          |
| [**ConnectedDomain**](taskservice-connecteddomain.md)<br/> | Obtiene el nombre del dominio al que está conectado el equipo [**TargetServer.**](taskservice-targetserver.md)<br/> |
| [**ConnectedUser**](taskservice-connecteduser.md)<br/>     | Obtiene el nombre del usuario que está conectado al servicio Programador de tareas usuario.<br/>                                       |
| HighestVersion<br/>                                         | Obtiene la versión más alta Programador de tareas que admite un equipo.<br/>                                             |
| [**TargetServer**](taskservice-targetserver.md)<br/>       | Obtiene el nombre del equipo que ejecuta el Programador de tareas al que está conectado el usuario.<br/>          |



 

## <a name="examples"></a>Ejemplos

Para obtener más información y código de ejemplo para este objeto de scripting, vea Ejemplo de desencadenador de tiempo [(scripting),](time-trigger-example--scripting-.md)Ejemplo de desencadenador de eventos [(scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), Ejemplo de desencadenador diario [(scripting),](daily-trigger-example--scripting-.md)Ejemplo de desencadenador de registro [(scripting)](registration-trigger-example--scripting-.md), Ejemplo de desencadenador semanal [(scripting)](weekly-trigger-example--scripting-.md), Ejemplo de desencadenador de inicio [(scripting)](logon-trigger-example--scripting-.md), Ejemplo de desencadenador de arranque [(scripting)](boot-trigger-example--scripting-.md)o Mostrar nombres y estados de tareas [(scripting).](displaying-task-names-and-state--scripting-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





