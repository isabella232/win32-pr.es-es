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
# <a name="wpa2-personal-profile-sample"></a>WPA2-Personal de perfil

Este perfil de ejemplo usa una clave previamente compartida para la autenticación de red. La clave se comparte con el cliente y el punto de acceso. Este perfil de ejemplo está configurado para usar Wi-Fi seguridad de acceso protegido 2 que se ejecuta en modo personal (WPA2-Personal). El Estándar de cifrado avanzado cifrado (AES) se usa para el cifrado.

**Windows 7 y Windows Server 2008 R2 con el servicio LAN inalámbrica instalado:** Los cambios se implementan en Windows 7 y Windows Server 2008 R2 con el servicio LAN inalámbrica instalado para optimizar el rendimiento de las redes inalámbricas. La configuración predeterminada de [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) cuando este elemento no está establecido en un perfil de LAN inalámbrica ha cambiado. La configuración predeterminada se cambia a "false" en Windows 7 y Windows Server 2008 R2 con el servicio laN inalámbrica instalado. El valor predeterminado era "true" en Windows Server 2008 y Windows Vista. Consulte la descripción del [**elemento de esquema autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md) para obtener más información.

**Windows XP con SP3 e API de LAN inalámbrica para Windows XP con SP2:** Se [**omite**](wlan-profileschema-name-wlanprofile-element.md) el elemento secundario name del elemento [**WLANProfile.**](wlan-profileschema-wlanprofile-element.md) El nombre del perfil, tal como se almacena en el almacén de perfiles, se deriva del elemento secundario [**name**](wlan-profileschema-name-ssid-element.md) del [**elemento SSID.**](wlan-profileschema-ssid-ssidconfig-element.md)

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

La clave compartida se ha omitido en este perfil de ejemplo. Si intenta usar este perfil de ejemplo para conectarse a una red, se le pedirá que escriba una clave compartida. Puede evitar este mensaje agregando un elemento secundario [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) al elemento [**de**](wlan-profileschema-security-msm-element.md) seguridad inmediatamente después del [**elemento authEncryption.**](wlan-profileschema-authencryption-security-element.md)

El fragmento de código siguiente muestra [**un elemento sharedKey**](wlan-profileschema-sharedkey-security-element.md) que contiene una clave sin cifrar. Debe reemplazar el comentario por la clave sin cifrar real antes de `<!-- insert key here -->` usar este fragmento de código en un perfil.

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

 

 



