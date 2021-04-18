---
description: Debido a las diferencias arquitectónicas subyacentes en el sistema operativo, Windows XP con Service Pack 3 (SP3) y la API de LAN inalámbrica para Windows XP con Service Pack 2 (SP2) solo admiten un subconjunto de los elementos descritos en el esquema de Perfil de WLAN \_ y el material de referencia de esquema de Onex.
ms.assetid: 28c956c0-a0e2-4843-956d-abeab418604e
title: Compatibilidad con perfiles inalámbricos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e0eebfa627fb99d50490907108a2ddc7360202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545678"
---
# <a name="wireless-profile-compatibility"></a>Compatibilidad con perfiles inalámbricos

Debido a las diferencias arquitectónicas subyacentes en el sistema operativo, Windows XP con Service Pack 3 (SP3) y la API de LAN inalámbrica para Windows XP con Service Pack 2 (SP2) solo admiten un subconjunto de los elementos descritos en el [ \_ esquema de Perfil de WLAN](wlan-profileschema-schema.md) y el material de referencia de esquema de [Onex](onexschema-schema.md) .

Todos los perfiles que cumplen con los requisitos de Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2 también se pueden usar en Windows Vista y Windows Server 2008.

## <a name="wlan_profile-support"></a>\_Compatibilidad con perfiles de WLAN

Los siguientes \_ elementos de Perfil de WLAN no se admiten en Windows XP con SP3 o la API de LAN inalámbrica para Windows XP con SP2:

-   Conectividad (IHV)
-   IHV (WLANProfile)
-   OUI (OUIHeader)
-   phyType (conectividad)
-   PMKCacheMode (seguridad)
-   PMKCacheSize (seguridad)
-   PMKCacheTTL (seguridad)
-   preAuthMode (seguridad)
-   preAuthThrottle (seguridad)
-   seguridad (IHV)
-   tipo (OUIHeader)
-   useMSOneX (IHV)

En la tabla siguiente se muestran los elementos de Perfil de WLAN \_ con valores restringidos para Windows XP con SP3 y la API de LAN inalámbrica para Windows XP con SP2:



| Elemento                                                                               | Restricción                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**nombre (WLANProfile)**](wlan-profileschema-name-wlanprofile-element.md)             | El elemento Name se omite cuando el perfil se guarda en el almacén de perfiles. El nombre del perfil se deriva automáticamente del SSID de la red. En el caso de los perfiles de red de infraestructura, el nombre del perfil es el SSID de la red. En el caso de los perfiles de red ad hoc, el nombre del perfil es el SSID de la red ad hoc seguido de `-adhoc` . |
| [**protegido (sharedKey)**](wlan-profileschema-protected-sharedkey-element.md)       | Debe tener un valor de FALSE.                                                                                                                                                                                                                                                                                                                                      |
| [**SSIDConfig (WLANProfile)**](wlan-profileschema-ssidconfig-wlanprofile-element.md) | Restringido a un elemento [**SSID secundario (SSIDConfig)**](wlan-profileschema-ssid-ssidconfig-element.md) .                                                                                                                                                                                                                                                         |



 

## <a name="onex-support"></a>Compatibilidad con OneX

Solo se admite el elemento [**EAPConfig**](onexschema-eapconfig-onex-element.md) en Windows XP con SP3 y la API de LAN inalámbrica para Windows XP con SP2. Otros elementos OneX, si están presentes en un perfil, se omitirán.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la API nativa WiFi](about-the-native-wifi-api.md)
</dt> <dt>

[Compatibilidad con la API WiFi nativa en Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> </dl>

 

 



