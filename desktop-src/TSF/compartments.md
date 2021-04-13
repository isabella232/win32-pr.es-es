---
title: Compartimientos
description: Compartimientos
ms.assetid: 7bffab6f-be40-4d3a-9342-6f81557a9656
keywords:
- Text Services Framework (TSF), compartimientos
- TSF (marco de trabajo de servicios de texto), compartimientos
- servicios de texto, compartimientos
- Aplicaciones habilitadas para TSF, compartimientos
- compartimientos
- Text Services Framework (TSF), tipos de compartimientos
- TSF (marco de trabajo de servicios de texto), tipos de compartimiento
- servicios de texto, tipos de compartimientos
- Aplicaciones habilitadas para TSF, tipos de compartimientos
- tipos de compartimientos
- Marco de trabajo de servicios de texto (TSF), notificaciones de cambios de compartimiento
- TSF (marco de trabajo de servicios de texto), notificaciones de cambios de compartimiento
- servicios de texto, notificaciones de cambios de compartimiento
- Aplicaciones habilitadas para TSF, notificaciones de cambios de compartimiento
- notificaciones de cambio de compartimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76636c684ee74f7e452b5602ebfd59d6d1947b0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268530"
---
# <a name="compartments"></a><span data-ttu-id="2e140-118">Compartimientos</span><span class="sxs-lookup"><span data-stu-id="2e140-118">Compartments</span></span>

## <a name="compartment-types"></a><span data-ttu-id="2e140-119">Tipos de compartimientos</span><span class="sxs-lookup"><span data-stu-id="2e140-119">Compartment Types</span></span>

<span data-ttu-id="2e140-120">Hay varios tipos diferentes de compartimientos.</span><span class="sxs-lookup"><span data-stu-id="2e140-120">There are several different types of compartments.</span></span> <span data-ttu-id="2e140-121">Hay un compartimiento global, y cada administrador de subprocesos, administrador de documentos y contexto puede contener un compartimiento.</span><span class="sxs-lookup"><span data-stu-id="2e140-121">There is a global compartment, and each thread manager, document manager, and context can contain a compartment.</span></span>

<span data-ttu-id="2e140-122">El compartimiento global permite a los clientes compartir datos entre procesos.</span><span class="sxs-lookup"><span data-stu-id="2e140-122">The global compartment enables clients to share data across processes.</span></span> <span data-ttu-id="2e140-123">Para obtener el administrador de compartimiento global, llame a [**ITfThreadMgr:: GetGlobalCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment).</span><span class="sxs-lookup"><span data-stu-id="2e140-123">To obtain the global compartment manager, call [**ITfThreadMgr::GetGlobalCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment).</span></span>

<span data-ttu-id="2e140-124">El administrador de subprocesos contiene un administrador de compartimientos que contiene compartimientos por subproceso.</span><span class="sxs-lookup"><span data-stu-id="2e140-124">The thread manager contains a compartment manager that contains compartments on a per-thread basis.</span></span> <span data-ttu-id="2e140-125">Esto permite compartir los datos dentro de un subproceso.</span><span class="sxs-lookup"><span data-stu-id="2e140-125">This allows data to be shared within a thread.</span></span> <span data-ttu-id="2e140-126">Para obtener un administrador de compartimientos del administrador de subprocesos, llame a **ITfThreadMgr:: QueryInterface** con IID \_ ITfCompartmentMgr.</span><span class="sxs-lookup"><span data-stu-id="2e140-126">To obtain a thread manager compartment manager, call **ITfThreadMgr::QueryInterface** with IID\_ITfCompartmentMgr.</span></span>

<span data-ttu-id="2e140-127">Cada administrador de documentos creado también contiene un administrador de compartimientos.</span><span class="sxs-lookup"><span data-stu-id="2e140-127">Each document manager created also contains a compartment manager.</span></span> <span data-ttu-id="2e140-128">Esto permite que los datos se compartan en un administrador de documentos específico.</span><span class="sxs-lookup"><span data-stu-id="2e140-128">This allows data to be shared within a specific document manager.</span></span> <span data-ttu-id="2e140-129">Para obtener el administrador de compartimientos del administrador de documentos, llame a **ITfDocumentMgr:: QueryInterface** con IID \_ ITfCompartmentMgr.</span><span class="sxs-lookup"><span data-stu-id="2e140-129">To obtain the document manager compartment manager, call **ITfDocumentMgr::QueryInterface** with IID\_ITfCompartmentMgr.</span></span>

<span data-ttu-id="2e140-130">Cada contexto creado también contiene un administrador de compartimientos.</span><span class="sxs-lookup"><span data-stu-id="2e140-130">Each context created also contains a compartment manager.</span></span> <span data-ttu-id="2e140-131">Esto permite que los datos se compartan en un contexto específico.</span><span class="sxs-lookup"><span data-stu-id="2e140-131">This allows data to be shared within a specific context.</span></span> <span data-ttu-id="2e140-132">Para obtener un administrador de compartimiento de contexto, llame a **ITfContext:: QueryInterface** con IID \_ ITfCompartmentMgr.</span><span class="sxs-lookup"><span data-stu-id="2e140-132">To obtain a context compartment manager, call **ITfContext::QueryInterface** with IID\_ITfCompartmentMgr.</span></span>

