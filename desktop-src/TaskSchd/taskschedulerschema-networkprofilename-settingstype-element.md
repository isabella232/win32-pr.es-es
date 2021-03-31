---
title: Elemento NetworkProfileName (settingsType)
description: Contiene el nombre de un perfil de red. El servicio Programador de tareas comprueba la disponibilidad de esta red cuando el elemento RunOnlyIfNetworkAvailable está establecido en true. El nombre se usa para fines de presentación.
ms.assetid: f02dc75c-6c48-4a42-8263-13d9704b993c
keywords:
- Programador de tareas del elemento NetworkProfileName
topic_type:
- apiref
api_name:
- NetworkProfileName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76a1e89b1d40a422f10512583563e9b1ac56c06f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802768"
---
# <a name="networkprofilename-settingstype-element"></a>Elemento NetworkProfileName (settingsType)

Contiene el nombre de un perfil de red. El servicio Programador de tareas comprueba la disponibilidad de esta red cuando el elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) está establecido en **true**. El nombre se usa para fines de presentación.

``` syntax
<xs:element name="NetworkProfileName"
    type="string"
    minOccurs="0"
 />
```

El elemento **NetworkProfileName** se define mediante el tipo complejo de [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento primario



| Elemento                                                                      | Derivado de                                                         | Descripción                                                                         |
|------------------------------------------------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**Configuración (taskType)**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Especifica la configuración que el Programador de tareas utiliza para realizar la tarea.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





