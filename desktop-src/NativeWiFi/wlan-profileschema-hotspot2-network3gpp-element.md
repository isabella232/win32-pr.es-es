---
description: Lista de los IDs de Public Land Mobile Network (PLMN).
ms.assetid: 2e5e23c0-e98f-48f8-97b8-c5f88c80c51e
title: Elemento Network3GPP (Hotspot2)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Network3GPP
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7e19a7ccbc1579eb02ed47da82afe1eeaf8fed53
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245492"
---
# <a name="network3gpp-hotspot2-element"></a>Elemento Network3GPP (Hotspot2)

Lista de los IDs de Public Land Mobile Network (PLMN).

``` syntax
<xs:element name="Network3GPP"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="PLMNID"
                minOccurs="0"
                maxOccurs="256"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:minLength
                            value="5"
                         />
                        <xs:maxLength
                            value="6"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

El elemento se define mediante el [**elemento Hotspot2.**](wlan-profileschema-hotspot2-element.md)

## <a name="child-elements"></a>Elementos secundarios



| Elemento | Tipo | Descripción                                                                                                             |
|---------|------|-------------------------------------------------------------------------------------------------------------------------|
| PLMNID  |      | Id. de PLMN individual. Se trata de un número decimal de 5 o 6 dígitos correspondiente al MCC/MNC de una red 3GPP.<br/> |



 

 




