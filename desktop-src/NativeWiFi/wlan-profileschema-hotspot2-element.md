---
description: Extiende el esquema de Perfil de WLAN V1 para admitir redes de zona activa 2,0.
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686916"
---
# <a name="hotspot2-wlanprofile-element"></a>Elemento Hotspot2 (WLANProfile)

Extiende el esquema de Perfil de WLAN V1 para admitir redes de zona activa 2,0. HotSpot 2,0 habilita la conexión automática a los servicios de Wi-Fi públicos mediante las credenciales existentes y la pertenencia a las redes del proveedor de servicios. Los proveedores de servicios especifican cómo se realizan las conexiones con los nuevos elementos de esquema para describir qué redes usar y cómo autenticarse en ellas.

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

El elemento se define mediante el elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .

## <a name="child-elements"></a>Elementos secundarios

| Elemento | Tipo | Descripción |
|-|-|-|
| [**DomainName**](wlan-profileschema-hotspot2-domainname-element.md) | | El nombre de dominio del proveedor de red doméstica del dispositivo, que identifica al operador de la red. |
| [**NAIRealm**](wlan-profileschema-hotspot2-nairealm-element.md) | | Una lista de identificadores de dominio de identificador de acceso de red (NAI). Las entradas de esta lista suelen tener el formato user@domain . |
| [**Network3GPP**](wlan-profileschema-hotspot2-network3gpp-element.md) | | Una lista de identificadores de red móvil de tierra (PLMN). |
| [**RoamingConsortium**](wlan-profileschema-hotspot2-roamingconsortium-element.md) | | Lista de identificadores únicos de la organización (OUI) asignados por IEEE.  |

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
