---
description: Contiene varias opciones de configuración del módulo específico del medio (MSM).
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
ms.openlocfilehash: b2e1ffdc5ad27524d3d2fc5b37b3a060a90c7575
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688114"
---
# <a name="msm-wlanprofile-element"></a><span data-ttu-id="d77a7-103">Elemento MSM (WLANProfile)</span><span class="sxs-lookup"><span data-stu-id="d77a7-103">MSM (WLANProfile) Element</span></span>

<span data-ttu-id="d77a7-104">El elemento MSM (WLANProfile) contiene varias opciones de configuración del módulo específico del medio (MSM).</span><span class="sxs-lookup"><span data-stu-id="d77a7-104">The MSM (WLANProfile) element contains various media-specific module (MSM) settings.</span></span>

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

<span data-ttu-id="d77a7-105">El elemento se define mediante el elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d77a7-105">The element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="d77a7-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d77a7-106">Child elements</span></span>



| <span data-ttu-id="d77a7-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="d77a7-107">Element</span></span>                                                                            | <span data-ttu-id="d77a7-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="d77a7-108">Type</span></span>                                                              | <span data-ttu-id="d77a7-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d77a7-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d77a7-110">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="d77a7-110">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)       |                                                                   | <span data-ttu-id="d77a7-111">Especifica el par de autenticación y cifrado que se usará para este perfil.</span><span class="sxs-lookup"><span data-stu-id="d77a7-111">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="d77a7-112">**autenticación**</span><span class="sxs-lookup"><span data-stu-id="d77a7-112">**authentication**</span></span>](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | <span data-ttu-id="d77a7-113">Especifica el par de autenticación y cifrado que se usará para este perfil.</span><span class="sxs-lookup"><span data-stu-id="d77a7-113">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="d77a7-114">**Conectividad**</span><span class="sxs-lookup"><span data-stu-id="d77a7-114">**connectivity**</span></span>](wlan-profileschema-connectivity-msm-element.md)                |                                                                   | <span data-ttu-id="d77a7-115">Contiene varias configuraciones de conectividad.</span><span class="sxs-lookup"><span data-stu-id="d77a7-115">Contains various connectivity settings.</span></span> <span data-ttu-id="d77a7-116">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="d77a7-116">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="d77a7-117">**cifra**</span><span class="sxs-lookup"><span data-stu-id="d77a7-117">**encryption**</span></span>](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | <span data-ttu-id="d77a7-118">Establece el cifrado de datos que se va a usar para conectarse a la LAN inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="d77a7-118">Sets the data encryption to use to connect to the wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="d77a7-119">**keyIndex**</span><span class="sxs-lookup"><span data-stu-id="d77a7-119">**keyIndex**</span></span>](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | <span data-ttu-id="d77a7-120">Especifica qué índice de clave se debe usar para cifrar el tráfico inalámbrico.</span><span class="sxs-lookup"><span data-stu-id="d77a7-120">Specifies which key index must be used to encrypt wireless traffic.</span></span> <span data-ttu-id="d77a7-121">Solo se utiliza cuando keyType está establecido en networkKey.</span><span class="sxs-lookup"><span data-stu-id="d77a7-121">This is only used when keyType is set to networkKey.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="d77a7-122">**keyMaterial**</span><span class="sxs-lookup"><span data-stu-id="d77a7-122">**keyMaterial**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md)            | [<span data-ttu-id="d77a7-123">string</span><span class="sxs-lookup"><span data-stu-id="d77a7-123">string</span></span>](/dotnet/api/system.string)   | <span data-ttu-id="d77a7-124">Contiene la clave o frase de contraseña de la red.</span><span class="sxs-lookup"><span data-stu-id="d77a7-124">Contains the network key or passphrase.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="d77a7-125">**keyType**</span><span class="sxs-lookup"><span data-stu-id="d77a7-125">**keyType**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | <span data-ttu-id="d77a7-126">Tipo de clave.</span><span class="sxs-lookup"><span data-stu-id="d77a7-126">Type of key.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="d77a7-127">**phyType**</span><span class="sxs-lookup"><span data-stu-id="d77a7-127">**phyType**</span></span>](wlan-profileschema-phytype-connectivity-element.md)                 |                                                                   | <span data-ttu-id="d77a7-128">Especifica el estándar de LAN inalámbrica 802,11 usado en la LAN inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="d77a7-128">Specifies the 802.11 wireless LAN standard used on the wireless LAN.</span></span> <span data-ttu-id="d77a7-129">El valor "n" solo se admite en Windows Vista con SP1 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d77a7-129">The value "n" is only supported on Windows Vista with SP1 and later versions of the operating system.</span></span><br/> <span data-ttu-id="d77a7-130">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="d77a7-130">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="d77a7-131">**PMKCacheMode**</span><span class="sxs-lookup"><span data-stu-id="d77a7-131">**PMKCacheMode**</span></span>](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | <span data-ttu-id="d77a7-132">Indica si se usará el almacenamiento en caché PMK.</span><span class="sxs-lookup"><span data-stu-id="d77a7-132">Indicates whether PMK caching will be used.</span></span> <span data-ttu-id="d77a7-133">Este elemento solo es válido para redes definidas por WPA2.</span><span class="sxs-lookup"><span data-stu-id="d77a7-133">This element is valid only for WPA2-defined networks.</span></span><br/> <span data-ttu-id="d77a7-134">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="d77a7-134">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="d77a7-135">**PMKCacheSize**</span><span class="sxs-lookup"><span data-stu-id="d77a7-135">**PMKCacheSize**</span></span>](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | <span data-ttu-id="d77a7-136">Especifica el número de entradas en la memoria caché de OMK en el cliente.</span><span class="sxs-lookup"><span data-stu-id="d77a7-136">Specifies the number of entries in the OMK cache on the client.</span></span> <span data-ttu-id="d77a7-137">Este elemento solo es válido para redes definidas por WPA2 con el modo PMKCache establecido en habilitado.</span><span class="sxs-lookup"><span data-stu-id="d77a7-137">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="d77a7-138">Si el modo PMKCache está habilitado y este elemento no está presente, el tamaño de la memoria caché tiene como valor predeterminado 128 entradas.</span><span class="sxs-lookup"><span data-stu-id="d77a7-138">If PMKCache mode is enabled, and this element is absent, the size of the cache defaults to 128 entries.</span></span><br/> <span data-ttu-id="d77a7-139">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="d77a7-139">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                   |
| [<span data-ttu-id="d77a7-140">**PMKCacheTTL**</span><span class="sxs-lookup"><span data-stu-id="d77a7-140">**PMKCacheTTL**</span></span>](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | <span data-ttu-id="d77a7-141">Indica el período de tiempo, en minutos, que se conservará una caché PMK.</span><span class="sxs-lookup"><span data-stu-id="d77a7-141">Indicates the length of time, in minutes, that a PMK cache will be kept.</span></span> <span data-ttu-id="d77a7-142">Este elemento solo es válido para redes definidas por WPA2 con el modo PMKCache establecido en habilitado.</span><span class="sxs-lookup"><span data-stu-id="d77a7-142">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span><br/> <span data-ttu-id="d77a7-143">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="d77a7-143">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="d77a7-144">**preAuthMode**</span><span class="sxs-lookup"><span data-stu-id="d77a7-144">**preAuthMode**</span></span>](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | <span data-ttu-id="d77a7-145">Determina si el cliente usará la autenticación previa.</span><span class="sxs-lookup"><span data-stu-id="d77a7-145">Determines if pre-authentication will be used by the client.</span></span> <span data-ttu-id="d77a7-146">La autenticación previa habilita la itinerancia rápida segura WPA2.</span><span class="sxs-lookup"><span data-stu-id="d77a7-146">Pre-authentication enables WPA2 secure fast roaming.</span></span> <span data-ttu-id="d77a7-147">Este elemento solo es válido para redes definidas por WPA2 con el modo PMKCache establecido en habilitado.</span><span class="sxs-lookup"><span data-stu-id="d77a7-147">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="d77a7-148">Si el modo PMKCache está habilitado y este elemento no está presente, el valor predeterminado es Disabled.</span><span class="sxs-lookup"><span data-stu-id="d77a7-148">If PMKCache mode is enabled, and this element is absent, the default value is disabled.</span></span><br/> <span data-ttu-id="d77a7-149">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="d77a7-149">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/> |
| [<span data-ttu-id="d77a7-150">**preAuthThrottle**</span><span class="sxs-lookup"><span data-stu-id="d77a7-150">**preAuthThrottle**</span></span>](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | <span data-ttu-id="d77a7-151">Indica el número de intentos cuando se realiza la autenticación en el APs vecino.</span><span class="sxs-lookup"><span data-stu-id="d77a7-151">Indicates the number of tries when preauthenticating to neighboring APs.</span></span> <span data-ttu-id="d77a7-152">Este elemento solo es válido para redes definidas por WPA2 con el modo PMKCache establecido en habilitado.</span><span class="sxs-lookup"><span data-stu-id="d77a7-152">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="d77a7-153">Si el modo PMKCache está habilitado y este elemento no está presente, el número de intentos predeterminado es 3.</span><span class="sxs-lookup"><span data-stu-id="d77a7-153">If PMKCache mode is enabled, and this element is absent, the number of tries defaults to 3.</span></span><br/> <span data-ttu-id="d77a7-154">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="d77a7-154">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="d77a7-155">**protected**</span><span class="sxs-lookup"><span data-stu-id="d77a7-155">**protected**</span></span>](wlan-profileschema-protected-sharedkey-element.md)                | [<span data-ttu-id="d77a7-156">boolean</span><span class="sxs-lookup"><span data-stu-id="d77a7-156">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="d77a7-157">Indica si la clave está cifrada.</span><span class="sxs-lookup"><span data-stu-id="d77a7-157">Indicates whether the key is encrypted.</span></span><br/> <span data-ttu-id="d77a7-158">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento debe tener un valor de FALSE.</span><span class="sxs-lookup"><span data-stu-id="d77a7-158">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element must have a value of FALSE.</span></span><br/>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="d77a7-159">**bursátil**</span><span class="sxs-lookup"><span data-stu-id="d77a7-159">**security**</span></span>](wlan-profileschema-security-msm-element.md)                        |                                                                   | <span data-ttu-id="d77a7-160">Contiene varias configuraciones de seguridad.</span><span class="sxs-lookup"><span data-stu-id="d77a7-160">Contains various security settings.</span></span> <span data-ttu-id="d77a7-161">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="d77a7-161">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="d77a7-162">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="d77a7-162">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | <span data-ttu-id="d77a7-163">Contiene la información de la clave compartida.</span><span class="sxs-lookup"><span data-stu-id="d77a7-163">Contains the shared key information.</span></span> <span data-ttu-id="d77a7-164">Este elemento solo es necesario si se requieren claves WEP o PSK para el par de autenticación y cifrado.</span><span class="sxs-lookup"><span data-stu-id="d77a7-164">This element is only required if WEP or PSK keys are required for the authentication and encryption pair.</span></span><br/>                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="d77a7-165">**useOneX**</span><span class="sxs-lookup"><span data-stu-id="d77a7-165">**useOneX**</span></span>](wlan-profileschema-useonex-authencryption-element.md)               | [<span data-ttu-id="d77a7-166">boolean</span><span class="sxs-lookup"><span data-stu-id="d77a7-166">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="d77a7-167">Indica si se usa 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="d77a7-167">Indicates whether 802.1X is used.</span></span> <span data-ttu-id="d77a7-168">Esta marca es opcional.</span><span class="sxs-lookup"><span data-stu-id="d77a7-168">This flag is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="d77a7-169">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d77a7-169">Remarks</span></span>

<span data-ttu-id="d77a7-170">El elemento [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) se puede insertar como elemento secundario del elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d77a7-170">The [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element can be inserted as a child of the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span> <span data-ttu-id="d77a7-171">El elemento [**Onex**](onexschema-onex-element.md) se puede insertar como elemento secundario del elemento de [**seguridad (MSM)**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d77a7-171">The [**OneX**](onexschema-onex-element.md) element can be inserted as a child of the [**security (MSM)**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="d77a7-172">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d77a7-172">Examples</span></span>

<span data-ttu-id="d77a7-173">Para ver los perfiles de ejemplo que usan el elemento **MSM** , consulte [ejemplos de perfiles inalámbricos](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="d77a7-173">To view sample profiles that use the **MSM** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d77a7-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d77a7-174">Requirements</span></span>



| <span data-ttu-id="d77a7-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="d77a7-175">Requirement</span></span> | <span data-ttu-id="d77a7-176">Value</span><span class="sxs-lookup"><span data-stu-id="d77a7-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="d77a7-177">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d77a7-177">Minimum supported client</span></span><br/> | <span data-ttu-id="d77a7-178">Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="d77a7-178">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d77a7-179">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d77a7-179">Minimum supported server</span></span><br/> | <span data-ttu-id="d77a7-180">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d77a7-180">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="d77a7-181">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="d77a7-181">Redistributable</span></span><br/>          | <span data-ttu-id="d77a7-182">API de LAN inalámbrica para Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="d77a7-182">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="d77a7-183">Vea también</span><span class="sxs-lookup"><span data-stu-id="d77a7-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d77a7-184">Ejemplos de perfil inalámbrico</span><span class="sxs-lookup"><span data-stu-id="d77a7-184">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> <dt>

<span data-ttu-id="d77a7-185">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="d77a7-185">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d77a7-186">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="d77a7-186">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="d77a7-187">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="d77a7-187">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d77a7-188">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="d77a7-188">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
