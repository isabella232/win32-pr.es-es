---
title: idleSettingsType (tipo complejo)
description: Define los elementos secundarios y la información de secuenciación para el elemento IdleSettings (settingsType).
ms.assetid: 0f50c4d6-fda9-42cc-8dab-4c9439fbea4b
keywords:
- tipo complejo idleSettingsType Programador de tareas
topic_type:
- apiref
api_name:
- idleSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c11c49266b208f92e52f7c1fc97291af6f99fb59367a389476768e65e99b53c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796525"
---
# <a name="idlesettingstype-complex-type"></a>idleSettingsType (tipo complejo)

Define los elementos secundarios y la información de secuenciación para [**el elemento IdleSettings (settingsType).**](taskschedulerschema-idlesettings-settingstype-element.md)

``` syntax
<xs:complexType name="idleSettingsType">
    <xs:all>
        <xs:element name="Duration"
            default="PT10M"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="PT1M"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="WaitTimeout"
            default="PT1H"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="PT1M"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="StopOnIdleEnd"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="RestartOnIdle"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                  | Tipo    | Descripción                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Duration**](taskschedulerschema-duration-idlesettingstype-element.md)                |         | Especifica la cantidad de tiempo permitido para iniciar la tarea mientras está en una condición inactiva.<br/>                                                                                                                     |
| [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md)      | boolean | La tarea se reinicia en cuanto se inicia una condición de inactividad.<br/>                                                                                                                                             |
| [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) | boolean | Especifica que la tarea finaliza si la condición de inactividad finaliza antes de que se supere la duración de inactividad.<br/>                                                                                                 |
| [**WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md)          |         | Especifica la cantidad de tiempo que se debe esperar a que se inicie una condición inactiva. Si no se especifica ningún valor para este elemento, el servicio de Programador de tareas esperará indefinidamente a que se produzca una condición de inactividad.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas complejos de esquema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





