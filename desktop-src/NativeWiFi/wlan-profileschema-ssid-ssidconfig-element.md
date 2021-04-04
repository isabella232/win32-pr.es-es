---
description: Contiene un SSID para una LAN inalámbrica.
ms.assetid: fb3466c4-a586-424b-96e2-ba287c99a1d9
title: SSID (elemento SSIDConfig)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910649"
---
# <a name="ssid-ssidconfig-element"></a>SSID (elemento SSIDConfig)

El elemento SSID (SSIDConfig) contiene un SSID para una LAN inalámbrica.

**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Como máximo, un elemento **SSID** puede aparecer en un perfil.

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

El elemento **SSID** se define mediante el elemento [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) .

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                              | Tipo | Descripción                                                           |
|------------------------------------------------------|------|-----------------------------------------------------------------------|
| [**hex**](wlan-profileschema-hex-ssid-element.md)   |      | Contiene el SSID de una LAN inalámbrica en formato hexadecimal.<br/> |
| [**name**](wlan-profileschema-name-ssid-element.md) |      | Contiene el SSID para una LAN inalámbrica.<br/>                      |



## <a name="remarks"></a>Observaciones

Aunque los elementos [**Hex**](wlan-profileschema-hex-ssid-element.md) y [**Name**](wlan-profileschema-name-ssid-element.md) son opcionales, al menos un elemento **Hex** o [**Name**](wlan-profileschema-name-ssid-element.md) debe aparecer como elemento secundario del elemento **SSID** .

Cuando la información de perfil se convierte en un SSID, el elemento [**Hex**](wlan-profileschema-hex-ssid-element.md) se convierte en el SSID (si existe) y se omite el elemento de [**nombre**](wlan-profileschema-name-ssid-element.md) . Si el elemento **Hex** no está presente, el elemento de [**nombre**](wlan-profileschema-name-ssid-element.md) se convierte en un SSID mediante la conversión de Unicode a ASCII.

Cuando se almacena un SSID en un perfil, siempre se genera el elemento [**Hex**](wlan-profileschema-hex-ssid-element.md) . El elemento [**Name**](wlan-profileschema-name-ssid-element.md) solo se genera si la conversión de ASCII a Unicode del SSID y la generación de perfiles XML son correctas. Es posible que se pierda parte de la información del SSID original cuando se convierte en un [**nombre**](wlan-profileschema-name-ssid-element.md).

## <a name="examples"></a>Ejemplos

Para ver los perfiles de ejemplo que usan el elemento **SSID** , consulte [ejemplos de perfiles inalámbricos](wireless-profile-samples.md).

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

[**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**SSIDConfig (WLANProfile)**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
</dt> </dl>

 

 




