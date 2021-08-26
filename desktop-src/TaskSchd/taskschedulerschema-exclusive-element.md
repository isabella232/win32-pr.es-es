---
title: Elemento Exclusive
description: Indica si el programador de tareas debe iniciar la tarea durante el mantenimiento automático en modo exclusivo.
ms.assetid: F690FD8F-BCCB-456D-92E3-25A262D6DCF1
keywords:
- Elementos exclusivos Programador de tareas
topic_type:
- apiref
api_name:
- Exclusive
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aab796abfdcad67a348b6d42186732d402bbe8eeeb359ac772588fe809dbf73c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991335"
---
# <a name="exclusive-element"></a>Elemento Exclusive

Indica si el programador de tareas debe iniciar la tarea durante el mantenimiento automático en modo exclusivo.

La exclusividad solo se garantiza entre otras tareas de mantenimiento y no concede ninguna prioridad de ordenación de la tarea. Si no se especifica la exclusividad, la tarea se inicia en paralelo con otras tareas de mantenimiento.

``` syntax
<xs:element name="Exclusive"
    type="xsd:boolean"
    maxOccurs="1"
    minOccurs="0"
 />
```

El **tipo** complejo [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) define el elemento Exclusive.

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                                                          | Derivado de                                                                               | Descripción                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**MaintenanceSettings (maintenanceSettingsType)**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) | Especifica la configuración de tareas que usará el programador de tareas para iniciar la tarea durante el mantenimiento automático.<br/> |



## <a name="remarks"></a>Comentarios

Para la programación de C++, esta configuración inactiva se especifica mediante la [**propiedad IMaintenanceSettings::Exclusive.**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_exclusive)

## <a name="examples"></a>Ejemplos

El xml siguiente define la tarea de mantenimiento con el requisito de fecha límite establecido en 15 días.


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
    <Deadline>P15D</Deadline>
    <Exclusive>true</Exclusive>
</MaintenanceSettings>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>           |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





