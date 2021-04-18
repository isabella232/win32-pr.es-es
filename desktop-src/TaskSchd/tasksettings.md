---
title: Objeto TaskSettings
description: Objeto de scripting que proporciona la configuración que usa el servicio de Programador de tareas para realizar la tarea.
ms.assetid: f2ba952b-7864-467d-8709-eb6995dd5df5
keywords:
- Objeto TaskSettings Programador de tareas
- Programador de tareas de objeto TaskSettings, descrito
topic_type:
- apiref
api_name:
- TaskSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e7690ba59b4794f952ca3b381fc28247f0dfb4e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676619"
---
# <a name="tasksettings-object"></a>Objeto TaskSettings

Objeto de scripting que proporciona la configuración que usa el servicio de Programador de tareas para realizar la tarea.

## <a name="members"></a>Miembros

El objeto **TaskSettings** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **TaskSettings** tiene estas propiedades.



| Propiedad                                                                                 | Tipo de acceso           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllowDemandStart**](tasksettings-allowdemandstart.md)<br/>                     | Lectura/escritura<br/> | Obtiene o establece un valor booleano que indica que la tarea se puede iniciar con el comando ejecutar o el menú contextual.<br/>                                                                                                                                                                                                                                                                                     |
| [**AllowHardTerminate**](tasksettings-allowhardterminate.md)<br/>                 | Lectura/escritura<br/> | Obtiene o establece un valor booleano que indica que la tarea se puede finalizar mediante [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess).<br/>                                                                                                                                                                                                                                                                               |
| [**Compatibilidad**](tasksettings-compatibility.md)<br/>                           | Lectura/escritura<br/> | Obtiene o establece un valor entero que indica la versión de Programador de tareas que una tarea es compatible con.<br/>                                                                                                                                                                                                                                                                                                           |
| [**DeleteExpiredTaskAfter**](tasksettings-deleteexpiredtaskafter.md)<br/>         | Lectura/escritura<br/> | Obtiene o establece la cantidad de tiempo que esperará el Programador de tareas antes de eliminar la tarea después de que expire.<br/>                                                                                                                                                                                                                                                                                                      |
| [**DisallowStartIfOnBatteries**](tasksettings-disallowstartifonbatteries.md)<br/> | Lectura/escritura<br/> | Obtiene o establece un valor booleano que indica que la tarea no se iniciará si el equipo se está ejecutando con batería.<br/>                                                                                                                                                                                                                                                                                        |
| [**habilitado**](tasksettings-enabled.md)<br/>                                       | Lectura/escritura<br/> | Obtiene o establece un valor booleano que indica que la tarea está habilitada. La tarea solo se puede realizar cuando este valor es true.<br/>                                                                                                                                                                                                                                                                                   |
| [**ExecutionTimeLimit**](tasksettings-executiontimelimit.md)<br/>                 | Lectura/escritura<br/> | Obtiene o establece la cantidad de tiempo permitido para completar la tarea.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| [**Plusvalía**](tasksettings-hidden.md)<br/>                                         | Lectura/escritura<br/> | Obtiene o establece un valor booleano que indica que la tarea no estará visible en la interfaz de usuario. Sin embargo, los administradores pueden invalidar esta configuración mediante el uso de un "modificador principal" que hace que todas las tareas sean visibles en la interfaz de usuario.<br/>                                                                                                                                                                                           |
| [**IdleSettings**](tasksettings-idlesettings.md)<br/>                             | Lectura/escritura<br/> | Obtiene o establece la información que especifica cómo realiza el Programador de tareas las tareas cuando el equipo está en un estado de inactividad.<br/>                                                                                                                                                                                                                                                                                          |
| [**MultipleInstances**](tasksettings-multipleinstances.md)<br/>                   | Lectura/escritura<br/> | Obtiene o establece la Directiva que define cómo el Programador de tareas trabaja con varias instancias de la tarea.<br/>                                                                                                                                                                                                                                                                                                            |
| [**NetworkSettings**](tasksettings-networksettings.md)<br/>                       | Lectura/escritura<br/> | Obtiene o establece el objeto de configuración de red que contiene un identificador y un nombre de Perfil de red. Si la propiedad [**RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md) de **TaskSettings** es **true** y se especifica una Propfile de red en la propiedad [**NetworkSettings**](tasksettings-networksettings.md) , la tarea se ejecutará solo si el perfil de red especificado está disponible.<br/> |
| [**Priority**](tasksettings-priority.md)<br/>                                     | Lectura/escritura<br/> | Obtiene o establece el nivel de prioridad de la tarea.<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| [**RestartCount**](tasksettings-restartcount.md)<br/>                             | Lectura/escritura<br/> | Obtiene o establece el número de veces que el Programador de tareas intentará reiniciar la tarea.<br/>                                                                                                                                                                                                                                                                                                                        |
| [**RestartInterval**](tasksettings-restartinterval.md)<br/>                       | Lectura/escritura<br/> | Obtiene o establece un valor que especifica cuánto tiempo el Programador de tareas intentará reiniciar la tarea.<br/>                                                                                                                                                                                                                                                                                                                 |
| [**RunOnlyIfIdle**](tasksettings-runonlyifidle.md)<br/>                           | Lectura/escritura<br/> | Obtiene o establece un valor booleano que indica que el Programador de tareas ejecutará la tarea solo si el equipo está en un estado de inactividad.<br/>                                                                                                                                                                                                                                                                                   |
| [**RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md)<br/>   | Lectura/escritura<br/> | Obtiene o establece un valor booleano que indica que el Programador de tareas ejecutará la tarea solo cuando una red esté disponible.<br/>                                                                                                                                                                                                                                                                                           |
| [**StartWhenAvailable**](tasksettings-startwhenavailable.md)<br/>                 | Lectura/escritura<br/> | Obtiene o establece un valor booleano que indica que el Programador de tareas puede iniciar la tarea en cualquier momento después de que haya transcurrido su hora programada.<br/>                                                                                                                                                                                                                                                                           |
| [**StopIfGoingOnBatteries**](tasksettings-stopifgoingonbatteries.md)<br/>         | Lectura/escritura<br/> | Obtiene o establece un valor booleano que indica que la tarea se detendrá si el equipo empieza a ejecutarse con la energía de la batería.<br/>                                                                                                                                                                                                                                                                                         |
| [**WakeToRun**](tasksettings-waketorun.md)<br/>                                   | Lectura/escritura<br/> | Obtiene o establece un valor booleano que indica que el Programador de tareas reactivará el equipo cuando llega el momento de ejecutar la tarea.<br/>                                                                                                                                                                                                                                                                                       |
| [**XmlText**](tasksettings-xmltext.md)<br/>                                       | Lectura/escritura<br/> | Obtiene o establece una definición con formato XML de la configuración de la tarea.<br/>                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Observaciones

De forma predeterminada, se detendrá una tarea 72 horas después de que empiece a ejecutarse. Puede cambiar esto cambiando el valor de [**ExecutionTimeLimit**](tasksettings-executiontimelimit.md) .

Al leer o escribir XML para una tarea, la configuración de la tarea se define en el elemento [**Settings**](taskschedulerschema-settings-tasktype-element.md) del esquema de programador de tareas.

## <a name="examples"></a>Ejemplos

Para obtener más información y un ejemplo de código para este objeto de scripting, vea [ejemplo de desencadenador de tiempo (scripting)](time-trigger-example--scripting-.md).

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

[**TaskDefinition**](taskdefinition.md)
</dt> <dt>

[**NetworkSettings**](networksettings.md)
</dt> <dt>

[**IdleSettings**](idlesettings.md)
</dt> </dl>

 

