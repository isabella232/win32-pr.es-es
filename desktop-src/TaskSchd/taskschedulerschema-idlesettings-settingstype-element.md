---
title: Elemento IdleSettings (settingsType)
description: Especifica cómo realiza el Programador de tareas las tareas cuando el equipo está en un estado de inactividad.
ms.assetid: 23d57417-95a9-42e3-904c-7f0859fcda7c
keywords:
- Programador de tareas del elemento IdleSettings
topic_type:
- apiref
api_name:
- IdleSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ae8b7953f31d7e9c6f01387d3136f01d8ab697a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150799"
---
# <a name="idlesettings-settingstype-element"></a>Elemento IdleSettings (settingsType)

Especifica cómo realiza el Programador de tareas las tareas cuando el equipo está en un estado de inactividad. Para obtener información sobre las condiciones de inactividad, consulte [condiciones de inactividad de tareas](task-idle-conditions.md).

``` syntax
<xs:element name="IdleSettings"
    type="idleSettingsType"
    minOccurs="0"
 />
```

El elemento **IdleSettings** se define mediante el tipo complejo de [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento primario

| Elemento                                                           | Derivado de                                                         | Descripción                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configuración**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene la configuración que el Programador de tareas utiliza para realizar la tarea.<br/> |

## <a name="child-elements"></a>Elementos secundarios

> [!NOTE]
> La configuración de *Duration* y *WaitTimeout* está en desuso. Todavía están presentes en la interfaz de usuario de Programador de tareas y sus métodos de interfaz todavía pueden devolver valores válidos, pero ya no se usan.

| Elemento                                                                                  | Tipo     | Descripción                                                                                                              |
|------------------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------|
| [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md)      | boolean  | Especifica si la tarea se reinicia cuando el equipo se recorre en una condición de inactividad más de una vez.<br/>       |
| [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) | boolean  | Especifica que el Programador de tareas detendrá la tarea si la condición de inactividad finaliza antes de que se complete la tarea.<br/> |
| En **desuso**: [ **duración**](taskschedulerschema-duration-idlesettingstype-element.md)                | duration | Especifica cuánto tiempo el equipo debe estar en un estado de inactividad antes de que se ejecute la tarea.<br/>                              |
| En **desuso**: [ **WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md)          | duration | Especifica la cantidad de tiempo que el Programador de tareas esperará a que se produzca una condición de inactividad.<br/>                |

## <a name="remarks"></a>Observaciones

Para el desarrollo de scripts, la configuración inactiva se especifica mediante la propiedad [**TaskSettings. IdleSettings**](tasksettings-idlesettings.md) .

En el desarrollo de C++, la configuración inactiva se especifica mediante la propiedad [**ITaskSettings:: IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings) .

## <a name="examples"></a>Ejemplos

En el código XML siguiente se define un elemento de configuración que permite a Programador de tareas esperar 24 horas por una condición de inactividad y, a continuación, solo permite 10 minutos {IdleDuration) para iniciar la tarea.

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |

## <a name="see-also"></a>Vea también

[Programador de tareas elementos de esquema](task-scheduler-schema-elements.md)

[Programador de tareas](task-scheduler-start-page.md)
