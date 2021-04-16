---
description: La API WiFi nativa contiene un conjunto de funciones que admiten el uso de Wi-Fi directo para aplicaciones de escritorio.
ms.assetid: A649EBBA-1076-4426-9C4D-85AB8C415C66
title: Acerca de la característica Wi-Fi Direct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e503cb2bf86f81904b1c85c2bdf96b66c0762e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678394"
---
# <a name="about-the-wi-fi-direct-feature"></a><span data-ttu-id="d9e0d-103">Acerca de la característica Wi-Fi Direct</span><span class="sxs-lookup"><span data-stu-id="d9e0d-103">About the Wi-Fi Direct feature</span></span>

<span data-ttu-id="d9e0d-104">La API WiFi nativa contiene un conjunto de funciones que admiten el uso de Wi-Fi directo para aplicaciones de escritorio.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-104">The Native Wifi API contains a set of functions that support the use of Wi-Fi Direct for desktop apps.</span></span> <span data-ttu-id="d9e0d-105">A partir de Windows 8 y Windows Server 2012, Wi-Fi funciones directas se agregaron a la API WiFi nativa.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-105">Starting on Windows 8 and Windows Server 2012, Wi-Fi Direct functions were added to the Native Wifi API.</span></span>

<span data-ttu-id="d9e0d-106">La característica Wi-Fi Direct se basa en el desarrollo de la Wi-Fi especificación técnica punto a punto v 1.1 de la Alianza de Wi-Fi (consulte las [especificaciones publicadas de Wi-Fi Alliance](https://www.wi-fi.org/)).</span><span class="sxs-lookup"><span data-stu-id="d9e0d-106">The Wi-Fi Direct feature is based on the development of the Wi-Fi Peer-to-Peer Technical Specification v1.1 by the Wi-Fi Alliance (see [Wi-Fi Alliance Published Specifications](https://www.wi-fi.org/)).</span></span> <span data-ttu-id="d9e0d-107">El objetivo del Wi-Fi especificación técnica punto a punto es proporcionar una solución para Wi-Fi la conectividad de dispositivo a dispositivo sin necesidad de que un punto de acceso inalámbrico (AP inalámbrico) Configure la conexión o el uso del mecanismo Wi-Fi ad hoc (IBSS) existente.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-107">The goal of the Wi-Fi Peer-to-Peer Technical Specification is to provide a solution for Wi-Fi device-to-device connectivity without the need for either a Wireless Access Point (wireless AP) to setup the connection or the use of the existing Wi-Fi ad hoc (IBSS) mechanism.</span></span>

> [!Note]  
> <span data-ttu-id="d9e0d-108">El modo ad hoc podría no estar disponible en versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-108">Ad hoc mode might not be available in future versions of Windows.</span></span> <span data-ttu-id="d9e0d-109">A partir de Windows 8.1 y Windows Server 2012 R2, utilice Wi-Fi Direct en su lugar.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-109">Starting with Windows 8.1 and Windows Server 2012 R2, use Wi-Fi Direct instead.</span></span>

 

<span data-ttu-id="d9e0d-110">En el caso de una aplicación de escritorio, la característica Wi-Fi Direct requiere que los dispositivos Wi-FI Direct estén emparejados previamente por el usuario con la interfaz de usuario de la experiencia de emparejamiento de Windows.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-110">For a desktop app, the Wi-Fi Direct feature requires that Wi-FI Direct devices be previously paired by the user with the Windows Pairing experience user interface.</span></span> <span data-ttu-id="d9e0d-111">Una vez completado este emparejamiento, se almacena un perfil que permite usar las funciones de Wi-Fi directo para iniciar una sesión Wi-Fi Direct para establecer una conexión entre el Wi-Fi dispositivos directos.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-111">Once this pairing is completed, a profile is stored that allows the Wi-Fi Direct functions to be used to start a Wi-Fi Direct session to establish a connection between the Wi-Fi Direct devices.</span></span>

<span data-ttu-id="d9e0d-112">Las funciones siguientes admiten la característica Wi-Fi Direct.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-112">The following functions support the Wi-Fi Direct feature.</span></span>

-   <span data-ttu-id="d9e0d-113">[**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) : indica que la aplicación desea cancelar una función de [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) pendiente que no se ha completado.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-113">[**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) - Indicates that the app wants to cancel a pending [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function that has not completed.</span></span>
-   <span data-ttu-id="d9e0d-114">[**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) : cierra un identificador para el servicio Wi-Fi Direct.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-114">[**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) - Closes a handle to the Wi-Fi Direct service.</span></span>
-   <span data-ttu-id="d9e0d-115">[**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) : cierra una sesión después de una llamada correcta previamente a la función [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) .</span><span class="sxs-lookup"><span data-stu-id="d9e0d-115">[**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) - Closes a session after a previously successful call to the [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function.</span></span>
-   <span data-ttu-id="d9e0d-116">[**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) : abre un identificador para el servicio Wi-Fi Direct y negocia una versión de la API de Wi-Fi Direct que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-116">[**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) - Opens a handle to the Wi-Fi Direct service and negotiates a version of the Wi-FI Direct API to use.</span></span>
-   <span data-ttu-id="d9e0d-117">[**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) : recupera y aplica un perfil almacenado para un Wi-Fi dispositivo heredado directo.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-117">[**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) - Retrieves and applies a stored profile for a Wi-Fi Direct legacy device.</span></span>
-   <span data-ttu-id="d9e0d-118">[**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) : inicia una conexión a petición a un dispositivo Wi-Fi Direct específico, que se ha emparejado previamente a través de la experiencia de emparejamiento de Windows.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-118">[**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) - Starts an on-demand connection to a specific Wi-Fi Direct device, which has been previously paired through the Windows Pairing experience.</span></span>
-   <span data-ttu-id="d9e0d-119">[**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) : actualiza la visibilidad del dispositivo para la dirección de dispositivo Wi-Fi Direct para un nodo de dispositivo directo de Wi-Fi directo instalado.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-119">[**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) - Updates device visibility for the Wi-Fi Direct device address for a given installed Wi-Fi Direct device node.</span></span>
-   <span data-ttu-id="d9e0d-120">[**WFD \_ \_Devolución de \_ \_ llamada completa de la sesión abierta**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) : define la función de devolución de llamada a la que llama la función [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) cuando se completa la operación **WFDStartOpenSession**</span><span class="sxs-lookup"><span data-stu-id="d9e0d-120">[**WFD\_OPEN\_SESSION\_COMPLETE\_CALLBACK**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) - Defines the callback function that is called by the [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function when the **WFDStartOpenSession** operation completes</span></span>

<span data-ttu-id="d9e0d-121">Para obtener más información sobre el uso de Wi-Fi directo en una aplicación de escritorio, consulte [uso de las funciones de Wi-Fi directo](using-the-wi-fi-direct-api.md).</span><span class="sxs-lookup"><span data-stu-id="d9e0d-121">For more information on using Wi-Fi Direct in a desktop app, see [Using the Wi-Fi Direct functions](using-the-wi-fi-direct-api.md).</span></span>

<span data-ttu-id="d9e0d-122">Para obtener más información sobre Wi-Fi directo para su uso en aplicaciones de la tienda Windows, consulte [**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) y las clases relacionadas en el espacio de nombres [**Windows. networking. Proximity**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="d9e0d-122">For more information on Wi-Fi Direct for use in Windows Store apps, see [**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) and related classes in the [**Windows.Networking.Proximity**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) namespace.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9e0d-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d9e0d-123">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d9e0d-124">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="d9e0d-124">**Other resources**</span></span>
</dt> <dt>

[<span data-ttu-id="d9e0d-125">Acerca de WiFi nativo</span><span class="sxs-lookup"><span data-stu-id="d9e0d-125">About Native Wifi</span></span>](about-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="d9e0d-126">Acerca de la API nativa WiFi</span><span class="sxs-lookup"><span data-stu-id="d9e0d-126">About the Native Wifi API</span></span>](about-the-native-wifi-api.md)
</dt> <dt>

[<span data-ttu-id="d9e0d-127">Acerca de la API ad hoc inalámbrica</span><span class="sxs-lookup"><span data-stu-id="d9e0d-127">About the Wireless Ad Hoc API</span></span>](about-the-wireless-ad-hoc-api.md)
</dt> <dt>

[<span data-ttu-id="d9e0d-128">Usar las funciones directas Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="d9e0d-128">Using the Wi-Fi Direct functions</span></span>](using-the-wi-fi-direct-api.md)
</dt> <dt>

<span data-ttu-id="d9e0d-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="d9e0d-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d9e0d-130">**PeerFinder**</span><span class="sxs-lookup"><span data-stu-id="d9e0d-130">**PeerFinder**</span></span>](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041)
</dt> <dt>

[<span data-ttu-id="d9e0d-131">**\_devolución de \_ \_ llamada completa de sesión abierta de WFD \_**</span><span class="sxs-lookup"><span data-stu-id="d9e0d-131">**WFD\_OPEN\_SESSION\_COMPLETE\_CALLBACK**</span></span>](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
</dt> <dt>

[<span data-ttu-id="d9e0d-132">**WFDCancelOpenSession**</span><span class="sxs-lookup"><span data-stu-id="d9e0d-132">**WFDCancelOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
</dt> <dt>

[<span data-ttu-id="d9e0d-133">**WFDCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="d9e0d-133">**WFDCloseHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
</dt> <dt>

[<span data-ttu-id="d9e0d-134">**WFDCloseSession**</span><span class="sxs-lookup"><span data-stu-id="d9e0d-134">**WFDCloseSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
</dt> <dt>

[<span data-ttu-id="d9e0d-135">**WFDOpenHandle**</span><span class="sxs-lookup"><span data-stu-id="d9e0d-135">**WFDOpenHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
</dt> <dt>

[<span data-ttu-id="d9e0d-136">**WFDOpenLegacySession**</span><span class="sxs-lookup"><span data-stu-id="d9e0d-136">**WFDOpenLegacySession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
</dt> <dt>

[<span data-ttu-id="d9e0d-137">**WFDStartOpenSession**</span><span class="sxs-lookup"><span data-stu-id="d9e0d-137">**WFDStartOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
</dt> <dt>

[<span data-ttu-id="d9e0d-138">**WFDUpdateDeviceVisibility**</span><span class="sxs-lookup"><span data-stu-id="d9e0d-138">**WFDUpdateDeviceVisibility**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)
</dt> <dt>

[<span data-ttu-id="d9e0d-139">**Windows.Networking.Proximity**</span><span class="sxs-lookup"><span data-stu-id="d9e0d-139">**Windows.Networking.Proximity**</span></span>](/uwp/api/Windows.Networking.Proximity?view=winrt-19041)
</dt> </dl>

 

 
