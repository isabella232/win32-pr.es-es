---
title: Objeto RegisteredTask
description: Objeto de scripting que proporciona los métodos que se usan para ejecutar la tarea inmediatamente, obtener las instancias en ejecución de la tarea, obtener o establecer las credenciales que se usan para registrar la tarea y las propiedades que describen la tarea.
ms.assetid: d280f22b-4dd1-44df-be12-286fb1c029a3
keywords:
- Objeto RegisteredTask Programador de tareas
- Programador de tareas de objeto RegisteredTask, descrito
topic_type:
- apiref
api_name:
- RegisteredTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7ce300375e5122a7b63266c0cd21cdddf34606b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801502"
---
# <a name="registeredtask-object"></a>Objeto RegisteredTask

Objeto de scripting que proporciona los métodos que se usan para ejecutar la tarea inmediatamente, obtener las instancias en ejecución de la tarea, obtener o establecer las credenciales que se usan para registrar la tarea y las propiedades que describen la tarea.

## <a name="members"></a>Miembros

El objeto **RegisteredTask** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **RegisteredTask** tiene estos métodos.



| Método                                                                | Descripción                                                                                     |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**GetInstances**](registeredtask-getinstances.md)                   | Devuelve todas las instancias de la tarea registrada que se están ejecutando actualmente.<br/>             |
| [**GetRunTimes**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-getruntimes)                    | Obtiene la hora a la que la tarea registrada está programada para ejecutarse durante un período de tiempo especificado.<br/> |
| [**GetSecurityDescriptor**](registeredtask-getsecuritydescriptor.md) | Obtiene el descriptor de seguridad que se usa como credenciales para la tarea registrada.<br/>    |
| [**Ejecutar**](registeredtask-run.md)                                     | Ejecuta la tarea registrada inmediatamente.<br/>                                                |
| [**RunEx**](registeredtask-runex.md)                                 | Ejecuta la tarea registrada inmediatamente con las marcas especificadas y un identificador de sesión.<br/> |
| [**SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md) | Establece el descriptor de seguridad que se usa como credenciales para la tarea registrada.<br/>    |
| [**Stop**](registeredtask-stop.md)                                   | Detiene inmediatamente la tarea registrada.<br/>                                               |



 

### <a name="properties"></a>Propiedades

El objeto **RegisteredTask** tiene estas propiedades.



| Propiedad                                                                   | Tipo de acceso           | Descripción                                                                               |
|:---------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------|
| [**Definición**](registeredtask-definition.md)<br/>                 | Solo lectura<br/>  | Obtiene la definición de la tarea.<br/>                                               |
| [**habilitado**](registeredtask-enabled.md)<br/>                       | Lectura/escritura<br/> | Obtiene o establece un valor booleano que indica si la tarea registrada está habilitada.<br/>  |
| [**LastRunTime**](registeredtask-lastruntime.md)<br/>               | Solo lectura<br/>  | Obtiene la hora en que se ejecutó la tarea registrada por última vez.<br/>                                |
| [**LastTaskResult**](registeredtask-lasttaskresult.md)<br/>         | Solo lectura<br/>  | Obtiene los resultados que se devolvieron la última vez que se ejecutó la tarea registrada.<br/> |
| [**Name**](registeredtask-name.md)<br/>                             | Solo lectura<br/>  | Obtiene el nombre de la tarea registrada.<br/>                                          |
| [**NextRunTime**](registeredtask-nextruntime.md)<br/>               | Solo lectura<br/>  | Obtiene la hora a la que se programa la próxima ejecución de la tarea registrada.<br/>               |
| [**NumberOfMissedRuns**](registeredtask-numberofmissedruns.md)<br/> | Solo lectura<br/>  | Obtiene el número de veces que la tarea registrada ha perdido una ejecución programada.<br/>       |
| [**Ruta**](registeredtask-path.md)<br/>                             | Solo lectura<br/>  | Obtiene la ruta de acceso donde se almacena la tarea registrada.<br/>                          |
| [**State**](registeredtask-state.md)<br/>                           | Solo lectura<br/>  | Obtiene el estado operativo de la tarea registrada.<br/>                             |
| [**XML**](registeredtask-xml.md)<br/>                               | Solo lectura<br/>  | Obtiene la información de registro con formato XML para la tarea registrada.<br/>       |



 

## <a name="examples"></a>Ejemplos

Para obtener más información y código de ejemplo de este objeto de scripting, vea [ejemplo de desencadenador de tiempo (scripting)](time-trigger-example--scripting-.md) y [Mostrar los nombres y Estados de las tareas (scripting)](displaying-task-names-and-state--scripting-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





