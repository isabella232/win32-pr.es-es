---
title: Implementar un complemento de DSP de audio
description: Implementar un complemento de DSP de audio
ms.assetid: 93ff0c45-f418-443d-8fba-c0a62f6e4e80
keywords:
- Complementos de Windows Media Player, audio DSP
- complementos, DSP de audio
- Complementos de procesamiento de señal digital, implementar código
- Complementos DSP, implementar código
- Complementos de procesamiento de señal digital, modificar código de ejemplo
- Complementos DSP, modificar código de ejemplo
- Complementos de procesamiento de señal digital, implementación de audio
- Complementos DSP, implementación de audio
- Complementos de DSP de audio, implementar código
- Complementos de DSP de audio, modificación del código de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdde8e7f00fc9ea3ad9bb8b7adb2d0a8bfba6b32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076039"
---
# <a name="implementing-an-audio-dsp-plug-in"></a><span data-ttu-id="50c1b-113">Implementar un complemento de DSP de audio</span><span class="sxs-lookup"><span data-stu-id="50c1b-113">Implementing an Audio DSP Plug-in</span></span>

<span data-ttu-id="50c1b-114">Para crear un complemento DSP de Windows Media Player que procese audio, deberá modificar el código de ejemplo de la función denominada **DoProcessOutput**.</span><span class="sxs-lookup"><span data-stu-id="50c1b-114">To create a Windows Media Player DSP plug-in that processes audio, you'll need to modify the sample code in the function named **DoProcessOutput**.</span></span> <span data-ttu-id="50c1b-115">Se llama a **DoProcessOutput** cada vez que Windows Media Player llama correctamente a **IMediaObject::P rocessoutput**.</span><span class="sxs-lookup"><span data-stu-id="50c1b-115">**DoProcessOutput** is called each time Windows Media Player successfully calls **IMediaObject::ProcessOutput**.</span></span> <span data-ttu-id="50c1b-116">Es la función que realiza las tareas de procesamiento de señal digital que producen el resultado audible que el complemento de DSP pretende producir.</span><span class="sxs-lookup"><span data-stu-id="50c1b-116">It is the function that performs the digital signal processing tasks that produce the audible result that the DSP plug-in is intended to produce.</span></span>

<span data-ttu-id="50c1b-117">El procesamiento de una secuencia de audio es como controlar un evento con hora.</span><span class="sxs-lookup"><span data-stu-id="50c1b-117">Processing an audio stream is like handling a timed event.</span></span> <span data-ttu-id="50c1b-118">Se llamará a **DoProcessOutput** repetidamente y a intervalos específicos.</span><span class="sxs-lookup"><span data-stu-id="50c1b-118">**DoProcessOutput** will be called repeatedly and at specific intervals.</span></span> <span data-ttu-id="50c1b-119">Cada vez que se ejecuta el código, tendrá que procesar un número específico de bytes de datos.</span><span class="sxs-lookup"><span data-stu-id="50c1b-119">Each time your code executes, it will need to process a specific number of bytes of data.</span></span> <span data-ttu-id="50c1b-120">**DoProcessOutput** contiene los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="50c1b-120">**DoProcessOutput** contains the following parameters:</span></span>



| <span data-ttu-id="50c1b-121">Parámetro</span><span class="sxs-lookup"><span data-stu-id="50c1b-121">Parameter</span></span>          | <span data-ttu-id="50c1b-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="50c1b-122">Description</span></span>                                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50c1b-123">*pbOutputData*</span><span class="sxs-lookup"><span data-stu-id="50c1b-123">*pbOutputData*</span></span>     | <span data-ttu-id="50c1b-124">Se trata de un puntero de **bytes** al búfer en el que la implementación de **DoProcessOutput** debe copiar sus datos procesados.</span><span class="sxs-lookup"><span data-stu-id="50c1b-124">This is a **BYTE** pointer to the buffer where your implementation of **DoProcessOutput** must copy its processed data.</span></span> |
| <span data-ttu-id="50c1b-125">*pbInputData*</span><span class="sxs-lookup"><span data-stu-id="50c1b-125">*pbInputData*</span></span>      | <span data-ttu-id="50c1b-126">Se trata de un puntero de **byte** constante al búfer que contiene los datos que se van a procesar.</span><span class="sxs-lookup"><span data-stu-id="50c1b-126">This is a constant **BYTE** pointer to the buffer that contains the data to be processed.</span></span>                               |
| <span data-ttu-id="50c1b-127">*cbBytesToProcess*</span><span class="sxs-lookup"><span data-stu-id="50c1b-127">*cbBytesToProcess*</span></span> | <span data-ttu-id="50c1b-128">Es un valor **DWORD** que contiene un recuento del número de bytes en el búfer de entrada que se va a procesar.</span><span class="sxs-lookup"><span data-stu-id="50c1b-128">This is a **DWORD** value that contains a count of the number of bytes in the input buffer to be processed.</span></span>             |



 

<span data-ttu-id="50c1b-129">En las secciones siguientes se proporcionan detalles sobre cómo modificar el código generado por el Asistente para complementos de Media Player de Windows para crear su propio complemento de DSP de audio:</span><span class="sxs-lookup"><span data-stu-id="50c1b-129">The following sections provide details about how to modify the code generated by the Windows Media Player Plug-in Wizard to create your own audio DSP plug-in:</span></span>

-   [<span data-ttu-id="50c1b-130">Implementación de DoProcessOutput</span><span class="sxs-lookup"><span data-stu-id="50c1b-130">Implementing DoProcessOutput</span></span>](implementing-doprocessoutput.md)
-   [<span data-ttu-id="50c1b-131">Agregar propiedades al complemento DSP de audio de ejemplo</span><span class="sxs-lookup"><span data-stu-id="50c1b-131">Adding Properties to the Sample Audio DSP Plug-in</span></span>](adding-properties-to-the-sample-audio-dsp-plug-in.md)
-   [<span data-ttu-id="50c1b-132">Implementar la página de propiedades de un complemento DSP</span><span class="sxs-lookup"><span data-stu-id="50c1b-132">Implementing the Property Page for a DSP Plug-in</span></span>](implementing-the-property-page-for-a-dsp-plug-in.md)
-   [<span data-ttu-id="50c1b-133">Cambio de la propiedad del complemento DSP de audio de ejemplo</span><span class="sxs-lookup"><span data-stu-id="50c1b-133">Changing the Sample Audio DSP Plug-in Property</span></span>](changing-the-sample-audio-dsp-plug-in-property.md)
-   [<span data-ttu-id="50c1b-134">Acerca de la discontinuidad</span><span class="sxs-lookup"><span data-stu-id="50c1b-134">About Discontinuity</span></span>](about-discontinuity.md)
-   [<span data-ttu-id="50c1b-135">Acerca de la asignación de recursos de streaming</span><span class="sxs-lookup"><span data-stu-id="50c1b-135">About Allocating Streaming Resources</span></span>](about-allocating-streaming-resources.md)

## <a name="related-topics"></a><span data-ttu-id="50c1b-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="50c1b-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50c1b-137">**Acerca de los complementos DSP**</span><span class="sxs-lookup"><span data-stu-id="50c1b-137">**About DSP Plug-ins**</span></span>](about-dsp-plug-ins.md)
</dt> </dl>

 

 