## <a name="creating-and-deleting-a-compartment"></a><span data-ttu-id="2e140-133">Crear y eliminar un compartimiento</span><span class="sxs-lookup"><span data-stu-id="2e140-133">Creating and Deleting a Compartment</span></span>

<span data-ttu-id="2e140-134">Se crea un compartimiento la primera vez que se llama a [**ITfCompartmentMgr:: GetCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment) con el GUID del compartimiento.</span><span class="sxs-lookup"><span data-stu-id="2e140-134">A compartment is created the first time [**ITfCompartmentMgr::GetCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment) is called with the compartment GUID.</span></span> <span data-ttu-id="2e140-135">El cliente de instalación debe establecer el valor inicial del compartimiento mediante [**ITfCompartment:: SetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue).</span><span class="sxs-lookup"><span data-stu-id="2e140-135">The installing client should set the initial value of the compartment using [**ITfCompartment::SetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue).</span></span> <span data-ttu-id="2e140-136">Hasta que se establece un valor, el valor del compartimiento está vacío.</span><span class="sxs-lookup"><span data-stu-id="2e140-136">Until a value is set, the compartment value is empty.</span></span> <span data-ttu-id="2e140-137">Por esta razón, no hay ninguna manera de comprobar que el compartimiento existía antes de que se llamara a **GetCompartment** .</span><span class="sxs-lookup"><span data-stu-id="2e140-137">Because of this, there is no way to verify that the compartment existed before **GetCompartment** was called.</span></span> <span data-ttu-id="2e140-138">Para evitar esta situación, el cliente de instalación debe establecer el valor en algún valor inicial para que otros clientes puedan determinar si el compartimiento ya existe.</span><span class="sxs-lookup"><span data-stu-id="2e140-138">To avoid this situation, the installing client should set the value to some initial value so that other clients can determine if the compartment already exists.</span></span>

<span data-ttu-id="2e140-139">El método [**ITfCompartmentMgr:: ClearCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment) se usa para quitar un compartimiento.</span><span class="sxs-lookup"><span data-stu-id="2e140-139">The [**ITfCompartmentMgr::ClearCompartment**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment) method is used to remove a compartment.</span></span> <span data-ttu-id="2e140-140">Las referencias existentes al compartimiento se marcan como no válidas.</span><span class="sxs-lookup"><span data-stu-id="2e140-140">Any existing references to the compartment are marked invalid.</span></span>

## <a name="obtaining-compartments"></a><span data-ttu-id="2e140-141">Obtener compartimientos</span><span class="sxs-lookup"><span data-stu-id="2e140-141">Obtaining Compartments</span></span>

<span data-ttu-id="2e140-142">Mediante la interfaz [**ITfCompartmentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr) , un cliente puede enumerar los compartimientos llamando a [**ITfCompartmentMgr:: EnumCompartments**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments).</span><span class="sxs-lookup"><span data-stu-id="2e140-142">Using the [**ITfCompartmentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr) interface, a client can enumerate compartments by calling [**ITfCompartmentMgr::EnumCompartments**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments).</span></span> <span data-ttu-id="2e140-143">Este método proporciona un objeto **IEnumGUID** que contiene los GUID de todos los compartimientos instalados.</span><span class="sxs-lookup"><span data-stu-id="2e140-143">This method provides an **IEnumGUID** object that contains the GUIDs of all of the installed compartments.</span></span>

<span data-ttu-id="2e140-144">Con el GUID de compartimiento, se usa **ITfCompartmentMgr:: GetCompartment** para obtener un compartimiento específico.</span><span class="sxs-lookup"><span data-stu-id="2e140-144">Using the compartment GUID , **ITfCompartmentMgr::GetCompartment** is used to obtain a specific compartment.</span></span> <span data-ttu-id="2e140-145">Este método proporciona al llamador un objeto [**ITfCompartment**](/windows/desktop/api/Msctf/nn-msctf-itfcompartment) que puede obtener y establecer los datos del compartimiento.</span><span class="sxs-lookup"><span data-stu-id="2e140-145">This method provides the caller with an [**ITfCompartment**](/windows/desktop/api/Msctf/nn-msctf-itfcompartment) object that can obtain and set the compartment data.</span></span>

## <a name="receiving-compartment-change-notifications"></a><span data-ttu-id="2e140-146">Recepción de notificaciones de cambio de compartimiento</span><span class="sxs-lookup"><span data-stu-id="2e140-146">Receiving Compartment Change Notifications</span></span>

