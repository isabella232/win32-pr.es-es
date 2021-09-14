---
description: Lista de identificadores de dominio de identificador de acceso de red (NAI).
ms.assetid: e77802ee-4017-4f04-ae71-5d6d0de8fcf3
title: Elemento NAIRealm (Hotspot2)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NAIRealm
api_type:
- Schema
api_location: ''
ms.openlocfilehash: a7c8fcf85bd23c13f0e7501d59c3db62c2bf82f5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245499"
---
# <a name="nairealm-hotspot2-element"></a>Elemento NAIRealm (Hotspot2)

Lista de identificadores de dominio de identificador de acceso de red (NAI). Las entradas de esta lista suelen tener el formato `user@domain` . La lista de dominios de NAI es el método preferido para identificar la mayoría de los operadores que no son móviles, como MSO, operadores de conexión y lugares públicos.

``` syntax
<xs:element name="NAIRealm"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                maxOccurs="256"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:minLength
                            value="1"
                         />
                        <xs:maxLength
                            value="255"
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



| Elemento | Tipo | Descripción                                                   |
|---------|------|---------------------------------------------------------------|
| name    |      | Identificador de dominio único. Normalmente, tiene el formato `user@domain` . |



 

 



