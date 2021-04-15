---
title: Acerca de IMFTransform
description: Acerca de IMFTransform
ms.assetid: 889f2d82-148a-4a7e-b78c-37ec86b37e0b
keywords:
- Complementos de Windows Media Player, interfaces
- complementos, interfaces
- Complementos de procesamiento de señal digital, interfaces
- Complementos DSP, interfaces
- interfaces, Complementos DSP
- Complementos de Media Player de Windows, interfaz IMFTransform
- complementos, interfaz IMFTransform
- Complementos de procesamiento de señal digital, interfaz IMFTransform
- Complementos DSP, interfaz IMFTransform
- Interfaz IMFTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb58ab84070a8cb9390e4525b9b642f15a29f14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695238"
---
# <a name="about-imftransform"></a><span data-ttu-id="489cd-113">Acerca de IMFTransform</span><span class="sxs-lookup"><span data-stu-id="489cd-113">About IMFTransform</span></span>

<span data-ttu-id="489cd-114">La interfaz **IMFTransform** es una de las interfaces que debe implementar un complemento DSP de modo dual.</span><span class="sxs-lookup"><span data-stu-id="489cd-114">The **IMFTransform** interface is one of the interfaces that must be implemented by a dual-mode DSP plug-in.</span></span> <span data-ttu-id="489cd-115">Windows Media Player llama a los métodos de la interfaz **IMFTransform** para proporcionar datos al complemento y recuperar los datos procesados del complemento.</span><span class="sxs-lookup"><span data-stu-id="489cd-115">Windows Media Player calls the methods of the **IMFTransform** interface to provide data to the plug-in and to retrieve processed data back from the plug-in.</span></span> <span data-ttu-id="489cd-116">Para obtener la documentación completa de la interfaz **IMFTransform** , consulte la sección Media Foundation del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="489cd-116">For complete documentation of the **IMFTransform** interface, see the Media Foundation section of the Windows SDK.</span></span>

<span data-ttu-id="489cd-117">Los métodos de **IMFTransform** se pueden categorizar de la manera siguiente.</span><span class="sxs-lookup"><span data-stu-id="489cd-117">The methods of **IMFTransform** can be categorized as follows.</span></span>

## <a name="methods-that-handle-format-negotiation"></a><span data-ttu-id="489cd-118">Métodos que controlan la negociación de formato</span><span class="sxs-lookup"><span data-stu-id="489cd-118">Methods That Handle Format Negotiation</span></span>

<span data-ttu-id="489cd-119">Windows Media Player llama a los métodos siguientes para obtener información sobre los formatos de datos admitidos por el complemento.</span><span class="sxs-lookup"><span data-stu-id="489cd-119">Windows Media Player calls the following methods to get information about the data formats supported by the plug-in.</span></span>

-   <span data-ttu-id="489cd-120">**GetStreamCount**</span><span class="sxs-lookup"><span data-stu-id="489cd-120">**GetStreamCount**</span></span>
-   <span data-ttu-id="489cd-121">**GetStreamLimits**</span><span class="sxs-lookup"><span data-stu-id="489cd-121">**GetStreamLimits**</span></span>
-   <span data-ttu-id="489cd-122">**GetInputStreamInfo**</span><span class="sxs-lookup"><span data-stu-id="489cd-122">**GetInputStreamInfo**</span></span>
-   <span data-ttu-id="489cd-123">**GetOutputStreamInfo**</span><span class="sxs-lookup"><span data-stu-id="489cd-123">**GetOutputStreamInfo**</span></span>
-   <span data-ttu-id="489cd-124">**GetInputAvailableType**</span><span class="sxs-lookup"><span data-stu-id="489cd-124">**GetInputAvailableType**</span></span>
-   <span data-ttu-id="489cd-125">**GetOutputAvailableType**</span><span class="sxs-lookup"><span data-stu-id="489cd-125">**GetOutputAvailableType**</span></span>
-   <span data-ttu-id="489cd-126">**SetInputType**</span><span class="sxs-lookup"><span data-stu-id="489cd-126">**SetInputType**</span></span>
-   <span data-ttu-id="489cd-127">**SetOutputType**</span><span class="sxs-lookup"><span data-stu-id="489cd-127">**SetOutputType**</span></span>
-   <span data-ttu-id="489cd-128">**GetAttributes**</span><span class="sxs-lookup"><span data-stu-id="489cd-128">**GetAttributes**</span></span>
-   <span data-ttu-id="489cd-129">**GetInputStreamAttributes**</span><span class="sxs-lookup"><span data-stu-id="489cd-129">**GetInputStreamAttributes**</span></span>
-   <span data-ttu-id="489cd-130">**GetOutputStreamAttributes**</span><span class="sxs-lookup"><span data-stu-id="489cd-130">**GetOutputStreamAttributes**</span></span>
-   <span data-ttu-id="489cd-131">**GetStreamIDs**</span><span class="sxs-lookup"><span data-stu-id="489cd-131">**GetStreamIDs**</span></span>

