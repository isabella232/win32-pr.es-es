---
description: El proceso de captura es el mismo para cada una de las cuatro interfaces NPP.
ms.assetid: f778aba5-8f66-4fc9-830b-f830c364da56
title: El proceso de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0ca1987266b7e042713f1d1c292cf63d5e3ccf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104552691"
---
# <a name="the-capture-process"></a><span data-ttu-id="7399d-103">El proceso de captura</span><span class="sxs-lookup"><span data-stu-id="7399d-103">The Capture Process</span></span>

<span data-ttu-id="7399d-104">El proceso de captura es el mismo para cada una de las cuatro interfaces NPP.</span><span class="sxs-lookup"><span data-stu-id="7399d-104">The capture process is the same for each of the four NPP interfaces.</span></span> <span data-ttu-id="7399d-105">En cada caso, el proceso incluye:</span><span class="sxs-lookup"><span data-stu-id="7399d-105">In each case, the process includes:</span></span>

-   <span data-ttu-id="7399d-106">Obtener el objeto de interfaz NPP que se va a usar</span><span class="sxs-lookup"><span data-stu-id="7399d-106">Obtaining the NPP interface object to use</span></span>
-   <span data-ttu-id="7399d-107">Conexión a la red</span><span class="sxs-lookup"><span data-stu-id="7399d-107">Connecting to the network</span></span>
-   <span data-ttu-id="7399d-108">Inicio y detención de la [ *captura*](c.md)</span><span class="sxs-lookup"><span data-stu-id="7399d-108">Starting and then stopping the [*capture*](c.md)</span></span>
-   <span data-ttu-id="7399d-109">Desconectar de la red</span><span class="sxs-lookup"><span data-stu-id="7399d-109">Disconnecting from the network</span></span>

> [!Note]  
> <span data-ttu-id="7399d-110">Cuando obtenga el objeto de interfaz que desee, asegúrese de llamar solo a los métodos incluidos en esa interfaz.</span><span class="sxs-lookup"><span data-stu-id="7399d-110">When you obtain the interface object that you want, ensure you call only the methods included in that interface.</span></span> <span data-ttu-id="7399d-111">En la ilustración siguiente se muestra que cada interfaz proporciona métodos similares para capturar datos de red.</span><span class="sxs-lookup"><span data-stu-id="7399d-111">The following illustration shows each interface provides similar methods for capturing network data.</span></span> <span data-ttu-id="7399d-112">Se devuelve un error si se conecta a la red con una interfaz y, a continuación, intenta ejecutar una captura con los métodos de otra interfaz.</span><span class="sxs-lookup"><span data-stu-id="7399d-112">An error is returned if you connect to the network with one interface and then try to run a capture using the methods from another interface.</span></span>

 

<span data-ttu-id="7399d-113">En las ilustraciones siguientes se muestran dos formas diferentes de ejecutar una captura.</span><span class="sxs-lookup"><span data-stu-id="7399d-113">The following illustrations show two different ways you could run a capture.</span></span> <span data-ttu-id="7399d-114">En la primera ilustración se muestra cómo ejecutar una o varias capturas secuenciales, lo que le permite crear cualquier número de capturas independientes.</span><span class="sxs-lookup"><span data-stu-id="7399d-114">The first illustration shows how to run one or more sequential captures, allowing you to create any number of independent captures.</span></span>

![captura secuencial](images/capt1.png)

<span data-ttu-id="7399d-116">Como se mostró anteriormente, después de conectarse a la red, puede iniciar y detener una captura tantas veces como desee, iniciando una nueva captura y generando nuevas estadísticas cada vez que reinicie la captura.</span><span class="sxs-lookup"><span data-stu-id="7399d-116">As shown above, after you connect to the network you can start and stop a capture as many times as you wish, starting a new capture and generating new statistics every time you restart the capture.</span></span> <span data-ttu-id="7399d-117">Por ejemplo, para una captura retrasada mediante la interfaz [**IDelaydC**](idelaydc.md) , se creará un nuevo [*archivo de captura*](c.md) cada vez que reinicie la captura.</span><span class="sxs-lookup"><span data-stu-id="7399d-117">For example, for a delayed capture using the [**IDelaydC**](idelaydc.md) interface, a new [*capture file*](c.md) would be created each time you restarted the capture.</span></span>

