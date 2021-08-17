---
title: Elemento NetworkProfileName (settingsType)
description: Contiene el nombre de un perfil de red. El Programador de tareas comprueba la disponibilidad de esta red cuando el elemento RunOnlyIfNetworkAvailable está establecido en True. El nombre se usa para mostrar.
ms.assetid: f02dc75c-6c48-4a42-8263-13d9704b993c
keywords:
- Elemento NetworkProfileName Programador de tareas
topic_type:
- apiref
api_name:
- NetworkProfileName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 464c8b8f23dfeed6ea7c3412c3eeec07f20e5a8a7fcea662b4a16dfac7cb3fb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758495"
---
# <a name="networkprofilename-settingstype-element"></a>Elemento NetworkProfileName (settingsType)

Contiene el nombre de un perfil de red. El Programador de tareas comprueba la disponibilidad de esta red cuando el [**elemento RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) está establecido en **True.** El nombre se usa para mostrar.

``` syntax
<xs:element name="NetworkProfileName"
    type="string"
    minOccurs="0"
 />
```

El **elemento NetworkProfileName** se define mediante el [**tipo complejo settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                      | Derivado de                                                         | Descripción                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**Configuración (taskType)**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Especifica la configuración que el Programador de tareas utiliza para realizar la tarea.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





