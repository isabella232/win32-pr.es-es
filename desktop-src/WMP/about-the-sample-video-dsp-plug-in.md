---
title: Acerca del complemento DSP de vídeo de ejemplo
description: Acerca del complemento DSP de vídeo de ejemplo
ms.assetid: f2ba8e9d-a0e4-4679-99dc-2bfe9e451ffd
keywords:
- Complementos de Media Player de Windows, ejemplos
- complementos, ejemplos
- Complementos de procesamiento de señal digital, ejemplos
- Complementos DSP, ejemplos
- Complementos de Windows Media Player, DSP de vídeo
- complementos, DSP de vídeo
- Complementos de procesamiento de señal digital, ejemplos de vídeo
- Complementos DSP, ejemplos de vídeo
- ejemplos, Complementos DSP
- Complementos de DSP de vídeo, ejemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ede2eda82c834cefad0e31009805f24941cd4a6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695240"
---
# <a name="about-the-sample-video-dsp-plug-in"></a><span data-ttu-id="977b3-113">Acerca del complemento DSP de vídeo de ejemplo</span><span class="sxs-lookup"><span data-stu-id="977b3-113">About the Sample Video DSP Plug-in</span></span>

<span data-ttu-id="977b3-114">El complemento DSP de vídeo de ejemplo proporciona una implementación de procesamiento simple que escala la saturación de color del vídeo en un factor proporcionado por el usuario en la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="977b3-114">The sample video DSP plug-in provides a simple processing implementation that scales the color saturation of the video by a factor provided by the user in the property page.</span></span> <span data-ttu-id="977b3-115">El complemento acepta valores entre cero y 1.</span><span class="sxs-lookup"><span data-stu-id="977b3-115">The plug-in accepts values between zero and 1.</span></span> <span data-ttu-id="977b3-116">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="977b3-116">The default value is 1.</span></span> <span data-ttu-id="977b3-117">Un valor de 1 no tiene ningún efecto sobre la imagen de vídeo. otros factores de escala desaturan el color de la imagen.</span><span class="sxs-lookup"><span data-stu-id="977b3-117">A value of 1 has no effect upon the video image; other scale factors desaturate the image color.</span></span> <span data-ttu-id="977b3-118">Por ejemplo, un valor de 0,5 daría como resultado una saturación de color del 50%.</span><span class="sxs-lookup"><span data-stu-id="977b3-118">For instance, a value of .5 would result in 50 percent color saturation.</span></span> <span data-ttu-id="977b3-119">Un valor de cero da como resultado un vídeo de escala de grises.</span><span class="sxs-lookup"><span data-stu-id="977b3-119">A value of zero results in grayscale video.</span></span>

<span data-ttu-id="977b3-120">El complemento DSP de vídeo de ejemplo funciona con los siguientes formatos de vídeo:</span><span class="sxs-lookup"><span data-stu-id="977b3-120">The sample video DSP plug-in works with the following video formats:</span></span>

-   <span data-ttu-id="977b3-121">NV12</span><span class="sxs-lookup"><span data-stu-id="977b3-121">NV12</span></span>
-   <span data-ttu-id="977b3-122">YV12</span><span class="sxs-lookup"><span data-stu-id="977b3-122">YV12</span></span>
-   <span data-ttu-id="977b3-123">YUY2</span><span class="sxs-lookup"><span data-stu-id="977b3-123">YUY2</span></span>
-   <span data-ttu-id="977b3-124">UYVY</span><span class="sxs-lookup"><span data-stu-id="977b3-124">UYVY</span></span>
-   <span data-ttu-id="977b3-125">RGB32</span><span class="sxs-lookup"><span data-stu-id="977b3-125">RGB32</span></span>
-   <span data-ttu-id="977b3-126">RGB24</span><span class="sxs-lookup"><span data-stu-id="977b3-126">RGB24</span></span>
-   <span data-ttu-id="977b3-127">RGB555</span><span class="sxs-lookup"><span data-stu-id="977b3-127">RGB555</span></span>
-   <span data-ttu-id="977b3-128">RGB565</span><span class="sxs-lookup"><span data-stu-id="977b3-128">RGB565</span></span>

## <a name="related-topics"></a><span data-ttu-id="977b3-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="977b3-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="977b3-130">**Crear un complemento DSP**</span><span class="sxs-lookup"><span data-stu-id="977b3-130">**Building a DSP Plug-in**</span></span>](building-a-dsp-plug-in.md)
</dt> </dl>

 

 




