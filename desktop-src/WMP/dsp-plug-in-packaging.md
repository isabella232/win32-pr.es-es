---
title: Empaquetado de complementos de DSP
description: Empaquetado de complementos de DSP
ms.assetid: 5d40a39b-0fe8-4f77-9465-8e31d1f2708e
keywords:
- Complementos de Windows Media Player, Media Foundation canalización
- complementos, canalización Media Foundation
- Complementos de procesamiento de señal digital, Media Foundation canalización
- Complementos DSP, canalización de Media Foundation
- Canalización de Media Foundation
- Complementos de Windows Media Player, canalización de DirectShow
- complementos, canalización de DirectShow
- Complementos de procesamiento de señal digital, canalización de DirectShow
- Complementos DSP, canalización de DirectShow
- Canalización de DirectShow
- Complementos de procesamiento de señal digital, básico
- Complementos DSP, básico
- Complementos de Windows Media Player, DSP básico
- complementos, DSP básico
- Complementos DSP básicos
- Complementos de Windows Media Player, DSP de modo dual
- complementos, DSP de modo dual
- Complementos de procesamiento de señal digital, modo dual
- Complementos DSP, modo dual
- Complementos DSP de modo dual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62535abe0d82975bf07fef178ac43cf066c6afbd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695662"
---
# <a name="dsp-plug-in-packaging"></a><span data-ttu-id="074ce-123">Empaquetado de complementos de DSP</span><span class="sxs-lookup"><span data-stu-id="074ce-123">DSP Plug-in Packaging</span></span>

<span data-ttu-id="074ce-124">Windows Media Player representa audio y vídeo mediante una de las siguientes canalizaciones.</span><span class="sxs-lookup"><span data-stu-id="074ce-124">Windows Media Player renders audio and video by using one of the following pipelines.</span></span>

-   <span data-ttu-id="074ce-125">DirectShow</span><span class="sxs-lookup"><span data-stu-id="074ce-125">DirectShow</span></span>
-   <span data-ttu-id="074ce-126">Media Foundation</span><span class="sxs-lookup"><span data-stu-id="074ce-126">Media Foundation</span></span>

<span data-ttu-id="074ce-127">En Microsoft Windows XP y versiones anteriores, el reproductor utiliza DirectShow.</span><span class="sxs-lookup"><span data-stu-id="074ce-127">In Microsoft Windows XP and earlier, the Player uses DirectShow.</span></span> <span data-ttu-id="074ce-128">En Windows Vista, el reproductor a veces usa DirectShow y a veces usa Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="074ce-128">In Windows Vista, the Player sometimes uses DirectShow and sometimes uses Media Foundation.</span></span>

<span data-ttu-id="074ce-129">Un complemento DSP diseñado para ejecutarse en la canalización de DirectShow se denomina *complemento DSP básico*.</span><span class="sxs-lookup"><span data-stu-id="074ce-129">A DSP plug-in that is designed to run in the DirectShow pipeline is called a *basic DSP plug-in*.</span></span> <span data-ttu-id="074ce-130">Los complementos de DSP básicos actúan como un objeto multimedia de DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="074ce-130">A basic DSP plug-ins acts as a DirectX Media Object (DMO).</span></span> <span data-ttu-id="074ce-131">Un complemento DSP básico se puede ejecutar de forma nativa en la canalización de DirectShow y también puede ejecutarse en la canalización de Media Foundation dentro de un contenedor proporcionado por Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="074ce-131">A basic DSP plug-in can run natively in the DirectShow pipeline and can also run in the Media Foundation pipeline inside a wrapper provided by Media Foundation.</span></span>

