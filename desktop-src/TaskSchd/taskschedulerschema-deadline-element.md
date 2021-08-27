---
title: Elemento Deadline
description: Especifica cuándo el programador de tareas debe iniciar la tarea durante el mantenimiento automático de emergencia, si no se pudo completar durante el mantenimiento automático normal.
ms.assetid: 34E33FAE-888E-4E82-83B8-059FB4A64B52
keywords:
- Elemento Deadline Programador de tareas
topic_type:
- apiref
api_name:
- Deadline
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 19d5560b57cfaa2a3fd3fa5167d13fa1722fe3f7dd736f19742e2efc895e15e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118857315"
---
# <a name="deadline-element"></a>Elemento Deadline

Especifica cuándo el programador de tareas debe iniciar la tarea durante el mantenimiento automático de emergencia, si no se pudo completar durante el mantenimiento automático normal.

El formato de esta cadena es *PnYnMnDTnHnMnS,* donde *nY* es el número de años, nM es el número de meses, *nD* es el número de días, *T* es el separador de fecha y hora, *nH* es el número de horas, *nM* es el número de minutos y *nS* es el número de segundos (por ejemplo, "PT5M" especifica 5 minutos y "P1M4DT2H5M" especifica un mes, cuatro días, dos horas y cinco minutos). El valor mínimo es un minuto. Para obtener más información sobre el tipo de duración, vea [XML Schema Part 2: Datatypes Second Edition](https://www.w3.org/TR/xmlschema-2/#duration). La fecha límite mínima que puede usar una tarea es de 1 día. El valor del **elemento Deadline** debe ser mayor que el valor del [**elemento Period.**](taskschedulerschema-period-element.md) Si no se especifica la fecha límite, la tarea no se inicia durante el mantenimiento automático de emergencia.

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

El tipo complejo [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) define el elemento **Deadline.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                                                          | Derivado de                                                                               | Descripción                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**MaintenanceSettings (maintenanceSettingsType)**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) | Especifica la configuración de tareas que usará el programador de tareas para iniciar la tarea durante el mantenimiento automático.<br/> |



## <a name="remarks"></a>Comentarios

Para la programación de C++, esta configuración inactiva se especifica mediante la [**propiedad IMaintenanceSettings::D eadline.**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_deadline)

## <a name="examples"></a>Ejemplos

El siguiente XML define un calendario de meses que ejecuta la tarea en marzo.


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
    <Deadline>P15D</Deadline>
</MaintenanceSettings>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>           |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





