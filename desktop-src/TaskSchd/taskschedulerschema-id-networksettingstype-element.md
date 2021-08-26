---
title: Elemento Id (networkSettingsType)
description: Contiene un valor GUID que identifica un perfil de red.
ms.assetid: 527912ab-9a81-4570-91c5-8f5943e79a28
keywords:
- Identificador del elemento Programador de tareas
topic_type:
- apiref
api_name:
- Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 06196710b9db9d39d45a24b78bccabf479ef210a97f3cea1fd19286b76f2fc42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125845"
---
# <a name="id-networksettingstype-element"></a>Elemento Id (networkSettingsType)

Contiene un valor GUID que identifica un perfil de red.

``` syntax
<xs:element name="Id"
    type="guidType"
    minOccurs="0"
 />
```

El tipo complejo [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) define el elemento **Id.**

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                            | Derivado de                                                                       | Descripción                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetworkSettings (settingsType)**](taskschedulerschema-networksettings-settingstype-element.md) | [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) | Contiene la configuración que el Programador de tareas utiliza para obtener un perfil de red. El Programador de tareas comprueba la disponibilidad de esta red cuando el [**elemento RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) está establecido en **True.**<br/> |



## <a name="remarks"></a>Comentarios

Para el desarrollo de C++, vea [**Id Property of INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_id).

Para el desarrollo de scripts, [**consulte NetworkSettings.Id**](networksettings-id.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





