---
title: Implementación de un complemento DSP de vídeo
description: Implementación de un complemento DSP de vídeo
ms.assetid: 36c06c57-7623-430b-8280-9dba7b0a2e9b
keywords:
- Complementos de Windows Media Player, DSP de vídeo
- complementos, DSP de vídeo
- Complementos de procesamiento de señal digital, implementar código
- Complementos DSP, implementar código
- Complementos de procesamiento de señal digital, modificar código de ejemplo
- Complementos DSP, modificar código de ejemplo
- Complementos de procesamiento de señal digital, implementación de vídeo
- Complementos DSP, implementación de vídeo
- Complementos de DSP de vídeo, implementar código
- Complementos de DSP de vídeo, modificar código de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43f1b819f328fc586d21208c00b6f0d03dca4fe9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357212"
---
# <a name="implementing-a-video-dsp-plug-in"></a><span data-ttu-id="c192c-113">Implementación de un complemento DSP de vídeo</span><span class="sxs-lookup"><span data-stu-id="c192c-113">Implementing a Video DSP Plug-in</span></span>

<span data-ttu-id="c192c-114">Los adaptadores de pantalla de vídeo del equipo admiten un conjunto de formatos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c192c-114">Computer video display adapters support a set of video formats.</span></span> <span data-ttu-id="c192c-115">Los códecs de vídeo digital también admiten un conjunto de formatos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c192c-115">Digital video codecs also support a set of video formats.</span></span> <span data-ttu-id="c192c-116">Al intentar reproducir un archivo de vídeo determinado, Windows Media Player debe elegir el formato que se va a usar para la representación.</span><span class="sxs-lookup"><span data-stu-id="c192c-116">When attempting to play a particular video file, Windows Media Player must choose a format to use for rendering.</span></span> <span data-ttu-id="c192c-117">El reproductor intenta encontrar la mejor coincidencia entre los formatos admitidos por el códec de vídeo y los formatos admitidos por el adaptador de pantalla de vídeo, es decir, el que produce la máxima calidad.</span><span class="sxs-lookup"><span data-stu-id="c192c-117">The Player attempts to find the best match between the formats supported by the video codec and the formats supported by the video display adapter—that is, the one that yields the highest quality.</span></span>

<span data-ttu-id="c192c-118">Para crear un complemento DSP de Windows Media Player que procese el vídeo, primero deberá decidir qué formatos de vídeo quiere que procese el complemento.</span><span class="sxs-lookup"><span data-stu-id="c192c-118">To create a Windows Media Player DSP plug-in that processes video, you'll first need to decide which video formats you'd like your plug-in to process.</span></span> <span data-ttu-id="c192c-119">El complemento DSP de vídeo de ejemplo funciona con los siguientes formatos de vídeo:</span><span class="sxs-lookup"><span data-stu-id="c192c-119">The sample video DSP plug-in works with the following video formats:</span></span>

-   <span data-ttu-id="c192c-120">NV12</span><span class="sxs-lookup"><span data-stu-id="c192c-120">NV12</span></span>
-   <span data-ttu-id="c192c-121">YV12</span><span class="sxs-lookup"><span data-stu-id="c192c-121">YV12</span></span>
-   <span data-ttu-id="c192c-122">YUY2</span><span class="sxs-lookup"><span data-stu-id="c192c-122">YUY2</span></span>
-   <span data-ttu-id="c192c-123">UYVY</span><span class="sxs-lookup"><span data-stu-id="c192c-123">UYVY</span></span>
-   <span data-ttu-id="c192c-124">RGB32</span><span class="sxs-lookup"><span data-stu-id="c192c-124">RGB32</span></span>
-   <span data-ttu-id="c192c-125">RGB24</span><span class="sxs-lookup"><span data-stu-id="c192c-125">RGB24</span></span>
-   <span data-ttu-id="c192c-126">RGB555</span><span class="sxs-lookup"><span data-stu-id="c192c-126">RGB555</span></span>
-   <span data-ttu-id="c192c-127">RGB565</span><span class="sxs-lookup"><span data-stu-id="c192c-127">RGB565</span></span>

<span data-ttu-id="c192c-128">Los formatos que decida procesar dependerán de usted.</span><span class="sxs-lookup"><span data-stu-id="c192c-128">Which formats you choose to process is up to you.</span></span> <span data-ttu-id="c192c-129">Puede quitar formatos del complemento de ejemplo para que no se admitan más tiempo y pueda agregar código para procesar formatos adicionales.</span><span class="sxs-lookup"><span data-stu-id="c192c-129">You can remove formats from the sample plug-in so that they aren't supported any longer and you can add code to process additional formats.</span></span>

<span data-ttu-id="c192c-130">En las secciones siguientes se proporciona información adicional que debe conocer antes de crear su propio complemento DSP de vídeo para Windows Media Player:</span><span class="sxs-lookup"><span data-stu-id="c192c-130">The following sections provide additional information you should know before creating your own video DSP plug-in for Windows Media Player:</span></span>

-   [<span data-ttu-id="c192c-131">Negociación del formato de vídeo en el complemento DSP de vídeo de ejemplo</span><span class="sxs-lookup"><span data-stu-id="c192c-131">Video Format Negotiation in the Sample Video DSP Plug-in</span></span>](video-format-negotiation-in-the-sample-video-dsp-plug-in.md)
-   [<span data-ttu-id="c192c-132">DoProcessOutput en el complemento DSP de vídeo de ejemplo</span><span class="sxs-lookup"><span data-stu-id="c192c-132">DoProcessOutput in the Sample Video DSP Plug-in</span></span>](doprocessoutput-in-the-sample-video-dsp-plug-in.md)
-   [<span data-ttu-id="c192c-133">Procesamiento del vídeo</span><span class="sxs-lookup"><span data-stu-id="c192c-133">Processing the Video</span></span>](processing-the-video.md)

## <a name="related-topics"></a><span data-ttu-id="c192c-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c192c-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c192c-135">**Implementación del código DSP**</span><span class="sxs-lookup"><span data-stu-id="c192c-135">**Implementing Your DSP Code**</span></span>](implementing-your-dsp-code.md)
</dt> </dl>

 

 




