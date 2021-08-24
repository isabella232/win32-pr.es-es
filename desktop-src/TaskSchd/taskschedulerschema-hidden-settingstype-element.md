---
title: Elemento Hidden (settingsType)
description: Especifica que la tarea no estará visible en la interfaz de usuario de forma predeterminada.
ms.assetid: a08c270f-6d4e-4473-9538-c1e1e21b3b10
keywords:
- Elemento oculto Programador de tareas
topic_type:
- apiref
api_name:
- Hidden
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9820008ead01930eff23a50408f4952d08e9190984432f65c3d9e5f4eedbef7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658915"
---
# <a name="hidden-settingstype-element"></a>Elemento Hidden (settingsType)

Especifica que la tarea no estará visible en la interfaz de usuario de forma predeterminada. Sin embargo, los administradores pueden invalidar esta configuración mediante el uso de un "modificador maestro" que hace que todas las tareas sean visibles en la interfaz de usuario.

``` syntax
<xs:element name="Hidden"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

El **elemento Hidden** se define mediante el tipo complejo [**settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                                                    |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**Configuración**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene la configuración que Programador de tareas para realizar la tarea.<br/> |



## <a name="remarks"></a>Comentarios

Para el desarrollo de C++, [**vea Propiedad oculta de ITaskSettings.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_hidden)

Para el desarrollo de scripts, [**vea TaskSettings.Hidden.**](tasksettings-hidden.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programador de tareas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