## <a name="methods-that-specify-or-retrieve-state-information"></a><span data-ttu-id="489cd-132">Métodos que especifican o recuperan información de estado</span><span class="sxs-lookup"><span data-stu-id="489cd-132">Methods That Specify or Retrieve State Information</span></span>

<span data-ttu-id="489cd-133">Windows Media Player llama a los métodos siguientes para obtener o establecer los valores relacionados con el estado actual del complemento.</span><span class="sxs-lookup"><span data-stu-id="489cd-133">Windows Media Player calls the following methods to get or set values related to the current state of the plug-in.</span></span>

-   <span data-ttu-id="489cd-134">**SetInputType**</span><span class="sxs-lookup"><span data-stu-id="489cd-134">**SetInputType**</span></span>
-   <span data-ttu-id="489cd-135">**SetOutputType**</span><span class="sxs-lookup"><span data-stu-id="489cd-135">**SetOutputType**</span></span>
-   <span data-ttu-id="489cd-136">**GetInputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="489cd-136">**GetInputCurrentType**</span></span>
-   <span data-ttu-id="489cd-137">**GetOutputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="489cd-137">**GetOutputCurrentType**</span></span>
-   <span data-ttu-id="489cd-138">**GetInputStatus**</span><span class="sxs-lookup"><span data-stu-id="489cd-138">**GetInputStatus**</span></span>
-   <span data-ttu-id="489cd-139">**AddInputStreams**</span><span class="sxs-lookup"><span data-stu-id="489cd-139">**AddInputStreams**</span></span>
-   <span data-ttu-id="489cd-140">**DeleteInputStreams**</span><span class="sxs-lookup"><span data-stu-id="489cd-140">**DeleteInputStreams**</span></span>
-   <span data-ttu-id="489cd-141">**GetOutputStatus**</span><span class="sxs-lookup"><span data-stu-id="489cd-141">**GetOutputStatus**</span></span>
-   <span data-ttu-id="489cd-142">**SetOutputBounds**</span><span class="sxs-lookup"><span data-stu-id="489cd-142">**SetOutputBounds**</span></span>

> [!Note]  
> <span data-ttu-id="489cd-143">**SetInputType** y **SetOutputType** se usan para la negociación de formato y para especificar y recuperar información de estado.</span><span class="sxs-lookup"><span data-stu-id="489cd-143">**SetInputType** and **SetOutputType** are used both for format negotiation and for specifying and retrieving state information.</span></span>

 

## <a name="methods-that-handle-buffering-and-processing-data"></a><span data-ttu-id="489cd-144">Métodos que controlan los datos de procesamiento y almacenamiento en búfer</span><span class="sxs-lookup"><span data-stu-id="489cd-144">Methods That Handle Buffering and Processing Data</span></span>

<span data-ttu-id="489cd-145">Windows Media Player llama a los métodos siguientes para iniciar los distintos procesos que realiza el complemento para realizar el procesamiento de la señal digital.</span><span class="sxs-lookup"><span data-stu-id="489cd-145">Windows Media Player calls the following methods to initiate the various processes that the plug-in performs to do the digital signal processing.</span></span>

-   <span data-ttu-id="489cd-146">**ProcessInput**</span><span class="sxs-lookup"><span data-stu-id="489cd-146">**ProcessInput**</span></span>
-   <span data-ttu-id="489cd-147">**ProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="489cd-147">**ProcessOutput**</span></span>
-   <span data-ttu-id="489cd-148">**ProcessMessage**</span><span class="sxs-lookup"><span data-stu-id="489cd-148">**ProcessMessage**</span></span>
-   <span data-ttu-id="489cd-149">**ProcessEvent**</span><span class="sxs-lookup"><span data-stu-id="489cd-149">**ProcessEvent**</span></span>

## <a name="related-topics"></a><span data-ttu-id="489cd-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="489cd-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="489cd-151">**Interfaces necesarias**</span><span class="sxs-lookup"><span data-stu-id="489cd-151">**Required Interfaces**</span></span>](required-interfaces.md)
</dt> </dl>

 

 




