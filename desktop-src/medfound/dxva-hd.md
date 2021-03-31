---
description: Microsoft DirectX video Acceleration High Definition (DXVA-HD) es una API para el procesamiento de vídeo acelerado por hardware.
ms.assetid: 38ebec28-c4fc-4e72-ac87-1e41707d1908
title: DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f8694a28d8d5871112590c90bf166d1aa9246e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808090"
---
# <a name="dxva-hd"></a><span data-ttu-id="32f05-103">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="32f05-103">DXVA-HD</span></span>

<span data-ttu-id="32f05-104">Microsoft DirectX video Acceleration High Definition (DXVA-HD) es una API para el procesamiento de vídeo acelerado por hardware.</span><span class="sxs-lookup"><span data-stu-id="32f05-104">Microsoft DirectX Video Acceleration High Definition (DXVA-HD) is an API for hardware-accelerated video processing.</span></span> <span data-ttu-id="32f05-105">DXVA-HD usa la GPU para realizar funciones como desentrelazado, composición y conversión de espacio de color.</span><span class="sxs-lookup"><span data-stu-id="32f05-105">DXVA-HD uses the GPU to perform functions such as deinterlacing, compositing, and color-space conversion.</span></span>

<span data-ttu-id="32f05-106">DXVA-HD es similar al [procesamiento de vídeo de DXVA](dxva-video-processing.md) (DXVA-VP), pero ofrece características mejoradas y un modelo de procesamiento más sencillo.</span><span class="sxs-lookup"><span data-stu-id="32f05-106">DXVA-HD is similar to [DXVA Video Processing](dxva-video-processing.md) (DXVA-VP), but offers enhanced features and a simpler processing model.</span></span> <span data-ttu-id="32f05-107">Al proporcionar un modelo de composición más flexible, DXVA-HD está diseñado para admitir la próxima generación de formatos ópticos HD y estándares de difusión.</span><span class="sxs-lookup"><span data-stu-id="32f05-107">By providing a more flexible composition model, DXVA-HD is designed to support the next generation of HD optical formats and broadcast standards.</span></span>

<span data-ttu-id="32f05-108">La API DXVA-HD requiere un controlador de pantalla WDDM que admita la interfaz de controlador de dispositivo (DDI) de DXVA, o bien un procesador de software de complemento.</span><span class="sxs-lookup"><span data-stu-id="32f05-108">The DXVA-HD API requires either a WDDM display driver that supports the DXVA-HD device driver interface (DDI), or a plug-in software processor.</span></span>

