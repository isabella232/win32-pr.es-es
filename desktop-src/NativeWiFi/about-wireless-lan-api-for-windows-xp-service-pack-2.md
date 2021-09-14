---
description: Se admite un subconjunto de la funcionalidad de la API de Wi-Fi nativa en Windows XP con Service Pack 2 (SP2) y Windows XP con Service Pack 3 (SP3).
ms.assetid: d32c4a03-59e8-4fdd-9d5a-e7ef0eb25e84
title: Compatibilidad nativa de la API wifi en Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cd422c6589b37f516b9d45d072489c9d5e00b82
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074188"
---
# <a name="native-wifi-api-support-on-windows-xp"></a>Compatibilidad nativa de la API wifi en Windows XP

Se admite un subconjunto de la funcionalidad de la API de Wi-Fi nativa en Windows XP con Service Pack 2 (SP2) y Windows XP con Service Pack 3 (SP3). Esta funcionalidad se incluye en Windows XP con SP3 de forma predeterminada. En Windows XP con SP2, esta funcionalidad se puede agregar aplicando una revisión, que se conoce como API de LAN inalámbrica para Windows XP con Service Pack 2 (SP2). Para obtener más información o descargar la revisión, vea "Los desarrolladores no pueden crear programas cliente inalámbricos que administren perfiles inalámbricos y conexiones a través del servicio configuración inalámbrica cero en Microsoft Windows XP Service Pack 2 (SP2)" en la página ayuda y soporte técnico Knowledge Base en [https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997) .

Debido a las diferencias de arquitectura subyacentes Windows XP, native Wifi API en tiene algunas limitaciones. Esta es una lista de limitaciones:

-   Como máximo, un SSID se puede asociar a un perfil.
-   Las redes de infraestructura siempre aparecen antes que las redes ad hoc en la lista de perfiles.
-   Los nombres de perfil se derivan del SSID y el usuario no puede establecerlo en una cadena arbitraria.
-   No se admiten los tipos PHY.
-   No se admite el almacenamiento en caché de claves maestras en pares (PMK).
-   No se admiten las funciones de extensibilidad del proveedor de hardware independiente (IHV).
-   No se admiten permisos de perfil.
-   Solo están disponibles \_ las notificaciones \_ wlan acm connection complete y \_ wlan notification \_ \_ \_ acm \_ disconnected notification.
-   No se admiten las opciones de configuración global 802.1X y EAPOL.

Las siguientes funciones son compatibles con Windows XP con SP3 e WIRELESS LAN API para Windows XP con SP2:

-   [**DEVOLUCIÓN \_ DE LLAMADA DE NOTIFICACIÓN DE WLAN \_**](/windows/win32/api/wlanapi/nc-wlanapi-wlan_notification_callback)
-   [**WlanAllocateMemory**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanallocatememory)
-   [**WlanCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle)
-   [**WlanConnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect)
-   [**WlanDeleteProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile)
-   [**WlanDisconnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect)
-   [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces)
-   [**WlanFreeMemory**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory)
-   [**WlanGetAvailableNetworkList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist)
-   [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)
-   [**WlanGetProfileList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilelist)
-   [**WlanOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle)
-   [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface)
-   [**WlanReasonCodeToString**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanreasoncodetostring)
-   [**WlanRegisterNotification**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification)
-   [**WlanScan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan)
-   [**WlanSetInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface)
-   [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)
-   [**WlanSetProfileEapXmlUserData**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileeapxmluserdata)
-   [**WlanSetProfileList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist)
-   [**WlanSetProfilePosition**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997)
</dt> <dt>

[Acerca de Wi-Fi nativo](about-native-wifi.md)
</dt> </dl>

 

 
