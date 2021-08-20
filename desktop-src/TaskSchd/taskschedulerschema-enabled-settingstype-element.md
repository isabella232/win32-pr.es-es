---
title: Elemento Enabled (settingsType)
description: Especifica que la tarea está habilitada. La tarea solo se puede realizar cuando esta configuración es True.
ms.assetid: d28f0d54-1205-4b70-a178-72d809da9ce1
keywords:
- Elemento Enabled Programador de tareas
topic_type:
- apiref
api_name:
- Enabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ff198520e354147ff092b2374bb5a766e1ce1c6db6a4b8fc6302b92670bddcda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131874"
---
# <a name="enabled-settingstype-element"></a>Elemento Enabled (settingsType)

Especifica que la tarea está habilitada. La tarea solo se puede realizar cuando esta configuración es True.

``` syntax
<xs:element name="Enabled"
    type="boolean"
    default="true"
    minOccurs="1"
 />
```

El **elemento Enabled** se define mediante el tipo complejo [**settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                           | Derivado de                                                         | Descripción                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configuración**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene la configuración que el Programador de tareas usa para realizar la tarea.<br/> |



## <a name="remarks"></a>Comentarios

Para el desarrollo de C++, [**vea Enabled Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_enabled).

Para el desarrollo de scripts, [**vea TaskSettings.Enabled.**](tasksettings-enabled.md)

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo completo del XML de una tarea habilitada, vea [Ejemplo de desencadenador de tiempo (XML).](time-trigger-example--xml-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





