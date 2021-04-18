---
description: Muestra cómo usar Wi-Fi funciones directas en aplicaciones de escritorio.
ms.assetid: 50B95B7D-B860-44DF-8E78-1E7D2DC5A9B6
title: Usar las funciones directas Wi-Fi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8850f5b278a158e32f78118cf5d0d408c123192e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667134"
---
# <a name="using-the-wi-fi-direct-functions"></a><span data-ttu-id="a1d2e-103">Usar las funciones directas Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="a1d2e-103">Using the Wi-Fi Direct functions</span></span>

<span data-ttu-id="a1d2e-104">En este tema se muestra cómo usar Wi-Fi funciones directas en aplicaciones de escritorio.</span><span class="sxs-lookup"><span data-stu-id="a1d2e-104">This topics shows how to use Wi-Fi Direct functions in desktop apps.</span></span> <span data-ttu-id="a1d2e-105">A partir de Windows 8 y Windows Server 2012, Wi-Fi funciones directas se agregaron a la API WiFi nativa.</span><span class="sxs-lookup"><span data-stu-id="a1d2e-105">Starting on Windows 8 and Windows Server 2012, Wi-Fi Direct functions were added to the Native Wifi API.</span></span>

<span data-ttu-id="a1d2e-106">La característica Wi-Fi Direct se basa en el desarrollo de la Wi-Fi especificación técnica punto a punto v 1.1 de la Alianza de Wi-Fi (consulte las [especificaciones publicadas de Wi-Fi Alliance](https://www.wi-fi.org/)).</span><span class="sxs-lookup"><span data-stu-id="a1d2e-106">The Wi-Fi Direct feature is based on the development of the Wi-Fi Peer-to-Peer Technical Specification v1.1 by the Wi-Fi Alliance (see [Wi-Fi Alliance Published Specifications](https://www.wi-fi.org/)).</span></span> <span data-ttu-id="a1d2e-107">El objetivo del Wi-Fi especificación técnica punto a punto es proporcionar una solución para Wi-Fi la conectividad de dispositivo a dispositivo sin necesidad de que un punto de acceso inalámbrico (AP inalámbrico) Configure la conexión o el uso del mecanismo Wi-Fi ad hoc (IBSS) existente.</span><span class="sxs-lookup"><span data-stu-id="a1d2e-107">The goal of the Wi-Fi Peer-to-Peer Technical Specification is to provide a solution for Wi-Fi device-to-device connectivity without the need for either a Wireless Access Point (wireless AP) to setup the connection or the use of the existing Wi-Fi ad hoc (IBSS) mechanism.</span></span>

> [!Note]  
> <span data-ttu-id="a1d2e-108">El modo ad hoc podría no estar disponible en versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="a1d2e-108">Ad hoc mode might not be available in future versions of Windows.</span></span> <span data-ttu-id="a1d2e-109">A partir de Windows 8.1 y Windows Server 2012 R2, utilice Wi-Fi Direct en su lugar.</span><span class="sxs-lookup"><span data-stu-id="a1d2e-109">Starting with Windows 8.1 and Windows Server 2012 R2, use Wi-Fi Direct instead.</span></span>

 

<span data-ttu-id="a1d2e-110">Las funciones siguientes admiten la característica Wi-Fi Direct.</span><span class="sxs-lookup"><span data-stu-id="a1d2e-110">The following functions support the Wi-Fi Direct feature.</span></span>

-   <span data-ttu-id="a1d2e-111">[**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) : indica que la aplicación desea cancelar una función de [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) pendiente que no se ha completado.</span><span class="sxs-lookup"><span data-stu-id="a1d2e-111">[**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) - Indicates that the app wants to cancel a pending [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function that has not completed.</span></span>
-   <span data-ttu-id="a1d2e-112">[**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) : cierra un identificador para el servicio Wi-Fi Direct.</span><span class="sxs-lookup"><span data-stu-id="a1d2e-112">[**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) - Closes a handle to the Wi-Fi Direct service.</span></span>
-   <span data-ttu-id="a1d2e-113">[**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) : cierra una sesión después de una llamada correcta previamente a la función [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) .</span><span class="sxs-lookup"><span data-stu-id="a1d2e-113">[**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) - Closes a session after a previously successful call to the [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function.</span></span>
-   <span data-ttu-id="a1d2e-114">[**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) : abre un identificador para el servicio Wi-Fi Direct y negocia una versión de la API de Wi-Fi Direct que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="a1d2e-114">[**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) - Opens a handle to the Wi-Fi Direct service and negotiates a version of the Wi-FI Direct API to use.</span></span>
-   <span data-ttu-id="a1d2e-115">[**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) : recupera y aplica un perfil almacenado para un Wi-Fi dispositivo heredado directo.</span><span class="sxs-lookup"><span data-stu-id="a1d2e-115">[**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) - Retrieves and applies a stored profile for a Wi-Fi Direct legacy device.</span></span>
-   <span data-ttu-id="a1d2e-116">[**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) : inicia una conexión a petición a un dispositivo Wi-Fi Direct específico, que se ha emparejado previamente a través de la experiencia de emparejamiento de Windows.</span><span class="sxs-lookup"><span data-stu-id="a1d2e-116">[**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) - Starts an on-demand connection to a specific Wi-Fi Direct device, which has been previously paired through the Windows Pairing experience.</span></span>
-   <span data-ttu-id="a1d2e-117">[**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) : actualiza la visibilidad del dispositivo para la dirección de dispositivo Wi-Fi Direct para un nodo de dispositivo directo de Wi-Fi directo instalado.</span><span class="sxs-lookup"><span data-stu-id="a1d2e-117">[**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) - Updates device visibility for the Wi-Fi Direct device address for a given installed Wi-Fi Direct device node.</span></span>
-   <span data-ttu-id="a1d2e-118">[**WFD \_ \_Devolución de \_ \_ llamada completa de la sesión abierta**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) : define la función de devolución de llamada a la que llama la función [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) cuando se completa la operación **WFDStartOpenSession**</span><span class="sxs-lookup"><span data-stu-id="a1d2e-118">[**WFD\_OPEN\_SESSION\_COMPLETE\_CALLBACK**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) - Defines the callback function that is called by the [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function when the **WFDStartOpenSession** operation completes</span></span>

<span data-ttu-id="a1d2e-119">En el caso de una aplicación de escritorio, la característica Wi-Fi Direct requiere que los dispositivos Wi-FI Direct estén emparejados previamente por el usuario con la interfaz de usuario de la experiencia de emparejamiento de Windows.</span><span class="sxs-lookup"><span data-stu-id="a1d2e-119">For a desktop app, the Wi-Fi Direct feature requires that Wi-FI Direct devices be previously paired by the user with the Windows Pairing experience user interface.</span></span> <span data-ttu-id="a1d2e-120">Una vez completado este emparejamiento, se almacena un perfil que permite usar las funciones de Wi-Fi directo para iniciar una sesión Wi-Fi Direct para establecer una conexión entre el Wi-Fi dispositivos directos.</span><span class="sxs-lookup"><span data-stu-id="a1d2e-120">Once this pairing is completed, a profile is stored that allows the Wi-Fi Direct functions to be used to start a Wi-Fi Direct session to establish a connection between the Wi-Fi Direct devices.</span></span>

<span data-ttu-id="a1d2e-121">Para usar Wi-Fi Direct, una aplicación primero debe obtener un identificador para el servicio Wi-Fi Direct llamando a la función [**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) .</span><span class="sxs-lookup"><span data-stu-id="a1d2e-121">In order to use Wi-Fi Direct, an app must first obtain a handle to the Wi-Fi Direct service by calling the [**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) function.</span></span> <span data-ttu-id="a1d2e-122">El identificador Wi-Fi directo (WFD) devuelto por la función **WFDOpenHandle** se utiliza para las llamadas a funciones Wi-Fi directas posteriores realizadas a la Wi-Fi servicio directo.</span><span class="sxs-lookup"><span data-stu-id="a1d2e-122">The Wi-Fi Direct (WFD) handle returned by the **WFDOpenHandle** function is used for subsequent Wi-Fi Direct function calls made to the Wi-Fi Direct service.</span></span>

<span data-ttu-id="a1d2e-123">La función [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) inicia una operación asincrónica para iniciar una conexión a petición a un dispositivo Wi-Fi Direct específico.</span><span class="sxs-lookup"><span data-stu-id="a1d2e-123">The [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function starts an asynchronous operation to start an on-demand connection to a specific Wi-Fi Direct device.</span></span> <span data-ttu-id="a1d2e-124">El dispositivo Wi-Fi de destino debe haberse emparejado anteriormente a través de la experiencia de emparejamiento de Windows.</span><span class="sxs-lookup"><span data-stu-id="a1d2e-124">The target Wi-Fi device must previously have been paired through the Windows Pairing experience.</span></span> <span data-ttu-id="a1d2e-125">Cuando se completa la operación asincrónica, se llama a la función de devolución de llamada especificada en el parámetro *pfnCallback* .</span><span class="sxs-lookup"><span data-stu-id="a1d2e-125">When the asynchronous operation completes, the callback function specified in the *pfnCallback* parameter is called.</span></span>

<span data-ttu-id="a1d2e-126">Una vez que se realiza una aplicación mediante el servicio de Wi-Fi Direct, la aplicación debe llamar a la función [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) para indicar al Wi-Fi servicio directo que la aplicación se realiza mediante el servicio.</span><span class="sxs-lookup"><span data-stu-id="a1d2e-126">Once an application is done using the Wi-Fi Direct service, the application should call the [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) function to signal to the Wi-Fi Direct service that the application is done using the service.</span></span> <span data-ttu-id="a1d2e-127">Esto permite al Wi-Fi servicio directo liberar los recursos utilizados por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a1d2e-127">This allows the Wi-Fi Direct service to release resources used by the application.</span></span>

<span data-ttu-id="a1d2e-128">Para obtener más información sobre Wi-Fi directo para su uso en aplicaciones de la tienda Windows, consulte [**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) y las clases relacionadas en el espacio de nombres [**Windows. networking. Proximity**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="a1d2e-128">For more information on Wi-Fi Direct for use in Windows Store apps, see [**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) and related classes in the [**Windows.Networking.Proximity**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) namespace.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1d2e-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a1d2e-129">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a1d2e-130">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="a1d2e-130">**Other resources**</span></span>
</dt> <dt>

[<span data-ttu-id="a1d2e-131">Acerca de WiFi nativo</span><span class="sxs-lookup"><span data-stu-id="a1d2e-131">About Native Wifi</span></span>](about-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="a1d2e-132">Acerca de la API nativa WiFi</span><span class="sxs-lookup"><span data-stu-id="a1d2e-132">About the Native Wifi API</span></span>](about-the-native-wifi-api.md)
</dt> <dt>

[<span data-ttu-id="a1d2e-133">Acerca de la característica Wi-Fi Direct</span><span class="sxs-lookup"><span data-stu-id="a1d2e-133">About the Wi-Fi Direct feature</span></span>](about-the-wi-fi-direct-api.md)
</dt> <dt>

<span data-ttu-id="a1d2e-134">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="a1d2e-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a1d2e-135">**PeerFinder**</span><span class="sxs-lookup"><span data-stu-id="a1d2e-135">**PeerFinder**</span></span>](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041)
</dt> <dt>

[<span data-ttu-id="a1d2e-136">**\_devolución de \_ \_ llamada completa de sesión abierta de WFD \_**</span><span class="sxs-lookup"><span data-stu-id="a1d2e-136">**WFD\_OPEN\_SESSION\_COMPLETE\_CALLBACK**</span></span>](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
</dt> <dt>

[<span data-ttu-id="a1d2e-137">**WFDCancelOpenSession**</span><span class="sxs-lookup"><span data-stu-id="a1d2e-137">**WFDCancelOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
</dt> <dt>

[<span data-ttu-id="a1d2e-138">**WFDCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="a1d2e-138">**WFDCloseHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
</dt> <dt>

[<span data-ttu-id="a1d2e-139">**WFDCloseSession**</span><span class="sxs-lookup"><span data-stu-id="a1d2e-139">**WFDCloseSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
</dt> <dt>

[<span data-ttu-id="a1d2e-140">**WFDOpenHandle**</span><span class="sxs-lookup"><span data-stu-id="a1d2e-140">**WFDOpenHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
</dt> <dt>

[<span data-ttu-id="a1d2e-141">**WFDOpenLegacySession**</span><span class="sxs-lookup"><span data-stu-id="a1d2e-141">**WFDOpenLegacySession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
</dt> <dt>

[<span data-ttu-id="a1d2e-142">**WFDStartOpenSession**</span><span class="sxs-lookup"><span data-stu-id="a1d2e-142">**WFDStartOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
</dt> <dt>

[<span data-ttu-id="a1d2e-143">**WFDUpdateDeviceVisibility**</span><span class="sxs-lookup"><span data-stu-id="a1d2e-143">**WFDUpdateDeviceVisibility**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)
</dt> <dt>

[<span data-ttu-id="a1d2e-144">**Windows.Networking.Proximity**</span><span class="sxs-lookup"><span data-stu-id="a1d2e-144">**Windows.Networking.Proximity**</span></span>](/uwp/api/Windows.Networking.Proximity?view=winrt-19041)
</dt> </dl>

 

 
