---
title: Elemento MaintenanceSettings (maintenanceSettingsType)
description: Especifica cómo realiza el Programador de tareas tareas durante el mantenimiento automático.
ms.assetid: 6A204980-851D-4487-A6CC-01BE262A517A
keywords:
- Elemento MaintenanceSettings Programador de tareas
topic_type:
- apiref
api_name:
- MaintenanceSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca68876d8742ea04faa972d2ea7fd5f4b2071ffc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259172"
---
# <a name="maintenancesettings-maintenancesettingstype-element"></a>Elemento MaintenanceSettings (maintenanceSettingsType)

Especifica cómo realiza el Programador de tareas tareas durante el mantenimiento automático.

``` syntax
<xs:element name="MaintenanceSettings"
    type="maintenanceSettingsType"
    minOccurs="0"
 />
```

El tipo complejo [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) define el elemento **MaintenanceSettings.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configuración**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene la configuración que el Programador de tareas usa para realizar la tarea.<br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                    | Tipo    | Descripción                                                                                                                                                                                     |
|------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Fecha límite**](taskschedulerschema-deadline-element.md)   |         | Especifica la cantidad de tiempo después de la cual el programador de tareas intentará iniciar la tarea durante el mantenimiento automático de emergencia, si no se pudo completar durante el mantenimiento normal. <br/> |
| [**Exclusivo**](taskschedulerschema-exclusive-element.md) | boolean | Si se establece en true, la tarea se inicia exclusivamente entre otras tareas de mantenimiento. <br/>                                                                                                 |
| [**Período**](taskschedulerschema-period-element.md)       |         | Especifica la frecuencia con la que se debe iniciar la tarea durante el mantenimiento automático. <br/>                                                                                                      |



## <a name="remarks"></a>Observaciones

Para la programación de C++, esta configuración inactiva se especifica mediante la [**propiedad ITaskSettings3::MaintenanceSettings.**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings)

## <a name="examples"></a>Ejemplos

El siguiente XML define un elemento de configuración que indica a Programador de tareas que ejecute la tarea una vez en 5 días durante el mantenimiento automático normal y, si se ha dado un error durante 15 días, empiece a intentar la tarea durante el mantenimiento automático de emergencia.


```XML
<Settings>
    <MaintenanceSettings>
        <Period>P5D</Period>
        <Deadline>P15D</Deadline>
    </MaintenanceSettings>       
</Settings>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>           |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





