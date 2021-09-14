---
description: Especifica el tipo de cifrado de datos que se usará para conectarse a una LAN inalámbrica.
ms.assetid: 0ba24106-bd6f-465a-af80-ce85501756b9
title: elemento encryption (authEncryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- encryption
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7efd9e0865cb489a7d033772112b0aaeb8a8fb23
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245523"
---
# <a name="encryption-authencryption-element"></a>elemento encryption (authEncryption)

El elemento encryption (authEncryption) especifica el tipo de cifrado de datos que se usará para conectarse a una LAN inalámbrica.

``` syntax
<xs:element name="encryption">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="none"
             />
            <xs:enumeration
                value="WEP"
             />
            <xs:enumeration
                value="TKIP"
             />
            <xs:enumeration
                value="AES"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

El elemento se define mediante el [**elemento authEncryption.**](wlan-profileschema-authencryption-security-element.md)

## <a name="remarks"></a>Observaciones

Cuando el **elemento de** cifrado tiene un valor de WEP, [**keyType**](wlan-profileschema-keytype-sharedkey-element.md) debe establecerse en **networkKey.**

El método de cifrado AES se especifica en las [especificaciones 802.1X](https://ieeexplore.ieee.org/document/1438730) y [802.11i.](https://standards.ieee.org/findstds/standard/802.11i-2004.html)

## <a name="examples"></a>Ejemplos

Para ver los perfiles de ejemplo que usan el **elemento de** cifrado, vea Ejemplos de [perfil inalámbrico](wireless-profile-samples.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP solo con aplicaciones de escritorio SP3 \[\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**authEncryption**](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**authEncryption (seguridad)**](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 




