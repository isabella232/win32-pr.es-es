---
description: Identifica el IHV.
ms.assetid: a99c231c-afd7-44e6-81af-3d49ffef8714
title: Elemento OUIHeader (IHV)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OUIHeader
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5293a6e69c1384922572764674cbadd9980702c49f8945518ff9b0c56beee2d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797926"
---
# <a name="ouiheader-ihv-element"></a>Elemento OUIHeader (IHV)

El elemento OUIHeader (IHV) identifica la IHV.

Windows XP con SP3 y LAN API inalámbrica **para Windows XP con SP2:** No se admite este elemento.

``` syntax
<xs:element name="OUIHeader">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OUI">
                <xs:simpleType>
                    <xs:restriction
                        base="hexBinary"
                    >
                        <xs:length
                            value="3"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="type">
                <xs:simpleType>
                    <xs:restriction
                        base="hexBinary"
                    >
                        <xs:length
                            value="1"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

El elemento [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) define el elemento .

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                   | Tipo | Descripción                                                                                |
|-----------------------------------------------------------|------|--------------------------------------------------------------------------------------------|
| [**Oui**](wlan-profileschema-oui-ouiheader-element.md)   |      | Contiene un hexBinary de 3 bytes que identifica el IHV.<br/>                            |
| [**Tipo**](wlan-profileschema-type-ouiheader-element.md) |      | Contiene un hexBinary de 1 byte que se usa para diferenciar las NIC por el mismo IHV.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**IHV**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**IHV (WLANProfile)**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




