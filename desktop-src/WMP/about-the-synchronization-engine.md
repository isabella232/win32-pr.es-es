---
title: Acerca del motor de sincronización
description: Acerca del motor de sincronización
ms.assetid: bb57ffb0-3833-463b-b66c-c23224fa2ba7
keywords:
- Windows Media Player, motor de sincronización
- Modelo de objetos de Windows Media Player, motor de sincronización
- modelo de objetos, motor de sincronización
- Control ActiveX de Windows Media Player, motor de sincronización
- Control ActiveX, motor de sincronización
- Control ActiveX móvil de Windows Media Player, motor de sincronización
- Windows Media Player Mobile, motor de sincronización
- sincronizar dispositivos, motor de sincronización
- sincronización de dispositivos, motor de sincronización
- motor de sincronización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe0768c4805b074fdaf628a25daf47b9ced97ee
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420291"
---
# <a name="about-the-synchronization-engine"></a><span data-ttu-id="d7fc4-113">Acerca del motor de sincronización</span><span class="sxs-lookup"><span data-stu-id="d7fc4-113">About the Synchronization Engine</span></span>

<span data-ttu-id="d7fc4-114">El motor de sincronización es el componente de Windows Media Player que administra la copia de contenido multimedia digital en dispositivos portátiles.</span><span class="sxs-lookup"><span data-stu-id="d7fc4-114">The synchronization engine is the component of Windows Media Player that manages copying digital media content to portable devices.</span></span> <span data-ttu-id="d7fc4-115">Windows Media Player admite una única instancia del motor de sincronización para cada dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d7fc4-115">Windows Media Player supports a single instance of the synchronization engine for each device.</span></span> <span data-ttu-id="d7fc4-116">Debe utilizar una instancia remota del control Media Player de Windows para realizar las tareas de sincronización mediante programación.</span><span class="sxs-lookup"><span data-stu-id="d7fc4-116">You must use a remoted instance of the Windows Media Player control to perform synchronization tasks programmatically.</span></span> <span data-ttu-id="d7fc4-117">En efecto, el programa comparte las instancias del motor de sincronización con Windows Media Player y todos los demás programas que usan las interfaces del reproductor para la sincronización de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d7fc4-117">In effect, your program shares the synchronization engine instances with Windows Media Player and all other programs that use the Player interfaces for device synchronization.</span></span>

<span data-ttu-id="d7fc4-118">Puede usar [IWMPSyncDevice:: Start](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-start) y [IWMPSyncDevice:: Stop](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-stop) para controlar el momento en que el motor de sincronización realiza su trabajo.</span><span class="sxs-lookup"><span data-stu-id="d7fc4-118">You can use [IWMPSyncDevice::start](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-start) and [IWMPSyncDevice::stop](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-stop) to control when the synchronization engine does its work.</span></span> <span data-ttu-id="d7fc4-119">En la mayoría de los casos, no debe utilizar estos métodos.</span><span class="sxs-lookup"><span data-stu-id="d7fc4-119">In most cases, you should not use these methods.</span></span> <span data-ttu-id="d7fc4-120">En su lugar, debe permitir que el motor de sincronización Programe su trabajo automáticamente.</span><span class="sxs-lookup"><span data-stu-id="d7fc4-120">Instead, you should let the synchronization engine schedule its work automatically.</span></span> <span data-ttu-id="d7fc4-121">Los métodos **Start** y **Stop** existen para que pueda usarlos si el programa está diseñado para reemplazar la interfaz de usuario de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="d7fc4-121">The **start** and **stop** methods exist so that you can use them if your program is designed to replace the Windows Media Player user interface.</span></span> <span data-ttu-id="d7fc4-122">En este caso, es posible que desee proporcionar un botón Iniciar/detener similar al que proporciona Windows Media Player en la pestaña **dispositivos** .</span><span class="sxs-lookup"><span data-stu-id="d7fc4-122">In this case, you might want to provide a start/stop button similar to the one Windows Media Player provides in the **Devices** tab.</span></span>

<span data-ttu-id="d7fc4-123">Puede supervisar el progreso de sincronización de un dispositivo mediante el sondeo de [IWMPSyncDevice:: get \_ Progress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress).</span><span class="sxs-lookup"><span data-stu-id="d7fc4-123">You can monitor the synchronization progress for a device by polling [IWMPSyncDevice::get\_progress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress).</span></span> <span data-ttu-id="d7fc4-124">Este método recupera un valor de progreso para todo el proceso de sincronización con un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="d7fc4-124">This method retrieves a progress value for the entire synchronization process with a particular device.</span></span> <span data-ttu-id="d7fc4-125">El valor recuperado es un número que representa el porcentaje de sincronización completada.</span><span class="sxs-lookup"><span data-stu-id="d7fc4-125">The value retrieved is a number that represents the percentage of synchronization complete.</span></span> <span data-ttu-id="d7fc4-126">Hay dos eventos que se pueden recibir y que están relacionados con la sincronización.</span><span class="sxs-lookup"><span data-stu-id="d7fc4-126">There are two events you can receive that are related to synchronization.</span></span> <span data-ttu-id="d7fc4-127">El evento **DeviceSyncError** le notifica cuando se produce un problema.</span><span class="sxs-lookup"><span data-stu-id="d7fc4-127">The **DeviceSyncError** event notifies you when a problem occurs.</span></span> <span data-ttu-id="d7fc4-128">El evento **DeviceSyncStateChange** le alerta cuando el motor de sincronización ha cambiado el estado del dispositivo actual.</span><span class="sxs-lookup"><span data-stu-id="d7fc4-128">The **DeviceSyncStateChange** event alerts you when the synchronization engine has changed state for the current device.</span></span>

<span data-ttu-id="d7fc4-129">Puede limitar la cantidad de almacenamiento de dispositivo que usa Windows Media Player para la sincronización mediante una llamada a [IWMPSyncDevice2:: setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo) con el atributo **PercentSpaceReserved** .</span><span class="sxs-lookup"><span data-stu-id="d7fc4-129">You can limit the amount of device storage that Windows Media Player uses for synchronization by calling [IWMPSyncDevice2::setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo) with the **PercentSpaceReserved** attribute.</span></span> <span data-ttu-id="d7fc4-130">El uso de esta interfaz requiere Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="d7fc4-130">Using this interface requires Windows Media Player 11.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7fc4-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d7fc4-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7fc4-132">**Acerca de la sincronización de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="d7fc4-132">**About Device Synchronization**</span></span>](about-device-synchronization.md)
</dt> <dt>

[<span data-ttu-id="d7fc4-133">**Interfaz IWMPEvents2**</span><span class="sxs-lookup"><span data-stu-id="d7fc4-133">**IWMPEvents2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[<span data-ttu-id="d7fc4-134">**Mostrando el progreso de la sincronización**</span><span class="sxs-lookup"><span data-stu-id="d7fc4-134">**Showing Synchronization Progress**</span></span>](showing-synchronization-progress.md)
</dt> </dl>

 

 




