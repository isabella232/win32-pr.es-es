---
description: Muestra el uso de las funciones básicas de administración de redes inalámbricas.
ms.assetid: 63af0b88-c20b-4b06-9db3-e8510fc80053
title: Ejemplo de API WiFi nativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98ac72000363fcb91f013c3f55d4686335c0a59e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687439"
---
# <a name="native-wifi-api-sample"></a>Ejemplo de API WiFi nativa

En el kit de desarrollo de software (SDK) de Microsoft Windows se incluye un ejemplo de API WiFi nativa que muestra el uso de las funciones básicas de administración de redes inalámbricas. La versión más reciente del Windows SDK está disponible en el [centro de descarga](https://developer.microsoft.com/windows/downloads).

De forma predeterminada, el código fuente de ejemplo Wi-Fi nativo se instala en el directorio siguiente:

**C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ <version number> \\ Samples \\ NetDs \\ WLAN**

El ejemplo de la API WiFi nativa se encuentra en la siguiente carpeta:

**configuración automática WLAN**

El ejemplo Wi-Fi nativo se puede compilar y ejecutar en Windows Vista y versiones posteriores, Windows XP con Service Pack 3 (SP3) y la API de LAN inalámbrica para Windows XP con Service Pack 2 (SP2). Algunas características del ejemplo no se admiten en Windows XP con SP3 y la API de LAN inalámbrica para Windows XP con SP2. Para obtener una lista de las funciones compatibles con Windows XP con SP3 y la API de LAN inalámbrica para Windows XP con SP2, consulte compatibilidad con la [API WiFi nativa en Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md).

El ejemplo Native WiFi muestra cómo realizar las tareas siguientes:

-   Enumerar interfaces inalámbricas. Vea [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces).
-   Obtiene las capacidades de una interfaz. Vea [**WlanGetInterfaceCapability**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetinterfacecapability).

    * * Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2: * * no se admite esta característica.

-   Consultar una interfaz. Vea [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface).
-   Establecer los parámetros de una interfaz de red. Vea [**WlanSetInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface). Esta función se puede usar para activar y desactivar la radio inalámbrica (y, por lo tanto, habilitar o deshabilitar la conectividad de red inalámbrica).
-   Busque redes inalámbricas disponibles. Vea [**WlanScan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan).
-   Obtiene la lista de redes inalámbricas disponibles o visibles. Vea [**WlanGetAvailableNetworkList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist).
-   Obtener, guardar o eliminar un perfil. Vea [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile), [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)y [**WlanDeleteProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile).
-   Conectarse o desconectarse de una red inalámbrica. Vea [**WlanConnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect) y [**WlanDisconnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar Wi-Fi nativo](using-native-wifi.md)
</dt> <dt>

[Foro del SDK inalámbrico de Windows Vista](https://social.msdn.microsoft.com/Forums/b6bbd8f0-a921-480f-9b4b-845336462bc0/welcome-to-the-windows-vista-wireless-sdk-forum)
</dt> <dt>

[Solución de problemas de conexiones inalámbricas de Windows Vista 802,11](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10))
</dt> </dl>

 

 
