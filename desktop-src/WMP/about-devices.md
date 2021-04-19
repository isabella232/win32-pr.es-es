---
title: Acerca de los dispositivos
description: Acerca de los dispositivos
ms.assetid: 9e68c5eb-5fcb-4d7d-8dbb-7e951f253df8
keywords:
- Windows Media Player, sincronizar dispositivos
- Modelo de objetos de Windows Media Player, sincronizar dispositivos
- modelo de objetos, sincronizar dispositivos
- Control ActiveX de Windows Media Player, sincronizar dispositivos
- Control ActiveX, sincronizar dispositivos
- Control ActiveX móvil de Windows Media Player, sincronizar dispositivos
- Windows Media Player Mobile, sincronizar dispositivos
- sincronizar dispositivos, acerca de
- sincronización de dispositivos, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e89a074e4edb5bdbc7d90391398d5e0e4133505a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105695526"
---
# <a name="about-devices"></a><span data-ttu-id="dd1c4-112">Acerca de los dispositivos</span><span class="sxs-lookup"><span data-stu-id="dd1c4-112">About Devices</span></span>

<span data-ttu-id="dd1c4-113">Los dispositivos portátiles son dispositivos de hardware que los usuarios llevan para disfrutar del contenido multimedia digital cuando están fuera de su equipo.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-113">Portable devices are hardware devices that users carry to enjoy digital media content when they are away from their computer.</span></span> <span data-ttu-id="dd1c4-114">Normalmente, los dispositivos portátiles funcionan con baterías.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-114">Typically, portable devices are battery operated.</span></span> <span data-ttu-id="dd1c4-115">Algunos dispositivos solo pueden reproducir música.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-115">Some devices can play music only.</span></span> <span data-ttu-id="dd1c4-116">Otros dispositivos pueden reproducir vídeo y música.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-116">Other devices can play video and music.</span></span>

<span data-ttu-id="dd1c4-117">Algunos dispositivos admiten la sincronización automática de contenido multimedia digital con Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-117">Some devices support automatic synchronization of digital media content with Windows Media Player.</span></span> <span data-ttu-id="dd1c4-118">Otros dispositivos solo admiten la transferencia manual.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-118">Other devices support only manual transfer.</span></span> <span data-ttu-id="dd1c4-119">Para determinar si un dispositivo determinado admite la sincronización automática, llame a [IWMPSyncDevice:: get \_ status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) y, a continuación, inspeccione el valor de [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) recuperado.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-119">You can determine whether a particular device supports automatic synchronization by calling [IWMPSyncDevice::get\_status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) and then inspecting the [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) value retrieved.</span></span> <span data-ttu-id="dd1c4-120">Si el valor recuperado es **wmpdsManualDevice**, el dispositivo no admite la sincronización automática.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-120">If the retrieved value is **wmpdsManualDevice**, the device does not support automatic synchronization.</span></span>

<span data-ttu-id="dd1c4-121">Puede enumerar los dispositivos conectados al equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-121">You can enumerate the devices connected to the user's computer.</span></span> <span data-ttu-id="dd1c4-122">Para ello, use primero [IWMPSyncServices:: get \_ deviceCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-get_devicecount) para recuperar el recuento de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-122">To do this, first use [IWMPSyncServices::get\_deviceCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-get_devicecount) to retrieve the count of devices.</span></span> <span data-ttu-id="dd1c4-123">A continuación, en un bucle, llame a [IWMPSyncServices:: getDevice](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-getdevice), pasando el valor de índice adecuado cada vez.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-123">Then, in a loop, call [IWMPSyncServices::getDevice](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-getdevice), passing the appropriate index value each time.</span></span> <span data-ttu-id="dd1c4-124">Puede usar [IWMPSyncDevice:: get \_ Connected](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected) para evaluar si un dispositivo determinado está conectado actualmente.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-124">You can use [IWMPSyncDevice::get\_connected](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected) to evaluate whether a particular device is currently connected.</span></span>

<span data-ttu-id="dd1c4-125">Para saber cuándo se conectan o desconectan los dispositivos, puede recibir los eventos **DeviceConnect** y **DeviceDisconnect** .</span><span class="sxs-lookup"><span data-stu-id="dd1c4-125">To know when devices connect or disconnect, you can receive the **DeviceConnect** and **DeviceDisconnect** events.</span></span> <span data-ttu-id="dd1c4-126">Estos eventos se reciben a través de la interfaz **IWMPEvents2** .</span><span class="sxs-lookup"><span data-stu-id="dd1c4-126">These events are received through the **IWMPEvents2** interface.</span></span>

<span data-ttu-id="dd1c4-127">La interfaz **IWMPSyncDevice** proporciona métodos adicionales que permiten obtener o establecer información sobre un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-127">The **IWMPSyncDevice** interface provides additional methods to enable you to get or set information about a device.</span></span> <span data-ttu-id="dd1c4-128">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="dd1c4-128">For example:</span></span>

-   <span data-ttu-id="dd1c4-129">Los métodos **Get \_ FriendlyName** y **Put \_ FriendlyName** permiten recuperar y especificar el nombre del dispositivo definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-129">The **get\_FriendlyName** and **put\_FriendlyName** methods enable you to retrieve and specify the user-defined device name.</span></span>
-   <span data-ttu-id="dd1c4-130">El método **Get \_ deviceName** permite recuperar el nombre del dispositivo que los usuarios ven en el shell de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-130">The **get\_deviceName** method enables you to retrieve the device name that users see in the Windows XP shell.</span></span>
-   <span data-ttu-id="dd1c4-131">El método **getItemInfo** permite recuperar metadatos de los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="dd1c4-131">The **getItemInfo** method enables you to retrieve metadata from devices.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd1c4-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dd1c4-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd1c4-133">**Acerca de la sincronización de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="dd1c4-133">**About Device Synchronization**</span></span>](about-device-synchronization.md)
</dt> <dt>

[<span data-ttu-id="dd1c4-134">**Interfaz IWMPEvents2**</span><span class="sxs-lookup"><span data-stu-id="dd1c4-134">**IWMPEvents2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[<span data-ttu-id="dd1c4-135">**Interfaz IWMPSyncDevice**</span><span class="sxs-lookup"><span data-stu-id="dd1c4-135">**IWMPSyncDevice Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[<span data-ttu-id="dd1c4-136">**Trabajar con dispositivos portátiles**</span><span class="sxs-lookup"><span data-stu-id="dd1c4-136">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




