---
title: Elemento Interval (restartType)
description: Especifica cuánto tiempo el Programador de tareas intentará reiniciar la tarea.
ms.assetid: 00b8fcbb-5be8-4bf1-92a0-2afd2a50f8e1
keywords:
- Elemento Interval Programador de tareas
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e731582364df23bdef800ab5d2cf15dd5c882ae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259239"
---
# <a name="interval-restarttype-element"></a>Elemento Interval (restartType)

Especifica cuánto tiempo el Programador de tareas intentará reiniciar la tarea. El formato de esta cadena es `P<days>DT<hours>H<minutes>M<seconds>S` (por ejemplo, "PT5M" es 5 minutos, "PT1H" es 1 hora y "PT20M" es 20 minutos). El tiempo máximo permitido es de 31 días y el tiempo mínimo permitido es de 1 minuto.

``` syntax
<xs:element name="Interval">
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
            <xs:maxInclusive
                value="P31D"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

El elemento se define mediante el [**tipo complejo restartType.**](taskschedulerschema-restarttype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                               | Derivado de                                                       | Descripción                                                                                                     |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**RestartOnFailure**](taskschedulerschema-restartonfailure-settingstype-element.md) | [**restartType**](taskschedulerschema-restarttype-complextype.md) | Especifica que el Programador de tareas intentará reiniciar la tarea si se produce un error en la tarea por cualquier motivo.<br/> |



## <a name="remarks"></a>Observaciones

Si se especifica este elemento, también se debe especificar el elemento [**Count**](taskschedulerschema-count-restarttype-element.md) para que el Programador de tareas el número de veces que debe intentar reiniciar la tarea.

Para el desarrollo de C++, [**vea Propiedad RestartInterval de ITaskSettings.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval)

Para el desarrollo de scripts, [**vea TaskSettings.RestartInterval**](tasksettings-restartinterval.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





