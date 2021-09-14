---
title: Elemento StopOnIdleEnd (idleSettingsType)
description: Especifica que el Programador de tareas detendrá la tarea si la condición de inactividad finaliza antes de que se complete la tarea.
ms.assetid: 5e8e4fd9-bba1-4ede-a0b3-9f50feb1b6f3
keywords:
- Elemento StopOnIdleEnd Programador de tareas
topic_type:
- apiref
api_name:
- TerminateOnIdleEnd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a47a01d7d77f3dd20f055bce8e4bb12fad82c771
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968611"
---
# <a name="stoponidleend-idlesettingstype-element"></a>Elemento StopOnIdleEnd (idleSettingsType)

Especifica que el Programador de tareas detendrá la tarea si la condición de inactividad finaliza antes de que se complete la tarea.

``` syntax
<xs:element name="StopOnIdleEnd"
    type="boolean"
    minOccurs="0"
    default="true"
 />
```

El tipo complejo [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) define el elemento **StopOnIdleEnd.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                       | Derivado de                                                                 | Descripción                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) | Especifica cómo el Programador de tareas realiza tareas cuando el equipo está en estado inactivo.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, [**vea Propiedad StopOnIdleEnd de IIdleSettings.**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_stoponidleend)

Para el desarrollo de scripts, [**vea IdleSettings.StopOnIdleEnd.**](idlesettings-stoponidleend.md)

## <a name="examples"></a>Ejemplos

El siguiente XML define una configuración inactiva que indica que la tarea no debe realizarse cuando finaliza la condición de inactividad.


```XML
<IdleSettings>
    <StopOnIdleEnd>false</StopOnIdleEnd>
</IdleSettings>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





