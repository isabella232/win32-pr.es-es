---
title: Elemento NetworkSettings (settingsType)
description: Contiene la configuración que el Programador de tareas utiliza para obtener un perfil de red. El Programador de tareas comprueba la disponibilidad de esta red cuando el elemento RunOnlyIfNetworkAvailable está establecido en True.
ms.assetid: 7452b788-a170-4afe-abc5-ebcd3722da0d
keywords:
- Elemento NetworkSettings Programador de tareas
topic_type:
- apiref
api_name:
- NetworkSettings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5b81e1ff2a9f03646d124f5fd2d3aae27f18069f4b32631f9f8d9e66a193ac3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758485"
---
# <a name="networksettings-settingstype-element"></a>Elemento NetworkSettings (settingsType)

Contiene la configuración que el Programador de tareas utiliza para obtener un perfil de red. El Programador de tareas comprueba la disponibilidad de esta red cuando el [**elemento RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) está establecido en **True.**

``` syntax
<xs:element name="NetworkSettings"
    type="networkSettingsType"
    minOccurs="0"
 />
```

El **elemento NetworkSettings** se define mediante el [**tipo complejo settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                      | Derivado de                                                         | Descripción                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**Configuración (taskType)**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Especifica la configuración que el Programador de tareas usa para realizar la tarea.<br/> |



## <a name="remarks"></a>Comentarios

Para el desarrollo de C++, [**vea Propiedad NetworkSettings de ITaskSettings.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_networksettings)

Para el desarrollo de scripts, [**vea TaskSettings.NetworkSettings**](tasksettings-networksettings.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





