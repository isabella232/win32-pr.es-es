---
title: Elemento Name (networkSettingsType)
description: Contiene el nombre de un perfil de red. El nombre se usa con fines para mostrar.
ms.assetid: 86e4e68d-3c36-41eb-8563-d7d5125a5957
keywords:
- Nombre, elemento Programador de tareas
topic_type:
- apiref
api_name:
- Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c41b92c7e63a820c2a2a34378b041bec3a49f432b52887a732c3f3bfd360b10f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758514"
---
# <a name="name-networksettingstype-element"></a>Elemento Name (networkSettingsType)

Contiene el nombre de un perfil de red. El nombre se usa con fines para mostrar.

``` syntax
<xs:element name="Name"
    type="nonEmptyString"
    minOccurs="0"
 />
```

El **tipo** complejo [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) define el elemento Name.

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                            | Derivado de                                                                       | Descripción                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetworkSettings (settingsType)**](taskschedulerschema-networksettings-settingstype-element.md) | [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) | Contiene la configuración que el Programador de tareas utiliza para obtener un perfil de red. El Programador de tareas comprueba la disponibilidad de esta red cuando el [**elemento RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) está establecido en **True.**<br/> |



## <a name="remarks"></a>Comentarios

Para el desarrollo de C++, [**vea Propiedad Name de INetworkSettings.**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_name)

Para el desarrollo de scripts, [**consulte NetworkSettings.Name**](networksettings-name.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





