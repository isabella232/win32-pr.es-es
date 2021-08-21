---
title: Elemento RestartOnIdle (idleSettingsType)
description: Especifica si la tarea se reinicia cuando el equipo entra en una condición de inactividad más de una vez.
ms.assetid: 7a7a388c-8dc9-4106-82c1-3435d9f89866
keywords:
- Elemento RestartOnIdle Programador de tareas
topic_type:
- apiref
api_name:
- RestartOnIdle
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16a636ebc052bb04a150390659909f0b73cae78871acaacfb4ba529ea2d8e917
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575145"
---
# <a name="restartonidle-idlesettingstype-element"></a>Elemento RestartOnIdle (idleSettingsType)

Especifica si la tarea se reinicia cuando el equipo entra en una condición de inactividad más de una vez.

``` syntax
<xs:element name="RestartOnIdle"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

El tipo complejo [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) define el elemento **RestartOnIdle.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                       | Derivado de                                                                 | Descripción                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) | Especifica cómo el Programador de tareas realiza tareas cuando el equipo está en estado inactivo.<br/> |



## <a name="remarks"></a>Comentarios

Este elemento solo se usa si el [**elemento TerminateOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) está establecido en True.

Para el desarrollo de scripts, esta configuración de tarea se especifica mediante la [**propiedad IdleSettings.RestartOnIdle.**](idlesettings-restartonidle.md)

Para el desarrollo de C++, esta configuración de tarea se especifica mediante la [**propiedad IIdleSettings::RestartOnIdle.**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle)

## <a name="examples"></a>Ejemplos

El xml siguiente define una configuración inactiva que indica que la tarea no debe reiniciarse cuando la condición de inactividad se cycle.


```XML
<IdleSettings>
     <TerminateOnIdleEnd>true</TerminateOnIdleEnd>
     <RestartOnIdle>true</RestartOnIdle>
</IdleSettings>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





