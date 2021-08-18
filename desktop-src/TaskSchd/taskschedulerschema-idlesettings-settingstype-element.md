---
title: Elemento IdleSettings (settingsType)
description: Especifica cómo el Programador de tareas realiza tareas cuando el equipo está en estado inactivo.
ms.assetid: 23d57417-95a9-42e3-904c-7f0859fcda7c
keywords:
- Elemento IdleSettings Programador de tareas
topic_type:
- apiref
api_name:
- IdleSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fc0a4c3fc978c93d13be8faa62012d3928d47da5b5a214ce50f5506992f1fc8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991225"
---
# <a name="idlesettings-settingstype-element"></a>Elemento IdleSettings (settingsType)

Especifica cómo el Programador de tareas realiza tareas cuando el equipo está en estado inactivo. Para obtener información sobre las condiciones de inactividad, vea [Task Idle Conditions](task-idle-conditions.md).

``` syntax
<xs:element name="IdleSettings"
    type="idleSettingsType"
    minOccurs="0"
 />
```

El **elemento IdleSettings** se define mediante el [**tipo complejo settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento primario

| Elemento                                                           | Derivado de                                                         | Descripción                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configuración**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene la configuración que el Programador de tareas usa para realizar la tarea.<br/> |

## <a name="child-elements"></a>Elementos secundarios

> [!NOTE]
> La *configuración de* *Duración y Tiempo de espera* está en desuso. Todavía están presentes en la interfaz Programador de tareas usuario y sus métodos de interfaz pueden devolver valores válidos, pero ya no se usan.

| Elemento                                                                                  | Tipo     | Descripción                                                                                                              |
|------------------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------|
| [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md)      | boolean  | Especifica si la tarea se reinicia cuando el equipo entra en una condición de inactividad más de una vez.<br/>       |
| [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) | boolean  | Especifica que el Programador de tareas detendrá la tarea si la condición de inactividad finaliza antes de que se complete la tarea.<br/> |
| **En desuso:** [ **Duración**](taskschedulerschema-duration-idlesettingstype-element.md)                | duration | Especifica cuánto tiempo debe estar el equipo en estado de inactividad antes de que se ejecute la tarea.<br/>                              |
| **En desuso:** [ **WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md)          | duration | Especifica la cantidad de tiempo que el Programador de tareas esperará a que se produzca una condición de inactividad.<br/>                |

## <a name="remarks"></a>Comentarios

Para el desarrollo de scripts, la configuración inactiva se especifica mediante la [**propiedad TaskSettings.IdleSettings.**](tasksettings-idlesettings.md)

Para el desarrollo de C++, la configuración inactiva se especifica mediante la [**propiedad ITaskSettings::IdleSettings.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings)

## <a name="examples"></a>Ejemplos

El xml siguiente define un elemento de configuración que permite a Programador de tareas esperar 24 horas para una condición de inactividad y, a continuación, permite que solo 10 minutos {IdleDuration) inicie la tarea.

```XML
<Settings>
    <IdleSettings>
        <StopOnIdleEnd>false</StopOnIdleEnd>
        <RestartOnIdle>false</RestartOnIdle> 
        <!-- WaitTimeout and Duration have been deprecated -->
        <Duration>PT5M</Duration>
        <WaitTimeout>PT24H</WaitTimeout>
    </IdleSettings>       
</Settings>
```

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |

## <a name="see-also"></a>Vea también

[Programador de tareas de esquema](task-scheduler-schema-elements.md)

[Programador de tareas](task-scheduler-start-page.md)
