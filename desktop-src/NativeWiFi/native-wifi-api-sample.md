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
# <a name="native-wifi-api-sample"></a><span data-ttu-id="e080f-103">Ejemplo de API WiFi nativa</span><span class="sxs-lookup"><span data-stu-id="e080f-103">Native Wifi API Sample</span></span>

<span data-ttu-id="e080f-104">En el kit de desarrollo de software (SDK) de Microsoft Windows se incluye un ejemplo de API WiFi nativa que muestra el uso de las funciones básicas de administración de redes inalámbricas.</span><span class="sxs-lookup"><span data-stu-id="e080f-104">A Native Wifi API sample that demonstrates the use of basic wireless network management functions is included with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e080f-105">La versión más reciente del Windows SDK está disponible en el [centro de descarga](https://developer.microsoft.com/windows/downloads).</span><span class="sxs-lookup"><span data-stu-id="e080f-105">The latest version of the Windows SDK is available from the [Download Center](https://developer.microsoft.com/windows/downloads).</span></span>

<span data-ttu-id="e080f-106">De forma predeterminada, el código fuente de ejemplo Wi-Fi nativo se instala en el directorio siguiente:</span><span class="sxs-lookup"><span data-stu-id="e080f-106">By default, the Native Wifi sample source code is installed in the following directory:</span></span>

<span data-ttu-id="e080f-107">**C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ <version number> \\ Samples \\ NetDs \\ WLAN**</span><span class="sxs-lookup"><span data-stu-id="e080f-107">**C:\\Program Files\\Microsoft SDKs\\Windows\\<version number>\\Samples\\NetDs\\Wlan**</span></span>

<span data-ttu-id="e080f-108">El ejemplo de la API WiFi nativa se encuentra en la siguiente carpeta:</span><span class="sxs-lookup"><span data-stu-id="e080f-108">The Native Wifi API sample is located under the following folder:</span></span>

<span data-ttu-id="e080f-109">**configuración automática WLAN**</span><span class="sxs-lookup"><span data-stu-id="e080f-109">**autoconfig**</span></span>

<span data-ttu-id="e080f-110">El ejemplo Wi-Fi nativo se puede compilar y ejecutar en Windows Vista y versiones posteriores, Windows XP con Service Pack 3 (SP3) y la API de LAN inalámbrica para Windows XP con Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="e080f-110">The Native Wifi sample can be compiled and run on Windows Vista and later, Windows XP with Service Pack 3 (SP3), and Wireless LAN API for Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="e080f-111">Algunas características del ejemplo no se admiten en Windows XP con SP3 y la API de LAN inalámbrica para Windows XP con SP2.</span><span class="sxs-lookup"><span data-stu-id="e080f-111">Some features of the sample are not supported on Windows XP with SP3 and Wireless LAN API for Windows XP with SP2.</span></span> <span data-ttu-id="e080f-112">Para obtener una lista de las funciones compatibles con Windows XP con SP3 y la API de LAN inalámbrica para Windows XP con SP2, consulte compatibilidad con la [API WiFi nativa en Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md).</span><span class="sxs-lookup"><span data-stu-id="e080f-112">For a list of functions supported by Windows XP with SP3 and Wireless LAN API for Windows XP with SP2, see [Native Wifi API Support on Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md).</span></span>

<span data-ttu-id="e080f-113">El ejemplo Native WiFi muestra cómo realizar las tareas siguientes:</span><span class="sxs-lookup"><span data-stu-id="e080f-113">The Native Wifi sample demonstrates how to perform the following tasks:</span></span>

-   <span data-ttu-id="e080f-114">Enumerar interfaces inalámbricas.</span><span class="sxs-lookup"><span data-stu-id="e080f-114">Enumerate wireless interfaces.</span></span> <span data-ttu-id="e080f-115">Vea [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces).</span><span class="sxs-lookup"><span data-stu-id="e080f-115">See [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces).</span></span>
-   <span data-ttu-id="e080f-116">Obtiene las capacidades de una interfaz.</span><span class="sxs-lookup"><span data-stu-id="e080f-116">Get the capabilities of an interface.</span></span> <span data-ttu-id="e080f-117">Vea [**WlanGetInterfaceCapability**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetinterfacecapability).</span><span class="sxs-lookup"><span data-stu-id="e080f-117">See [**WlanGetInterfaceCapability**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetinterfacecapability).</span></span>

    <span data-ttu-id="e080f-118">\* \* Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2: \* \* no se admite esta característica.</span><span class="sxs-lookup"><span data-stu-id="e080f-118">\*\*Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  \*\* This feature is not supported.</span></span>

