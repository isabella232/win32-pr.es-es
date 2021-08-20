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
ms.openlocfilehash: e90dc83c47b37343c41489ca2d7b3288f727086e769e83104b57ca5b6de13b2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681645"
---
# <a name="registeredtask-object"></a>Objeto RegisteredTask

Objeto de scripting que proporciona los métodos que se usan para ejecutar la tarea inmediatamente, obtener las instancias en ejecución de la tarea, obtener o establecer las credenciales que se usan para registrar la tarea y las propiedades que describen la tarea.

## <a name="members"></a>Miembros

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
| [**habilitado**](registeredtask-enabled.md)<br/>                       | Lectura/escritura<br/> | Obtiene o establece un valor booleano que indica si la tarea registrada está habilitada.<br/>  |
| [**LastRunTime**](registeredtask-lastruntime.md)<br/>               | Solo lectura<br/>  | Obtiene la hora de la última ejecución de la tarea registrada.<br/>                                |
| [**LastTaskResult**](registeredtask-lasttaskresult.md)<br/>         | Solo lectura<br/>  | Obtiene los resultados devueltos la última vez que se ha ejecutado la tarea registrada.<br/> |
| [**Nombre**](registeredtask-name.md)<br/>                             | Solo lectura<br/>  | Obtiene el nombre de la tarea registrada.<br/>                                          |
| [**NextRunTime**](registeredtask-nextruntime.md)<br/>               | Solo lectura<br/>  | Obtiene la hora a la que se programa la siguiente ejecución de la tarea registrada.<br/>               |
| [**NumberOfMissedRuns**](registeredtask-numberofmissedruns.md)<br/> | Solo lectura<br/>  | Obtiene el número de veces que la tarea registrada ha perdido una ejecución programada.<br/>       |
| [**Ruta de acceso**](registeredtask-path.md)<br/>                             | Solo lectura<br/>  | Obtiene la ruta de acceso a donde se almacena la tarea registrada.<br/>                          |
| [**Estado**](registeredtask-state.md)<br/>                           | Solo lectura<br/>  | Obtiene el estado operativo de la tarea registrada.<br/>                             |
| [**XML**](registeredtask-xml.md)<br/>                               | Solo lectura<br/>  | Obtiene la información de registro con formato XML para la tarea registrada.<br/>       |



 

## <a name="examples"></a>Ejemplos

Para obtener más información y código de ejemplo para este objeto de scripting, vea Ejemplo de desencadenador de tiempo [(scripting)](time-trigger-example--scripting-.md) y Mostrar nombres y estados de [tarea (scripting).](displaying-task-names-and-state--scripting-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





