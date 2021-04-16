---
description: Una lista de identificadores de red móvil de tierra (PLMN).
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687129"
---
# <a name="network3gpp-hotspot2-element"></a>Elemento Network3GPP (Hotspot2)

Una lista de identificadores de red móvil de tierra (PLMN).

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

El elemento se define mediante el elemento [**Hotspot2**](wlan-profileschema-hotspot2-element.md) .

## <a name="child-elements"></a>Elementos secundarios



| Elemento | Tipo | Descripción                                                                                                             |
|---------|------|-------------------------------------------------------------------------------------------------------------------------|
| PLMNID  |      | Un identificador PLMN individual. Se trata de un número decimal de 5 o 6 dígitos correspondiente a la MCC/MNC de una red 3GPP.<br/> |



 

 




