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
# <a name="non-broadcast-profile-sample"></a>Ejemplo de perfil sin difusión

El ejemplo de perfil sin difusión se puede usar para conectarse a redes que no difundan su nombre de red o SSID.

Este perfil de ejemplo está configurado para usar Wi-Fi seguridad de acceso protegido que se ejecuta en modo personal (WPA-Personal). El protocolo de integridad de clave temporal (TKIP) se usa para el cifrado. Los perfiles que usan otros tipos de cifrado y seguridad también se pueden configurar como perfiles que no son de difusión.

**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Se omite el [**nombre**](wlan-profileschema-name-wlanprofile-element.md) secundario del elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) . El nombre del perfil, tal como se almacena en el almacén de perfiles, se deriva del [**nombre**](wlan-profileschema-name-ssid-element.md) secundario del elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .

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

 

 



