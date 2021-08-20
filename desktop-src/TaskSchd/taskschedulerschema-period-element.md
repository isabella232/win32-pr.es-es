---
title: Elemento Period
description: Especifica la frecuencia con la que se debe iniciar la tarea durante el mantenimiento automático.
ms.assetid: E4BE2466-3119-41F8-8238-4627C28B26E5
keywords:
- Elemento Period Programador de tareas
topic_type:
- apiref
api_name:
- Period
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: daf00a32dd7d614b4586dcb010f7841d2f66c2e1e9e133736ec095d59d1e1c5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117942803"
---
# <a name="period-element"></a>Elemento Period

Especifica la frecuencia con la que se debe iniciar la tarea durante el mantenimiento automático.

El formato de esta cadena es *PnYnMnDTnHnMnS,* donde *nY* es el número de años, nM es el número de meses, *nD* es el número de días, *T* es el separador de fecha y hora, *nH* es el número de horas, *nM* es el número de minutos y *nS* es el número de segundos (por ejemplo, "PT5M" especifica 5 minutos y "P1M4DT2H5M" especifica un mes, cuatro días, dos horas y cinco minutos). El valor mínimo es un minuto. Para obtener más información sobre el tipo de duración, vea [Xml Schema Part 2: Datatypes Second Edition](https://www.w3.org/TR/xmlschema-2/#duration).

``` syntax
<xs:element name="Period"
    maxOccurs="1"
    minOccurs="1"
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

El tipo complejo [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) define el elemento **Period.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                                                          | Derivado de                                                                               | Descripción                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**MaintenanceSettings (maintenanceSettingsType)**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) | Especifica la configuración de tareas que usará el programador de tareas para iniciar la tarea durante el mantenimiento automático.<br/> |



## <a name="remarks"></a>Comentarios

Para la programación de C++, esta configuración inactiva se especifica mediante la [**propiedad IMaintenanceSettings::P eriod.**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_period)

## <a name="examples"></a>Ejemplos

El xml siguiente define la tarea de mantenimiento con requisitos de periodicidad establecidos en 5 días.


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
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

 

 





