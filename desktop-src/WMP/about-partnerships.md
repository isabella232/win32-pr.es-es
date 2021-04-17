---
title: Acerca de las asociaciones
description: Acerca de las asociaciones
ms.assetid: d21813ed-efe0-48a2-a1bf-f10f4b7ac3e6
keywords:
- Windows Media Player, asociaciones
- Modelo de objetos de Windows Media Player, asociaciones
- modelo de objetos, asociaciones
- Control ActiveX de Windows Media Player, asociaciones
- Control ActiveX, asociaciones
- Control ActiveX móvil de Windows Media Player, asociaciones
- Windows Media Player Mobile, asociaciones
- sincronizar dispositivos, asociaciones
- sincronización de dispositivos, asociaciones
- asociaciones entre dispositivos y Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cfc3fa20e1e8a4b6a4c7993ea7dcc5842719f2a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104487283"
---
# <a name="about-partnerships"></a><span data-ttu-id="45225-113">Acerca de las asociaciones</span><span class="sxs-lookup"><span data-stu-id="45225-113">About Partnerships</span></span>

<span data-ttu-id="45225-114">Una asociación es una relación especial entre un dispositivo portátil y un Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="45225-114">A partnership is a special relationship between a portable device and Windows Media Player.</span></span> <span data-ttu-id="45225-115">Los usuarios pueden establecer una asociación para un dispositivo determinado mediante el uso de la interfaz de usuario de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="45225-115">Users can establish a partnership for a particular device by using the Windows Media Player user interface.</span></span> <span data-ttu-id="45225-116">Puede administrar mediante programación las asociaciones mediante [IWMPSyncDevice:: createPartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-createpartnership) y [IWMPSyncDevice::d eletepartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-deletepartnership).</span><span class="sxs-lookup"><span data-stu-id="45225-116">You can programmatically manage partnerships by using [IWMPSyncDevice::createPartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-createpartnership) and [IWMPSyncDevice::deletePartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-deletepartnership).</span></span> <span data-ttu-id="45225-117">El método **createPartnership** inicia un proceso asincrónico que finaliza cuando se recibe el evento **CreatePartnershipComplete** a través de la interfaz **IWMPEvents2** .</span><span class="sxs-lookup"><span data-stu-id="45225-117">The **createPartnership** method starts an asynchronous process that ends when the **CreatePartnershipComplete** event is received through the **IWMPEvents2** interface.</span></span>

<span data-ttu-id="45225-118">Windows Media Player 10 o versiones posteriores admiten la creación de asociaciones con hasta 16 dispositivos.</span><span class="sxs-lookup"><span data-stu-id="45225-118">Windows Media Player 10 or later supports creating partnerships with up to 16 devices.</span></span> <span data-ttu-id="45225-119">Cada asociación tiene un índice de asociación asociado.</span><span class="sxs-lookup"><span data-stu-id="45225-119">Each partnership has an associated partnership index.</span></span> <span data-ttu-id="45225-120">Puede recuperar el índice de Asociación para un dispositivo determinado mediante una llamada a [IWMPSyncDevice:: get \_ partnershipIndex](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex).</span><span class="sxs-lookup"><span data-stu-id="45225-120">You can retrieve the partnership index for a particular device by calling [IWMPSyncDevice::get\_partnershipIndex](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex).</span></span> <span data-ttu-id="45225-121">Los índices de asociación se numeran de 1 a 16.</span><span class="sxs-lookup"><span data-stu-id="45225-121">Partnership indices are numbered from 1 to 16.</span></span> <span data-ttu-id="45225-122">Cuando un dispositivo determinado no tiene una asociación con Windows Media Player, **getPartnershipIndex** devuelve cero para el índice.</span><span class="sxs-lookup"><span data-stu-id="45225-122">When a particular device does not have a partnership with Windows Media Player, **getPartnershipIndex** returns zero for the index.</span></span>

<span data-ttu-id="45225-123">Puede recuperar el estado de Asociación de un dispositivo determinado llamando a [IWMPSyncDevice:: get \_ status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) y, a continuación, inspeccionando el valor de [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) recuperado.</span><span class="sxs-lookup"><span data-stu-id="45225-123">You can retrieve the partnership status of a particular device by calling [IWMPSyncDevice::get\_status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) and then inspecting the [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) value retrieved.</span></span> <span data-ttu-id="45225-124">Windows Media Player permite una asociación con una biblioteca de un usuario en un equipo para cada dispositivo.</span><span class="sxs-lookup"><span data-stu-id="45225-124">Windows Media Player allows one partnership with one user's library on one computer for each device.</span></span> <span data-ttu-id="45225-125">Esto significa que la creación de una nueva asociación destruye cualquier asociación existente que el dispositivo actual pueda tener con otro equipo.</span><span class="sxs-lookup"><span data-stu-id="45225-125">This means that creating a new partnership destroys any existing partnership the current device might have with another computer.</span></span> <span data-ttu-id="45225-126">Para saber cuándo cambia el estado de un dispositivo, puede recibir el evento **DeviceStatusChange** .</span><span class="sxs-lookup"><span data-stu-id="45225-126">To know when the status changes for a device, you can receive the **DeviceStatusChange** event.</span></span>

<span data-ttu-id="45225-127">Windows Media Player no puede crear una asociación con un dispositivo que tenga el estado **wmpdsManualDevice**.</span><span class="sxs-lookup"><span data-stu-id="45225-127">Windows Media Player cannot create a partnership with a device having the status **wmpdsManualDevice**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="45225-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="45225-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45225-129">**Acerca de la sincronización de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="45225-129">**About Device Synchronization**</span></span>](about-device-synchronization.md)
</dt> <dt>

[<span data-ttu-id="45225-130">**Interfaz IWMPEvents2**</span><span class="sxs-lookup"><span data-stu-id="45225-130">**IWMPEvents2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[<span data-ttu-id="45225-131">**Trabajar con dispositivos portátiles**</span><span class="sxs-lookup"><span data-stu-id="45225-131">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




