---
title: Elemento fecha límite
description: Especifica el momento en que el programador de tareas debe iniciar la tarea durante el mantenimiento automático de emergencia, si no se pudo completar durante el mantenimiento automático normal.
ms.assetid: 34E33FAE-888E-4E82-83B8-059FB4A64B52
keywords:
- Programador de tareas de elementos de fecha límite
topic_type:
- apiref
api_name:
- Deadline
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e12524971e8b713d4d17817a8a7c7602017bd68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801772"
---
# <a name="deadline-element"></a>Elemento fecha límite

Especifica el momento en que el programador de tareas debe iniciar la tarea durante el mantenimiento automático de emergencia, si no se pudo completar durante el mantenimiento automático normal.

El formato de esta cadena es *PnYnMnDTnHnMnS*, donde *NY* es el número de años. nm es el número de meses, *ND* es el número de días, *T* es el separador de fecha y hora, *NH* es el número de horas, *nm* es el número de minutos y *NS* es el número de segundos (por ejemplo, "PT5M" especifica 5 minutos y "P1M4DT2H5M" especifica un mes, cuatro días, dos horas y cinco minutos). El valor mínimo es un minuto. Para obtener más información sobre el tipo de duración, vea [esquema XML parte 2: tipos de datos segunda edición](https://www.w3.org/TR/xmlschema-2/#duration). Fecha límite mínima que una tarea puede usar es 1 día. El valor del elemento **fecha límite** debe ser mayor que el valor del elemento [**period**](taskschedulerschema-period-element.md) . Si no se especifica la fecha límite, la tarea no se iniciará durante el mantenimiento automático de emergencia.

``` syntax
<xs:element name="Deadline"
    maxOccurs="1"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="P1D"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

El elemento de **fecha límite** se define mediante el tipo complejo de [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                                                          | Derivado de                                                                               | Descripción                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**MaintenanceSettings (maintenanceSettingsType)**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) | Especifica la configuración de tarea que usará el programador de tareas para iniciar la tarea durante el mantenimiento automático.<br/> |



## <a name="remarks"></a>Observaciones

Para la programación en C++, esta configuración de inactividad se especifica mediante la propiedad [**IMaintenanceSettings::D eadline**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_deadline) .

## <a name="examples"></a>Ejemplos

El siguiente código XML define un calendario de meses que ejecuta la tarea en marzo.


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
    <Deadline>P15D</Deadline>
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

 

 





