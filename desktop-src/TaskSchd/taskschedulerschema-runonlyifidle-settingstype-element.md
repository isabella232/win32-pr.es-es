---
title: Elemento RunOnlyIfIdle (settingsType)
description: Especifica que la tarea se ejecuta solo cuando el equipo está en estado inactivo.
ms.assetid: 2ef3dd19-4d5c-4399-89b8-d737be4ef85e
keywords:
- Elemento RunOnlyIfIdle Programador de tareas
topic_type:
- apiref
api_name:
- RunOnlyIfIdle
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a623ac6b6ede3f3920ae792bdfb87b7678bdb3047d7bff44f373371fd4cd5c41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099925"
---
# <a name="runonlyifidle-settingstype-element"></a>Elemento RunOnlyIfIdle (settingsType)

Especifica que la tarea se ejecuta solo cuando el equipo está en estado inactivo.

``` syntax
<xs:element name="RunOnlyIfIdle"
    type="boolean"
 />
```

El **elemento RunOnlyIfIdle** se define mediante el [**tipo complejo settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configuración**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene la configuración que el Programador de tareas usa para realizar la tarea.<br/> |



## <a name="remarks"></a>Comentarios

Para el desarrollo de C++, [**vea Propiedad RunOnlyIfIdle de ITaskSettings.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifidle)

Para el desarrollo de scripts, [**vea TaskSettings.RunOnlyIfIdle**](tasksettings-runonlyifidle.md).

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

 

 





