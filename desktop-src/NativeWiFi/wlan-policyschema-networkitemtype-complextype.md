---
description: Especifica el nombre y el tipo de una red inalámbrica.
ms.assetid: 839afae0-b8e1-489f-8811-19a82c173627
title: Tipo complejo de networkItemType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkItemType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5db7c5fc4d9b5227d9cd29c5e2dfc69da6fad139
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678310"
---
# <a name="networkitemtype-complex-type"></a>Tipo complejo de networkItemType

El tipo complejo de networkItemType especifica el nombre y el tipo de una red inalámbrica.

``` syntax
<xs:complexType name="networkItemType">
    <xs:sequence>
        <xs:element name="networkName"
            type="networkNameType"
         />
        <xs:element name="networkType"
            type="networkTypeType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                      | Tipo                                                                    | Descripción                                                   |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------|
| [**networkName**](wlan-policyschema-networkname-networkitemtype-element.md) | [**networkNameType**](wlan-policyschema-networknametype-simpletype.md) | El identificador del conjunto de servicios (SSID) de la red. <br/> |
| [**networkType**](wlan-policyschema-networktype-networkitemtype-element.md) | [**networkTypeType**](wlan-policyschema-networktypetype-simpletype.md) | El tipo de red. <br/>                                 |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 




