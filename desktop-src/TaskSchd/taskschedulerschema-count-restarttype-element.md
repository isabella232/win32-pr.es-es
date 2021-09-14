---
title: Elemento Count (restartType)
description: Especifica el número de veces que el Programador de tareas intentará reiniciar la tarea.
ms.assetid: 67466c14-c9dd-49c8-a6ed-df7531fc63b8
keywords:
- Recuento de elementos Programador de tareas
topic_type:
- apiref
api_name:
- Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 655f636b725e48749540d67710afa57b3c45c89c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071047"
---
# <a name="count-restarttype-element"></a>Elemento Count (restartType)

Especifica el número de veces que el Programador de tareas intentará reiniciar la tarea.

``` syntax
<xs:element name="Count">
    <xs:simpleType>
        <xs:restriction
            base="unsignedByte"
        >
            <xs:minInclusive
                value="1"
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

Si se especifica este elemento, también se debe especificar el elemento [**Interval**](taskschedulerschema-interval-restarttype-element.md) para que el Programador de tareas cuánto tiempo se intente reiniciar la tarea.

Para el desarrollo de C++, [**vea Propiedad RestartCount de ITaskSettings.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount)

Para el desarrollo de scripts, [**vea TaskSettings.RestartCount**](tasksettings-restartcount.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





