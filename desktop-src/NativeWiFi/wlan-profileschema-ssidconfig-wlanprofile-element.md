---
description: Contiene uno o más SSID para LAN inalámbricas.
ms.assetid: f9c46db8-2933-48e1-8cb3-effeb13c43ed
title: Elemento SSIDConfig (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SSIDConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5665b385c3264ff9d36e79ad671c8f9e8377d4bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910357"
---
# <a name="ssidconfig-wlanprofile-element"></a>Elemento SSIDConfig (WLANProfile)

El elemento SSIDConfig (WLANProfile) contiene uno o más SSID para LAN inalámbricas.

``` syntax
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
```

El elemento **SSIDConfig** se define mediante el elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                    | Tipo                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**hex**](wlan-profileschema-hex-ssid-element.md)                         |                                                                   | Contiene el SSID de una LAN inalámbrica en formato hexadecimal.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**name**](wlan-profileschema-name-ssid-element.md)                       |                                                                   | Contiene el nombre (distingue mayúsculas de minúsculas) del SSID de una LAN inalámbrica.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**Difusión**](wlan-profileschema-nonbroadcast-ssidconfig-element.md) | [boolean](/dotnet/api/system.boolean) | Indica si la red difunde su SSID.<br/> Si [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) se establece en ESS, este valor puede ser **true** o **false**. El valor predeterminado es **true** si este elemento no está presente.<br/> Si [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) se establece en IBSS, este valor debe ser **false**.<br/> **Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.<br/> |
| [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md)                 |                                                                   | Contiene un SSID para una LAN inalámbrica.<br/> **Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Como máximo, un elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) puede aparecer en un perfil.<br/>                                                                                                                                                                                                                                                                                                        |



## <a name="examples"></a>Ejemplos

Para ver los perfiles de ejemplo que usan el elemento **SSIDConfig** , consulte [ejemplos de perfiles inalámbricos](wireless-profile-samples.md).

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

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
