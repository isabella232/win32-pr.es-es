---
description: Muestra el uso de funciones básicas de administración de redes inalámbricas.
ms.assetid: 63af0b88-c20b-4b06-9db3-e8510fc80053
title: Ejemplo de API Wifi nativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ed28fadcd73eb4b3e632702078280ddba55d683c66decfdf03bc948182c52d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801065"
---
# <a name="native-wifi-api-sample"></a>Ejemplo de API Wifi nativa

Se incluye un ejemplo de API Wi-Fi nativa que muestra el uso de funciones básicas de administración de redes inalámbricas con el Kit de desarrollo de software (SDK) de Microsoft Windows. La versión más reciente del SDK Windows está disponible en el [Centro de descarga.](https://developer.microsoft.com/windows/downloads)

De forma predeterminada, el código fuente de ejemplo de Wi-Fi nativo se instala en el directorio siguiente:

**C: \\ Archivos de programa Sdk de Microsoft Windows \\ \\ \\ <version number> \\ \\ netDs \\ Wlan**

El ejemplo de API Wi-Fi nativa se encuentra en la carpeta siguiente:

**Autoconfig**

El ejemplo de Wi-Fi nativo se puede compilar y ejecutar en Windows Vista y versiones posteriores, Windows XP con Service Pack 3 (SP3) y wireless LAN API para Windows XP con Service Pack 2 (SP2). Algunas características del ejemplo no se admiten en Windows XP con SP3 e WIRELESS LAN API para Windows XP con SP2. Para obtener una lista de las funciones compatibles con Windows XP con SP3 y la API de LAN inalámbrica para Windows XP con SP2, consulte Compatibilidad con la API De Wi-Fi nativa [en Windows XP.](about-wireless-lan-api-for-windows-xp-service-pack-2.md)

En el ejemplo de Wi-Fi nativo se muestra cómo realizar las siguientes tareas:

-   Enumerar interfaces inalámbricas. Vea [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces).
-   Obtenga las funcionalidades de una interfaz. Vea [**WlanGetInterfaceCapability**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetinterfacecapability).

    **Windows XP con SP3 e WIRELESS LAN API para Windows XP con SP2: ** Esta característica no se admite.

-   Consultar una interfaz. Vea [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface).
-   Establecer parámetros para una interfaz de red. Vea [**WlanSetInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface). Esta función se puede usar para activar y desactivar la radio inalámbrica (y, por tanto, habilitar o deshabilitar la conectividad de red inalámbrica).
-   Busque redes inalámbricas disponibles. Vea [**WlanScan.**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan)
-   Obtenga la lista de redes inalámbricas disponibles o visibles. Vea [**WlanGetAvailableNetworkList.**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist)
-   Obtener, guardar o eliminar un perfil. Vea [**WlanGetProfile,**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile) [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)y [**WlanDeleteProfile.**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile)
-   Conectar a una red inalámbrica o desconéctese de esta. Consulte [**WlanConnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect) y [**WlanDisconnect.**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de Wi-Fi nativo](using-native-wifi.md)
</dt> <dt>

[Windows Foro del SDK inalámbrico de Vista](https://social.msdn.microsoft.com/Forums/b6bbd8f0-a921-480f-9b4b-845336462bc0/welcome-to-the-windows-vista-wireless-sdk-forum)
</dt> <dt>

[Solución de Windows conexiones inalámbricas de Vista 802.11](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10))
</dt> </dl>

 

 
