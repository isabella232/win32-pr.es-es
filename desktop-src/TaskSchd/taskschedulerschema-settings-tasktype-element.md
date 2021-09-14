---
title: Configuración (taskType) (Elemento)
description: Especifica la configuración que el Programador de tareas utiliza para realizar la tarea.
ms.assetid: 72d2929a-0dd2-44cd-be7b-72eca23a5e14
keywords:
- Configuración elemento Programador de tareas
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968660"
---
# <a name="settings-tasktype-element"></a>Configuración (taskType) (Elemento)

Especifica la configuración que el Programador de tareas utiliza para realizar la tarea.

``` syntax
<xs:element name="Settings"
    type="settingsType"
    minOccurs="0"
 />
```

El **Configuración** elemento se define mediante el [**tipo complejo taskType.**](taskschedulerschema-tasktype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                          | Derivado de                                                 | Descripción                                                                    |
|--------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**Task**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Especifica la tarea que realiza el servicio Programador de tareas trabajo.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                                          | Tipo                                                                                              | Descripción                                                                                                          |
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**AllowHardTerminate**](taskschedulerschema-allowhardterminate-settingstype-element.md)                        | boolean                                                                                           | Especifica que la tarea se puede finalizar mediante TerminateProcess.<br/>                                         |
| [**AllowStartOnDemand**](taskschedulerschema-allowstartondemand-settingstype-element.md)                        | boolean                                                                                           | Especifica que la tarea se puede iniciar mediante el comando Ejecutar o el menú Contextual.<br/>                  |
| [**DeleteExpiredTaskAfter**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md)                | duration                                                                                          | Especifica la cantidad de tiempo que el Programador de tareas esperará antes de eliminar la tarea después de que expire.<br/> |
| [**DisallowStartIfOnBatteries**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md)        | boolean                                                                                           | Especifica que la tarea no se iniciará si el equipo se ejecuta con baterías.<br/>                      |
| [**Habilitado**](taskschedulerschema-enabled-settingstype-element.md)                                              | boolean                                                                                           | Especifica que la tarea está habilitada. La tarea solo se puede realizar cuando esta configuración es True.<br/>             |
| [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-settingstype-element.md)                        | duration                                                                                          | Cantidad de tiempo permitido para completar la tarea.<br/>                                                              |
| [**Hidden**](taskschedulerschema-hidden-settingstype-element.md)                                                | boolean                                                                                           | Especifica que la tarea no estará visible en la interfaz de usuario de forma predeterminada.<br/>                                         |
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md)                                    | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md)                      | Especifica cómo el Programador de tareas realiza tareas cuando el equipo está en estado inactivo.<br/>                    |
| [**MaintenanceSettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md)           | [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md)        | Especifica cómo realiza el Programador de tareas tareas durante el mantenimiento automático.<br/>                             |
| [**MultipleInstancesPolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)              | [**multipleInstancesPolicyType**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) | Especifica la directiva que define cómo el Programador de tareas trata con varias instancias de la tarea.<br/>       |
| [**Priority**](taskschedulerschema-priority-settingstype-element.md)                                            | [**priorityType**](taskschedulerschema-prioritytype-simpletype.md)                               | Especifica el nivel de prioridad de la tarea.<br/>                                                                |
| [**RestartOnFailure**](taskschedulerschema-restartonfailure-settingstype-element.md)                            | [**restartType**](taskschedulerschema-restarttype-complextype.md)                                | Especifica que el Programador de tareas intentará reiniciar la tarea si se produce un error en la tarea por cualquier motivo.<br/>      |
| [**RunOnlyIfIdle**](taskschedulerschema-runonlyifidle-settingstype-element.md)                                  | boolean                                                                                           | Especifica que la tarea se ejecuta solo cuando el equipo está en estado inactivo.<br/>                                |
| [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md)          | boolean                                                                                           | Especifica que el Programador de tareas ejecutará la tarea solo cuando haya una red disponible.<br/>                     |
| [**StartWhenAvailable**](taskschedulerschema-startwhenavailable-settingstype-element.md)                        | boolean                                                                                           | Especifica que el Programador de tareas puede iniciar la tarea en cualquier momento después de que haya transcurrido su hora programada.<br/>     |
| [**StopIfGoingOnBatteries (settingsType)**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) | boolean                                                                                           | Especifica que la tarea se detendrán si el equipo va a usar baterías.<br/>                          |
| [**Volátil**](taskschedulerschema-volatile-element.md)                                                         | boolean                                                                                           | Especifica si la tarea se deshabilita automáticamente mediante Programador de tareas inicio Windows inicio.<br/>                     |
| [**WakeToRun (settingsType)**](taskschedulerschema-waketorun-settingstype-element.md)                           | boolean                                                                                           | Especifica que Programador de tareas reactivará el equipo cuando llegue el momento de ejecutar la tarea.<br/>                     |



## <a name="remarks"></a>Observaciones

Puede seleccionar uno o varios de los elementos secundarios a los que se hace referencia anteriormente.

Para el desarrollo de C++, la información de registro de una tarea se especifica mediante [**la Configuración propiedad de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_settings).

Para el desarrollo de scripting, la información de registro de una tarea se especifica mediante la [**propiedad TaskDefinition.Configuración.**](taskdefinition-settings.md)

## <a name="examples"></a>Ejemplos

En el ejemplo de código XML siguiente se define un elemento de configuración que permite una terminación de la tarea de forma fija.


```XML
<task>
    <Settings>
        <AllowHardTerminate>true</AllowHardTerminate>
        <AllowStartOnDemand>true</AllowStartOnDemand>
    </Settings>
</task>
```



Para obtener más información y un ejemplo completo del XML para establecer la configuración de tareas, vea Ejemplo de desencadenador [de tiempo (XML).](time-trigger-example--xml-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





