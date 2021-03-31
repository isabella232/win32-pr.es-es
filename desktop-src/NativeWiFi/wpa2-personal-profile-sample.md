---
description: Usa una clave previamente compartida para la autenticación de red.
ms.assetid: dbbadac6-1b7e-4161-a775-a934cf201c9d
title: Ejemplo de Perfil de WPA2-Personal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0054bc28962113a85bb909d4e8cd173b3bc16974
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361223"
---
# <a name="wpa2-personal-profile-sample"></a><span data-ttu-id="5d386-103">Ejemplo de Perfil de WPA2-Personal</span><span class="sxs-lookup"><span data-stu-id="5d386-103">WPA2-Personal Profile Sample</span></span>

<span data-ttu-id="5d386-104">Este perfil de ejemplo usa una clave previamente compartida para la autenticación de red.</span><span class="sxs-lookup"><span data-stu-id="5d386-104">This sample profile uses a pre-shared key for network authentication.</span></span> <span data-ttu-id="5d386-105">La clave se comparte con el cliente y el punto de acceso.</span><span class="sxs-lookup"><span data-stu-id="5d386-105">The key is shared with the client and the access point.</span></span> <span data-ttu-id="5d386-106">Este perfil de ejemplo está configurado para usar Wi-Fi seguridad de acceso protegido 2 que se ejecuta en modo personal (WPA2-Personal).</span><span class="sxs-lookup"><span data-stu-id="5d386-106">This sample profile is configured to use Wi-Fi Protected Access 2 security running in Personal mode (WPA2-Personal).</span></span> <span data-ttu-id="5d386-107">El tipo de cifrado Estándar de cifrado avanzado (AES) se usa para el cifrado.</span><span class="sxs-lookup"><span data-stu-id="5d386-107">The Advanced Encryption Standard (AES) cipher type is used for encryption.</span></span>

<span data-ttu-id="5d386-108">**Windows 7 y Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado:** Los cambios se implementan en Windows 7 y Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado para optimizar el rendimiento de las redes inalámbricas.</span><span class="sxs-lookup"><span data-stu-id="5d386-108">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="5d386-109">La configuración predeterminada de [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) cuando este elemento no está establecida en un perfil de LAN inalámbrica ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="5d386-109">The default setting for [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="5d386-110">La configuración predeterminada se cambia a "false" en Windows 7 y Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado.</span><span class="sxs-lookup"><span data-stu-id="5d386-110">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="5d386-111">La configuración predeterminada era "true" en Windows Server 2008 y Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5d386-111">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="5d386-112">Para obtener más información, consulte la descripción del elemento de esquema [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5d386-112">Please refer to the [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) schema element description for more information.</span></span>

<span data-ttu-id="5d386-113">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Se omite el [**nombre**](wlan-profileschema-name-wlanprofile-element.md) secundario del elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5d386-113">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The [**name**](wlan-profileschema-name-wlanprofile-element.md) child of the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element is ignored.</span></span> <span data-ttu-id="5d386-114">El nombre del perfil, tal como se almacena en el almacén de perfiles, se deriva del [**nombre**](wlan-profileschema-name-ssid-element.md) secundario del elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5d386-114">The name of the profile, as stored in the profile store, is derived from the [**name**](wlan-profileschema-name-ssid-element.md) child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

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

<span data-ttu-id="5d386-115">Se ha omitido la clave compartida de este perfil de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="5d386-115">The shared key has been omitted from this sample profile.</span></span> <span data-ttu-id="5d386-116">Si intenta usar este perfil de ejemplo para conectarse a una red, se le pedirá que escriba una clave compartida.</span><span class="sxs-lookup"><span data-stu-id="5d386-116">If you try to use this sample profile to connect to a network, you will be prompted to enter a shared key.</span></span> <span data-ttu-id="5d386-117">Puede evitar este mensaje agregando un elemento secundario [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) al elemento de [**seguridad**](wlan-profileschema-security-msm-element.md) inmediatamente después del elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5d386-117">You can avoid this prompt by adding a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) child element to the [**security**](wlan-profileschema-security-msm-element.md) element immediately following the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

<span data-ttu-id="5d386-118">En el fragmento de código siguiente se muestra un elemento [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) que contiene una clave no cifrada.</span><span class="sxs-lookup"><span data-stu-id="5d386-118">The following snippet shows a [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element that contains an unencrypted key.</span></span> <span data-ttu-id="5d386-119">Debe reemplazar el comentario `<!-- insert key here -->` con la clave sin cifrar real antes de usar este fragmento de código en un perfil.</span><span class="sxs-lookup"><span data-stu-id="5d386-119">You must replace the comment `<!-- insert key here -->` with the actual unencrypted key before using this snippet in a profile.</span></span>

``` syntax
<sharedKey>
    <keyType>passPhrase</keyType>
    <protected>false</protected>
    <keyMaterial> <!-- insert key here --> </keyMaterial>
</sharedKey>
```

## <a name="related-topics"></a><span data-ttu-id="5d386-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5d386-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d386-121">Ejemplos de perfil inalámbrico</span><span class="sxs-lookup"><span data-stu-id="5d386-121">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 



