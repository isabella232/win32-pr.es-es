---
title: Acerca de la copia de CD
description: Acerca de la copia de CD
ms.assetid: 1a179284-2909-4fc0-82be-996794ee4f31
keywords:
- Windows Media Player, copia desde CD
- Modelo de objetos de Windows Media Player, copia desde CD
- modelo de objetos, copia desde CD
- Control ActiveX de Windows Media Player, copia desde CD
- Control ActiveX, copiar CD
- Control ActiveX móvil de Windows Media Player, copia desde CD
- Windows Media Player Mobile, copia desde CD
- CD, acerca de
- copiar CDs, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e28769c6af666e510fb97ebc98e44fadc7c3e472
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105695548"
---
# <a name="about-cd-ripping"></a><span data-ttu-id="c282b-112">Acerca de la copia de CD</span><span class="sxs-lookup"><span data-stu-id="c282b-112">About CD Ripping</span></span>

<span data-ttu-id="c282b-113">El SDK de Windows Media Player 11 presenta nuevas funciones para copiar pistas de audio de CDs en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="c282b-113">The Windows Media Player 11 SDK introduces new functionality for copying audio tracks from CDs to the user's computer.</span></span> <span data-ttu-id="c282b-114">Este proceso se denomina *copia desde CD*.</span><span class="sxs-lookup"><span data-stu-id="c282b-114">This process is called *ripping*.</span></span>

<span data-ttu-id="c282b-115">Cuando se copian pistas de audio mediante las interfaces del SDK de Windows Media Player, las pistas de música resultantes se crean mediante la configuración definida por el usuario en el cuadro de diálogo **Opciones** de Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="c282b-115">When you rip audio tracks by using the Windows Media Player SDK interfaces, the resulting music tracks are created by using the settings that the user defined in the Windows Media Player **Options** dialog box.</span></span>

<span data-ttu-id="c282b-116">Para enumerar las unidades de CD en el equipo del usuario, use la interfaz **IWMPCdromCollection** .</span><span class="sxs-lookup"><span data-stu-id="c282b-116">To enumerate the CD drives on the user's computer, use the **IWMPCdromCollection** interface.</span></span> <span data-ttu-id="c282b-117">Para recuperar un puntero a esta interfaz, llame a [IWMPCore:: get \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).</span><span class="sxs-lookup"><span data-stu-id="c282b-117">You retrieve a pointer to this interface by calling [IWMPCore::get\_cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).</span></span> <span data-ttu-id="c282b-118">Mediante el uso de los métodos **Count** y **Item** , puede recorrer en iteración la colección para recuperar un puntero de la interfaz **IWMPCDROM** para cada unidad de CD del equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="c282b-118">By using the **count** and **item** methods, you can iterate the collection to retrieve an **IWMPCdrom** interface pointer for each CD drive on the user's computer.</span></span> <span data-ttu-id="c282b-119">La interfaz **IWMPCdrom** representa una unidad de CD individual.</span><span class="sxs-lookup"><span data-stu-id="c282b-119">The **IWMPCdrom** interface represents an individual CD drive.</span></span> <span data-ttu-id="c282b-120">Antes de empezar a copiar un CD, primero debe llamar a **QueryInterface** a través de un puntero **IWMPCdrom** para recuperar un puntero a la interfaz **IWMPCdromRip** .</span><span class="sxs-lookup"><span data-stu-id="c282b-120">Before you begin ripping a CD, you must first call **QueryInterface** through an **IWMPCdrom** pointer to retrieve a pointer to the **IWMPCdromRip** interface.</span></span>

