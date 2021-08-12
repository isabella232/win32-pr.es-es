---
title: Elemento WaitTimeout (idleSettingsType)
description: Especifica la cantidad de tiempo que el Programador de tareas esperará a que se produzca una condición inactiva.
ms.assetid: 6a4cc80d-adc2-47a7-946f-a9f12eeb35a4
keywords:
- Elemento WaitTimeout Programador de tareas
topic_type:
- apiref
api_name:
- WaitTimeout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d078acecf39f9bd4848cabaa8b203787049ca8a66e565e6183b8b1998389ad8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610400"
---
# <a name="waittimeout-idlesettingstype-element"></a>Elemento WaitTimeout (idleSettingsType)

Especifica la cantidad de tiempo que el Programador de tareas esperará a que se produzca una condición inactiva. Si no se especifica ningún valor para este elemento, el servicio de Programador de tareas esperará indefinidamente a que se produzca una condición de inactividad. El formato de esta cadena es PnYnMnDTnHnMnS, donde nY es el número de años, nM es el número de meses, nD es el número de días, "T" es el separador de fecha y hora, nH es el número de horas, nM es el número de minutos y nS es el número de segundos (por ejemplo, PT5M especifica 5 minutos y P1M4DT2H5M especifica un mes, cuatro días, dos horas y cinco minutos). Para obtener más información sobre el tipo de duración, vea <https://go.microsoft.com/fwlink/p/?linkid=106886> . El tiempo mínimo permitido es de 1 minuto.

``` syntax
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
```

El elemento se define mediante el [**tipo complejo idleSettingsType.**](taskschedulerschema-idlesettingstype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                       | Derivado de                                                                 | Descripción                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) | Especifica cómo el Programador de tareas realiza tareas cuando el equipo está en estado inactivo.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de scripts, esta configuración inactiva se especifica mediante la [**propiedad IdleSettings.WaitTimeout.**](idlesettings-waittimeout.md)

Para el desarrollo de C++, esta configuración inactiva se especifica mediante la [**propiedad IIdleSettings::WaitTimeout.**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_waittimeout)

## <a name="examples"></a>Ejemplos

El siguiente XML define una configuración inactiva que espera 24 horas a que se produzca una condición de inactividad.


```XML
<IdleSettings>
    <WaitTimeout>PT24H</WaitTimeout>
</IdleSettings>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





