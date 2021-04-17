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
# <a name="security-msm-element-lan_policy-for-wlan"></a><span data-ttu-id="ed41c-103">Elemento Security (MSM) (LAN_policy) para WLAN</span><span class="sxs-lookup"><span data-stu-id="ed41c-103">Security (MSM) Element (LAN_policy) for WLAN</span></span>

<span data-ttu-id="ed41c-104">El elemento de seguridad (MSM) contiene varias configuraciones de seguridad.</span><span class="sxs-lookup"><span data-stu-id="ed41c-104">The security (MSM) element contains various security settings.</span></span>

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

<span data-ttu-id="ed41c-105">El elemento se define mediante el elemento [**MSM**](wlan-profileschema-msm-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ed41c-105">The element is defined by the [**MSM**](wlan-profileschema-msm-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ed41c-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ed41c-106">Child elements</span></span>



| <span data-ttu-id="ed41c-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="ed41c-107">Element</span></span>                                                                            | <span data-ttu-id="ed41c-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed41c-108">Type</span></span>                                                              | <span data-ttu-id="ed41c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed41c-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ed41c-110">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="ed41c-110">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)       |                                                                   | <span data-ttu-id="ed41c-111">Especifica el par de autenticación y cifrado que se usará para este perfil.</span><span class="sxs-lookup"><span data-stu-id="ed41c-111">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="ed41c-112">**autenticación**</span><span class="sxs-lookup"><span data-stu-id="ed41c-112">**authentication**</span></span>](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | <span data-ttu-id="ed41c-113">Especifica el par de autenticación y cifrado que se usará para este perfil.</span><span class="sxs-lookup"><span data-stu-id="ed41c-113">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="ed41c-114">**cifra**</span><span class="sxs-lookup"><span data-stu-id="ed41c-114">**encryption**</span></span>](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | <span data-ttu-id="ed41c-115">Establece el cifrado de datos que se va a usar para conectarse a la LAN inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="ed41c-115">Sets the data encryption to use to connect to the wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="ed41c-116">**keyIndex**</span><span class="sxs-lookup"><span data-stu-id="ed41c-116">**keyIndex**</span></span>](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | <span data-ttu-id="ed41c-117">Especifica qué índice de clave se debe usar para cifrar el tráfico inalámbrico.</span><span class="sxs-lookup"><span data-stu-id="ed41c-117">Specifies which key index must be used to encrypt wireless traffic.</span></span> <span data-ttu-id="ed41c-118">Solo se utiliza cuando keyType está establecido en networkKey.</span><span class="sxs-lookup"><span data-stu-id="ed41c-118">This is only used when keyType is set to networkKey.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="ed41c-119">**keyMaterial**</span><span class="sxs-lookup"><span data-stu-id="ed41c-119">**keyMaterial**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md)            | [<span data-ttu-id="ed41c-120">string</span><span class="sxs-lookup"><span data-stu-id="ed41c-120">string</span></span>](/dotnet/api/system.string)   | <span data-ttu-id="ed41c-121">Contiene la clave o frase de contraseña de la red.</span><span class="sxs-lookup"><span data-stu-id="ed41c-121">Contains the network key or passphrase.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="ed41c-122">**keyType**</span><span class="sxs-lookup"><span data-stu-id="ed41c-122">**keyType**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | <span data-ttu-id="ed41c-123">Tipo de clave.</span><span class="sxs-lookup"><span data-stu-id="ed41c-123">Type of key.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="ed41c-124">**PMKCacheMode**</span><span class="sxs-lookup"><span data-stu-id="ed41c-124">**PMKCacheMode**</span></span>](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | <span data-ttu-id="ed41c-125">Indica si se usará el almacenamiento en caché PMK.</span><span class="sxs-lookup"><span data-stu-id="ed41c-125">Indicates whether PMK caching will be used.</span></span> <span data-ttu-id="ed41c-126">Este elemento solo es válido para redes definidas por WPA2.</span><span class="sxs-lookup"><span data-stu-id="ed41c-126">This element is valid only for WPA2-defined networks.</span></span><br/> <span data-ttu-id="ed41c-127">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="ed41c-127">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="ed41c-128">**PMKCacheSize**</span><span class="sxs-lookup"><span data-stu-id="ed41c-128">**PMKCacheSize**</span></span>](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | <span data-ttu-id="ed41c-129">Especifica el número de entradas en la memoria caché de OMK en el cliente.</span><span class="sxs-lookup"><span data-stu-id="ed41c-129">Specifies the number of entries in the OMK cache on the client.</span></span> <span data-ttu-id="ed41c-130">Este elemento solo es válido para redes definidas por WPA2 con el modo PMKCache establecido en habilitado.</span><span class="sxs-lookup"><span data-stu-id="ed41c-130">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="ed41c-131">Si el modo PMKCache está habilitado y este elemento no está presente, el tamaño de la memoria caché tiene como valor predeterminado 128 entradas.</span><span class="sxs-lookup"><span data-stu-id="ed41c-131">If PMKCache mode is enabled, and this element is absent, the size of the cache defaults to 128 entries.</span></span><br/> <span data-ttu-id="ed41c-132">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="ed41c-132">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                   |
| [<span data-ttu-id="ed41c-133">**PMKCacheTTL**</span><span class="sxs-lookup"><span data-stu-id="ed41c-133">**PMKCacheTTL**</span></span>](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | <span data-ttu-id="ed41c-134">Indica el período de tiempo, en minutos, que se conservará una caché PMK.</span><span class="sxs-lookup"><span data-stu-id="ed41c-134">Indicates the length of time, in minutes, that a PMK cache will be kept.</span></span> <span data-ttu-id="ed41c-135">Este elemento solo es válido para redes definidas por WPA2 con el modo PMKCache establecido en habilitado.</span><span class="sxs-lookup"><span data-stu-id="ed41c-135">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span><br/> <span data-ttu-id="ed41c-136">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="ed41c-136">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="ed41c-137">**preAuthMode**</span><span class="sxs-lookup"><span data-stu-id="ed41c-137">**preAuthMode**</span></span>](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | <span data-ttu-id="ed41c-138">Determina si el cliente usará la autenticación previa.</span><span class="sxs-lookup"><span data-stu-id="ed41c-138">Determines if pre-authentication will be used by the client.</span></span> <span data-ttu-id="ed41c-139">La autenticación previa habilita la itinerancia rápida segura WPA2.</span><span class="sxs-lookup"><span data-stu-id="ed41c-139">Pre-authentication enables WPA2 secure fast roaming.</span></span> <span data-ttu-id="ed41c-140">Este elemento solo es válido para redes definidas por WPA2 con el modo PMKCache establecido en habilitado.</span><span class="sxs-lookup"><span data-stu-id="ed41c-140">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="ed41c-141">Si el modo PMKCache está habilitado y este elemento no está presente, el valor predeterminado es Disabled.</span><span class="sxs-lookup"><span data-stu-id="ed41c-141">If PMKCache mode is enabled, and this element is absent, the default value is disabled.</span></span><br/> <span data-ttu-id="ed41c-142">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="ed41c-142">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/> |
| [<span data-ttu-id="ed41c-143">**preAuthThrottle**</span><span class="sxs-lookup"><span data-stu-id="ed41c-143">**preAuthThrottle**</span></span>](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | <span data-ttu-id="ed41c-144">Indica el número de intentos cuando se realiza la autenticación en el APs vecino.</span><span class="sxs-lookup"><span data-stu-id="ed41c-144">Indicates the number of tries when preauthenticating to neighboring APs.</span></span> <span data-ttu-id="ed41c-145">Este elemento solo es válido para redes definidas por WPA2 con el modo PMKCache establecido en habilitado.</span><span class="sxs-lookup"><span data-stu-id="ed41c-145">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="ed41c-146">Si el modo PMKCache está habilitado y este elemento no está presente, el número de intentos predeterminado es 3.</span><span class="sxs-lookup"><span data-stu-id="ed41c-146">If PMKCache mode is enabled, and this element is absent, the number of tries defaults to 3.</span></span><br/> <span data-ttu-id="ed41c-147">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="ed41c-147">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="ed41c-148">**protected**</span><span class="sxs-lookup"><span data-stu-id="ed41c-148">**protected**</span></span>](wlan-profileschema-protected-sharedkey-element.md)                | [<span data-ttu-id="ed41c-149">boolean</span><span class="sxs-lookup"><span data-stu-id="ed41c-149">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="ed41c-150">Indica si la clave está cifrada.</span><span class="sxs-lookup"><span data-stu-id="ed41c-150">Indicates whether the key is encrypted.</span></span><br/> <span data-ttu-id="ed41c-151">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento debe tener un valor de **false**.</span><span class="sxs-lookup"><span data-stu-id="ed41c-151">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element must have a value of **FALSE**.</span></span><br/>                                                                                                                                                                                                                                             |
| [<span data-ttu-id="ed41c-152">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="ed41c-152">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | <span data-ttu-id="ed41c-153">Contiene la información de la clave compartida.</span><span class="sxs-lookup"><span data-stu-id="ed41c-153">Contains the shared key information.</span></span> <span data-ttu-id="ed41c-154">Este elemento solo es necesario si se requieren claves WEP o PSK para el par de autenticación y cifrado.</span><span class="sxs-lookup"><span data-stu-id="ed41c-154">This element is only required if WEP or PSK keys are required for the authentication and encryption pair.</span></span><br/>                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="ed41c-155">**useOneX**</span><span class="sxs-lookup"><span data-stu-id="ed41c-155">**useOneX**</span></span>](wlan-profileschema-useonex-authencryption-element.md)               | [<span data-ttu-id="ed41c-156">boolean</span><span class="sxs-lookup"><span data-stu-id="ed41c-156">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="ed41c-157">Indica si se usa 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="ed41c-157">Indicates whether 802.1X is used.</span></span> <span data-ttu-id="ed41c-158">Esta marca es opcional.</span><span class="sxs-lookup"><span data-stu-id="ed41c-158">This flag is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="ed41c-159">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed41c-159">Remarks</span></span>

<span data-ttu-id="ed41c-160">El elemento [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) se puede insertar como elemento secundario del elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ed41c-160">The [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element can be inserted as a child of the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span> <span data-ttu-id="ed41c-161">El elemento [**Onex**](onexschema-onex-element.md) se puede insertar como elemento secundario del elemento de **seguridad (MSM)** .</span><span class="sxs-lookup"><span data-stu-id="ed41c-161">The [**OneX**](onexschema-onex-element.md) element can be inserted as a child of the **security (MSM)** element.</span></span>

## <a name="examples"></a><span data-ttu-id="ed41c-162">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ed41c-162">Examples</span></span>

<span data-ttu-id="ed41c-163">Para ver los perfiles de ejemplo que usan el elemento de **seguridad** , consulte [ejemplos de perfiles inalámbricos](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="ed41c-163">To view sample profiles that use the **security** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ed41c-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed41c-164">Requirements</span></span>



| <span data-ttu-id="ed41c-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed41c-165">Requirement</span></span> | <span data-ttu-id="ed41c-166">Value</span><span class="sxs-lookup"><span data-stu-id="ed41c-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="ed41c-167">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed41c-167">Minimum supported client</span></span><br/> | <span data-ttu-id="ed41c-168">Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="ed41c-168">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ed41c-169">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed41c-169">Minimum supported server</span></span><br/> | <span data-ttu-id="ed41c-170">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ed41c-170">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="ed41c-171">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="ed41c-171">Redistributable</span></span><br/>          | <span data-ttu-id="ed41c-172">API de LAN inalámbrica para Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="ed41c-172">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="ed41c-173">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed41c-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed41c-174">Ejemplos de perfil inalámbrico</span><span class="sxs-lookup"><span data-stu-id="ed41c-174">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> <dt>

<span data-ttu-id="ed41c-175">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="ed41c-175">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ed41c-176">**MSM**</span><span class="sxs-lookup"><span data-stu-id="ed41c-176">**MSM**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="ed41c-177">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="ed41c-177">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ed41c-178">**MSM (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="ed41c-178">**MSM (WLANProfile)**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
</dt> </dl>

 

 
