---
title: Nombre (networkSettingsType) (elemento)
description: Contiene el nombre de un perfil de red. El nombre se usa para fines de presentación.
ms.assetid: 86e4e68d-3c36-41eb-8563-d7d5125a5957
keywords:
- Name (elemento) Programador de tareas
topic_type:
- apiref
api_name:
- Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed877b731b64ee8f2d807067b59399decc0eefe4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534456"
---
# <a name="name-networksettingstype-element"></a>Nombre (networkSettingsType) (elemento)

Contiene el nombre de un perfil de red. El nombre se usa para fines de presentación.

``` syntax
<xs:element name="Name"
    type="nonEmptyString"
    minOccurs="0"
 />
```

El elemento **Name** se define mediante el tipo complejo [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                                            | Derivado de                                                                       | Descripción                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetworkSettings (settingsType)**](taskschedulerschema-networksettings-settingstype-element.md) | [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md) | Contiene la configuración que usa el servicio de Programador de tareas para obtener un perfil de red. El servicio Programador de tareas comprueba la disponibilidad de esta red cuando el elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) está establecido en **true**.<br/> |



## <a name="remarks"></a>Observaciones

Para el desarrollo de C++, vea la [**propiedad Name de INetworkSettings**](/windows/desktop/api/taskschd/nf-taskschd-inetworksettings-get_name).

Para el desarrollo de scripts, vea [**NetworkSettings.Name**](networksettings-name.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





