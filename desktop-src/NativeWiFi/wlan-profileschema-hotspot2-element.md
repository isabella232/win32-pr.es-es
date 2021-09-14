---
description: Extiende el esquema de perfil WLAN v1 para admitir redes hotspot 2.0.
ms.assetid: DE30DBCB-80B9-43D0-8DE1-56BBA99DBF31
title: Elemento Hotspot2 (WLANProfile)
ms.topic: reference
ms.date: 10/08/2019
topic_type:
- APIRef
- kbSyntax
api_name:
- Hotspot2
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 0e372c1025a74dfb304cacdb0f3a4cf18bcdbabd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245505"
---
# <a name="hotspot2-wlanprofile-element"></a>Elemento Hotspot2 (WLANProfile)

Extiende el esquema de perfil WLAN v1 para admitir redes hotspot 2.0. Hotspot 2.0 permite la conexión automática a servicios de Wi-Fi con credenciales existentes y pertenencia a redes de proveedor de servicios. Los proveedores de servicios especifican cómo se realizan las conexiones mediante los nuevos elementos de esquema para describir qué redes usar y cómo autenticarse en ellas.

``` syntax
<xs:element name="Hotspot2">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="DomainName"
                minOccurs="0"
             />
            <xs:element name="NAIRealm"
                minOccurs="0"
             />
            <xs:element name="Network3GPP"
                minOccurs="0"
             />
            <xs:element name="RoamingConsortium"
                minOccurs="0"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

El elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) define el elemento .

## <a name="child-elements"></a>Elementos secundarios

| Elemento | Tipo | Descripción |
|-|-|-|
| [**DomainName**](wlan-profileschema-hotspot2-domainname-element.md) | | Nombre de dominio del proveedor de red principal del dispositivo, que identifica el operador de la red. |
| [**NAIRealm**](wlan-profileschema-hotspot2-nairealm-element.md) | | Lista de identificadores de dominio del identificador de acceso de red (NAI). Las entradas de esta lista suelen tener el formato user@domain . |
| [**Network3GPP**](wlan-profileschema-hotspot2-network3gpp-element.md) | | Lista de los IDs de Public Land Mobile Network (PLMN). |
| [**RoamingConsortium**](wlan-profileschema-hotspot2-roamingconsortium-element.md) | | Lista de identificadores únicos de organización (OUI) asignados por IEEE.  |

## <a name="examples"></a>Ejemplos

```xml
<Hotspot2>
  <DomainName>contoso.com</DomainName>
  <NAIRealm>
    <name>test1@contoso.com</name>
    <name>test2@contoso.com</name>
  </NAIRealm>
  <Network3GPP>
    <PLMNID>12345</PLMNID>
    <PLMNID>123456</PLMNID>
  </Network3GPP>
  <RoamingConsortium>
    <OUI>00AABB</OUI>
    <OUI>001122</OUI>
  </RoamingConsortium>
</Hotspot2>
```
