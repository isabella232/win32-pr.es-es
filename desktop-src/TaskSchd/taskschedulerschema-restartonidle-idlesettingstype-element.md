---
title: Elemento RestartOnIdle (idleSettingsType)
description: Especifica si la tarea se reinicia cuando el equipo se recorre en una condición de inactividad más de una vez.
ms.assetid: 7a7a388c-8dc9-4106-82c1-3435d9f89866
keywords:
- Programador de tareas del elemento RestartOnIdle
topic_type:
- apiref
api_name:
- RestartOnIdle
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec1d20798b7ceb6ad6ebe2c3a92896600e36eec1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686224"
---
# <a name="restartonidle-idlesettingstype-element"></a>Elemento RestartOnIdle (idleSettingsType)

Especifica si la tarea se reinicia cuando el equipo se recorre en una condición de inactividad más de una vez.

``` syntax
<xs:element name="RestartOnIdle"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

El elemento **RestartOnIdle** se define mediante el tipo complejo de [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                       | Derivado de                                                                 | Descripción                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) | Especifica cómo realiza el Programador de tareas las tareas cuando el equipo está en un estado de inactividad.<br/> |



## <a name="remarks"></a>Observaciones

Este elemento solo se utiliza si el elemento [**TerminateOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) está establecido en true.

Para el desarrollo de scripts, esta configuración de tarea se especifica mediante la propiedad [**IdleSettings. RestartOnIdle**](idlesettings-restartonidle.md) .

En el desarrollo de C++, esta configuración de tarea se especifica mediante la propiedad [**IIdleSettings:: RestartOnIdle**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle) .

## <a name="examples"></a>Ejemplos

El siguiente código XML define un valor de inactivo que indica que la tarea no debe reiniciarse cuando la condición de inactividad se repite.


```XML
<IdleSettings>
     <TerminateOnIdleEnd>true</TerminateOnIdleEnd>
     <RestartOnIdle>true</RestartOnIdle>
</IdleSettings>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas elementos de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> </dl>

 

 





