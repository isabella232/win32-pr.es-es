---
title: Configuración de secuencias de vídeo para buscar rendimiento
description: Configuración de secuencias de vídeo para buscar rendimiento
ms.assetid: 2df507f9-60a5-4489-b3db-7fe15604e625
keywords:
- flujos, configurar secuencias de vídeo
- códecs, configurar secuencias de vídeo
- secuencias de vídeo, configurar
- secuencias de vídeo, rendimiento
- rendimiento, secuencias de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33b4fc68e0b3a91cf135d29dc7123d5af88db84c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788716"
---
# <a name="configuring-video-streams-for-seeking-performance"></a><span data-ttu-id="8d7b5-108">Configuración de secuencias de vídeo para buscar rendimiento</span><span class="sxs-lookup"><span data-stu-id="8d7b5-108">Configuring Video Streams for Seeking Performance</span></span>

<span data-ttu-id="8d7b5-109">Algunas aplicaciones de reproducción realizan muchas búsquedas en flujos individuales.</span><span class="sxs-lookup"><span data-stu-id="8d7b5-109">Some playback applications perform a lot of seeking on individual streams.</span></span> <span data-ttu-id="8d7b5-110">La búsqueda es un área en la que el rendimiento puede variar considerablemente en función de la configuración de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="8d7b5-110">Seeking is an area where performance can vary greatly depending upon the settings of the stream.</span></span> <span data-ttu-id="8d7b5-111">Si sabe que el contenido debe optimizarse para una búsqueda rápida, puede adaptar la configuración del flujo para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="8d7b5-111">If you know your content needs to be optimized for quick seeking, you can tailor your stream configuration to improve performance.</span></span>

<span data-ttu-id="8d7b5-112">El mayor factor que afecta a la velocidad de las operaciones de búsqueda en vídeo es el espaciado de los fotogramas clave.</span><span class="sxs-lookup"><span data-stu-id="8d7b5-112">The biggest factor affecting the speed of seeking operations in video is the spacing of the key frames.</span></span> <span data-ttu-id="8d7b5-113">Dado que cada fotograma entre fotogramas clave debe reconstruirse en función de los fotogramas anteriores, los fotogramas clave muy espaciados resultan en tiempos de búsqueda más largos.</span><span class="sxs-lookup"><span data-stu-id="8d7b5-113">Because every frame between key frames needs to be reconstructed based on the frames that come before it, widely spaced key frames result longer seek times.</span></span> <span data-ttu-id="8d7b5-114">Por ejemplo, si una secuencia de vídeo con 30 fotogramas por segundo tiene un espaciado de fotogramas de clave máximo de 10 segundos, habrá fotogramas potencialmente 300 entre fotogramas clave.</span><span class="sxs-lookup"><span data-stu-id="8d7b5-114">For example, if a video stream with 30 frames per second has a maximum key-frame spacing of 10 seconds, there are potentially 300 frames between key frames.</span></span> <span data-ttu-id="8d7b5-115">Si busca en el último [*fotograma Delta*](wmformat-glossary.md), se deben reconstruir 299 fotogramas para que el fotograma se descomprime.</span><span class="sxs-lookup"><span data-stu-id="8d7b5-115">If you seek to the last [*delta frame*](wmformat-glossary.md), 299 frames have to be reconstructed for the frame to be decompressed.</span></span> <span data-ttu-id="8d7b5-116">Si cada reconstrucción del fotograma tardó .01 segundo, la búsqueda tardaría casi 3 segundos.</span><span class="sxs-lookup"><span data-stu-id="8d7b5-116">If each frame reconstruction took .01 second, the seek would take almost 3 seconds.</span></span> <span data-ttu-id="8d7b5-117">Si desea aumentar la eficacia de la búsqueda, puede ser útil reducir el espaciado de fotogramas clave.</span><span class="sxs-lookup"><span data-stu-id="8d7b5-117">If you want to increase the efficiency of seeking, lowering the key-frame spacing can help.</span></span> <span data-ttu-id="8d7b5-118">Sin embargo, si establece los fotogramas clave demasiado próximos, puede perder calidad.</span><span class="sxs-lookup"><span data-stu-id="8d7b5-118">However, if you set the key frames too close together, you can lose quality.</span></span>

