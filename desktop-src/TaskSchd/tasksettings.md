---
title: Objeto TaskSettings
description: Objeto de scripting que proporciona la configuración que el Programador de tareas utiliza para realizar la tarea.
ms.assetid: f2ba952b-7864-467d-8709-eb6995dd5df5
keywords:
- Objetos TaskSettings Programador de tareas
- Objeto TaskSettings Programador de tareas , descrito
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
ms.openlocfilehash: a687e82248598d9732e91acfd40e9f3dd4d6d3c3fe6c4954cb8706489c814126
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738105"
---
# <a name="tasksettings-object"></a>Objeto TaskSettings

Objeto de scripting que proporciona la configuración que el Programador de tareas utiliza para realizar la tarea.

## <a name="members"></a>Miembros

El **objeto TaskSettings** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto TaskSettings** tiene estas propiedades.



| Propiedad                                                                                 | Tipo de acceso           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllowDemandStart**](tasksettings-allowdemandstart.md)<br/>                     | Lectura/escritura<br/> | Obtiene o establece un valor booleano que indica que la tarea se puede iniciar mediante el comando Ejecutar o el menú contextual.<br/>                                                                                                                                                                                                                                                                                     |
| [**AllowHardTerminate**](tasksettings-allowhardterminate.md)<br/>                 | Lectura/escritura<br/> | Obtiene o establece un valor booleano que indica que la tarea puede finalizarse mediante [**TerminateProcess.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess)<br/>                                                                                                                                                                                                                                                                               |
| [**Compatibilidad**](tasksettings-compatibility.md)<br/>                           | Lectura/escritura<br/> | Obtiene o establece un valor entero que indica con qué versión Programador de tareas una tarea es compatible.<br/>                                                                                                                                                                                                                                                                                                           |
| [**DeleteExpiredTaskAfter**](tasksettings-deleteexpiredtaskafter.md)<br/>         | Lectura/escritura<br/> | Obtiene o establece la cantidad de tiempo que el Programador de tareas esperará antes de eliminar la tarea después de que expire.<br/>                                                                                                                                                                                                                                                                                                      |
| [**DisallowStartIfOnBatteries**](tasksettings-disallowstartifonbatteries.md)<br/> | Lectura/escritura<br/> | Obtiene o establece un valor booleano que indica que la tarea no se iniciará si el equipo se ejecuta con batería.<br/>                                                                                                                                                                                                                                                                                        |
| [**habilitado**](tasksettings-enabled.md)<br/>                                       | Lectura/escritura<br/> | Obtiene o establece un valor booleano que indica que la tarea está habilitada. La tarea solo se puede realizar cuando esta configuración es True.<br/>                                                                                                                                                                                                                                                                                   |
| [**ExecutionTimeLimit**](tasksettings-executiontimelimit.md)<br/>                 | Lectura/escritura<br/> | Obtiene o establece la cantidad de tiempo permitido para completar la tarea.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| [**Oculto**](tasksettings-hidden.md)<br/>                                         | Lectura/escritura<br/> | Obtiene o establece un valor booleano que indica que la tarea no estará visible en la interfaz de usuario. Sin embargo, los administradores pueden invalidar esta configuración mediante el uso de un "modificador maestro" que hace que todas las tareas sean visibles en la interfaz de usuario.<br/>                                                                                                                                                                                           |
| [**IdleSettings**](tasksettings-idlesettings.md)<br/>                             | Lectura/escritura<br/> | Obtiene o establece la información que especifica cómo el Programador de tareas realiza tareas cuando el equipo está en estado inactivo.<br/>                                                                                                                                                                                                                                                                                          |
| [**MultipleInstances**](tasksettings-multipleinstances.md)<br/>                   | Lectura/escritura<br/> | Obtiene o establece la directiva que define cómo el Programador de tareas trata con varias instancias de la tarea.<br/>                                                                                                                                                                                                                                                                                                            |
| [**NetworkSettings**](tasksettings-networksettings.md)<br/>                       | Lectura/escritura<br/> | Obtiene o establece el objeto de configuración de red que contiene un identificador y un nombre de perfil de red. Si la propiedad [**RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md) de **TaskSettings** es **True** y se especifica un archivo propfile de red en la [**propiedad NetworkSettings,**](tasksettings-networksettings.md) la tarea solo se ejecutará si el perfil de red especificado está disponible.<br/> |
| [**Priority**](tasksettings-priority.md)<br/>                                     | Lectura/escritura<br/> | Obtiene o establece el nivel de prioridad de la tarea.<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| [**RestartCount**](tasksettings-restartcount.md)<br/>                             | Lectura/escritura<br/> | Obtiene o establece el número de veces que el Programador de tareas intentará reiniciar la tarea.<br/>                                                                                                                                                                                                                                                                                                                        |
| [**RestartInterval**](tasksettings-restartinterval.md)<br/>                       | Lectura/escritura<br/> | Obtiene o establece un valor que especifica cuánto tiempo el Programador de tareas intentará reiniciar la tarea.<br/>                                                                                                                                                                                                                                                                                                                 |
| [**RunOnlyIfIdle**](tasksettings-runonlyifidle.md)<br/>                           | Lectura/escritura<br/> | Obtiene o establece un valor booleano que indica que el Programador de tareas ejecutará la tarea solo si el equipo está en estado inactivo.<br/>                                                                                                                                                                                                                                                                                   |
| [**RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md)<br/>   | Lectura/escritura<br/> | Obtiene o establece un valor booleano que indica que el Programador de tareas ejecutará la tarea solo cuando haya una red disponible.<br/>                                                                                                                                                                                                                                                                                           |
| [**StartWhenAvailable**](tasksettings-startwhenavailable.md)<br/>                 | Lectura/escritura<br/> | Obtiene o establece un valor booleano que indica que el Programador de tareas puede iniciar la tarea en cualquier momento después de que haya transcurrido su hora programada.<br/>                                                                                                                                                                                                                                                                           |
| [**StopIfGoingOnBatteries**](tasksettings-stopifgoingonbatteries.md)<br/>         | Lectura/escritura<br/> | Obtiene o establece un valor booleano que indica que la tarea se detendrán si el equipo comienza a ejecutarse con batería.<br/>                                                                                                                                                                                                                                                                                         |
| [**WakeToRun**](tasksettings-waketorun.md)<br/>                                   | Lectura/escritura<br/> | Obtiene o establece un valor booleano que indica que el Programador de tareas reactivará el equipo cuando sea el momento de ejecutar la tarea.<br/>                                                                                                                                                                                                                                                                                       |
| [**Xmltext**](tasksettings-xmltext.md)<br/>                                       | Lectura/escritura<br/> | Obtiene o establece una definición con formato XML de la configuración de la tarea.<br/>                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Comentarios

De forma predeterminada, una tarea se detendrán 72 horas después de que empiece a ejecutarse. Para cambiar esto, cambie la opción [**ExecutionTimeLimit.**](tasksettings-executiontimelimit.md)

Al leer o escribir XML para una tarea, la configuración de la tarea se define en el [**elemento Configuración**](taskschedulerschema-settings-tasktype-element.md) del esquema Programador de tareas tarea.

## <a name="examples"></a>Ejemplos

Para obtener más información y un ejemplo de código para este objeto de scripting, vea [Ejemplo de desencadenador de tiempo (scripting).](time-trigger-example--scripting-.md)

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

[**TaskDefinition**](taskdefinition.md)
</dt> <dt>

[**NetworkSettings**](networksettings.md)
</dt> <dt>

[**IdleSettings**](idlesettings.md)
</dt> </dl>

 

