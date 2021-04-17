---
description: Se usa para conectarse a redes que no difunden su nombre de red o SSID.
ms.assetid: 564324ad-6723-4676-ab5c-0b5d2957d201
title: Ejemplo de perfil sin difusión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a09bfd9cf9eac724f882a9aa3cf16064f051fdf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677755"
---
# <a name="non-broadcast-profile-sample"></a><span data-ttu-id="77b41-103">Ejemplo de perfil sin difusión</span><span class="sxs-lookup"><span data-stu-id="77b41-103">Non-Broadcast Profile Sample</span></span>

<span data-ttu-id="77b41-104">El ejemplo de perfil sin difusión se puede usar para conectarse a redes que no difundan su nombre de red o SSID.</span><span class="sxs-lookup"><span data-stu-id="77b41-104">The non-broadcast profile sample can be used to connect to networks which do not broadcast their network name or SSID.</span></span>

<span data-ttu-id="77b41-105">Este perfil de ejemplo está configurado para usar Wi-Fi seguridad de acceso protegido que se ejecuta en modo personal (WPA-Personal).</span><span class="sxs-lookup"><span data-stu-id="77b41-105">This sample profile is configured to use Wi-Fi Protected Access security running in Personal mode (WPA-Personal).</span></span> <span data-ttu-id="77b41-106">El protocolo de integridad de clave temporal (TKIP) se usa para el cifrado.</span><span class="sxs-lookup"><span data-stu-id="77b41-106">Temporal Key Integrity Protocol (TKIP) is used for encryption.</span></span> <span data-ttu-id="77b41-107">Los perfiles que usan otros tipos de cifrado y seguridad también se pueden configurar como perfiles que no son de difusión.</span><span class="sxs-lookup"><span data-stu-id="77b41-107">Profiles that use other security and cipher types can also be configured as non-broadcast profiles.</span></span>

<span data-ttu-id="77b41-108">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Se omite el [**nombre**](wlan-profileschema-name-wlanprofile-element.md) secundario del elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="77b41-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="77b41-109">El nombre del perfil, tal como se almacena en el almacén de perfiles, se deriva del [**nombre**](wlan-profileschema-name-ssid-element.md) secundario del elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="77b41-109">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleNonBroadcast</name>
    <SSIDConfig>
        <SSID>
            <name>SampleNonBroadcast</name>
        </SSID>
        <nonBroadcast>true</nonBroadcast>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPAPSK</authentication>
                <encryption>TKIP</encryption>
                <useOneX>false</useOneX>
            </authEncryption>
        </security>
    </MSM>
</WLANProfile>
```

<span data-ttu-id="77b41-110">Se ha omitido la clave compartida de este perfil de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="77b41-110">The shared key has been omitted from this sample profile.</span></span> <span data-ttu-id="77b41-111">Si intenta usar este perfil de ejemplo para conectarse a una red, se le pedirá que escriba una clave compartida.</span><span class="sxs-lookup"><span data-stu-id="77b41-111">If you try to use this sample profile to connect to a network, you will be prompted to enter a shared key.</span></span> <span data-ttu-id="77b41-112">Puede evitar este mensaje agregando un elemento secundario [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) al elemento de [**seguridad**](wlan-profileschema-security-msm-element.md) inmediatamente después del elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="77b41-112">You can avoid this prompt by adding a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) child element to the [**security**](wlan-profileschema-security-msm-element.md) element immediately following the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

<span data-ttu-id="77b41-113">En el fragmento de código siguiente se muestra un elemento [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) que contiene una clave no cifrada.</span><span class="sxs-lookup"><span data-stu-id="77b41-113">The following snippet shows a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element that contains an unencrypted key.</span></span> <span data-ttu-id="77b41-114">Debe reemplazar el comentario `<!-- insert key here -->` con la clave sin cifrar real antes de usar este fragmento de código en un perfil.</span><span class="sxs-lookup"><span data-stu-id="77b41-114">You must replace the comment `<!-- insert key here -->` with the actual unencrypted key before using this snippet in a profile.</span></span>

``` syntax
<sharedKey>
    <keyType>passPhrase</keyType>
    <protected>false</protected>
    <keyMaterial> <!-- insert key here --> </keyMaterial>
</sharedKey>
```

## <a name="related-topics"></a><span data-ttu-id="77b41-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="77b41-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77b41-116">Ejemplos de perfil inalámbrico</span><span class="sxs-lookup"><span data-stu-id="77b41-116">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 



