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
# <a name="wpa2-personal-profile-sample"></a>Ejemplo de Perfil de WPA2-Personal

Este perfil de ejemplo usa una clave previamente compartida para la autenticación de red. La clave se comparte con el cliente y el punto de acceso. Este perfil de ejemplo está configurado para usar Wi-Fi seguridad de acceso protegido 2 que se ejecuta en modo personal (WPA2-Personal). El tipo de cifrado Estándar de cifrado avanzado (AES) se usa para el cifrado.

**Windows 7 y Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado:** Los cambios se implementan en Windows 7 y Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado para optimizar el rendimiento de las redes inalámbricas. La configuración predeterminada de [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) cuando este elemento no está establecida en un perfil de LAN inalámbrica ha cambiado. La configuración predeterminada se cambia a "false" en Windows 7 y Windows Server 2008 R2 con el servicio de LAN inalámbrica instalado. La configuración predeterminada era "true" en Windows Server 2008 y Windows Vista. Para obtener más información, consulte la descripción del elemento de esquema [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) .

**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Se omite el [**nombre**](wlan-profileschema-name-wlanprofile-element.md) secundario del elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) . El nombre del perfil, tal como se almacena en el almacén de perfiles, se deriva del [**nombre**](wlan-profileschema-name-ssid-element.md) secundario del elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .

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

Se ha omitido la clave compartida de este perfil de ejemplo. Si intenta usar este perfil de ejemplo para conectarse a una red, se le pedirá que escriba una clave compartida. Puede evitar este mensaje agregando un elemento secundario [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) al elemento de [**seguridad**](wlan-profileschema-security-msm-element.md) inmediatamente después del elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .

En el fragmento de código siguiente se muestra un elemento [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) que contiene una clave no cifrada. Debe reemplazar el comentario `<!-- insert key here -->` con la clave sin cifrar real antes de usar este fragmento de código en un perfil.

``` syntax
<sharedKey>
    <keyType>passPhrase</keyType>
    <protected>false</protected>
    <keyMaterial> <!-- insert key here --> </keyMaterial>
</sharedKey>
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplos de perfil inalámbrico](wireless-profile-samples.md)
</dt> </dl>

 

 



