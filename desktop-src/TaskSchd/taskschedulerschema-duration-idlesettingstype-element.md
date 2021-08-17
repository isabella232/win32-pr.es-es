---
title: Elemento Duration (idleSettingsType)
description: Especifica cuánto tiempo debe estar inactivo el equipo antes de ejecutar la tarea.
ms.assetid: 89584694-0685-44e2-b8b7-69e47ee28d5d
keywords:
- Elemento Duration Programador de tareas
topic_type:
- apiref
api_name:
- Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46523caa10f96d7dd76947540932107106ad0d5c8a4b7f26fc6f6d5bebb40325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356572"
---
# <a name="duration-idlesettingstype-element"></a>Elemento Duration (idleSettingsType)

Especifica cuánto tiempo debe estar inactivo el equipo antes de ejecutar la tarea. El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años, nM es el número de meses, nD es el número de días, "T" es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos). El valor mínimo es de un minuto. Para obtener más información sobre el tipo de duración, vea <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
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
```

El elemento se define mediante el [**tipo complejo idleSettingsType.**](taskschedulerschema-idlesettingstype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                       | Derivado de                                                                 | Descripción                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) | Especifica cómo el Programador de tareas realiza tareas cuando el equipo está en estado inactivo.<br/> |



## <a name="remarks"></a>Comentarios

Para la programación de scripts, esta configuración inactiva se especifica mediante la [**propiedad IdleSettings.IdleDuration.**](idlesettings-idleduration.md)

Para la programación de C++, esta configuración inactiva se especifica mediante la [**propiedad IIdleSettings::IdleDuration.**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_idleduration)

## <a name="examples"></a>Ejemplos

El siguiente XML define una configuración inactiva que permite que la tarea se inicie en 5 minutos.


```XML
<IdleSettings>
    <Duration>PT5M</Duration>
</IdleSettings>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





