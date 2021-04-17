---
description: Contiene varias configuraciones de seguridad.
ms.assetid: 1d912fb1-8fb4-4761-8991-5a50ffb0399e
title: Elemento Security (MSM) (LAN_policy) (WLAN)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: f6ea42a83d39c328db88e992555e5d593cc778b6
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/26/2021
ms.locfileid: "105691116"
---
# <a name="security-msm-element-lan_policy-for-wlan"></a>Elemento Security (MSM) (LAN_policy) para WLAN

El elemento de seguridad (MSM) contiene varias configuraciones de seguridad.

``` syntax
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
```

El elemento se define mediante el elemento [**MSM**](wlan-profileschema-msm-wlanprofile-element.md) .

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                            | Tipo                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**authEncryption**](wlan-profileschema-authencryption-security-element.md)       |                                                                   | Especifica el par de autenticación y cifrado que se usará para este perfil.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**autenticación**](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | Especifica el par de autenticación y cifrado que se usará para este perfil.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**cifra**](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | Establece el cifrado de datos que se va a usar para conectarse a la LAN inalámbrica.<br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**keyIndex**](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | Especifica qué índice de clave se debe usar para cifrar el tráfico inalámbrico. Solo se utiliza cuando keyType está establecido en networkKey.<br/>                                                                                                                                                                                                                                                                                          |
| [**keyMaterial**](wlan-profileschema-keymaterial-sharedkey-element.md)            | [string](/dotnet/api/system.string)   | Contiene la clave o frase de contraseña de la red.<br/>                                                                                                                                                                                                                                                                                                                                                                           |
| [**keyType**](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | Tipo de clave.<br/>                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | Indica si se usará el almacenamiento en caché PMK. Este elemento solo es válido para redes definidas por WPA2.<br/> **Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.<br/>                                                                                                                                                                                                 |
| [**PMKCacheSize**](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | Especifica el número de entradas en la memoria caché de OMK en el cliente. Este elemento solo es válido para redes definidas por WPA2 con el modo PMKCache establecido en habilitado. Si el modo PMKCache está habilitado y este elemento no está presente, el tamaño de la memoria caché tiene como valor predeterminado 128 entradas.<br/> **Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.<br/>                                   |
| [**PMKCacheTTL**](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | Indica el período de tiempo, en minutos, que se conservará una caché PMK. Este elemento solo es válido para redes definidas por WPA2 con el modo PMKCache establecido en habilitado.<br/> **Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.<br/>                                                                                                                                  |
| [**preAuthMode**](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | Determina si el cliente usará la autenticación previa. La autenticación previa habilita la itinerancia rápida segura WPA2. Este elemento solo es válido para redes definidas por WPA2 con el modo PMKCache establecido en habilitado. Si el modo PMKCache está habilitado y este elemento no está presente, el valor predeterminado es Disabled.<br/> **Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.<br/> |
| [**preAuthThrottle**](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | Indica el número de intentos cuando se realiza la autenticación en el APs vecino. Este elemento solo es válido para redes definidas por WPA2 con el modo PMKCache establecido en habilitado. Si el modo PMKCache está habilitado y este elemento no está presente, el número de intentos predeterminado es 3.<br/> **Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.<br/>                                      |
| [**protected**](wlan-profileschema-protected-sharedkey-element.md)                | [boolean](/dotnet/api/system.boolean) | Indica si la clave está cifrada.<br/> **Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento debe tener un valor de **false**.<br/>                                                                                                                                                                                                                                             |
| [**sharedKey**](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | Contiene la información de la clave compartida. Este elemento solo es necesario si se requieren claves WEP o PSK para el par de autenticación y cifrado.<br/>                                                                                                                                                                                                                                                                    |
| [**useOneX**](wlan-profileschema-useonex-authencryption-element.md)               | [boolean](/dotnet/api/system.boolean) | Indica si se usa 802.1 X. Esta marca es opcional.<br/>                                                                                                                                                                                                                                                                                                                                                          |



## <a name="remarks"></a>Observaciones

El elemento [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) se puede insertar como elemento secundario del elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) . El elemento [**Onex**](onexschema-onex-element.md) se puede insertar como elemento secundario del elemento de **seguridad (MSM)** .

## <a name="examples"></a>Ejemplos

Para ver los perfiles de ejemplo que usan el elemento de **seguridad** , consulte [ejemplos de perfiles inalámbricos](wireless-profile-samples.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Ejemplos de perfil inalámbrico](wireless-profile-samples.md)
</dt> <dt>

**Contexto de definición del elemento en el esquema**
</dt> <dt>

[**MSM**](wlan-profileschema-msm-wlanprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**MSM (WLANProfile)**](wlan-profileschema-msm-wlanprofile-element.md)
</dt> </dl>

 

 
