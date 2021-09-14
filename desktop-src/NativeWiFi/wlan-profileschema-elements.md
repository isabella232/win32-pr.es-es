---
description: El esquema \_ de perfil WLAN define los siguientes elementos.
ms.assetid: 9eb0f446-1202-4770-b09e-250e83524119
title: WLAN_profile de esquema
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a94394c32712d8ee8871ada753f342861e1f530e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245522"
---
# <a name="wlan_profile-schema-elements"></a>Elementos de esquema de perfil WLAN \_

El esquema \_ de perfil WLAN define los siguientes elementos. La mayoría de los elementos están en el espacio de nombres , excepto `https://www.microsoft.com/networking/WLAN/profile/v1` [**FIPSMode (authEncryption),**](wlan-profileschema-fipsmode-authencryption-element.md)que se encuentra en el espacio de nombres `https://www.microsoft.com/networking/WLAN/profile/v2` .

En la lista siguiente se muestran los elementos definidos en el orden en que los elementos aparecen en un perfil. Se aplica el orden de los elementos. No todos los elementos están en todos los perfiles, ya que algunos elementos son opcionales.

Esta lista no muestra todos los elementos posibles que pueden aparecer en un perfil inalámbrico, ya que los elementos se pueden agregar en **xs:any puntos de** inserción.

-   [**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
    -   [**name (WLANProfile)**](wlan-profileschema-name-wlanprofile-element.md)
    -   [**SSIDConfig (WLANProfile)**](wlan-profileschema-ssidconfig-wlanprofile-element.md)
        -   [**SSID (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md)
            -   [**hexadecimal (SSID)**](wlan-profileschema-hex-ssid-element.md)
            -   [**name (SSID)**](wlan-profileschema-name-ssid-element.md)
        -   [**nonBroadcast (SSIDConfig)**](wlan-profileschema-nonbroadcast-ssidconfig-element.md)
    -   [**Hotspot2 (WLANProfile)**](wlan-profileschema-hotspot2-element.md)
        -   [**DomainName (Hotspot2)**](wlan-profileschema-hotspot2-domainname-element.md)
        -   [**NAIRealm (Hotspot2)**](wlan-profileschema-hotspot2-nairealm-element.md)
        -   [**Network3GPP (Hotspot2)**](wlan-profileschema-hotspot2-network3gpp-element.md)
        -   [**RoamingConsortium (Hotspot2)**](wlan-profileschema-hotspot2-roamingconsortium-element.md)
    -   [**connectionType (WLANProfile)**](wlan-profileschema-connectiontype-wlanprofile-element.md)
    -   [**connectionMode (WLANProfile)**](wlan-profileschema-connectionmode-wlanprofile-element.md)
    -   [**autoSwitch (WLANProfile)**](wlan-profileschema-autoswitch-wlanprofile-element.md)
    -   [**MSM (WLANProfile)**](wlan-profileschema-msm-wlanprofile-element.md)
        -   [**connectivity (MSM)**](wlan-profileschema-connectivity-msm-element.md)
            -   [**phyType (conectividad)**](wlan-profileschema-phytype-connectivity-element.md)
        -   [**seguridad (MSM)**](wlan-profileschema-security-msm-element.md)
            -   [**authEncryption (seguridad)**](wlan-profileschema-authencryption-security-element.md)
                -   [**autenticación (authEncryption)**](wlan-profileschema-authentication-authencryption-element.md)
                -   [**cifrado (authEncryption)**](wlan-profileschema-encryption-authencryption-element.md)
                -   [**useOneX (authEncryption)**](wlan-profileschema-useonex-authencryption-element.md)
                -   [**FIPSMode (authEncryption)**](wlan-profileschema-fipsmode-authencryption-element.md)
            -   [**sharedKey (seguridad)**](wlan-profileschema-sharedkey-security-element.md)
                -   [**keyType (sharedKey)**](wlan-profileschema-keytype-sharedkey-element.md)
                -   [**protected (sharedKey)**](wlan-profileschema-protected-sharedkey-element.md)
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
            -   [**type (OUIHeader)**](wlan-profileschema-type-ouiheader-element.md)
        -   [**conectividad (IHV)**](wlan-profileschema-connectivity-ihv-element.md)
        -   [**seguridad (IHV)**](wlan-profileschema-security-ihv-element.md)
        -   [**useMSOneX (IHV)**](wlan-profileschema-usemsonex-ihv-element.md)

 

 



