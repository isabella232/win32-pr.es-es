---
title: Elemento Settings (taskType)
description: Especifica la configuración que el Programador de tareas utiliza para realizar la tarea.
ms.assetid: 72d2929a-0dd2-44cd-be7b-72eca23a5e14
keywords:
- Elemento Settings Programador de tareas
topic_type:
- apiref
api_name:
- Settings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9133d536aef692a5f9928e10963dff8c454f25fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422162"
---
# <a name="settings-tasktype-element"></a>Elemento Settings (taskType)

Especifica la configuración que el Programador de tareas utiliza para realizar la tarea.

``` syntax
<xs:element name="Settings"
    type="settingsType"
    minOccurs="0"
 />
```

El elemento **Settings** se define mediante el tipo complejo [**taskType**](taskschedulerschema-tasktype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                          | Derivado de                                                 | Descripción                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**Task**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Especifica la tarea que realiza el servicio Programador de tareas.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                                          | Tipo                                                                                              | Descripción                                                                                                          |
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**AllowHardTerminate**](taskschedulerschema-allowhardterminate-settingstype-element.md)                        | boolean                                                                                           | Especifica que la tarea puede terminar con TerminateProcess.<br/>                                         |
| [**AllowStartOnDemand**](taskschedulerschema-allowstartondemand-settingstype-element.md)                        | boolean                                                                                           | Especifica que la tarea se puede iniciar con el comando ejecutar o el menú contextual.<br/>                  |
| [**DeleteExpiredTaskAfter**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md)                | duration                                                                                          | Especifica la cantidad de tiempo que esperará el Programador de tareas antes de eliminar la tarea después de que expire.<br/> |
| [**DisallowStartIfOnBatteries**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md)        | boolean                                                                                           | Especifica que la tarea no se iniciará si el equipo se está ejecutando con baterías.<br/>                      |
| [**habilitado**](taskschedulerschema-enabled-settingstype-element.md)                                              | boolean                                                                                           | Especifica que la tarea está habilitada. La tarea solo se puede realizar cuando este valor es true.<br/>             |
| [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-settingstype-element.md)                        | duration                                                                                          | Cantidad de tiempo permitido para completar la tarea.<br/>                                                              |
| [**Plusvalía**](taskschedulerschema-hidden-settingstype-element.md)                                                | boolean                                                                                           | Especifica que la tarea no será visible de forma predeterminada en la interfaz de usuario.<br/>                                         |
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md)                                    | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md)                      | Especifica cómo realiza el Programador de tareas las tareas cuando el equipo está en un estado de inactividad.<br/>                    |
| [**MaintenanceSettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md)           | [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md)        | Especifica cómo realiza el Programador de tareas las tareas durante el mantenimiento automático.<br/>                             |
| [**MultipleInstancesPolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)              | [**multipleInstancesPolicyType**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) | Especifica la Directiva que define el modo en que el Programador de tareas se encarga de varias instancias de la tarea.<br/>       |
| [**Priority**](taskschedulerschema-priority-settingstype-element.md)                                            | [**priorityType**](taskschedulerschema-prioritytype-simpletype.md)                               | Especifica el nivel de prioridad de la tarea.<br/>                                                                |
| [**RestartOnFailure**](taskschedulerschema-restartonfailure-settingstype-element.md)                            | [**restartType**](taskschedulerschema-restarttype-complextype.md)                                | Especifica que el Programador de tareas intentará reiniciar la tarea si se produce un error en la tarea por cualquier motivo.<br/>      |
| [**RunOnlyIfIdle**](taskschedulerschema-runonlyifidle-settingstype-element.md)                                  | boolean                                                                                           | Especifica que la tarea se ejecuta solo cuando el equipo está en un estado de inactividad.<br/>                                |
| [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md)          | boolean                                                                                           | Especifica que el Programador de tareas ejecutará la tarea solo cuando una red esté disponible.<br/>                     |
| [**StartWhenAvailable**](taskschedulerschema-startwhenavailable-settingstype-element.md)                        | boolean                                                                                           | Especifica que el Programador de tareas puede iniciar la tarea en cualquier momento después de que haya transcurrido su hora programada.<br/>     |
| [**StopIfGoingOnBatteries (settingsType)**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) | boolean                                                                                           | Especifica que la tarea se detendrá si el equipo pasa a baterías.<br/>                          |
| [**Volatil**](taskschedulerschema-volatile-element.md)                                                         | boolean                                                                                           | Especifica si la tarea se deshabilitará automáticamente mediante Programador de tareas en el inicio de Windows.<br/>                     |
| [**WakeToRun (settingsType)**](taskschedulerschema-waketorun-settingstype-element.md)                           | boolean                                                                                           | Especifica que Programador de tareas reactivará el equipo cuando sea el momento de ejecutar la tarea.<br/>                     |



## <a name="remarks"></a>Observaciones

Puede seleccionar uno o varios de los elementos secundarios a los que se hace referencia anteriormente.

En el desarrollo de C++, la información de registro de una tarea se especifica mediante la [**propiedad settings de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_settings).

Para el desarrollo de scripting, la información de registro de una tarea se especifica mediante la propiedad [**TaskDefinition. Settings**](taskdefinition-settings.md) .

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código XML se define un elemento de configuración que permite una finalización rígida de la tarea.


```XML
<task>
    <Settings>
        <AllowHardTerminate>true</AllowHardTerminate>
        <AllowStartOnDemand>true</AllowStartOnDemand>
    </Settings>
</task>
```



Para obtener más información y un ejemplo completo del XML para establecer la configuración de la tarea, vea [ejemplo de desencadenador de tiempo (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas elementos de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





