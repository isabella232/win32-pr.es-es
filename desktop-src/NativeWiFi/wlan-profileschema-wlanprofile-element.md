---
description: Contiene un perfil de LAN inalámbrica.
ms.assetid: bc97cb49-3891-4a4a-aab4-895cd9ce6908
title: Elemento WLANProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLANProfile
api_type:
- Schema
api_location: ''
ms.openlocfilehash: f7dae0d600553411a5a0a9287ab78d052a9ab9a0aa3c94220638adaf78dc5f11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912484"
---
# <a name="wlanprofile-element"></a>Elemento WLANProfile

El **elemento WLANProfile** contiene un perfil de LAN inalámbrica. Este elemento es el elemento raíz único para un perfil inalámbrico.

El espacio de nombres de destino para el elemento WLANProfile es `https://www.microsoft.com/networking/WLAN/profile/v1` .

``` syntax
<xs:element name="WLANProfile">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                type="nameType"
             />
            <xs:element name="SSIDConfig"
                maxOccurs="256"
            >
                <xs:complexType>
                    <xs:sequence>
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
                        <xs:element name="nonBroadcast"
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
            <xs:element name="connectionType">
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="IBSS"
                         />
                        <xs:enumeration
                            value="ESS"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="connectionMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="auto"
                         />
                        <xs:enumeration
                            value="manual"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="autoSwitch"
                type="boolean"
                minOccurs="0"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
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
            <xs:element name="IHV"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
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
                        <xs:element name="connectivity"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:any
                                        processContents="lax"
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
                                    <xs:any
                                        processContents="lax"
                                        namespace="##other"
                                     />
                                </xs:sequence>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="useMSOneX"
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

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                            | Tipo                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**authEncryption**](wlan-profileschema-authencryption-security-element.md)       |                                                                   | Especifica el par de autenticación y cifrado que se usará para este perfil.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**Autenticación**](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | Especifica el método de autenticación que se usará para conectarse a la LAN inalámbrica.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md)            | [boolean](/dotnet/api/system.boolean) | Determina el comportamiento de itinerancia de una red conectada automáticamente cuando hay una red más preferida en el intervalo. Este elemento es opcional y no tiene ningún efecto en una red conectada manualmente.<br/> **Windows XP con SP3 y la API de LAN inalámbrica para Windows XP con SP2:** No se admite este elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md)    |                                                                   | Indica si la conexión a la LAN inalámbrica debe ser automática ("automática") o iniciada ("manual") por el usuario. Este elemento es opcional.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md)    |                                                                   | Indica si la red es de infraestructura ("ESS") o ad hoc ("IBSS").<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**Conectividad**](wlan-profileschema-connectivity-msm-element.md)                |                                                                   | Contiene varias configuraciones de conectividad. Este elemento es opcional.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**Conectividad**](wlan-profileschema-connectivity-ihv-element.md)                |                                                                   | Contiene la configuración de conectividad relacionada con IHV.<br/> **Windows XP con SP3 y la API de LAN inalámbrica para Windows XP con SP2:** No se admite este elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**Cifrado**](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | Establece el cifrado de datos que se usará para conectarse a la LAN inalámbrica.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Hexagonal**](wlan-profileschema-hex-ssid-element.md)                                 |                                                                   | Contiene el SSID de una LAN inalámbrica en formato hexadecimal.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md)                          |                                                                   | Contiene la configuración opcional del proveedor de hardware independiente (IHV).<br/> **Windows XP con SP3 y la API de LAN inalámbrica para Windows XP con SP2:** No se admite este elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**keyIndex**](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | Especifica qué índice de clave se debe usar para cifrar el tráfico inalámbrico. Solo se usa cuando [**keyType**](wlan-profileschema-keytype-sharedkey-element.md) se establece en "networkKey".<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**keyMaterial**](wlan-profileschema-keymaterial-sharedkey-element.md)            | [string](/dotnet/api/system.string)   | Contiene la clave de red o frase de contraseña.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**keyType**](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | Tipo de clave.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**Msm**](wlan-profileschema-msm-wlanprofile-element.md)                          |                                                                   | Contiene varias configuraciones de MSM. Este elemento es opcional.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**Nombre**](wlan-profileschema-name-wlanprofile-element.md)                        | [**nameType**](wlan-profileschema-nametype-simpletype.md)        | Nombre del perfil de WLAN.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**Nombre**](wlan-profileschema-name-ssid-element.md)                               |                                                                   | Contiene el SSID de una LAN inalámbrica.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**nonBroadcast**](wlan-profileschema-nonbroadcast-ssidconfig-element.md)         | [boolean](/dotnet/api/system.boolean) | Indica si la red difunde su SSID.<br/> **Windows XP con SP3 y la API de LAN inalámbrica para Windows XP con SP2:** No se admite este elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**Oui**](wlan-profileschema-oui-ouiheader-element.md)                            |                                                                   | Contiene un hexBinary de 3 bytes que identifica el IHV.<br/> **Windows XP con SP3 y la API de LAN inalámbrica para Windows XP con SP2:** No se admite este elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md)                      |                                                                   | Identifica el IHV.<br/> **Windows XP con SP3 y la API de LAN inalámbrica para Windows XP con SP2:** No se admite este elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**phyType**](wlan-profileschema-phytype-connectivity-element.md)                 |                                                                   | Especifica el estándar de LAN inalámbrica 802.11 que se usa en la LAN inalámbrica. El valor "n" solo se admite en Windows Vista con SP1 y versiones posteriores del sistema operativo.<br/> **Windows XP con SP3 y la API de LAN inalámbrica para Windows XP con SP2:** No se admite este elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | Indica si se usará el almacenamiento en caché de PMK. Este elemento solo es válido para redes definidas por WPA2.<br/> **Windows XP con SP3 y la API de LAN inalámbrica para Windows XP con SP2:** No se admite este elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**PMKCacheSize**](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | Especifica el número de entradas de la caché de PMK en el cliente. Este elemento solo es válido para redes definidas por WPA2 con [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) establecido en "enabled". Si **PMKCacheMode** está habilitado y este elemento no está presente, el tamaño de la memoria caché tiene como valor predeterminado 128 entradas.<br/> **Windows XP con SP3 y la API de LAN inalámbrica para Windows XP con SP2:** No se admite este elemento.<br/>                                                                                                                                                                                                                                                                                                                           |
| [**PMKCacheTTL**](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | Indica el período de tiempo, en minutos, que se conservará una caché de PMK. Este elemento solo es válido para redes definidas por WPA2 con [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) establecido en "enabled".<br/> **Windows XP con SP3 y la API de LAN inalámbrica para Windows XP con SP2:** No se admite este elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**preAuthMode**](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | Determina si el cliente usará la autenticación previa. La autenticación previa habilita la itinerancia rápida segura de WPA2. Este elemento solo es válido para redes definidas por WPA2 con [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) establecido en "enabled". Si **PMKCacheMode** está habilitado y este elemento no está presente, el valor predeterminado está deshabilitado.<br/> **Windows XP con SP3 y la API de LAN inalámbrica para Windows XP con SP2:** No se admite este elemento.<br/>                                                                                                                                                                                                                                                                                         |
| [**preAuthThrottle**](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | Indica el número de intentos al autenticar previamente a los AP vecinos. Este elemento solo es válido para redes definidas por WPA2 con [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) establecido en "enabled". Si **PMKCacheMode** está habilitado y este elemento no está presente, el número de intentos tiene como valor predeterminado 3.<br/> **Windows XP con SP3 y la API de LAN inalámbrica para Windows XP con SP2:** No se admite este elemento.<br/>                                                                                                                                                                                                                                                                                                                              |
| [**protected**](wlan-profileschema-protected-sharedkey-element.md)                | [boolean](/dotnet/api/system.boolean) | Indica si la clave está cifrada.<br/> **Windows XP con SP3 y la API de LAN inalámbrica para Windows XP con SP2:** Este elemento debe tener un valor **de FALSE.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**Seguridad**](wlan-profileschema-security-msm-element.md)                        |                                                                   | Contiene varias opciones de seguridad. Este elemento es opcional.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**Seguridad**](wlan-profileschema-security-ihv-element.md)                        |                                                                   | Contiene la configuración de seguridad específica de IHV. La configuración de seguridad de Microsoft y la configuración de seguridad de IHV son mutuamente excluyentes. Si ambos conjuntos de configuración de seguridad están presentes en el mismo perfil, el perfil no es válido.<br/> **Windows XP con SP3 y la API de LAN inalámbrica para Windows XP con SP2:** No se admite este elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**sharedKey**](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | Contiene la información de clave compartida. Este elemento solo es necesario si se requieren claves WEP o PSK para el par de autenticación y cifrado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**Ssid**](wlan-profileschema-ssid-ssidconfig-element.md)                         |                                                                   | Especifica el SSID de una LAN inalámbrica.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md)            |                                                                   | Contiene uno o varios SSID junto con otras configuraciones comunes. <br/> Un perfil puede tener varios [**elementos SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) y cada elemento [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) puede tener varios [**elementos SSID.**](wlan-profileschema-ssid-ssidconfig-element.md) Sin embargo, Windows solo tiene en cuenta el primer [**elemento SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) en un [**elemento WLANProfile.**](wlan-profileschema-wlanprofile-element.md)<br/> **Windows XP con SP3 y la API de LAN inalámbrica para Windows XP con SP2:** Como máximo, [**un elemento SSID**](wlan-profileschema-ssid-ssidconfig-element.md) puede aparecer en un perfil.<br/> |
| [**Tipo**](wlan-profileschema-type-ouiheader-element.md)                          |                                                                   | Contiene un **hexBinary** de 1 byte que se usa para diferenciar las NIC por el mismo IHV.<br/> **Windows XP con SP3 y la API de LAN inalámbrica para Windows XP con SP2:** No se admite este elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md)                      | [boolean](/dotnet/api/system.boolean) | Especifica el origen de la configuración de seguridad 802.1X que usa un componente de seguridad de IHV. Cuando [**useMSOneX es**](wlan-profileschema-usemsonex-ihv-element.md) true, los componentes de seguridad de IHV usan la configuración 802.1X definida por Microsoft. Cuando **useMSOneX es** false, los componentes de seguridad de IHV usan la configuración 802.1X proporcionada por el proveedor. De forma predeterminada, **useMSOneX** es false. Este elemento es opcional.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [**useOneX**](wlan-profileschema-useonex-authencryption-element.md)               | [boolean](/dotnet/api/system.boolean) | Indica si se usa 802.1X. Esta marca es opcional.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



## <a name="remarks"></a>Comentarios

La mayoría de los elementos secundarios del elemento WLANProfile están en el espacio de `https://www.microsoft.com/networking/WLAN/profile/v1` nombres . Hay dos excepciones: el elemento [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) está en el espacio de nombres `https://www.microsoft.com/networking/WLAN/profile/v2` y el elemento [**OneX**](onexschema-onex-element.md) está en el espacio de `https://www.microsoft.com/networking/OneX/v1` nombres .

El [**elemento FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) se puede insertar como elemento secundario del [**elemento authEncryption.**](wlan-profileschema-authencryption-security-element.md) El [**elemento OneX**](onexschema-onex-element.md) se puede insertar como elemento secundario del elemento de seguridad [**(MSM).**](wlan-profileschema-security-msm-element.md)

Para ver la lista de elementos secundarios en una estructura similar a un árbol, vea [Elementos de esquema del \_ perfil WLAN](wlan-profileschema-elements.md).

## <a name="examples"></a>Ejemplos

Para ver perfiles de ejemplo, vea [Ejemplos de perfil inalámbrico.](wireless-profile-samples.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, Windows XP solo con aplicaciones de escritorio sp3 \[\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                |
| Redistribuible<br/>          | API de LAN inalámbrica para Windows XP con SP2<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Ejemplos de perfil inalámbrico](wireless-profile-samples.md)
</dt> </dl>

 

 
