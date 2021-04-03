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
ms.openlocfilehash: 227d912128bf3f656fca7aecbaf0fe0640659465
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913253"
---
# <a name="wlanprofile-element"></a><span data-ttu-id="bf1ba-103">Elemento WLANProfile</span><span class="sxs-lookup"><span data-stu-id="bf1ba-103">WLANProfile Element</span></span>

<span data-ttu-id="bf1ba-104">El elemento **WLANProfile** contiene un perfil de LAN inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-104">The **WLANProfile** element contains a wireless LAN profile.</span></span> <span data-ttu-id="bf1ba-105">Este elemento es el elemento raíz único para un perfil inalámbrico.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-105">This element is the unique root element for a wireless profile.</span></span>

<span data-ttu-id="bf1ba-106">El espacio de nombres de destino para el elemento WLANProfile es `https://www.microsoft.com/networking/WLAN/profile/v1` .</span><span class="sxs-lookup"><span data-stu-id="bf1ba-106">The target namespace for the WLANProfile element is `https://www.microsoft.com/networking/WLAN/profile/v1`.</span></span>

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

## <a name="child-elements"></a><span data-ttu-id="bf1ba-107">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="bf1ba-107">Child elements</span></span>



| <span data-ttu-id="bf1ba-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="bf1ba-108">Element</span></span>                                                                            | <span data-ttu-id="bf1ba-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="bf1ba-109">Type</span></span>                                                              | <span data-ttu-id="bf1ba-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf1ba-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bf1ba-111">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-111">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)       |                                                                   | <span data-ttu-id="bf1ba-112">Especifica el par de autenticación y cifrado que se usará para este perfil.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-112">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="bf1ba-113">**autenticación**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-113">**authentication**</span></span>](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | <span data-ttu-id="bf1ba-114">Especifica el método de autenticación que se va a usar para conectarse a la LAN inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-114">Specifies the authentication method to be used to connect to the wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="bf1ba-115">**AutoSwitch**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-115">**autoSwitch**</span></span>](wlan-profileschema-autoswitch-wlanprofile-element.md)            | [<span data-ttu-id="bf1ba-116">boolean</span><span class="sxs-lookup"><span data-stu-id="bf1ba-116">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="bf1ba-117">Determina el comportamiento de itinerancia de una red conectada automáticamente cuando una red más preferida está dentro del alcance.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-117">Determines the roaming behavior of an auto-connected network when a more preferred network is in range.</span></span> <span data-ttu-id="bf1ba-118">Este elemento es opcional y no tiene ningún efecto en una red conectada manualmente.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-118">This element is optional and has no effect on a manually connected network.</span></span><br/> <span data-ttu-id="bf1ba-119">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-119">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="bf1ba-120">**connectionMode**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-120">**connectionMode**</span></span>](wlan-profileschema-connectionmode-wlanprofile-element.md)    |                                                                   | <span data-ttu-id="bf1ba-121">Indica si la conexión a la LAN inalámbrica debe ser automática ("auto") o iniciada ("manual") por el usuario.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-121">Indicates whether connection to the wireless LAN should be automatic ("auto") or initiated ("manual") by user.</span></span> <span data-ttu-id="bf1ba-122">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-122">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="bf1ba-123">**connectionType**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-123">**connectionType**</span></span>](wlan-profileschema-connectiontype-wlanprofile-element.md)    |                                                                   | <span data-ttu-id="bf1ba-124">Indica si la red es de infraestructura ("ESS") o ad hoc ("IBSS").</span><span class="sxs-lookup"><span data-stu-id="bf1ba-124">Indicates whether the network is infrastructure ("ESS") or ad-hoc ("IBSS").</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="bf1ba-125">**Conectividad**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-125">**connectivity**</span></span>](wlan-profileschema-connectivity-msm-element.md)                |                                                                   | <span data-ttu-id="bf1ba-126">Contiene varias configuraciones de conectividad.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-126">Contains various connectivity settings.</span></span> <span data-ttu-id="bf1ba-127">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-127">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="bf1ba-128">**Conectividad**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-128">**connectivity**</span></span>](wlan-profileschema-connectivity-ihv-element.md)                |                                                                   | <span data-ttu-id="bf1ba-129">Contiene la configuración de conectividad relacionada con IHV.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-129">Contains IHV-related connectivity settings.</span></span><br/> <span data-ttu-id="bf1ba-130">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-130">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="bf1ba-131">**cifra**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-131">**encryption**</span></span>](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | <span data-ttu-id="bf1ba-132">Establece el cifrado de datos que se va a usar para conectarse a la LAN inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-132">Sets the data encryption to use to connect to the wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="bf1ba-133">**hex**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-133">**hex**</span></span>](wlan-profileschema-hex-ssid-element.md)                                 |                                                                   | <span data-ttu-id="bf1ba-134">Contiene el SSID de una LAN inalámbrica en formato hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-134">Contains the SSID of a wireless LAN in hexadecimal format.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="bf1ba-135">**IHV**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-135">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)                          |                                                                   | <span data-ttu-id="bf1ba-136">Contiene la configuración opcional de proveedor de hardware independiente (IHV).</span><span class="sxs-lookup"><span data-stu-id="bf1ba-136">Contains optional independent hardware vendor (IHV) settings.</span></span><br/> <span data-ttu-id="bf1ba-137">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-137">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="bf1ba-138">**keyIndex**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-138">**keyIndex**</span></span>](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | <span data-ttu-id="bf1ba-139">Especifica qué índice de clave se debe usar para cifrar el tráfico inalámbrico.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-139">Specifies which key index should be used to encrypt wireless traffic.</span></span> <span data-ttu-id="bf1ba-140">Solo se utiliza cuando [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md) está establecido en "networkKey".</span><span class="sxs-lookup"><span data-stu-id="bf1ba-140">This is only used when [**keyType**](wlan-profileschema-keytype-sharedkey-element.md) is set to "networkKey".</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="bf1ba-141">**keyMaterial**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-141">**keyMaterial**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md)            | [<span data-ttu-id="bf1ba-142">string</span><span class="sxs-lookup"><span data-stu-id="bf1ba-142">string</span></span>](/dotnet/api/system.string)   | <span data-ttu-id="bf1ba-143">Contiene la clave o frase de contraseña de la red.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-143">Contains the network key or passphrase.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="bf1ba-144">**keyType**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-144">**keyType**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | <span data-ttu-id="bf1ba-145">Tipo de clave.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-145">Type of key.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="bf1ba-146">**MSM**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-146">**MSM**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)                          |                                                                   | <span data-ttu-id="bf1ba-147">Contiene varias opciones de configuración de MSM.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-147">Contains various MSM settings.</span></span> <span data-ttu-id="bf1ba-148">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-148">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="bf1ba-149">**name**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-149">**name**</span></span>](wlan-profileschema-name-wlanprofile-element.md)                        | [<span data-ttu-id="bf1ba-150">**nameType**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-150">**nameType**</span></span>](wlan-profileschema-nametype-simpletype.md)        | <span data-ttu-id="bf1ba-151">Nombre del perfil de WLAN.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-151">Name of the WLAN profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="bf1ba-152">**name**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-152">**name**</span></span>](wlan-profileschema-name-ssid-element.md)                               |                                                                   | <span data-ttu-id="bf1ba-153">Contiene el SSID de una LAN inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-153">Contains the SSID of a wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="bf1ba-154">**Difusión**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-154">**nonBroadcast**</span></span>](wlan-profileschema-nonbroadcast-ssidconfig-element.md)         | [<span data-ttu-id="bf1ba-155">boolean</span><span class="sxs-lookup"><span data-stu-id="bf1ba-155">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="bf1ba-156">Indica si la red difunde su SSID.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-156">Indicates whether the network broadcasts its SSID.</span></span><br/> <span data-ttu-id="bf1ba-157">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-157">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="bf1ba-158">**OUI**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-158">**OUI**</span></span>](wlan-profileschema-oui-ouiheader-element.md)                            |                                                                   | <span data-ttu-id="bf1ba-159">Contiene un hexBinary de 3 bytes que identifica el IHV.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-159">Contains a 3 byte hexBinary that identifies the IHV.</span></span><br/> <span data-ttu-id="bf1ba-160">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-160">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="bf1ba-161">**OUIHeader**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-161">**OUIHeader**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)                      |                                                                   | <span data-ttu-id="bf1ba-162">Identifica el IHV.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-162">Identifies the IHV.</span></span><br/> <span data-ttu-id="bf1ba-163">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-163">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="bf1ba-164">**phyType**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-164">**phyType**</span></span>](wlan-profileschema-phytype-connectivity-element.md)                 |                                                                   | <span data-ttu-id="bf1ba-165">Especifica el estándar de LAN inalámbrica 802,11 usado en la LAN inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-165">Specifies the 802.11 wireless LAN standard used on the wireless LAN.</span></span> <span data-ttu-id="bf1ba-166">El valor "n" solo se admite en Windows Vista con SP1 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-166">The value "n" is only supported on Windows Vista with SP1 and later versions of the operating system.</span></span><br/> <span data-ttu-id="bf1ba-167">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-167">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="bf1ba-168">**PMKCacheMode**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-168">**PMKCacheMode**</span></span>](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | <span data-ttu-id="bf1ba-169">Indica si se usará el almacenamiento en caché PMK.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-169">Indicates whether PMK caching will be used.</span></span> <span data-ttu-id="bf1ba-170">Este elemento solo es válido para redes definidas por WPA2.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-170">This element is valid only for WPA2-defined networks.</span></span><br/> <span data-ttu-id="bf1ba-171">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-171">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="bf1ba-172">**PMKCacheSize**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-172">**PMKCacheSize**</span></span>](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | <span data-ttu-id="bf1ba-173">Especifica el número de entradas en la caché de PMK en el cliente.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-173">Specifies the number of entries in the PMK cache on the client.</span></span> <span data-ttu-id="bf1ba-174">Este elemento solo es válido para redes definidas por WPA2 con [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) establecido en "habilitado".</span><span class="sxs-lookup"><span data-stu-id="bf1ba-174">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="bf1ba-175">Si **PMKCacheMode** está habilitado y este elemento no está presente, el tamaño de la memoria caché tiene como valor predeterminado 128 entradas.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-175">If **PMKCacheMode** is enabled, and this element is absent, the size of the cache defaults to 128 entries.</span></span><br/> <span data-ttu-id="bf1ba-176">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-176">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="bf1ba-177">**PMKCacheTTL**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-177">**PMKCacheTTL**</span></span>](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | <span data-ttu-id="bf1ba-178">Indica el período de tiempo, en minutos, que se conservará una caché PMK.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-178">Indicates the length of time, in minutes, that a PMK cache will be kept.</span></span> <span data-ttu-id="bf1ba-179">Este elemento solo es válido para redes definidas por WPA2 con [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) establecido en "habilitado".</span><span class="sxs-lookup"><span data-stu-id="bf1ba-179">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span><br/> <span data-ttu-id="bf1ba-180">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-180">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="bf1ba-181">**preAuthMode**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-181">**preAuthMode**</span></span>](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | <span data-ttu-id="bf1ba-182">Determina si el cliente usará la autenticación previa.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-182">Determines if pre-authentication will be used by the client.</span></span> <span data-ttu-id="bf1ba-183">La autenticación previa habilita la itinerancia rápida segura WPA2.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-183">Pre-authentication enables WPA2 secure fast roaming.</span></span> <span data-ttu-id="bf1ba-184">Este elemento solo es válido para redes definidas por WPA2 con [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) establecido en "habilitado".</span><span class="sxs-lookup"><span data-stu-id="bf1ba-184">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="bf1ba-185">Si **PMKCacheMode** está habilitado y este elemento no está presente, el valor predeterminado es Disabled.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-185">If **PMKCacheMode** is enabled, and this element is absent, the default value is disabled.</span></span><br/> <span data-ttu-id="bf1ba-186">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-186">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="bf1ba-187">**preAuthThrottle**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-187">**preAuthThrottle**</span></span>](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | <span data-ttu-id="bf1ba-188">Indica el número de intentos cuando se realiza la autenticación en el APs vecino.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-188">Indicates the number of tries when preauthenticating to neighboring APs.</span></span> <span data-ttu-id="bf1ba-189">Este elemento solo es válido para redes definidas por WPA2 con [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) establecido en "habilitado".</span><span class="sxs-lookup"><span data-stu-id="bf1ba-189">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="bf1ba-190">Si **PMKCacheMode** está habilitado y este elemento no está presente, el número de intentos predeterminado es 3.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-190">If **PMKCacheMode** is enabled, and this element is absent, the number of tries defaults to 3.</span></span><br/> <span data-ttu-id="bf1ba-191">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-191">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="bf1ba-192">**protected**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-192">**protected**</span></span>](wlan-profileschema-protected-sharedkey-element.md)                | [<span data-ttu-id="bf1ba-193">boolean</span><span class="sxs-lookup"><span data-stu-id="bf1ba-193">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="bf1ba-194">Indica si la clave está cifrada.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-194">Indicates whether the key is encrypted.</span></span><br/> <span data-ttu-id="bf1ba-195">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento debe tener un valor de **false**.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-195">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element must have a value of **FALSE**.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="bf1ba-196">**bursátil**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-196">**security**</span></span>](wlan-profileschema-security-msm-element.md)                        |                                                                   | <span data-ttu-id="bf1ba-197">Contiene varias configuraciones de seguridad.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-197">Contains various security settings.</span></span> <span data-ttu-id="bf1ba-198">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-198">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="bf1ba-199">**bursátil**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-199">**security**</span></span>](wlan-profileschema-security-ihv-element.md)                        |                                                                   | <span data-ttu-id="bf1ba-200">Contiene la configuración de seguridad específica de IHV.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-200">Contains IHV-specific security settings.</span></span> <span data-ttu-id="bf1ba-201">La configuración de seguridad de Microsoft y la configuración de seguridad de IHV son mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-201">Microsoft security settings and IHV security settings are mutually exclusive.</span></span> <span data-ttu-id="bf1ba-202">Si ambos conjuntos de configuración de seguridad están presentes en el mismo perfil, el perfil no es válido.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-202">If both sets of security settings are present in the same profile, the profile is invalid.</span></span><br/> <span data-ttu-id="bf1ba-203">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-203">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="bf1ba-204">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-204">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | <span data-ttu-id="bf1ba-205">Contiene la información de la clave compartida.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-205">Contains the shared key information.</span></span> <span data-ttu-id="bf1ba-206">Este elemento solo es necesario si se requieren claves WEP o PSK para el par de autenticación y cifrado.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-206">This element is only required if WEP or PSK keys are required for the authentication and encryption pair.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="bf1ba-207">**SSID**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-207">**SSID**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)                         |                                                                   | <span data-ttu-id="bf1ba-208">Especifica el SSID de una LAN inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-208">Specifies the SSID of a wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="bf1ba-209">**SSIDConfig**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-209">**SSIDConfig**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)            |                                                                   | <span data-ttu-id="bf1ba-210">Contiene uno o más SSID junto con otras opciones de configuración comunes.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-210">Contains one or more SSIDs along with other common settings.</span></span> <br/> <span data-ttu-id="bf1ba-211">Un perfil puede tener varios elementos [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) y cada elemento [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) puede tener varios elementos [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="bf1ba-211">A profile can have multiple [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) elements and each [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) element can have multiple [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) elements.</span></span> <span data-ttu-id="bf1ba-212">Sin embargo, Windows solo tiene en cuenta el primer elemento [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) en un elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="bf1ba-212">However, Windows only ever considers the first [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) element in a [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span><br/> <span data-ttu-id="bf1ba-213">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Como máximo, un elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) puede aparecer en un perfil.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-213">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** At most one [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element can appear in a profile.</span></span><br/> |
| [<span data-ttu-id="bf1ba-214">**automáticamente**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-214">**type**</span></span>](wlan-profileschema-type-ouiheader-element.md)                          |                                                                   | <span data-ttu-id="bf1ba-215">Contiene un **hexBinary** de 1 byte que se usa para diferenciar las NIC del mismo IHV.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-215">Contains a 1 byte **hexBinary** that is used to differentiate NICs by the same IHV.</span></span><br/> <span data-ttu-id="bf1ba-216">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-216">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="bf1ba-217">**useMSOneX**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-217">**useMSOneX**</span></span>](wlan-profileschema-usemsonex-ihv-element.md)                      | [<span data-ttu-id="bf1ba-218">boolean</span><span class="sxs-lookup"><span data-stu-id="bf1ba-218">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="bf1ba-219">Especifica el origen de la configuración de seguridad de 802.1 X usada por un componente de seguridad IHV.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-219">Specifies the origin of 802.1X security settings used by an IHV security component.</span></span> <span data-ttu-id="bf1ba-220">Cuando [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) es true, los componentes de seguridad de IHV usan la configuración de 802.1 x definida por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-220">When [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) is true, IHV security components use Microsoft-defined 802.1X settings.</span></span> <span data-ttu-id="bf1ba-221">Cuando **useMSOneX** es false, los componentes de seguridad de IHV usan la configuración de 802.1 x suministrada por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-221">When **useMSOneX** is false, IHV security components use vendor-supplied 802.1X settings.</span></span> <span data-ttu-id="bf1ba-222">De forma predeterminada, **useMSOneX** es false.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-222">By default, **useMSOneX** is false.</span></span> <span data-ttu-id="bf1ba-223">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-223">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="bf1ba-224">**useOneX**</span><span class="sxs-lookup"><span data-stu-id="bf1ba-224">**useOneX**</span></span>](wlan-profileschema-useonex-authencryption-element.md)               | [<span data-ttu-id="bf1ba-225">boolean</span><span class="sxs-lookup"><span data-stu-id="bf1ba-225">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="bf1ba-226">Indica si se usa 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-226">Indicates whether 802.1X is used.</span></span> <span data-ttu-id="bf1ba-227">Esta marca es opcional.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-227">This flag is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



## <a name="remarks"></a><span data-ttu-id="bf1ba-228">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bf1ba-228">Remarks</span></span>

<span data-ttu-id="bf1ba-229">La mayoría de los elementos secundarios del elemento WLANProfile se encuentran en el `https://www.microsoft.com/networking/WLAN/profile/v1` espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-229">Most child elements of the WLANProfile element are in the `https://www.microsoft.com/networking/WLAN/profile/v1` namespace.</span></span> <span data-ttu-id="bf1ba-230">Hay dos excepciones: el elemento [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) está en el `https://www.microsoft.com/networking/WLAN/profile/v2` espacio de nombres y el elemento [**Onex**](onexschema-onex-element.md) está en el `https://www.microsoft.com/networking/OneX/v1` espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="bf1ba-230">There are two exceptions: the [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element is in the `https://www.microsoft.com/networking/WLAN/profile/v2` namespace and the [**OneX**](onexschema-onex-element.md) element is in the `https://www.microsoft.com/networking/OneX/v1` namespace.</span></span>

<span data-ttu-id="bf1ba-231">El elemento [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) se puede insertar como elemento secundario del elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="bf1ba-231">The [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element can be inserted as a child of the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span> <span data-ttu-id="bf1ba-232">El elemento [**Onex**](onexschema-onex-element.md) se puede insertar como elemento secundario del elemento de [**seguridad (MSM)**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="bf1ba-232">The [**OneX**](onexschema-onex-element.md) element can be inserted as a child of the [**security (MSM)**](wlan-profileschema-security-msm-element.md) element.</span></span>

<span data-ttu-id="bf1ba-233">Para ver la lista de elementos secundarios en una estructura similar a un árbol, [vea \_ elementos de esquema de Perfil de WLAN](wlan-profileschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="bf1ba-233">To view the list of child elements in a tree-like structure, see [WLAN\_profile Schema Elements](wlan-profileschema-elements.md).</span></span>

## <a name="examples"></a><span data-ttu-id="bf1ba-234">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="bf1ba-234">Examples</span></span>

<span data-ttu-id="bf1ba-235">Para ver los perfiles de ejemplo, consulte [ejemplos de perfiles inalámbricos](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="bf1ba-235">To view sample profiles, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf1ba-236">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf1ba-236">Requirements</span></span>



| <span data-ttu-id="bf1ba-237">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf1ba-237">Requirement</span></span> | <span data-ttu-id="bf1ba-238">Value</span><span class="sxs-lookup"><span data-stu-id="bf1ba-238">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="bf1ba-239">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf1ba-239">Minimum supported client</span></span><br/> | <span data-ttu-id="bf1ba-240">Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="bf1ba-240">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bf1ba-241">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf1ba-241">Minimum supported server</span></span><br/> | <span data-ttu-id="bf1ba-242">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="bf1ba-242">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="bf1ba-243">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="bf1ba-243">Redistributable</span></span><br/>          | <span data-ttu-id="bf1ba-244">API de LAN inalámbrica para Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="bf1ba-244">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="bf1ba-245">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf1ba-245">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf1ba-246">Ejemplos de perfil inalámbrico</span><span class="sxs-lookup"><span data-stu-id="bf1ba-246">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 