<span data-ttu-id="074ce-132">Un complemento DSP diseñado para ejecutarse de forma nativa (no se requiere ningún contenedor) en las canalizaciones de DirectShow y Media Foundation se denomina *complemento DSP de modo dual*.</span><span class="sxs-lookup"><span data-stu-id="074ce-132">A DSP plug-in that is designed to run natively (no wrapper required) in both the DirectShow and Media Foundation pipelines is called a *dual-mode DSP plug-in*.</span></span> <span data-ttu-id="074ce-133">Un complemento DSP de modo dual puede actuar como un DMO o como una transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="074ce-133">A dual-mode DSP plug-in can act as a DMO or as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="074ce-134">Un complemento DSP es un objeto COM que se empaqueta como un archivo. dll de registro automático.</span><span class="sxs-lookup"><span data-stu-id="074ce-134">A DSP plug-in is a COM object that is packaged as a self-registering .dll file.</span></span> <span data-ttu-id="074ce-135">Las interfaces que implementa el complemento dependen de si el complemento está diseñado como un complemento de DSP básico o como un complemento de DSP de modo dual.</span><span class="sxs-lookup"><span data-stu-id="074ce-135">The interfaces that the plug-in implements depend on whether the plug-in is designed as a basic DSP plug-in or as a dual-mode DSP plug-in.</span></span> <span data-ttu-id="074ce-136">Para obtener información detallada sobre las interfaces que deben implementar los complementos DSP, consulte [interfaces necesarias](required-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="074ce-136">For detailed information about the interfaces that DSP plug-ins must implement, see [Required Interfaces](required-interfaces.md).</span></span>

<span data-ttu-id="074ce-137">Un complemento DSP que se ejecuta en la canalización de Media Foundation (ya sea de forma nativa o ajustada) debe registrar su modelo de subprocesos como "both".</span><span class="sxs-lookup"><span data-stu-id="074ce-137">A DSP plug-in that runs in the Media Foundation pipeline (either natively or wrapped) must register its threading model as "Both".</span></span> <span data-ttu-id="074ce-138">Para obtener información detallada acerca de las subclaves del registro y las entradas asociadas a los complementos de DSP, consulte [registrar complementos de DSP](registering-dsp-plug-ins.md).</span><span class="sxs-lookup"><span data-stu-id="074ce-138">For detailed information about registry subkeys and entries associated with DSP plug-ins, see [Registering DSP Plug-ins](registering-dsp-plug-ins.md).</span></span>

<span data-ttu-id="074ce-139">Un complemento DSP que implementa interfaces personalizadas y que se ejecuta en la canalización Media Foundation (ya sea de forma nativa o ajustada) debe estar emparejado con un archivo. dll de código auxiliar de proxy que pueda serializar las interfaces personalizadas a través de los límites del proceso.</span><span class="sxs-lookup"><span data-stu-id="074ce-139">A DSP plug-in that implements custom interfaces and runs in the Media Foundation pipeline (either natively or wrapped) must be paired with a proxy-stub .dll file that can marshal the custom interfaces across process boundaries.</span></span> <span data-ttu-id="074ce-140">Para obtener información acerca del componente proxy-stub, vea [actualizar complementos de DSP existentes](updating-existing-dsp-plug-ins.md) y [actualizaciones del Asistente para complementos de dsp para Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).</span><span class="sxs-lookup"><span data-stu-id="074ce-140">For information about the proxy-stub component, see [Updating Existing DSP Plug-ins](updating-existing-dsp-plug-ins.md) and [Updates to the DSP Plug-in Wizard for Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).</span></span>

<span data-ttu-id="074ce-141">Los objetos de complemento de DSP no deben crearse como singletons.</span><span class="sxs-lookup"><span data-stu-id="074ce-141">DSP plug-in objects must not be created as singletons.</span></span> <span data-ttu-id="074ce-142">Windows Media Player debe ser capaz de crear varias instancias independientes de un complemento DSP determinado.</span><span class="sxs-lookup"><span data-stu-id="074ce-142">Windows Media Player must be able to create multiple separate instances of a particular DSP plug-in.</span></span>

<span data-ttu-id="074ce-143">Los complementos DSP que se ejecutan en la ruta de acceso multimedia protegida (PMP) de Windows Vista deben estar firmados.</span><span class="sxs-lookup"><span data-stu-id="074ce-143">DSP plug-ins that run in the Windows Vista Protected Media Path (PMP) must be signed.</span></span> <span data-ttu-id="074ce-144">Para obtener más información, vea [firma de código para componentes multimedia protegidos en Windows Vista](/windows-hardware/test/hlk/).</span><span class="sxs-lookup"><span data-stu-id="074ce-144">For more information, see [Code Signing for Protected Media Components in Windows Vista](/windows-hardware/test/hlk/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="074ce-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="074ce-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="074ce-146">**Introducción al desarrollador de complementos de DSP**</span><span class="sxs-lookup"><span data-stu-id="074ce-146">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 