<span data-ttu-id="7399d-118">Sin embargo, tenga en cuenta también que cada vez que reinicie el proceso de captura, debe llamar al método configure adecuado para volver a configurar la conexión.</span><span class="sxs-lookup"><span data-stu-id="7399d-118">However, also be aware that every time you restart the capture process you must call the appropriate configure method to reconfigure the connection.</span></span> <span data-ttu-id="7399d-119">Para que la llamada inicial inicie la captura, la llamada la configura para conectarse a la red.</span><span class="sxs-lookup"><span data-stu-id="7399d-119">For the initial call to start the capture, the connection is configured by the call to connect to the network.</span></span>

<span data-ttu-id="7399d-120">En la segunda ilustración se muestra cómo se puede ejecutar una sola captura pausando y reiniciando.</span><span class="sxs-lookup"><span data-stu-id="7399d-120">The second illustration shows how you could run a single capture by pausing and restarting.</span></span>

![captura única mediante pausa y reinicio](images/capt2.png)

<span data-ttu-id="7399d-122">En este caso, puede pausar y reiniciar una captura tantas veces como desee.</span><span class="sxs-lookup"><span data-stu-id="7399d-122">In this case, you can pause and restart a capture as many times as you want.</span></span> <span data-ttu-id="7399d-123">Con este enfoque, puede ejecutar una captura cuyos datos (y sus estadísticas relacionadas) se registran como una captura única.</span><span class="sxs-lookup"><span data-stu-id="7399d-123">With this approach, you can run a capture whose data (and its related statistics) are recorded as a single capture.</span></span> <span data-ttu-id="7399d-124">Por ejemplo, para realizar una captura diferida mediante la interfaz [**IDelaydC**](idelaydc.md) , toda la información de red capturada se guardaría en un único [*archivo de captura*](c.md).</span><span class="sxs-lookup"><span data-stu-id="7399d-124">For example, to perform a delayed capture using the [**IDelaydC**](idelaydc.md) interface, all the captured network information would be saved in a single [*capture file*](c.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7399d-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7399d-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7399d-126">**CreateNPPInterface**</span><span class="sxs-lookup"><span data-stu-id="7399d-126">**CreateNPPInterface**</span></span>](createnppinterface.md)
</dt> <dt>

[<span data-ttu-id="7399d-127">**IDelaydC:: configure**</span><span class="sxs-lookup"><span data-stu-id="7399d-127">**IDelaydC::Configure**</span></span>](idelaydc-configure.md)
</dt> <dt>

[<span data-ttu-id="7399d-128">**IDelaydC:: Connect**</span><span class="sxs-lookup"><span data-stu-id="7399d-128">**IDelaydC::Connect**</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="7399d-129">**IDelaydC::D Ulta**</span><span class="sxs-lookup"><span data-stu-id="7399d-129">**IDelaydC::Disconnect**</span></span>](idelaydc-disconnect.md)
</dt> <dt>

[<span data-ttu-id="7399d-130">**IDelaydC::P ause**</span><span class="sxs-lookup"><span data-stu-id="7399d-130">**IDelaydC::Pause**</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="7399d-131">**IDelaydC:: resume**</span><span class="sxs-lookup"><span data-stu-id="7399d-131">**IDelaydC::Resume**</span></span>](idelaydc-resume.md)
</dt> <dt>

[<span data-ttu-id="7399d-132">**IDelaydC:: Start**</span><span class="sxs-lookup"><span data-stu-id="7399d-132">**IDelaydC::Start**</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="7399d-133">**IDelaydC:: Stop**</span><span class="sxs-lookup"><span data-stu-id="7399d-133">**IDelaydC::Stop**</span></span>](idelaydc-stop.md)
</dt> <dt>

[<span data-ttu-id="7399d-134">**IESP:: configure**</span><span class="sxs-lookup"><span data-stu-id="7399d-134">**IESP::Configure**</span></span>](iesp-configure.md)
</dt> <dt>

[<span data-ttu-id="7399d-135">**IESP:: Connect**</span><span class="sxs-lookup"><span data-stu-id="7399d-135">**IESP::Connect**</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="7399d-136">**IESP::D Ulta**</span><span class="sxs-lookup"><span data-stu-id="7399d-136">**IESP::Disconnect**</span></span>](iesp-disconnect.md)
</dt> <dt>

[<span data-ttu-id="7399d-137">**IESP::P ause**</span><span class="sxs-lookup"><span data-stu-id="7399d-137">**IESP::Pause**</span></span>](iesp-pause.md)
</dt> <dt>

[<span data-ttu-id="7399d-138">**IESP:: resume**</span><span class="sxs-lookup"><span data-stu-id="7399d-138">**IESP::Resume**</span></span>](iesp-resume.md)
</dt> <dt>

[<span data-ttu-id="7399d-139">**IESP:: Start**</span><span class="sxs-lookup"><span data-stu-id="7399d-139">**IESP::Start**</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="7399d-140">**IESP:: Stop**</span><span class="sxs-lookup"><span data-stu-id="7399d-140">**IESP::Stop**</span></span>](iesp-stop.md)
</dt> <dt>

[<span data-ttu-id="7399d-141">**IRTC:: configure**</span><span class="sxs-lookup"><span data-stu-id="7399d-141">**IRTC::Configure**</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="7399d-142">**IRTC:: Connect**</span><span class="sxs-lookup"><span data-stu-id="7399d-142">**IRTC::Connect**</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="7399d-143">**IRTC::D Ulta**</span><span class="sxs-lookup"><span data-stu-id="7399d-143">**IRTC::Disconnect**</span></span>](irtc-disconnect.md)
</dt> <dt>

[<span data-ttu-id="7399d-144">**IRTC::P ause**</span><span class="sxs-lookup"><span data-stu-id="7399d-144">**IRTC::Pause**</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="7399d-145">**IRTC:: resume**</span><span class="sxs-lookup"><span data-stu-id="7399d-145">**IRTC::Resume**</span></span>](irtc-resume.md)
</dt> <dt>

[<span data-ttu-id="7399d-146">**IRTC:: Start**</span><span class="sxs-lookup"><span data-stu-id="7399d-146">**IRTC::Start**</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="7399d-147">**IRTC:: Stop**</span><span class="sxs-lookup"><span data-stu-id="7399d-147">**IRTC::Stop**</span></span>](irtc-stop.md)
</dt> <dt>

[<span data-ttu-id="7399d-148">**ISta:: configurar**</span><span class="sxs-lookup"><span data-stu-id="7399d-148">**IStats::Configure**</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="7399d-149">**ISta:: Connect**</span><span class="sxs-lookup"><span data-stu-id="7399d-149">**IStats::Connect**</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="7399d-150">**IStas::D Ulta**</span><span class="sxs-lookup"><span data-stu-id="7399d-150">**IStats::Disconnect**</span></span>](istats-disconnect.md)
</dt> <dt>

[<span data-ttu-id="7399d-151">**IStas::P ause**</span><span class="sxs-lookup"><span data-stu-id="7399d-151">**IStats::Pause**</span></span>](istats-pause.md)
</dt> <dt>

[<span data-ttu-id="7399d-152">**IStas:: resume**</span><span class="sxs-lookup"><span data-stu-id="7399d-152">**IStats::Resume**</span></span>](istats-resume.md)
</dt> <dt>

[<span data-ttu-id="7399d-153">**ISta:: Start**</span><span class="sxs-lookup"><span data-stu-id="7399d-153">**IStats::Start**</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="7399d-154">**IStas:: Stop**</span><span class="sxs-lookup"><span data-stu-id="7399d-154">**IStats::Stop**</span></span>](istats-stop.md)
</dt> </dl>

 

 



