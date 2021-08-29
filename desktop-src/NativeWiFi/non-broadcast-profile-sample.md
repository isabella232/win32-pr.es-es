---
description: Se usa para conectarse a redes que no difunden su nombre de red o SSID.
ms.assetid: 564324ad-6723-4676-ab5c-0b5d2957d201
title: Ejemplo de perfil que no es de difusión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8cab5a6ae274c90d1eeec40248ee73d04e610dba54e0024fca7eb3f463dabbc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801025"
---
# <a name="non-broadcast-profile-sample"></a>Ejemplo de perfil que no es de difusión

El ejemplo de perfil que no es de difusión se puede usar para conectarse a redes que no difunden su nombre de red o SSID.

Este perfil de ejemplo está configurado para usar Wi-Fi seguridad de acceso protegido que se ejecuta en modo personal (WPA-Personal). El Protocolo de integridad de clave temporal (TKIP) se usa para el cifrado. Los perfiles que usan otros tipos de seguridad y cifrado también se pueden configurar como perfiles que no son de difusión.

Windows XP con SP3 y LAN API inalámbrica **para Windows XP con SP2:** Se [**omite**](wlan-profileschema-name-wlanprofile-element.md) el elemento secundario name del elemento [**WLANProfile.**](wlan-profileschema-wlanprofile-element.md) El nombre del perfil, tal como se almacena en el almacén de perfiles, se deriva del nombre [**secundario**](wlan-profileschema-name-ssid-element.md) del [**elemento SSID.**](wlan-profileschema-ssid-ssidconfig-element.md)

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

 

 



