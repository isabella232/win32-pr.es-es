---
description: Especifica el método de autenticación que se va a usar para conectarse a la LAN inalámbrica.
ms.assetid: fb6c5cce-05d6-41a2-acf4-9ae2713079dd
title: Elemento Authentication (authEncryption)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275801"
---
# <a name="authentication-authencryption-element"></a>Elemento Authentication (authEncryption)

El elemento Authentication (authEncryption) especifica el método de autenticación que se va a usar para conectarse a la LAN inalámbrica.

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

El elemento se define mediante el elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .

## <a name="remarks"></a>Observaciones

En la tabla siguiente se describen los valores de enumeración.



| Value   | Descripción                            |
|---------|----------------------------------------|
| abrir    | Abra la autenticación 802,11.            |
| shared  | Autenticación 802,11 compartida.          |
| WPA     | Autenticación WPA-Enterprise 802,11.  |
| WPAPSK  | Autenticación WPA-Personal 802,11.    |
| WPA2    | Autenticación WPA2-Enterprise 802,11. |
| WPA2PSK | Autenticación WPA2-Personal 802,11.   |



 

Para obtener más información acerca de los métodos de autenticación de 802,11, consulte las especificaciones de [WPA](https://en.wikipedia.org/wiki/Wi-Fi_Protected_Access), [802.1 x](https://ieeexplore.ieee.org/document/1438730)y [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .

## <a name="examples"></a>Ejemplos

Para ver los perfiles de ejemplo que usan el elemento de **autenticación** , consulte [ejemplos de perfiles inalámbricos](wireless-profile-samples.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                |
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

 

 




