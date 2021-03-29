---
description: Se admite un subconjunto de la funcionalidad nativa de la API WiFi en Windows XP con Service Pack 2 (SP2) y Windows XP con Service Pack 3 (SP3).
ms.assetid: d32c4a03-59e8-4fdd-9d5a-e7ef0eb25e84
title: Compatibilidad con la API WiFi nativa en Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cd422c6589b37f516b9d45d072489c9d5e00b82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360801"
---
# <a name="native-wifi-api-support-on-windows-xp"></a>Compatibilidad con la API WiFi nativa en Windows XP

Se admite un subconjunto de la funcionalidad nativa de la API WiFi en Windows XP con Service Pack 2 (SP2) y Windows XP con Service Pack 3 (SP3). Esta funcionalidad se incluye de forma predeterminada en Windows XP con SP3. En Windows XP con SP2, esta funcionalidad se puede agregar mediante la aplicación de una revisión, que se conoce como API de LAN inalámbrica para Windows XP con Service Pack 2 (SP2). Para obtener más información o descargar la revisión, consulte "los desarrolladores no pueden crear programas cliente inalámbricos que administren perfiles inalámbricos y conexiones a través del servicio de configuración inalámbrica rápida en Microsoft Windows XP Service Pack 2 (SP2)" en la Knowledge base de ayuda y soporte técnico en [https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997) .

Debido a las diferencias arquitectónicas subyacentes en Windows XP, la API WiFi nativa de tiene algunas limitaciones. Esta es una lista de limitaciones:

-   Como máximo, un SSID puede asociarse a un perfil.
-   Las redes de infraestructura siempre aparecen antes que las redes ad hoc en la lista de perfiles.
-   Los nombres de perfil se derivan del SSID y el usuario no puede establecerlo en una cadena arbitraria.
-   No se admiten los tipos de PHY.
-   No se admite el almacenamiento en caché de clave maestra en pares (PMK).
-   No se admiten las funciones de extensibilidad del proveedor de hardware independiente (IHV).
-   No se admiten los permisos de perfil.
-   Solo \_ se completa la conexión ACM de notificación de WLAN \_ \_ \_ y las \_ notificaciones de WLAN desconectadas de la notificación de WLAN \_ \_ están disponibles.
-   No se admiten las opciones de configuración de 802.1 X y EAPOL globales.

Las siguientes funciones son compatibles con Windows XP con SP3 y la API de LAN inalámbrica para Windows XP con SP2:

-   [**devolución de llamada de \_ notificación de WLAN \_**](/windows/win32/api/wlanapi/nc-wlanapi-wlan_notification_callback)
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

[Acerca de WiFi nativo](about-native-wifi.md)
</dt> </dl>

 

 
