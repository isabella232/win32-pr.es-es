---
description: El esquema de Perfil de WLAN \_ define los siguientes elementos.
ms.assetid: 9eb0f446-1202-4770-b09e-250e83524119
title: WLAN_profile elementos de esquema
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a94394c32712d8ee8871ada753f342861e1f530e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810381"
---
# <a name="wlan_profile-schema-elements"></a>Elementos de esquema de Perfil de WLAN \_

El esquema de Perfil de WLAN \_ define los siguientes elementos. La mayoría de los elementos se encuentran en el espacio de nombres `https://www.microsoft.com/networking/WLAN/profile/v1` , excepto en el caso de [**FIPSMode (authEncryption)**](wlan-profileschema-fipsmode-authencryption-element.md), que se encuentra en el espacio de nombres `https://www.microsoft.com/networking/WLAN/profile/v2` .

En la lista siguiente se muestran los elementos definidos en el orden en que los elementos aparecen en un perfil. Se aplica el orden de los elementos. No todos los elementos están en cada perfil, ya que algunos elementos son opcionales.

En esta lista no se muestran todos los elementos posibles que pueden aparecer en un perfil inalámbrico, ya que los elementos se pueden agregar en **xs: cualquier** punto de inserción.

-   [**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
    -   [**nombre (WLANProfile)**](wlan-profileschema-name-wlanprofile-element.md)
    -   [**SSIDConfig (WLANProfile)**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
        -   [**SSID (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md)
            -   [**Hex (SSID)**](wlan-profileschema-hex-ssid-element.md)
            -   [**nombre (SSID)**](wlan-profileschema-name-ssid-element.md)
        -   [**nondifusión (SSIDConfig)**](wlan-profileschema-nonbroadcast-ssidconfig-element.md)
    -   [**Hotspot2 (WLANProfile)**](wlan-profileschema-hotspot2-element.md)
        -   [**NombreDeDominio (Hotspot2)**](wlan-profileschema-hotspot2-domainname-element.md)
        -   [**NAIRealm (Hotspot2)**](wlan-profileschema-hotspot2-nairealm-element.md)
        -   [**Network3GPP (Hotspot2)**](wlan-profileschema-hotspot2-network3gpp-element.md)
        -   [**RoamingConsortium (Hotspot2)**](wlan-profileschema-hotspot2-roamingconsortium-element.md)
    -   [**connectionType (WLANProfile)**](wlan-profileschema-connectiontype-wlanprofile-element.md)
    -   [**connectionMode (WLANProfile)**](wlan-profileschema-connectionmode-wlanprofile-element.md)
    -   [**AutoSwitch (WLANProfile)**](wlan-profileschema-autoswitch-wlanprofile-element.md)
    -   [**MSM (WLANProfile)**](wlan-profileschema-msm-wlanprofile-element.md)
        -   [**Conectividad (MSM)**](wlan-profileschema-connectivity-msm-element.md)
            -   [**phyType (conectividad)**](wlan-profileschema-phytype-connectivity-element.md)
        -   [**seguridad (MSM)**](wlan-profileschema-security-msm-element.md)
            -   [**authEncryption (seguridad)**](wlan-profileschema-authencryption-security-element.md)
                -   [**autenticación (authEncryption)**](wlan-profileschema-authentication-authencryption-element.md)
                -   [**cifrado (authEncryption)**](wlan-profileschema-encryption-authencryption-element.md)
                -   [**useOneX (authEncryption)**](wlan-profileschema-useonex-authencryption-element.md)
                -   [**FIPSMode (authEncryption)**](wlan-profileschema-fipsmode-authencryption-element.md)
            -   [**sharedKey (seguridad)**](wlan-profileschema-sharedkey-security-element.md)
                -   [**keyType (sharedKey)**](wlan-profileschema-keytype-sharedkey-element.md)
                -   [**protegido (sharedKey)**](wlan-profileschema-protected-sharedkey-element.md)
                -   [**keyMaterial (sharedKey)**](wlan-profileschema-keymaterial-sharedkey-element.md)
            -   [**keyIndex (seguridad)**](wlan-profileschema-keyindex-security-element.md)
            -   [**PMKCacheMode (seguridad)**](wlan-profileschema-pmkcachemode-security-element.md)
            -   [**PMKCacheTTL (seguridad)**](wlan-profileschema-pmkcachettl-security-element.md)
            -   [**PMKCacheSize (seguridad)**](wlan-profileschema-pmkcachesize-security-element.md)
            -   [**preAuthMode (seguridad)**](wlan-profileschema-preauthmode-security-element.md)
            -   [**preAuthThrottle (seguridad)**](wlan-profileschema-preauththrottle-security-element.md)
    -   [**IHV (WLANProfile)**](wlan-profileschema-ihv-wlanprofile-element.md)
        -   [**OUIHeader (IHV)**](wlan-profileschema-ouiheader-ihv-element.md)
            -   [**OUI (OUIHeader)**](wlan-profileschema-oui-ouiheader-element.md)
            -   [**tipo (OUIHeader)**](wlan-profileschema-type-ouiheader-element.md)
        -   [**Conectividad (IHV)**](wlan-profileschema-connectivity-ihv-element.md)
        -   [**seguridad (IHV)**](wlan-profileschema-security-ihv-element.md)
        -   [**useMSOneX (IHV)**](wlan-profileschema-usemsonex-ihv-element.md)

 

 



