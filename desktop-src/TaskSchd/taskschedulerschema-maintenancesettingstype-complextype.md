---
title: tipo complejo maintenanceSettingsType
description: Define los elementos secundarios y la información de secuenciación para el elemento MaintenanceSettings.
ms.assetid: CA4C452E-CA25-4E2D-B5E2-ED64C59AB3AD
keywords:
- maintenanceSettingsType tipo complejo Programador de tareas
topic_type:
- apiref
api_name:
- maintenanceSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f261e84fe2af1239cce1bbd377e991ede6e8506
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264983"
---
# <a name="maintenancesettingstype-complex-type"></a>tipo complejo maintenanceSettingsType

Define los elementos secundarios y la información de secuenciación para el [**elemento MaintenanceSettings.**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md)

``` syntax
<xs:complexType name="maintenanceSettingsType">
    <xs:all>
        <xs:element name="Period"
            minOccurs="1"
            maxOccurs="1"
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
        <xs:element name="Deadline"
            minOccurs="1"
            maxOccurs="1"
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
        <xs:element name="Exclusive"
            type="boolean"
            maxOccurs="1"
            minOccurs="1"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                        | Tipo    | Descripción                                                                                                                                                                                    |
|--------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Fecha límite**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) |         | Especifica la cantidad de tiempo después de la cual el programador de tareas intentará iniciar la tarea durante el mantenimiento automático de emergencia, si no se pudo completar durante el mantenimiento normal.<br/> |
| **Exclusivo**                                                                  | boolean | Si se establece en true, la tarea se inicia exclusivamente entre otras tareas de mantenimiento.<br/>                                                                                                 |
| [**Período**](taskschedulerschema-daysinterval-dailyscheduletype-element.md)   |         | Especifica la frecuencia con la que se debe iniciar la tarea durante el mantenimiento automático.<br/>                                                                                                      |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>           |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas tipos complejos de esquema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





