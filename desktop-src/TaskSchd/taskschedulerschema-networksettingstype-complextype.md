---
title: Tipo complejo de networkSettingsType
description: Define los elementos que proporcionan los valores que el servicio Programador de tareas utiliza para obtener un perfil de red.
ms.assetid: e5df1dda-b691-47ff-a956-50ff1ce9c7cc
keywords:
- tipo complejo de networkSettingsType Programador de tareas
topic_type:
- apiref
api_name:
- networkSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb2a8389b1e1f368bedf03fa38dce9c8e262a401
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996606"
---
# <a name="networksettingstype-complex-type"></a>Tipo complejo de networkSettingsType

Define los elementos que proporcionan los valores que el servicio Programador de tareas utiliza para obtener un perfil de red.

``` syntax
<xs:complexType name="networkSettingsType">
    <xs:all>
        <xs:element name="Name"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="Id"
            type="guidType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                              | Tipo                                                        | Descripción                                                                                 |
|----------------------------------------------------------------------|-------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**Sesión**](taskschedulerschema-id-networksettingstype-element.md)     | [**guidType**](taskschedulerschema-guidtype-simpletype.md) | Especifica un valor de GUID que identifica un perfil de red. <br/>                       |
| [**Name**](taskschedulerschema-name-networksettingstype-element.md) | nonEmptyString                                              | Especifica el nombre de un perfil de red. El nombre se usa para fines de presentación. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 