<span data-ttu-id="2e140-147">Cuando el valor de un compartimiento cambia, el administrador de TSF notifica a todos los receptores de notificaciones instalados que el compartimiento ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="2e140-147">When the value of a compartment changes, the TSF manager notifies any installed advise sinks that the compartment has changed.</span></span> <span data-ttu-id="2e140-148">Para instalar un receptor de notificaciones de cambio de compartimiento, cree un objeto que implemente [**ITfCompartmentEventSink**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink).</span><span class="sxs-lookup"><span data-stu-id="2e140-148">To install a compartment change advise sink, create an object that implements [**ITfCompartmentEventSink**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink).</span></span> <span data-ttu-id="2e140-149">Después, llame a **ITfCompartment:: QueryInterface** con IID \_ ITfSource en el objeto de compartimiento que se va a supervisar para obtener una interfaz [**ITfSource**](/windows/desktop/api/Msctf/nn-msctf-itfsource) .</span><span class="sxs-lookup"><span data-stu-id="2e140-149">Then call **ITfCompartment::QueryInterface** with IID\_ITfSource on the compartment object to be monitored to obtain an [**ITfSource**](/windows/desktop/api/Msctf/nn-msctf-itfsource) interface.</span></span> <span data-ttu-id="2e140-150">Ahora, llame a [**ITfSource:: AdviseSink**](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) con IID \_ ITfCompartmentEventSink y el puntero al objeto **ITfCompartmentEventSink** .</span><span class="sxs-lookup"><span data-stu-id="2e140-150">Now call [**ITfSource::AdviseSink**](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) with IID\_ITfCompartmentEventSink and the pointer to the **ITfCompartmentEventSink** object.</span></span> <span data-ttu-id="2e140-151">Cuando cambia el valor del compartimiento, se llama a [**ITfCompartmentEventSink:: onchange**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange) del receptor de notificaciones con el GUID del compartimiento.</span><span class="sxs-lookup"><span data-stu-id="2e140-151">When the value of the compartment changes, the advise sink's [**ITfCompartmentEventSink::OnChange**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange) is called with the GUID of the compartment.</span></span> <span data-ttu-id="2e140-152">El receptor de notificaciones puede llamar a [**ITfCompartment:: GetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-getvalue) para obtener el nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="2e140-152">The advise sink can call [**ITfCompartment::GetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-getvalue) to obtain the new value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e140-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2e140-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e140-154">**ITfCompartmentMgr**</span><span class="sxs-lookup"><span data-stu-id="2e140-154">**ITfCompartmentMgr**</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr)
</dt> <dt>

[<span data-ttu-id="2e140-155">**ITfCompartment**</span><span class="sxs-lookup"><span data-stu-id="2e140-155">**ITfCompartment**</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfcompartment)
</dt> <dt>

[<span data-ttu-id="2e140-156">**ITfCompartmentEventSink**</span><span class="sxs-lookup"><span data-stu-id="2e140-156">**ITfCompartmentEventSink**</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink)
</dt> <dt>

[<span data-ttu-id="2e140-157">**TfClientId**</span><span class="sxs-lookup"><span data-stu-id="2e140-157">**TfClientId**</span></span>](tfclientid.md)
</dt> <dt>

[<span data-ttu-id="2e140-158">**ITfThreadMgr::GetGlobalCompartment**</span><span class="sxs-lookup"><span data-stu-id="2e140-158">**ITfThreadMgr::GetGlobalCompartment**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment)
</dt> <dt>

[<span data-ttu-id="2e140-159">**ITfCompartmentMgr::GetCompartment**</span><span class="sxs-lookup"><span data-stu-id="2e140-159">**ITfCompartmentMgr::GetCompartment**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment)
</dt> <dt>

[<span data-ttu-id="2e140-160">**ITfCompartment:: SetValue**</span><span class="sxs-lookup"><span data-stu-id="2e140-160">**ITfCompartment::SetValue**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue)
</dt> <dt>

[<span data-ttu-id="2e140-161">**ITfCompartmentMgr::ClearCompartment**</span><span class="sxs-lookup"><span data-stu-id="2e140-161">**ITfCompartmentMgr::ClearCompartment**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment)
</dt> <dt>

[<span data-ttu-id="2e140-162">**ITfCompartmentMgr::EnumCompartments**</span><span class="sxs-lookup"><span data-stu-id="2e140-162">**ITfCompartmentMgr::EnumCompartments**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments)
</dt> <dt>

[<span data-ttu-id="2e140-163">**ITfSource**</span><span class="sxs-lookup"><span data-stu-id="2e140-163">**ITfSource**</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfsource)
</dt> <dt>

[<span data-ttu-id="2e140-164">**ITfSource::AdviseSink**</span><span class="sxs-lookup"><span data-stu-id="2e140-164">**ITfSource::AdviseSink**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink)
</dt> <dt>

[<span data-ttu-id="2e140-165">**ITfCompartmentEventSink:: onchange**</span><span class="sxs-lookup"><span data-stu-id="2e140-165">**ITfCompartmentEventSink::OnChange**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange)
</dt> </dl>

 

 