-   <span data-ttu-id="e080f-119">Consultar una interfaz.</span><span class="sxs-lookup"><span data-stu-id="e080f-119">Query an interface.</span></span> <span data-ttu-id="e080f-120">Vea [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface).</span><span class="sxs-lookup"><span data-stu-id="e080f-120">See [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface).</span></span>
-   <span data-ttu-id="e080f-121">Establecer los parámetros de una interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="e080f-121">Set parameters for a network interface.</span></span> <span data-ttu-id="e080f-122">Vea [**WlanSetInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface).</span><span class="sxs-lookup"><span data-stu-id="e080f-122">See [**WlanSetInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface).</span></span> <span data-ttu-id="e080f-123">Esta función se puede usar para activar y desactivar la radio inalámbrica (y, por lo tanto, habilitar o deshabilitar la conectividad de red inalámbrica).</span><span class="sxs-lookup"><span data-stu-id="e080f-123">This function can be used to turn the wireless radio on and off (and therefore enable or disable wireless network connectivity).</span></span>
-   <span data-ttu-id="e080f-124">Busque redes inalámbricas disponibles.</span><span class="sxs-lookup"><span data-stu-id="e080f-124">Scan for available wireless networks.</span></span> <span data-ttu-id="e080f-125">Vea [**WlanScan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan).</span><span class="sxs-lookup"><span data-stu-id="e080f-125">See [**WlanScan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan).</span></span>
-   <span data-ttu-id="e080f-126">Obtiene la lista de redes inalámbricas disponibles o visibles.</span><span class="sxs-lookup"><span data-stu-id="e080f-126">Get the list of available or visible wireless networks.</span></span> <span data-ttu-id="e080f-127">Vea [**WlanGetAvailableNetworkList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist).</span><span class="sxs-lookup"><span data-stu-id="e080f-127">See [**WlanGetAvailableNetworkList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist).</span></span>
-   <span data-ttu-id="e080f-128">Obtener, guardar o eliminar un perfil.</span><span class="sxs-lookup"><span data-stu-id="e080f-128">Get, save, or delete a profile.</span></span> <span data-ttu-id="e080f-129">Vea [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile), [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)y [**WlanDeleteProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile).</span><span class="sxs-lookup"><span data-stu-id="e080f-129">See [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile), [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile), and [**WlanDeleteProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile).</span></span>
-   <span data-ttu-id="e080f-130">Conectarse o desconectarse de una red inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="e080f-130">Connect to or disconnect from a wireless network.</span></span> <span data-ttu-id="e080f-131">Vea [**WlanConnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect) y [**WlanDisconnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect).</span><span class="sxs-lookup"><span data-stu-id="e080f-131">See [**WlanConnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect) and [**WlanDisconnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e080f-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e080f-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e080f-133">Usar Wi-Fi nativo</span><span class="sxs-lookup"><span data-stu-id="e080f-133">Using Native Wifi</span></span>](using-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="e080f-134">Foro del SDK inalámbrico de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e080f-134">Windows Vista Wireless SDK Forum</span></span>](https://social.msdn.microsoft.com/Forums/b6bbd8f0-a921-480f-9b4b-845336462bc0/welcome-to-the-windows-vista-wireless-sdk-forum)
</dt> <dt>

<span data-ttu-id="e080f-135">[Solución de problemas de conexiones inalámbricas de Windows Vista 802,11](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="e080f-135">[Troubleshooting Windows Vista 802.11 Wireless Connections](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10))</span></span>
</dt> </dl>

 

 