-   [<span data-ttu-id="32f05-109">Mejoras en DXVA-VP</span><span class="sxs-lookup"><span data-stu-id="32f05-109">Improvements over DXVA-VP</span></span>](#improvements-over-dxva-vp)
-   [<span data-ttu-id="32f05-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="32f05-110">Related topics</span></span>](#related-topics)

## <a name="improvements-over-dxva-vp"></a><span data-ttu-id="32f05-111">Mejoras en DXVA-VP</span><span class="sxs-lookup"><span data-stu-id="32f05-111">Improvements over DXVA-VP</span></span>

<span data-ttu-id="32f05-112">DXVA-HD expande el conjunto de características que proporciona DXVA-VP.</span><span class="sxs-lookup"><span data-stu-id="32f05-112">DXVA-HD expands the set of features provided by DXVA-VP.</span></span> <span data-ttu-id="32f05-113">Entre las mejoras se incluyen:</span><span class="sxs-lookup"><span data-stu-id="32f05-113">Enhancements include:</span></span>

-   <span data-ttu-id="32f05-114">Combinación de RGB y YUV.</span><span class="sxs-lookup"><span data-stu-id="32f05-114">RGB and YUV mixing.</span></span> <span data-ttu-id="32f05-115">Cualquier flujo puede ser RGB o YUV.</span><span class="sxs-lookup"><span data-stu-id="32f05-115">Any stream can be either RGB or YUV.</span></span> <span data-ttu-id="32f05-116">Ya no hay una distinción entre el flujo principal y los subflujos.</span><span class="sxs-lookup"><span data-stu-id="32f05-116">There is no longer a distinction between the primary stream and the substreams.</span></span>
-   <span data-ttu-id="32f05-117">Desentrelazado de varias secuencias.</span><span class="sxs-lookup"><span data-stu-id="32f05-117">Deinterlacing of multiple streams.</span></span> <span data-ttu-id="32f05-118">Cualquier flujo puede ser progresiva o entrelazado.</span><span class="sxs-lookup"><span data-stu-id="32f05-118">Any stream can be either progressive or interlaced.</span></span> <span data-ttu-id="32f05-119">Además, la cadencia y la velocidad de fotogramas pueden variar de un flujo de entrada a otro.</span><span class="sxs-lookup"><span data-stu-id="32f05-119">Moreover, the cadence and frame rate can can vary from one input stream to the next.</span></span>
-   <span data-ttu-id="32f05-120">Colores de fondo RGB.</span><span class="sxs-lookup"><span data-stu-id="32f05-120">RGB background colors.</span></span> <span data-ttu-id="32f05-121">Anteriormente, solo se admitían los colores de fondo YUV.</span><span class="sxs-lookup"><span data-stu-id="32f05-121">Previously, only YUV background colors were supported.</span></span>
-   <span data-ttu-id="32f05-122">Creación de claves de luminancia.</span><span class="sxs-lookup"><span data-stu-id="32f05-122">Luma keying.</span></span> <span data-ttu-id="32f05-123">Cuando está habilitada la creación de claves de luminancia, los valores de luminancia que se encuentran dentro de un intervalo designado se vuelven transparentes.</span><span class="sxs-lookup"><span data-stu-id="32f05-123">When luma keying is enabled, luma values that fall within a designated range become transparent.</span></span>
-   <span data-ttu-id="32f05-124">Cambio dinámico entre los modos de desentrelazado.</span><span class="sxs-lookup"><span data-stu-id="32f05-124">Dynamic switching between deinterlace modes.</span></span>

<span data-ttu-id="32f05-125">DXVA: HD también define algunas características avanzadas que los controladores pueden admitir.</span><span class="sxs-lookup"><span data-stu-id="32f05-125">DXVA-HD also defines some advanced features that drivers can support.</span></span> <span data-ttu-id="32f05-126">Sin embargo, las aplicaciones no deben suponer que todos los controladores serán compatibles con estas características.</span><span class="sxs-lookup"><span data-stu-id="32f05-126">However, applications should not assume that all drivers will support these features.</span></span> <span data-ttu-id="32f05-127">Las características avanzadas incluyen:</span><span class="sxs-lookup"><span data-stu-id="32f05-127">The advanced features include:</span></span>

-   <span data-ttu-id="32f05-128">Telecine inversa (por ejemplo, 60i a 24p).</span><span class="sxs-lookup"><span data-stu-id="32f05-128">Inverse telecine (for example, 60i to 24p).</span></span>
-   <span data-ttu-id="32f05-129">Conversión de velocidad de fotogramas (por ejemplo, 24p a 120P).</span><span class="sxs-lookup"><span data-stu-id="32f05-129">Frame-rate conversion (for example, 24p to 120p).</span></span>
-   <span data-ttu-id="32f05-130">Modos de relleno alfa.</span><span class="sxs-lookup"><span data-stu-id="32f05-130">Alpha-fill modes.</span></span>
-   <span data-ttu-id="32f05-131">Filtro de reducción de ruido y mejora del borde.</span><span class="sxs-lookup"><span data-stu-id="32f05-131">Noise reduction and edge enhancement filtering.</span></span>
-   <span data-ttu-id="32f05-132">Escala no lineal anamorphic.</span><span class="sxs-lookup"><span data-stu-id="32f05-132">Anamorphic non-linear scaling.</span></span>
-   <span data-ttu-id="32f05-133">YCbCr extendido (xvYCC).</span><span class="sxs-lookup"><span data-stu-id="32f05-133">Extended YCbCr (xvYCC).</span></span>

<span data-ttu-id="32f05-134">Esta sección contiene los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="32f05-134">This section contains the following topics.</span></span>

-   [<span data-ttu-id="32f05-135">Creación de un procesador de vídeo DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="32f05-135">Creating a DXVA-HD Video Processor</span></span>](creating-a-dxva-hd-video-processor.md)
-   [<span data-ttu-id="32f05-136">Comprobando formatos de DXVA compatibles: HD</span><span class="sxs-lookup"><span data-stu-id="32f05-136">Checking Supported DXVA-HD Formats</span></span>](checking-supported-dxva-hd-formats.md)
-   [<span data-ttu-id="32f05-137">Creación de superficies de vídeo de HD de DXVA</span><span class="sxs-lookup"><span data-stu-id="32f05-137">Creating DXVA-HD Video Surfaces</span></span>](creating-dxva-hd-video-surfaces.md)
-   [<span data-ttu-id="32f05-138">Configuración de los Estados de la HD de DXVA</span><span class="sxs-lookup"><span data-stu-id="32f05-138">Setting DXVA-HD States</span></span>](setting-dxva-hd-states.md)
-   [<span data-ttu-id="32f05-139">Realización de DXVA: HD blit</span><span class="sxs-lookup"><span data-stu-id="32f05-139">Performing the DXVA-HD Blit</span></span>](performing-the-dxva-hd-blit.md)

## <a name="related-topics"></a><span data-ttu-id="32f05-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="32f05-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32f05-141">Aceleración de vídeo de DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="32f05-141">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> <dt>

[<span data-ttu-id="32f05-142">DXVA: ejemplo HD</span><span class="sxs-lookup"><span data-stu-id="32f05-142">DXVA-HD Sample</span></span>](dxva-hd-sample.md)
</dt> </dl>

 

 



