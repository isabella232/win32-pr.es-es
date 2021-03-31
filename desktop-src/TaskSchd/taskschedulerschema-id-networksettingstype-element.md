---
title: Identificador (networkSettingsType) (elemento)
description: Contiene un valor GUID que identifica un perfil de red.
ms.assetid: 527912ab-9a81-4570-91c5-8f5943e79a28
keywords:
- Elemento ID Programador de tareas
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151182"
---
# <a name="id-networksettingstype-element"></a>Identificador (networkSettingsType) (elemento)

Contiene un valor GUID que identifica un perfil de red.

``` syntax
<xs:element name="Id"
    type="guidType"
    minOccurs="0"
 />
```

El elemento **ID** se define mediante el tipo complejo [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                            | Derivado de                                                                       | Descripción                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetworkSettings (settingsType)**](taskschedulerschema-networksettings-settingstype-element.md) | [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) | Contiene la configuración que usa el servicio de Programador de tareas para obtener un perfil de red. El servicio Programador de tareas comprueba la disponibilidad de esta red cuando el elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) está establecido en **true**.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, vea [**propiedad ID de INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_id).

Para el desarrollo de scripts, vea [**NetworkSettings.ID**](networksettings-id.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





