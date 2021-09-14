---
description: Contiene un SSID para una LAN inalámbrica.
ms.assetid: fb3466c4-a586-424b-96e2-ba287c99a1d9
title: Elemento SSID (SSIDConfig)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SSID
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 644a4afbd10fbfff870007befda964fc9babd593
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074186"
---
# <a name="ssid-ssidconfig-element"></a>Elemento SSID (SSIDConfig)

El elemento SSID (SSIDConfig) contiene un SSID para una LAN inalámbrica.

**Windows XP con SP3 e WIRELESS LAN API para Windows XP con SP2:** Como máximo, un **elemento SSID** puede aparecer en un perfil.

``` syntax
<xs:element name="SSID"
    maxOccurs="256"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="hex"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="hexBinary"
                    >
                        <xs:minLength
                            value="1"
                         />
                        <xs:maxLength
                            value="32"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="name"
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
                            value="32"
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

El **elemento SSID** se define mediante el [**elemento SSIDConfig.**](wlan-profileschema-ssidconfig-wlanprofile-element.md)

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                              | Tipo | Descripción                                                           |
|------------------------------------------------------|------|-----------------------------------------------------------------------|
| [**Hexagonal**](wlan-profileschema-hex-ssid-element.md)   |      | Contiene el SSID de una LAN inalámbrica en formato hexadecimal.<br/> |
| [**Nombre**](wlan-profileschema-name-ssid-element.md) |      | Contiene el SSID de una LAN inalámbrica.<br/>                      |



## <a name="remarks"></a>Observaciones

Aunque los [**elementos hexadecimal**](wlan-profileschema-hex-ssid-element.md) y [**name**](wlan-profileschema-name-ssid-element.md) son opcionales, al menos un **elemento hexadecimal** o [**name**](wlan-profileschema-name-ssid-element.md) debe aparecer como elemento secundario del **elemento SSID.**

Cuando la información del perfil se convierte en un SSID, el elemento [**hexadecimal**](wlan-profileschema-hex-ssid-element.md) [](wlan-profileschema-name-ssid-element.md) se convierte al SSID (si está presente) y se omite el elemento name. Si el **elemento hexadecimal** no está presente, el elemento [**name**](wlan-profileschema-name-ssid-element.md) se convierte en un SSID mediante la conversión unicode a ASCII.

Cuando un SSID se almacena en un perfil, siempre [**se**](wlan-profileschema-hex-ssid-element.md) genera el elemento hexadecimal. El [**elemento name**](wlan-profileschema-name-ssid-element.md) solo se genera si la conversión ASCII a Unicode del SSID y la generación del perfil XML son correctas. Es posible que se pierda cierta información del SSID original cuando se convierte a un [**nombre**](wlan-profileschema-name-ssid-element.md).

## <a name="examples"></a>Ejemplos

Para ver perfiles de ejemplo que usan el **elemento SSID,** vea [Ejemplos de perfil inalámbrico.](wireless-profile-samples.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP solo con aplicaciones de escritorio SP3 \[\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                 |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**SSIDConfig (WLANProfile)**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> </dl>

 

 




