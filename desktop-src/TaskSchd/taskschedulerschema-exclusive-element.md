---
title: Elemento exclusivo
description: Indica si el programador de tareas debe iniciar la tarea durante el mantenimiento automático en modo exclusivo.
ms.assetid: F690FD8F-BCCB-456D-92E3-25A262D6DCF1
keywords:
- Programador de tareas de elemento exclusivo
topic_type:
- apiref
api_name:
- Exclusive
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e0cd7cf5b2a5ce3aa68f92834aa45563000945d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685884"
---
# <a name="exclusive-element"></a>Elemento exclusivo

Indica si el programador de tareas debe iniciar la tarea durante el mantenimiento automático en modo exclusivo.

La exclusividad solo está garantizada entre otras tareas de mantenimiento y no concede ninguna prioridad de ordenación de la tarea. Si no se especifica la exclusividad, la tarea se inicia en paralelo con otras tareas de mantenimiento.

``` syntax
<xs:element name="Exclusive"
    type="xsd:boolean"
    maxOccurs="1"
    minOccurs="0"
 />
```

El elemento **Exclusive** se define mediante el tipo complejo de [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                                                          | Derivado de                                                                               | Descripción                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**MaintenanceSettings (maintenanceSettingsType)**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) | Especifica la configuración de tarea que usará el programador de tareas para iniciar la tarea durante el mantenimiento automático.<br/> |



## <a name="remarks"></a>Observaciones

En la programación de C++, esta configuración de inactividad se especifica mediante la propiedad [**IMaintenanceSettings:: Exclusive**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_exclusive) .

## <a name="examples"></a>Ejemplos

El siguiente código XML define la tarea de mantenimiento con el requisito de fecha límite establecido en 15 días.


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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas elementos de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





