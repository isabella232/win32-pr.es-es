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
# <a name="hotspot2-wlanprofile-element"></a><span data-ttu-id="8147d-103">Elemento Hotspot2 (WLANProfile)</span><span class="sxs-lookup"><span data-stu-id="8147d-103">Hotspot2 (WLANProfile) element</span></span>

<span data-ttu-id="8147d-104">Extiende el esquema de Perfil de WLAN V1 para admitir redes de zona activa 2,0.</span><span class="sxs-lookup"><span data-stu-id="8147d-104">Extends the WLAN Profile Schema v1 to support Hotspot 2.0 networks.</span></span> <span data-ttu-id="8147d-105">HotSpot 2,0 habilita la conexión automática a los servicios de Wi-Fi públicos mediante las credenciales existentes y la pertenencia a las redes del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="8147d-105">Hotspot 2.0 enables automatic connection to public Wi-Fi services using existing credentials and membership in service provider networks.</span></span> <span data-ttu-id="8147d-106">Los proveedores de servicios especifican cómo se realizan las conexiones con los nuevos elementos de esquema para describir qué redes usar y cómo autenticarse en ellas.</span><span class="sxs-lookup"><span data-stu-id="8147d-106">Service providers specify how connections are made using the new schema elements to describe which networks to use, and how to authenticate to them.</span></span>

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

<span data-ttu-id="8147d-107">El elemento se define mediante el elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8147d-107">The element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="8147d-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8147d-108">Child elements</span></span>

| <span data-ttu-id="8147d-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="8147d-109">Element</span></span> | <span data-ttu-id="8147d-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="8147d-110">Type</span></span> | <span data-ttu-id="8147d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="8147d-111">Description</span></span> |
|-|-|-|
| [<span data-ttu-id="8147d-112">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="8147d-112">**DomainName**</span></span>](wlan-profileschema-hotspot2-domainname-element.md) | | <span data-ttu-id="8147d-113">El nombre de dominio del proveedor de red doméstica del dispositivo, que identifica al operador de la red.</span><span class="sxs-lookup"><span data-stu-id="8147d-113">The domain name for the device's Home Network Provider, identifying the operator of the network.</span></span> |
| [<span data-ttu-id="8147d-114">**NAIRealm**</span><span class="sxs-lookup"><span data-stu-id="8147d-114">**NAIRealm**</span></span>](wlan-profileschema-hotspot2-nairealm-element.md) | | <span data-ttu-id="8147d-115">Una lista de identificadores de dominio de identificador de acceso de red (NAI).</span><span class="sxs-lookup"><span data-stu-id="8147d-115">A list of Network Access Identifier (NAI) Realm identifiers.</span></span> <span data-ttu-id="8147d-116">Las entradas de esta lista suelen tener el formato user@domain .</span><span class="sxs-lookup"><span data-stu-id="8147d-116">Entries in this list are usually of the form user@domain.</span></span> |
| [<span data-ttu-id="8147d-117">**Network3GPP**</span><span class="sxs-lookup"><span data-stu-id="8147d-117">**Network3GPP**</span></span>](wlan-profileschema-hotspot2-network3gpp-element.md) | | <span data-ttu-id="8147d-118">Una lista de identificadores de red móvil de tierra (PLMN).</span><span class="sxs-lookup"><span data-stu-id="8147d-118">A list of Public Land Mobile Network (PLMN) IDs.</span></span> |
| [<span data-ttu-id="8147d-119">**RoamingConsortium**</span><span class="sxs-lookup"><span data-stu-id="8147d-119">**RoamingConsortium**</span></span>](wlan-profileschema-hotspot2-roamingconsortium-element.md) | | <span data-ttu-id="8147d-120">Lista de identificadores únicos de la organización (OUI) asignados por IEEE.</span><span class="sxs-lookup"><span data-stu-id="8147d-120">A list of Organizationally Unique Identifiers (OUI) assigned by IEEE.</span></span>  |

## <a name="examples"></a><span data-ttu-id="8147d-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8147d-121">Examples</span></span>

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
