---
title: Elemento period
description: Especifica la frecuencia con que se debe iniciar la tarea durante el mantenimiento automático.
ms.assetid: E4BE2466-3119-41F8-8238-4627C28B26E5
keywords:
- Elemento period Programador de tareas
topic_type:
- apiref
api_name:
- Period
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a507a9b0a8f97d1ae4e6c8df654a45d67b77767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493121"
---
# <a name="period-element"></a>Elemento period

Especifica la frecuencia con que se debe iniciar la tarea durante el mantenimiento automático.

El formato de esta cadena es *PnYnMnDTnHnMnS*, donde *NY* es el número de años. nm es el número de meses, *ND* es el número de días, *T* es el separador de fecha y hora, *NH* es el número de horas, *nm* es el número de minutos y *NS* es el número de segundos (por ejemplo, "PT5M" especifica 5 minutos y "P1M4DT2H5M" especifica un mes, cuatro días, dos horas y cinco minutos). El valor mínimo es un minuto. Para obtener más información sobre el tipo de duración, vea [esquema XML parte 2: tipos de datos segunda edición](https://www.w3.org/TR/xmlschema-2/#duration).

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

El elemento de **punto** se define mediante el tipo complejo de [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                                                          | Derivado de                                                                               | Descripción                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**MaintenanceSettings (maintenanceSettingsType)**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) | Especifica la configuración de tarea que usará el programador de tareas para iniciar la tarea durante el mantenimiento automático.<br/> |



## <a name="remarks"></a>Observaciones

Para la programación en C++, esta configuración de inactividad se especifica mediante la propiedad [**IMaintenanceSettings::P Eriod**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_period) .

## <a name="examples"></a>Ejemplos

El siguiente código XML define la tarea de mantenimiento con el requisito de periodicidad establecido en 5 días.


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
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

 

 





