---
description: Debido a las diferencias de arquitectura subyacentes en el sistema operativo, Windows XP con Service Pack 3 (SP3) y la API de LAN inalámbrica para Windows XP con Service Pack 2 (SP2) solo admiten un subconjunto de los elementos descritos en el esquema de perfil WLAN y el material de referencia del \_ esquema OneX.
ms.assetid: 28c956c0-a0e2-4843-956d-abeab418604e
title: Compatibilidad de perfiles inalámbricos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36db0ecea6f85341d904603c99308ec10e79cee20d7567160cd3beee3b13c35
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684575"
---
# <a name="wireless-profile-compatibility"></a>Compatibilidad de perfiles inalámbricos

Debido a las diferencias de arquitectura subyacentes en el sistema operativo, Windows XP con Service Pack 3 (SP3) y la API de LAN inalámbrica para Windows XP con Service Pack 2 (SP2) solo admiten un subconjunto de los elementos descritos en el esquema de perfil [WLAN \_ ](wlan-profileschema-schema.md) y el material de referencia del [esquema OneX.](onexschema-schema.md)

Todos los perfiles que cumplan los requisitos de Windows XP con SP3 e WIRELESS LAN API para Windows XP con SP2 también se pueden usar en Windows Vista y Windows Server 2008.

## <a name="wlan_profile-support"></a>Compatibilidad con \_ perfiles WLAN

Los siguientes elementos de perfil WLAN no se admiten en Windows XP con SP3 o la API de LAN inalámbrica \_ para Windows XP con SP2:

-   conectividad (IHV)
-   IHV (WLANProfile)
-   OUI (OUIHeader)
-   phyType (conectividad)
-   PMKCacheMode (seguridad)
-   PMKCacheSize (seguridad)
-   PMKCacheTTL (seguridad)
-   preAuthMode (seguridad)
-   preAuthThrottle (seguridad)
-   seguridad (IHV)
-   type (OUIHeader)
-   useMSOneX (IHV)

En la tabla siguiente se muestran elementos de perfil WLAN con valores restringidos para Windows XP con SP3 e API de LAN inalámbrica \_ para Windows XP con SP2:



| Elemento                                                                               | Restricción                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**name (WLANProfile)**](wlan-profileschema-name-wlanprofile-element.md)             | El elemento name se omite cuando el perfil se guarda en el almacén de perfiles. El nombre del perfil se deriva automáticamente del SSID de la red. Para los perfiles de red de infraestructura, el nombre del perfil es el SSID de la red. Para los perfiles de red ad hoc, el nombre del perfil es el SSID de la red ad hoc seguido de `-adhoc` . |
| [**protected (sharedKey)**](wlan-profileschema-protected-sharedkey-element.md)       | Debe tener el valor FALSE.                                                                                                                                                                                                                                                                                                                                      |
| [**SSIDConfig (WLANProfile)**](wlan-profileschema-ssidconfig-wlanprofile-element.md) | Restringido a un elemento [**secundario SSID (SSIDConfig).**](wlan-profileschema-ssid-ssidconfig-element.md)                                                                                                                                                                                                                                                         |



 

## <a name="onex-support"></a>Compatibilidad con OneX

Solo se [**admite el elemento EAPConfig**](onexschema-eapconfig-onex-element.md) en Windows XP con SP3 e WIRELESS LAN API para Windows XP con SP2. Otros elementos OneX, si están presentes en un perfil, se omitirán.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la API Wi-Fi nativa](about-the-native-wifi-api.md)
</dt> <dt>

[Compatibilidad nativa con la API Wifi en Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> </dl>

 

 



