---
description: Especifica el nombre y el tipo de una red inalámbrica.
ms.assetid: 839afae0-b8e1-489f-8811-19a82c173627
title: tipo complejo networkItemType
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
ms.openlocfilehash: 9c5a08eafebc81a1ff9f18c3d4c2cc9df9c096ac0fef9c10ff1caf1142a1ecf8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800195"
---
# <a name="networkitemtype-complex-type"></a>tipo complejo networkItemType

El tipo complejo networkItemType especifica el nombre y el tipo de una red inalámbrica.

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
| [**networkName**](wlan-policyschema-networkname-networkitemtype-element.md) | [**networkNameType**](wlan-policyschema-networknametype-simpletype.md) | Identificador del conjunto de servicios (SSID) de la red. <br/> |
| [**networkType**](wlan-policyschema-networktype-networkitemtype-element.md) | [**networkTypeType**](wlan-policyschema-networktypetype-simpletype.md) | El tipo de red. <br/>                                 |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 




