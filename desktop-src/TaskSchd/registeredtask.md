---
title: Objeto RegisteredTask
description: Objeto de scripting que proporciona los métodos que se usan para ejecutar la tarea inmediatamente, obtener las instancias en ejecución de la tarea, obtener o establecer las credenciales que se usan para registrar la tarea y las propiedades que describen la tarea.
ms.assetid: d280f22b-4dd1-44df-be12-286fb1c029a3
keywords:
- Registro de objetos RegisteredTask Programador de tareas
- Objeto RegisteredTask Programador de tareas , descrito
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172945"
---
# <a name="registeredtask-object"></a>Objeto RegisteredTask

Objeto de scripting que proporciona los métodos que se usan para ejecutar la tarea inmediatamente, obtener las instancias en ejecución de la tarea, obtener o establecer las credenciales que se usan para registrar la tarea y las propiedades que describen la tarea.

## <a name="members"></a>Members

El **objeto RegisteredTask** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto RegisteredTask** tiene estos métodos.



| Método                                                                | Descripción                                                                                     |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**GetInstances**](registeredtask-getinstances.md)                   | Devuelve todas las instancias de la tarea registrada que se están ejecutando actualmente.<br/>             |
| [**GetRunTimes**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-getruntimes)                    | Obtiene las horas a las que está programada la ejecución de la tarea registrada durante un tiempo especificado.<br/> |
| [**GetSecurityDescriptor**](registeredtask-getsecuritydescriptor.md) | Obtiene el descriptor de seguridad que se usa como credenciales para la tarea registrada.<br/>    |
| [**Ejecutar**](registeredtask-run.md)                                     | Ejecuta la tarea registrada inmediatamente.<br/>                                                |
| [**RunEx**](registeredtask-runex.md)                                 | Ejecuta la tarea registrada inmediatamente con las marcas especificadas y un identificador de sesión.<br/> |
| [**SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md) | Establece el descriptor de seguridad que se usa como credenciales para la tarea registrada.<br/>    |
| [**Stop**](registeredtask-stop.md)                                   | Detiene la tarea registrada inmediatamente.<br/>                                               |



 

### <a name="properties"></a>Propiedades

El **objeto RegisteredTask** tiene estas propiedades.



| Propiedad                                                                   | Tipo de acceso           | Descripción                                                                               |
|:---------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------|
| [**Definición**](registeredtask-definition.md)<br/>                 | Solo lectura<br/>  | Obtiene la definición de la tarea.<br/>                                               |
| [**Enabled**](registeredtask-enabled.md)<br/>                       | Lectura y escritura<br/> | Obtiene o establece un valor booleano que indica si la tarea registrada está habilitada.<br/>  |
| [**LastRunTime**](registeredtask-lastruntime.md)<br/>               | Solo lectura<br/>  | Obtiene la hora de la última ejecución de la tarea registrada.<br/>                                |
| [**LastTaskResult**](registeredtask-lasttaskresult.md)<br/>         | Solo lectura<br/>  | Obtiene los resultados devueltos la última vez que se ha ejecutado la tarea registrada.<br/> |
| [**Nombre**](registeredtask-name.md)<br/>                             | Solo lectura<br/>  | Obtiene el nombre de la tarea registrada.<br/>                                          |
| [**NextRunTime**](registeredtask-nextruntime.md)<br/>               | Solo lectura<br/>  | Obtiene la hora a la que se programa la siguiente ejecución de la tarea registrada.<br/>               |
| [**NumberOfMissedRuns**](registeredtask-numberofmissedruns.md)<br/> | Solo lectura<br/>  | Obtiene el número de veces que la tarea registrada ha perdido una ejecución programada.<br/>       |
| [**Path**](registeredtask-path.md)<br/>                             | Solo lectura<br/>  | Obtiene la ruta de acceso a donde se almacena la tarea registrada.<br/>                          |
| [**State**](registeredtask-state.md)<br/>                           | Solo lectura<br/>  | Obtiene el estado operativo de la tarea registrada.<br/>                             |
| [**XML**](registeredtask-xml.md)<br/>                               | Solo lectura<br/>  | Obtiene la información de registro con formato XML para la tarea registrada.<br/>       |



 

## <a name="examples"></a>Ejemplos

Para obtener más información y código de ejemplo para este objeto de scripting, vea Ejemplo de desencadenador de tiempo [(scripting)](time-trigger-example--scripting-.md) y Mostrar nombres y estados de [tarea (scripting).](displaying-task-names-and-state--scripting-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





