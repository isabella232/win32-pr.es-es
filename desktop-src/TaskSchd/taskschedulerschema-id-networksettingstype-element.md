---
title: Elemento Id (networkSettingsType)
description: Contiene un valor GUID que identifica un perfil de red.
ms.assetid: 527912ab-9a81-4570-91c5-8f5943e79a28
keywords:
- Id, elemento Programador de tareas
topic_type:
- apiref
api_name:
- Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3d14865d50e9c3418e3ef65cdbeaea747a98a4ab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259271"
---
# <a name="id-networksettingstype-element"></a>Elemento Id (networkSettingsType)

Contiene un valor GUID que identifica un perfil de red.

``` syntax
<xs:element name="Id"
    type="guidType"
    minOccurs="0"
 />
```

El **elemento Id** se define mediante el tipo complejo [**networkSettingsType.**](taskschedulerschema-networksettingstype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                            | Derivado de                                                                       | Descripción                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetworkSettings (settingsType)**](taskschedulerschema-networksettings-settingstype-element.md) | [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) | Contiene la configuración que el Programador de tareas utiliza para obtener un perfil de red. El Programador de tareas comprueba la disponibilidad de esta red cuando el [**elemento RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) está establecido en **True.**<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, vea [**Id Property of INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_id).

Para el desarrollo de scripts, [**vea NetworkSettings.Id**](networksettings-id.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





