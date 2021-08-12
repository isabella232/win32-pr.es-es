---
description: Contiene uno o varios SSID para LAN inalámbricas.
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
ms.openlocfilehash: 6df6edc3affa551d62473b616562257cd422fcc4a4021ea7e4ef05ba3c8af9dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619051"
---
# <a name="ssidconfig-wlanprofile-element"></a>Elemento SSIDConfig (WLANProfile)

El elemento SSIDConfig (WLANProfile) contiene uno o varios SSID para redes LAN inalámbricas.

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

El **elemento SSIDConfig** se define mediante el [**elemento WLANProfile.**](wlan-profileschema-wlanprofile-element.md)

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                    | Tipo                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Hexagonal**](wlan-profileschema-hex-ssid-element.md)                         |                                                                   | Contiene el SSID de una LAN inalámbrica en formato hexadecimal.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Nombre**](wlan-profileschema-name-ssid-element.md)                       |                                                                   | Contiene el nombre (que distingue mayúsculas de minúsculas) del SSID de una LAN inalámbrica.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**nonBroadcast**](wlan-profileschema-nonbroadcast-ssidconfig-element.md) | [boolean](/dotnet/api/system.boolean) | Indica si la red difunde su SSID.<br/> Si [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) se establece en ESS, este valor puede ser **TRUE** o **FALSE.** El valor predeterminado es **TRUE** si este elemento está ausente.<br/> Si [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) se establece en IBSS, este valor debe ser **FALSE.**<br/> Windows XP con SP3 y LAN API inalámbrica **para Windows XP con SP2:** No se admite este elemento.<br/> |
| [**Ssid**](wlan-profileschema-ssid-ssidconfig-element.md)                 |                                                                   | Contiene un SSID para una LAN inalámbrica.<br/> Windows XP con SP3 y LAN API inalámbrica **para Windows XP con SP2:** Como máximo, [**un elemento SSID**](wlan-profileschema-ssid-ssidconfig-element.md) puede aparecer en un perfil.<br/>                                                                                                                                                                                                                                                                                                        |



## <a name="examples"></a>Ejemplos

Para ver los perfiles de ejemplo que usan el **elemento SSIDConfig,** vea [Ejemplos de perfil inalámbrico.](wireless-profile-samples.md)

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

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Posible elemento primario inmediato en la instancia de esquema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
