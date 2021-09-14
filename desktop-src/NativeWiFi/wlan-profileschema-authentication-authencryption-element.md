---
description: Especifica el método de autenticación que se usará para conectarse a la LAN inalámbrica.
ms.assetid: fb6c5cce-05d6-41a2-acf4-9ae2713079dd
title: elemento authentication (authEncryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authentication
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 02895da685c78484c907af51745264abb81086da
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245570"
---
# <a name="authentication-authencryption-element"></a>elemento authentication (authEncryption)

El elemento authentication (authEncryption) especifica el método de autenticación que se usará para conectarse a la LAN inalámbrica.

``` syntax
<xs:element name="authentication">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="open"
             />
            <xs:enumeration
                value="shared"
             />
            <xs:enumeration
                value="WPA"
             />
            <xs:enumeration
                value="WPAPSK"
             />
            <xs:enumeration
                value="WPA2"
             />
            <xs:enumeration
                value="WPA2PSK"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

El elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) define el elemento .

## <a name="remarks"></a>Observaciones

En la tabla siguiente se describen los valores de enumeración.



| Value   | Descripción                            |
|---------|----------------------------------------|
| abierto    | Abra la autenticación 802.11.            |
| shared  | Autenticación compartida 802.11.          |
| WPA     | WPA-Enterprise autenticación 802.11.  |
| WPAPSK  | WPA-Personal autenticación 802.11.    |
| WPA2    | WPA2-Enterprise autenticación 802.11. |
| WPA2PSK | WPA2-Personal autenticación 802.11.   |



 

Para obtener más información sobre los métodos de autenticación 802.11, vea las especificaciones [WPA](https://en.wikipedia.org/wiki/Wi-Fi_Protected_Access), [802.1X](https://ieeexplore.ieee.org/document/1438730)y [802.11i.](https://standards.ieee.org/findstds/standard/802.11i-2004.html)

## <a name="examples"></a>Ejemplos

Para ver los perfiles de ejemplo que usan el **elemento de autenticación,** vea [Ejemplos de perfil inalámbrico.](wireless-profile-samples.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP solo con aplicaciones de escritorio sp3 \[\]<br/> |
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

 

 