<span data-ttu-id="c282b-121">Para iniciar la operación de copia, simplemente llame a [IWMPCdromRip:: startRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip).</span><span class="sxs-lookup"><span data-stu-id="c282b-121">To start the ripping operation, simply call [IWMPCdromRip::startRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip).</span></span> <span data-ttu-id="c282b-122">Puede supervisar el progreso de la operación de copia desde CD llamando periódicamente a [IWMPCdromRip:: get \_ ripProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress).</span><span class="sxs-lookup"><span data-stu-id="c282b-122">You can monitor the progress of the ripping operation by periodically calling [IWMPCdromRip::get\_ripProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress).</span></span> <span data-ttu-id="c282b-123">Este método recupera un valor de progreso para toda la operación de copia.</span><span class="sxs-lookup"><span data-stu-id="c282b-123">This method retrieves a progress value for the entire ripping operation.</span></span> <span data-ttu-id="c282b-124">El valor recuperado es un número que representa el porcentaje de copia completada.</span><span class="sxs-lookup"><span data-stu-id="c282b-124">The value retrieved is a number that represents the percentage of ripping completed.</span></span> <span data-ttu-id="c282b-125">Puede supervisar el estado de la operación de copia desde CD llamando periódicamente a [IWMPCdromRip:: get \_ ripState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate).</span><span class="sxs-lookup"><span data-stu-id="c282b-125">You can monitor the state of the ripping operation by periodically calling [IWMPCdromRip::get\_ripState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate).</span></span> <span data-ttu-id="c282b-126">Este método recupera un valor de enumeración [WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) que indica si la operación está en curso o detenido.</span><span class="sxs-lookup"><span data-stu-id="c282b-126">This method retrieves a [WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) enumeration value that indicates whether the operation is in progress or stopped.</span></span> <span data-ttu-id="c282b-127">También puede supervisar el estado de la operación de copia desde CD mediante el control del evento [IWMPEvents3:: CdromRipStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) .</span><span class="sxs-lookup"><span data-stu-id="c282b-127">You can also monitor the state of the ripping operation by handling the [IWMPEvents3::CdromRipStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) event.</span></span> <span data-ttu-id="c282b-128">Debe tener cuidado de comparar el puntero **IWMPCdromRip** (proporcionado por el evento) con el puntero que representa la operación de copia desde CD para asegurarse de que la operación ha generado el evento.</span><span class="sxs-lookup"><span data-stu-id="c282b-128">You should be careful to compare the **IWMPCdromRip** pointer (provided by the event) to the pointer that represents your ripping operation to ensure that the event was raised by your operation.</span></span> <span data-ttu-id="c282b-129">Puede detener la operación de copia desde CD llamando a [IWMPCdromRip:: stopRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip).</span><span class="sxs-lookup"><span data-stu-id="c282b-129">You can stop the ripping operation by calling [IWMPCdromRip::stopRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip).</span></span>

<span data-ttu-id="c282b-130">Para recibir notificaciones de error sobre una operación de copia desde CD, puede controlar el evento [IWMPEvents3:: CdromRipMediaError](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripmediaerror) .</span><span class="sxs-lookup"><span data-stu-id="c282b-130">To receive error notifications about a ripping operation, you can handle the [IWMPEvents3::CdromRipMediaError](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripmediaerror) event.</span></span> <span data-ttu-id="c282b-131">Al igual que **CdromRipStateChange**, este evento proporciona un puntero de interfaz **IWMPCdromRip** que representa la operación de copia desde CD que ha generado el evento.</span><span class="sxs-lookup"><span data-stu-id="c282b-131">Like **CdromRipStateChange**, this event provides an **IWMPCdromRip** interface pointer that represents the ripping operation that raised the event.</span></span> <span data-ttu-id="c282b-132">El evento también proporciona un puntero **IDispatch** que representa el elemento multimedia que provocó el evento.</span><span class="sxs-lookup"><span data-stu-id="c282b-132">The event also provides an **IDispatch** pointer that represents the media item that raised the event.</span></span> <span data-ttu-id="c282b-133">Puede llamar a **QueryInterface** a través de este puntero para recuperar un puntero **IWMPMedia** .</span><span class="sxs-lookup"><span data-stu-id="c282b-133">You can call **QueryInterface** through this pointer to retrieve an **IWMPMedia** pointer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c282b-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c282b-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c282b-135">**Acerca del modelo de objetos de Player**</span><span class="sxs-lookup"><span data-stu-id="c282b-135">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> </dl>

 

 




