---
description: Usa una clave previamente compartida para la autenticación de red. Este perfil de ejemplo usa Wi-Fi seguridad de acceso protegido 2 que se ejecuta en modo personal (WPA2-Personal).
ms.assetid: dbbadac6-1b7e-4161-a775-a934cf201c9d
title: WPA2-Personal de perfil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75e0df238b83a27155e640d56fc81ed5606a76e3
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394870"
---
# <a name="wpa2-personal-profile-sample"></a><span data-ttu-id="cb89e-104">WPA2-Personal de perfil</span><span class="sxs-lookup"><span data-stu-id="cb89e-104">WPA2-Personal Profile Sample</span></span>

<span data-ttu-id="cb89e-105">Este perfil de ejemplo usa una clave previamente compartida para la autenticación de red.</span><span class="sxs-lookup"><span data-stu-id="cb89e-105">This sample profile uses a pre-shared key for network authentication.</span></span> <span data-ttu-id="cb89e-106">La clave se comparte con el cliente y el punto de acceso.</span><span class="sxs-lookup"><span data-stu-id="cb89e-106">The key is shared with the client and the access point.</span></span> <span data-ttu-id="cb89e-107">Este perfil de ejemplo está configurado para usar Wi-Fi seguridad de acceso protegido 2 que se ejecuta en modo personal (WPA2-Personal).</span><span class="sxs-lookup"><span data-stu-id="cb89e-107">This sample profile is configured to use Wi-Fi Protected Access 2 security running in Personal mode (WPA2-Personal).</span></span> <span data-ttu-id="cb89e-108">El Estándar de cifrado avanzado cifrado (AES) se usa para el cifrado.</span><span class="sxs-lookup"><span data-stu-id="cb89e-108">The Advanced Encryption Standard (AES) cipher type is used for encryption.</span></span>

<span data-ttu-id="cb89e-109">**Windows 7 y Windows Server 2008 R2 con el servicio LAN inalámbrica instalado:** Los cambios se implementan en Windows 7 y Windows Server 2008 R2 con el servicio LAN inalámbrica instalado para optimizar el rendimiento de las redes inalámbricas.</span><span class="sxs-lookup"><span data-stu-id="cb89e-109">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="cb89e-110">La configuración predeterminada de [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) cuando este elemento no está establecido en un perfil de LAN inalámbrica ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="cb89e-110">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="cb89e-111">La configuración predeterminada se cambia a "false" en Windows 7 y Windows Server 2008 R2 con el servicio laN inalámbrica instalado.</span><span class="sxs-lookup"><span data-stu-id="cb89e-111">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="cb89e-112">El valor predeterminado era "true" en Windows Server 2008 y Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cb89e-112">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="cb89e-113">Consulte la descripción del [**elemento de esquema autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="cb89e-113">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="cb89e-114">**Windows XP con SP3 e API de LAN inalámbrica para Windows XP con SP2:** Se [**omite**](wlan-profileschema-name-wlanprofile-element.md) el elemento secundario name del elemento [**WLANProfile.**](wlan-profileschema-wlanprofile-element.md)</span><span class="sxs-lookup"><span data-stu-id="cb89e-114">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="cb89e-115">El nombre del perfil, tal como se almacena en el almacén de perfiles, se deriva del elemento secundario [**name**](wlan-profileschema-name-ssid-element.md) del [**elemento SSID.**](wlan-profileschema-ssid-ssidconfig-element.md)</span><span class="sxs-lookup"><span data-stu-id="cb89e-115">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

``` syntax
<?xml version="1.0" encoding="US-ASCII"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
    <name>SampleWPA2PSK</name>
    <SSIDConfig>
        <SSID>
            <name>SampleWPA2PSK</name>
        </SSID>
    </SSIDConfig>
    <connectionType>ESS</connectionType>
    <connectionMode>auto</connectionMode>
    <autoSwitch>false</autoSwitch>
    <MSM>
        <security>
            <authEncryption>
                <authentication>WPA2PSK</authentication>
                <encryption>AES</encryption>
                <useOneX>false</useOneX>
            </authEncryption>
        </security>
    </MSM>
</WLANProfile>
```

<span data-ttu-id="cb89e-116">La clave compartida se ha omitido en este perfil de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="cb89e-116">The shared key has been omitted from this sample profile.</span></span> <span data-ttu-id="cb89e-117">Si intenta usar este perfil de ejemplo para conectarse a una red, se le pedirá que escriba una clave compartida.</span><span class="sxs-lookup"><span data-stu-id="cb89e-117">If you try to use this sample profile to connect to a network, you will be prompted to enter a shared key.</span></span> <span data-ttu-id="cb89e-118">Puede evitar este mensaje agregando un elemento secundario [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) al elemento [**de**](wlan-profileschema-security-msm-element.md) seguridad inmediatamente después del [**elemento authEncryption.**](wlan-profileschema-authencryption-security-element.md)</span><span class="sxs-lookup"><span data-stu-id="cb89e-118">You can avoid this prompt by adding a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) child element to the [**security**](wlan-profileschema-security-msm-element.md) element immediately following the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

<span data-ttu-id="cb89e-119">El fragmento de código siguiente muestra [**un elemento sharedKey**](wlan-profileschema-sharedkey-security-element.md) que contiene una clave sin cifrar.</span><span class="sxs-lookup"><span data-stu-id="cb89e-119">The following snippet shows a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element that contains an unencrypted key.</span></span> <span data-ttu-id="cb89e-120">Debe reemplazar el comentario por la clave sin cifrar real antes de `<!-- insert key here -->` usar este fragmento de código en un perfil.</span><span class="sxs-lookup"><span data-stu-id="cb89e-120">You must replace the comment `<!-- insert key here -->` with the actual unencrypted key before using this snippet in a profile.</span></span>

``` syntax
<sharedKey>
    <keyType>passPhrase</keyType>
    <protected>false</protected>
    <keyMaterial> <!-- insert key here --> </keyMaterial>
</sharedKey>
```

## <a name="related-topics"></a><span data-ttu-id="cb89e-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cb89e-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb89e-122">Ejemplos de perfil inalámbrico</span><span class="sxs-lookup"><span data-stu-id="cb89e-122">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 



