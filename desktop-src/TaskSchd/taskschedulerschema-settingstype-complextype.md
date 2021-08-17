---
title: settingsType Complex Type
description: Define los elementos secundarios y la información de secuenciación para el Configuración elemento (taskType).
ms.assetid: dba6b82d-aaa4-4f77-aeb1-c5a8f81aec25
keywords:
- configuraciónTipo de tipo complejo Programador de tareas
topic_type:
- apiref
api_name:
- settingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a48a124230a27a0c23cc9c2a9fa983b6ef3088b8ec22e8ac03fc371caadf0f00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356357"
---
# <a name="settingstype-complex-type"></a>settingsType Complex Type

Define los elementos secundarios y la información de secuenciación [**para Configuración elemento (taskType).**](taskschedulerschema-settings-tasktype-element.md)

``` syntax
<xs:complexType name="settingsType">
    <xs:all>
        <xs:element name="AllowStartOnDemand"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="RestartOnFailure"
            type="restartType"
            minOccurs="0"
         />
        <xs:element name="MultipleInstancesPolicy"
            type="multipleInstancesPolicyType"
            default="IgnoreNew"
            minOccurs="0"
         />
        <xs:element name="DisallowStartIfOnBatteries"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StopIfGoingOnBatteries"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="AllowHardTerminate"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StartWhenAvailable"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="NetworkProfileName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="RunOnlyIfNetworkAvailable"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="WakeToRun"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="Enabled"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="Hidden"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="DeleteExpiredTaskAfter"
            type="duration"
            default="PT0S"
            minOccurs="0"
         />
        <xs:element name="IdleSettings"
            type="idleSettingsType"
            minOccurs="0"
         />
        <xs:element name="NetworkSettings"
            type="networkSettingsType"
            minOccurs="0"
         />
        <xs:element name="ExecutionTimeLimit"
            type="duration"
            minOccurs="0"
         />
        <xs:element name="Priority"
            type="priorityType"
            default="7"
            minOccurs="0"
         />
        <xs:element name="RunOnlyIfIdle"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="UseUnifiedSchedulingEngine"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="DisallowStartOnRemoteAppSession"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                                             | Tipo                                                                                              | Descripción                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllowHardTerminate**](taskschedulerschema-allowhardterminate-settingstype-element.md)                           | boolean                                                                                           | Especifica si el servicio Programador de tareas permite la terminación de la tarea de forma automática.<br/>                                                                                                                                                                                                                             |
| [**AllowStartOnDemand**](taskschedulerschema-allowstartondemand-settingstype-element.md)                           | boolean                                                                                           | Especifica que la tarea se puede iniciar mediante el comando Ejecutar o el menú Contextual. <br/>                                                                                                                                                                                                             |
| [**DeleteExpiredTaskAfter**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md)                   | duration                                                                                          | Especifica la cantidad de tiempo que el Programador de tareas esperará antes de eliminar la tarea después de que expire. Si no se especifica ningún valor para este elemento, el Programador de tareas no eliminará la tarea.<br/>                                                                                           |
| [**DisallowStartIfOnBatteries**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md)           | boolean                                                                                           | Especifica que la tarea no se iniciará si el equipo se ejecuta con batería.<br/>                                                                                                                                                                                                                 |
| [**DisallowStartOnRemoteAppSession**](taskschedulerschema-disallowstartonremoteappsession-settingstype-element.md) | boolean                                                                                           | Especifica que la tarea no debe iniciarse si la tarea se desencadena para ejecutarse en una sesión de Aplicaciones remotas integradas localmente (RAIL).<br/>                                                                                                                                                                     |
| [**habilitado**](taskschedulerschema-enabled-settingstype-element.md)                                                 | boolean                                                                                           | Especifica que la tarea está habilitada. La tarea solo se puede realizar cuando esta configuración es **True.**<br/>                                                                                                                                                                                                        |
| [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-settingstype-element.md)                           | duration                                                                                          | Especifica la cantidad de tiempo permitido para completar la tarea.<br/>                                                                                                                                                                                                                                               |
| [**Oculto**](taskschedulerschema-hidden-settingstype-element.md)                                                   | boolean                                                                                           | Especifica, de forma predeterminada, que la tarea no será visible en la interfaz de usuario (UI).<br/>                                                                                                                                                                                                                     |
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md)                                       | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md)                      | Especifica cómo el Programador de tareas realiza tareas cuando el equipo está en estado inactivo.<br/>                                                                                                                                                                                                                   |
| [**MultipleInstancesPolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)                 | [**multipleInstancesPolicyType**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) | Especifica la directiva que define cómo el Programador de tareas trata con varias instancias de la tarea. <br/>                                                                                                                                                                                                     |
| [**NetworkProfileName**](taskschedulerschema-networkprofilename-settingstype-element.md)                           | string                                                                                            | Especifica el nombre de un perfil de red. El Programador de tareas comprueba la disponibilidad de esta red cuando el [**elemento RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) está establecido en **True.** El nombre se usa con fines para mostrar.<br/>        |
| [**NetworkSettings**](taskschedulerschema-networksettings-settingstype-element.md)                                 | [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md)                | Especifica la configuración que el servicio Programador de tareas utiliza para obtener un perfil de red. El Programador de tareas comprueba la disponibilidad de esta red cuando el [**elemento RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) está establecido en **True.**<br/> |
| [**Priority**](taskschedulerschema-priority-settingstype-element.md)                                               | [**priorityType**](taskschedulerschema-prioritytype-simpletype.md)                               | Especifica el nivel de prioridad de la tarea.<br/>                                                                                                                                                                                                                                                               |
| [**RestartOnFailure**](taskschedulerschema-restartonfailure-settingstype-element.md)                               | [**restartType**](taskschedulerschema-restarttype-complextype.md)                                | Especifica que el Programador de tareas intentará reiniciar la tarea si se produce un error por cualquier motivo. <br/>                                                                                                                                                                                                          |
| [**RunOnlyIfIdle**](taskschedulerschema-runonlyifidle-settingstype-element.md)                                     | boolean                                                                                           | Especifica que la tarea se ejecuta solo cuando el equipo está en estado inactivo.<br/>                                                                                                                                                                                                                               |
| [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md)             | boolean                                                                                           | Especifica que el Programador de tareas ejecutará la tarea solo cuando haya una red disponible.<br/>                                                                                                                                                                                                                    |
| [**StartWhenAvailable**](taskschedulerschema-startwhenavailable-settingstype-element.md)                           | boolean                                                                                           | Especifica que el Programador de tareas puede iniciar la tarea en cualquier momento después de que haya transcurrido su hora programada.<br/>                                                                                                                                                                                                    |
| [**StopIfGoingOnBatteries**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md)                   | boolean                                                                                           | Especifica que la tarea se detendrán si el equipo cambia a la energía de la batería. <br/>                                                                                                                                                                                                                      |
| [**UseUnifiedSchedulingEngine**](taskschedulerschema-useunifiedschedulingengine-settingstype-element.md)           | boolean                                                                                           | Especifica que la tarea se ejecuta mediante el motor de programación unificado.<br/>                                                                                                                                                                                                                                   |
| [**WakeToRun**](taskschedulerschema-waketorun-settingstype-element.md)                                             | boolean                                                                                           | Especifica que Programador de tareas reactivará el equipo antes de ejecutar la tarea.<br/>                                                                                                                                                                                                                            |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas tipos complejos de esquema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