<span data-ttu-id="8d7b5-119">Puede establecer el espaciado máximo de fotogramas clave mediante una llamada a [**IWMVideoMediaProps:: SetMaxKeyFrameSpacing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setmaxkeyframespacing).</span><span class="sxs-lookup"><span data-stu-id="8d7b5-119">You can set the maximum key-frame spacing by calling [**IWMVideoMediaProps::SetMaxKeyFrameSpacing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setmaxkeyframespacing).</span></span> <span data-ttu-id="8d7b5-120">En la tabla siguiente se enumeran los valores recomendados, en función de la velocidad de bits de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="8d7b5-120">The recommended values, based on the bit rate of the stream, are listed in the following table.</span></span> <span data-ttu-id="8d7b5-121">Estos valores proporcionan un buen equilibrio de búsqueda de rendimiento y calidad.</span><span class="sxs-lookup"><span data-stu-id="8d7b5-121">These values provide a good balance of seeking performance and quality.</span></span> <span data-ttu-id="8d7b5-122">El SDK no impone ningún límite en el tiempo entre fotogramas clave.</span><span class="sxs-lookup"><span data-stu-id="8d7b5-122">The SDK does not enforce any limit on the time between key frames.</span></span> <span data-ttu-id="8d7b5-123">En general, los tiempos de más de 30 segundos pueden afectar negativamente a los tiempos de búsqueda cuando el contenido se transmite por secuencias a través de una red y cuando se reproduce de forma local.</span><span class="sxs-lookup"><span data-stu-id="8d7b5-123">In general, times longer than 30 seconds can adversely affect seek times both when the content is streamed over a network, and when it is played back locally.</span></span>



| <span data-ttu-id="8d7b5-124">Velocidad de bits</span><span class="sxs-lookup"><span data-stu-id="8d7b5-124">Bit rate</span></span>             | <span data-ttu-id="8d7b5-125">Espaciado máximo sugerido de fotogramas clave</span><span class="sxs-lookup"><span data-stu-id="8d7b5-125">Suggested maximum key-frame spacing</span></span> |
|----------------------|-------------------------------------|
| <span data-ttu-id="8d7b5-126">22 Kbps a 300 kbps</span><span class="sxs-lookup"><span data-stu-id="8d7b5-126">22 Kbps to 300 Kbps</span></span>  | <span data-ttu-id="8d7b5-127">8 segundos</span><span class="sxs-lookup"><span data-stu-id="8d7b5-127">8 seconds</span></span>                           |
| <span data-ttu-id="8d7b5-128">300 kbps a 600 Kbps</span><span class="sxs-lookup"><span data-stu-id="8d7b5-128">300 Kbps to 600 Kbps</span></span> | <span data-ttu-id="8d7b5-129">6 segundos</span><span class="sxs-lookup"><span data-stu-id="8d7b5-129">6 seconds</span></span>                           |
| <span data-ttu-id="8d7b5-130">600 Kbps a 2 Mbps</span><span class="sxs-lookup"><span data-stu-id="8d7b5-130">600 Kbps to 2 Mbps</span></span>   | <span data-ttu-id="8d7b5-131">4 segundos</span><span class="sxs-lookup"><span data-stu-id="8d7b5-131">4 seconds</span></span>                           |
| <span data-ttu-id="8d7b5-132">2 Mbps y superior</span><span class="sxs-lookup"><span data-stu-id="8d7b5-132">2 Mbps and higher</span></span>    | <span data-ttu-id="8d7b5-133">3 segundos</span><span class="sxs-lookup"><span data-stu-id="8d7b5-133">3 seconds</span></span>                           |



 

<span data-ttu-id="8d7b5-134">Para obtener más información sobre cómo obtener el mejor rendimiento al buscar archivos de vídeo, consulte [obtención del mejor rendimiento de búsqueda de vídeo](getting-the-best-video-seeking-performance.md).</span><span class="sxs-lookup"><span data-stu-id="8d7b5-134">For more information about getting the best performance when seeking video files, see [Getting the Best Video Seeking Performance](getting-the-best-video-seeking-performance.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d7b5-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8d7b5-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d7b5-136">**Configuración de secuencias**</span><span class="sxs-lookup"><span data-stu-id="8d7b5-136">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




