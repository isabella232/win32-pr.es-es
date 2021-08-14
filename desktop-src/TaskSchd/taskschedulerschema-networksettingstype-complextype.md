---
title: tipo complejo networkSettingsType
description: Define los elementos que proporcionan la configuración que el Programador de tareas utiliza para obtener un perfil de red.
ms.assetid: e5df1dda-b691-47ff-a956-50ff1ce9c7cc
keywords:
- tipo complejo networkSettingsType Programador de tareas
topic_type:
- apiref
api_name:
- networkSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d9969e4e3827d926d8c295d4e1a3ce7b77550804eb4995a267a920a16871837f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758475"
---
# <a name="networksettingstype-complex-type"></a>tipo complejo networkSettingsType

Define los elementos que proporcionan la configuración que el Programador de tareas utiliza para obtener un perfil de red.

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
| [**Id**](taskschedulerschema-id-networksettingstype-element.md)     | [**guidType**](taskschedulerschema-guidtype-simpletype.md) | Especifica un valor GUID que identifica un perfil de red. <br/>                       |
| [**Nombre**](taskschedulerschema-name-networksettingstype-element.md) | nonEmptyString                                              | Especifica el nombre de un perfil de red. El nombre se usa con fines para mostrar. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 





