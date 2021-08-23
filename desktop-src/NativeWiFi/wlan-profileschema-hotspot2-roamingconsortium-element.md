---
description: Lista de identificadores únicos organizativos (OUI) asignados por IEEE.
ms.assetid: 4a9885b6-2e57-4a16-8e1d-b5b0797e09db
title: Elemento RoamingConsortium (Hotspot2)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RoamingConsortium
api_type:
- Schema
api_location: ''
ms.openlocfilehash: ca2ee96deaddad14d8def14c59b490eaea54803d779e288dbf826f6514d674a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684155"
---
# <a name="roamingconsortium-hotspot2-element"></a>Elemento RoamingConsortium (Hotspot2)

Lista de identificadores únicos organizativos (OUI) asignados por IEEE.

``` syntax
<xs:element name="RoamingConsortium"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OUI"
                minOccurs="0"
                maxOccurs="256"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="hexBinary"
                    >
                        <xs:minLength
                            value="3"
                         />
                        <xs:maxLength
                            value="5"
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



| Elemento | Tipo | Descripción                                                               |
|---------|------|---------------------------------------------------------------------------|
| Oui     |      | Una única OUI, con formato de número hexadecimal de tamaño variable.<br/> |



 

 




