---
description: Contiene varios valores de módulo específicos del medio (MSM).
ms.assetid: 31f98af8-a577-4f6a-9a0a-b182b5a89cc3
title: Elemento MSM (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSM
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 78540c29239df9118732561562985021a512e104b0ddc5e05d43d89f37dd5e33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797945"
---
# <a name="msm-wlanprofile-element"></a>Elemento MSM (WLANProfile)

El elemento MSM (WLANProfile) contiene varias configuraciones de módulos específicos del medio (MSM).

``` syntax
<xs:element name="MSM"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="connectivity"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="phyType"
                            minOccurs="0"
                            maxOccurs="4"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="string"
                                >
                                    <xs:enumeration
                                        value="a"
                                     />
                                    <xs:enumeration
                                        value="b"
                                     />
                                    <xs:enumeration
                                        value="g"
                                     />
                                    <xs:enumeration
                                        value="n"
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
            <xs:element name="security"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="authEncryption">
                            <xs:complexType>
                                <xs:sequence>
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
                                    <xs:element name="useOneX"
                                        type="boolean"
                                        minOccurs="0"
                                     />
                                    <xs:any
                                        processContents="lax"
                                        minOccurs="0"
                                        maxOccurs="unbounded"
                                        namespace="##other"
                                     />
                                </xs:sequence>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="sharedKey"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="keyType">
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="string"
                                            >
                                                <xs:enumeration
                                                    value="networkKey"
                                                 />
                                                <xs:enumeration
                                                    value="passPhrase"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="protected"
                                        type="boolean"
                                     />
                                    <xs:element name="keyMaterial"
                                        type="string"
                                     />
                                    <xs:any
                                        processContents="lax"
                                        minOccurs="0"
                                        maxOccurs="unbounded"
                                        namespace="##other"
                                     />
                                </xs:sequence>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="keyIndex"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="integer"
                                >
                                    <xs:minInclusive
                                        value="0"
                                     />
                                    <xs:maxInclusive
                                        value="3"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="PMKCacheMode"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="string"
                                >
                                    <xs:enumeration
                                        value="disabled"
                                     />
                                    <xs:enumeration
                                        value="enabled"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="PMKCacheTTL"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="integer"
                                >
                                    <xs:minInclusive
                                        value="5"
                                     />
                                    <xs:maxInclusive
                                        value="1400"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="PMKCacheSize"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="integer"
                                >
                                    <xs:minInclusive
                                        value="1"
                                     />
                                    <xs:maxInclusive
                                        value="255"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="preAuthMode"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="string"
                                >
                                    <xs:enumeration
                                        value="disabled"
                                     />
                                    <xs:enumeration
                                        value="enabled"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="preAuthThrottle"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="integer"
                                >
                                    <xs:minInclusive
                                        value="1"
                                     />
                                    <xs:maxInclusive
                                        value="16"
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

El elemento se define mediante el [**elemento WLANProfile.**](wlan-profileschema-wlanprofile-element.md)

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                            | Tipo                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**authEncryption**](wlan-profileschema-authencryption-security-element.md)       |                                                                   | Especifica el par de autenticación y cifrado que se usará para este perfil.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**Autenticación**](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | Especifica el par de autenticación y cifrado que se usará para este perfil.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**Conectividad**](wlan-profileschema-connectivity-msm-element.md)                |                                                                   | Contiene varias configuraciones de conectividad. Este elemento es opcional.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**Cifrado**](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | Establece el cifrado de datos que se usará para conectarse a la LAN inalámbrica.<br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**keyIndex**](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | Especifica qué índice de clave se debe usar para cifrar el tráfico inalámbrico. Esto solo se usa cuando keyType se establece en networkKey.<br/>                                                                                                                                                                                                                                                                                          |
| [**keyMaterial**](wlan-profileschema-keymaterial-sharedkey-element.md)            | [string](/dotnet/api/system.string)   | Contiene la clave de red o frase de contraseña.<br/>                                                                                                                                                                                                                                                                                                                                                                           |
| [**keyType**](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | Tipo de clave.<br/>                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**phyType**](wlan-profileschema-phytype-connectivity-element.md)                 |                                                                   | Especifica el estándar de LAN inalámbrica 802.11 que se usa en la LAN inalámbrica. El valor "n" solo se admite en Windows Vista con SP1 y versiones posteriores del sistema operativo.<br/> **Windows XP con SP3 e WIRELESS LAN API para Windows XP con SP2:** No se admite este elemento.<br/>                                                                                                                        |
| [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | Indica si se usará el almacenamiento en caché de PMK. Este elemento solo es válido para redes definidas por WPA2.<br/> **Windows XP con SP3 e WIRELESS LAN API para Windows XP con SP2:** No se admite este elemento.<br/>                                                                                                                                                                                                 |
| [**PMKCacheSize**](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | Especifica el número de entradas de la caché de OMK en el cliente. Este elemento solo es válido para redes definidas por WPA2 con el modo PMKCache establecido en habilitado. Si el modo PMKCache está habilitado y este elemento no está presente, el tamaño de la memoria caché tiene como valor predeterminado 128 entradas.<br/> **Windows XP con SP3 e WIRELESS LAN API para Windows XP con SP2:** No se admite este elemento.<br/>                                   |
| [**PMKCacheTTL**](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | Indica el período de tiempo, en minutos, que se conservará una caché de PMK. Este elemento solo es válido para redes definidas por WPA2 con el modo PMKCache establecido en habilitado.<br/> **Windows XP con SP3 e WIRELESS LAN API para Windows XP con SP2:** No se admite este elemento.<br/>                                                                                                                                  |
| [**preAuthMode**](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | Determina si el cliente usará la autenticación previa. La autenticación previa habilita la itinerancia rápida segura de WPA2. Este elemento solo es válido para redes definidas por WPA2 con el modo PMKCache establecido en habilitado. Si el modo PMKCache está habilitado y este elemento no está presente, se deshabilita el valor predeterminado.<br/> **Windows XP con SP3 e WIRELESS LAN API para Windows XP con SP2:** No se admite este elemento.<br/> |
| [**preAuthThrottle**](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | Indica el número de intentos al autenticarse previamente en los AP vecinos. Este elemento solo es válido para redes definidas por WPA2 con el modo PMKCache establecido en habilitado. Si el modo PMKCache está habilitado y este elemento no está presente, el número de intentos tiene como valor predeterminado 3.<br/> **Windows XP con SP3 e WIRELESS LAN API para Windows XP con SP2:** No se admite este elemento.<br/>                                      |
| [**protected**](wlan-profileschema-protected-sharedkey-element.md)                | [boolean](/dotnet/api/system.boolean) | Indica si la clave está cifrada.<br/> **Windows XP con SP3 e WIRELESS LAN API para Windows XP con SP2:** Este elemento debe tener el valor FALSE.<br/>                                                                                                                                                                                                                                                 |
| [**Seguridad**](wlan-profileschema-security-msm-element.md)                        |                                                                   | Contiene varias configuraciones de seguridad. Este elemento es opcional.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| [**sharedKey**](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | Contiene la información de clave compartida. Este elemento solo es necesario si se requieren claves WEP o PSK para el par de autenticación y cifrado.<br/>                                                                                                                                                                                                                                                                    |
| [**useOneX**](wlan-profileschema-useonex-authencryption-element.md)               | [boolean](/dotnet/api/system.boolean) | Indica si se usa 802.1X. Esta marca es opcional.<br/>                                                                                                                                                                                                                                                                                                                                                          |



## <a name="remarks"></a>Comentarios

El [**elemento FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) se puede insertar como elemento secundario del [**elemento authEncryption.**](wlan-profileschema-authencryption-security-element.md) El [**elemento OneX**](onexschema-onex-element.md) se puede insertar como elemento secundario del elemento de seguridad [**(MSM).**](wlan-profileschema-security-msm-element.md)

## <a name="examples"></a>Ejemplos

Para ver perfiles de ejemplo que usan el **elemento MSM,** vea [Ejemplos de perfil inalámbrico.](wireless-profile-samples.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP solo con aplicaciones de escritorio SP3 \[\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Ejemplos de perfil inalámbrico](wireless-profile-samples.md)
</dt> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
