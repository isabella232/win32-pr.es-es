---
description: Se usa para conectarse a una red que requiere una configuración de seguridad que cumpla con los estándares federales de procesamiento de información (FIPS) 140-2.
ms.assetid: 169df4a3-e8b9-4f05-874f-a7eef6658d01
title: Ejemplo de Perfil de FIPS
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6d24f82a815c752a662af5f093dd9a7c34de33d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156681"
---
# <a name="fips-profile-sample"></a><span data-ttu-id="56857-103">Ejemplo de Perfil de FIPS</span><span class="sxs-lookup"><span data-stu-id="56857-103">FIPS Profile Sample</span></span>

<span data-ttu-id="56857-104">El ejemplo de Perfil de FIPS se puede usar para conectarse a una red que requiera una configuración de seguridad que cumpla con los estándares federales de procesamiento de información (FIPS) 140-2.</span><span class="sxs-lookup"><span data-stu-id="56857-104">The FIPS profile sample can be used to connect to a network that requires security settings that comply with Federal Information Processing Standards (FIPS) 140-2 standard.</span></span> <span data-ttu-id="56857-105">Para obtener más información sobre FIPS, vea [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md).</span><span class="sxs-lookup"><span data-stu-id="56857-105">For more information about FIPS, see [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md).</span></span>

<span data-ttu-id="56857-106">**Windows 7 y Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado:** Los cambios se implementan en Windows 7 y Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado para optimizar el rendimiento de las redes inalámbricas.</span><span class="sxs-lookup"><span data-stu-id="56857-106">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="56857-107">La configuración predeterminada de [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) cuando este elemento no está establecida en un perfil de LAN inalámbrica ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="56857-107">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="56857-108">La configuración predeterminada se cambia a "false" en Windows 7 y Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado.</span><span class="sxs-lookup"><span data-stu-id="56857-108">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="56857-109">La configuración predeterminada era "true" en Windows Server 2008 y Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="56857-109">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="56857-110">Para obtener más información, consulte la descripción del elemento de esquema [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="56857-110">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="56857-111">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Se omite el [**nombre**](wlan-profileschema-name-wlanprofile-element.md) secundario del elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="56857-111">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="56857-112">El nombre del perfil, tal como se almacena en el almacén de perfiles, se deriva del [**nombre**](wlan-profileschema-name-ssid-element.md) secundario del elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="56857-112">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span> <span data-ttu-id="56857-113">No se admite el elemento [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) .</span><span class="sxs-lookup"><span data-stu-id="56857-113">The [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element is not supported.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>FIPS_TEST</name>
    <SSIDConfig>
        <SSID>
            <hex>464950535F54455354</hex>
            <name>FIPS_TEST</name>
        </SSID>
        <nonBroadcast>false</nonBroadcast>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <autoSwitch>false</autoSwitch>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPA2</authentication>
                <encryption>AES</encryption>
                <useOneX>true</useOneX>
                <FIPSMode xmlns="https://www.microsoft.com/networking/WLAN/profile/v2">true</FIPSMode>
            </authEncryption>
            <OneX xmlns="https://www.microsoft.com/networking/OneX/v1">
                <EAPConfig>
                    <EapHostConfig xmlns="https://www.microsoft.com/provisioning/EapHostConfig">
                    <EapMethod>
                        <Type xmlns="https://www.microsoft.com/provisioning/EapCommon">25</Type>
                        <VendorId xmlns="https://www.microsoft.com/provisioning/EapCommon">0</VendorId>
                        <VendorType xmlns="https://www.microsoft.com/provisioning/EapCommon">0</VendorType>
                        <AuthorId xmlns="https://www.microsoft.com/provisioning/EapCommon">0</AuthorId>
                    </EapMethod>
                    <ConfigBlob></ConfigBlob>
                    </EapHostConfig>
                </EAPConfig>
            </OneX>
        </security>
    </MSM>
</WLANProfile>
```

## <a name="related-topics"></a><span data-ttu-id="56857-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="56857-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56857-115">Ejemplos de perfil inalámbrico</span><span class="sxs-lookup"><span data-stu-id="56857-115">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 



