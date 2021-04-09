---
title: Obtener buenos resultados con el códec de pantalla de Windows Media Video 9
description: Obtener buenos resultados con el códec de pantalla de Windows Media Video 9
ms.assetid: c5b080d3-2934-4af7-8f01-9ab0829db05d
keywords:
- Códec de pantalla de Windows Media Format, Windows Media Video 9
- Códec Advanced Systems Format (ASF), Windows Media Video 9 Screen Codec
- ASF (formato de sistemas avanzados), códec de pantalla de Windows Media Video 9
- códecs, pantalla de Windows Media Video 9
- Códec de pantalla de Windows Media Video 9, resultados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a297638c7c50a6380fd4c43ea1d4b9971d44db5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103994964"
---
# <a name="getting-good-results-with-the-windows-media-video-9-screen-codec"></a><span data-ttu-id="d605b-108">Obtener buenos resultados con el códec de pantalla de Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="d605b-108">Getting Good Results with the Windows Media Video 9 Screen Codec</span></span>

<span data-ttu-id="d605b-109">El códec de pantalla de Windows Media Video 9 está diseñado para generar vídeo muy comprimido para la captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="d605b-109">The Windows Media Video 9 Screen codec is designed to produce highly compressed video for screen capture.</span></span> <span data-ttu-id="d605b-110">Dado que la mayoría de las necesidades de captura de pantalla implican imágenes bastante simples y estáticas, los altos niveles de compresión que se alcanzan no suelen significar un gran sacrificio de la calidad de la imagen.</span><span class="sxs-lookup"><span data-stu-id="d605b-110">Because most of the need for screen capture involves fairly simple and static images, the high levels of compression attained do not usually mean a great sacrifice in image quality.</span></span> <span data-ttu-id="d605b-111">Sin embargo, cada captura de pantalla es diferente y la calidad de la imagen resultante puede variar considerablemente en función de las circunstancias.</span><span class="sxs-lookup"><span data-stu-id="d605b-111">However, each screen capture is different, and the resulting image quality can vary considerably depending upon the circumstances.</span></span>

<span data-ttu-id="d605b-112">La mejor manera de determinar la configuración de perfil para una sesión de códec de pantalla es codificar un archivo de prueba mediante un flujo de velocidad de bits variable basado en la calidad.</span><span class="sxs-lookup"><span data-stu-id="d605b-112">The best way to determine the profile settings for a screen codec session is to encode a test file using a quality-based variable bit rate stream.</span></span> <span data-ttu-id="d605b-113">Establezca la calidad en el valor que desee y codifique una captura de pantalla como si estuviera grabando el archivo final.</span><span class="sxs-lookup"><span data-stu-id="d605b-113">Set the quality to the value you desire, and encode a screen capture as if you were recording the final file.</span></span> <span data-ttu-id="d605b-114">Cuando se escribe el archivo, reproduzca el uso del objeto lector asincrónico y realice llamadas regulares a [**IWMReaderAdvanced:: GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics).</span><span class="sxs-lookup"><span data-stu-id="d605b-114">When the file is written, play it using the asynchronous reader object, making regular calls to [**IWMReaderAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics).</span></span> <span data-ttu-id="d605b-115">Al supervisar el valor del miembro **dwBandwidth** de la estructura [**de \_ \_ estadísticas del lector de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) para cada llamada, puede determinar la velocidad de bits aproximada necesaria para lograr la calidad deseada.</span><span class="sxs-lookup"><span data-stu-id="d605b-115">By monitoring the value of the **dwBandwidth** member of the [**WM\_READER\_STATISTICS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) structure for each call, you can determine the approximate bit rate required to achieve the quality you want.</span></span> <span data-ttu-id="d605b-116">Después, puede usar esa velocidad de bits para la codificación de velocidad de bits constante.</span><span class="sxs-lookup"><span data-stu-id="d605b-116">You can then use that bit rate for constant bit rate encoding.</span></span>

<span data-ttu-id="d605b-117">Si descubre que la calidad deseada requiere una velocidad de bits superior a la que puede usar para el escenario de entrega, puede probar las siguientes técnicas para obtener una mayor eficacia del códec.</span><span class="sxs-lookup"><span data-stu-id="d605b-117">If you discover that the quality you want requires a higher bit rate than you can use for your delivery scenario, you can try the following techniques to get more efficiency from the codec.</span></span>

-   <span data-ttu-id="d605b-118">Use una resolución más pequeña para la captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="d605b-118">Use a smaller resolution for the screen capture.</span></span> <span data-ttu-id="d605b-119">La captura de una resolución de pantalla mayor que la que necesita también puede crear confusión en el visor presentando más información de la necesaria.</span><span class="sxs-lookup"><span data-stu-id="d605b-119">Capturing a larger screen resolution than you need can also create confusion for the viewer by presenting more information than is needed.</span></span>
-   <span data-ttu-id="d605b-120">Use menos gráficos en la captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="d605b-120">Use fewer graphics in the screen capture.</span></span> <span data-ttu-id="d605b-121">El códec de pantalla de Windows Media Video 9 está optimizado para codificar texto y primitivas de Windows con alta calidad.</span><span class="sxs-lookup"><span data-stu-id="d605b-121">The Windows Media Video 9 Screen codec is optimized to encode Windows primitives and text with high quality.</span></span> <span data-ttu-id="d605b-122">Normalmente, los problemas se producen debido a los gráficos de mapa Dete, que a menudo contienen miles de colores individuales.</span><span class="sxs-lookup"><span data-stu-id="d605b-122">Usually problems occur because of bitmapped graphics, which often contain thousands of individual colors.</span></span> <span data-ttu-id="d605b-123">Cuantos menos mapas de bits haya en la pantalla al capturar, mejor serán los resultados.</span><span class="sxs-lookup"><span data-stu-id="d605b-123">The fewer bitmaps that are on the screen when you capture, the better your results will be.</span></span> <span data-ttu-id="d605b-124">Si no puede eliminar gráficos de la captura de pantalla, hay varias maneras de minimizar el impacto que tiene un mapa de bits en la calidad de la imagen:</span><span class="sxs-lookup"><span data-stu-id="d605b-124">If you cannot eliminate graphics from your screen capture, there are several ways to minimize the impact a bitmap has on image quality:</span></span>
    -   <span data-ttu-id="d605b-125">Reduzca el tamaño del gráfico.</span><span class="sxs-lookup"><span data-stu-id="d605b-125">Reduce the size of the graphic.</span></span>
    -   <span data-ttu-id="d605b-126">Reducir el número de gráficos individuales que aparecen en la pantalla al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="d605b-126">Reduce the number of individual graphics that appear on the screen concurrently.</span></span>
    -   <span data-ttu-id="d605b-127">Reduzca la cantidad de movimiento del gráfico.</span><span class="sxs-lookup"><span data-stu-id="d605b-127">Reduce the amount of movement of the graphic.</span></span> <span data-ttu-id="d605b-128">Por ejemplo, si el gráfico está en una ventana, mantenga la ventana como estacional como sea posible.</span><span class="sxs-lookup"><span data-stu-id="d605b-128">For example, if the graphic is in a window, keep the window as stationary as possible.</span></span>
    -   <span data-ttu-id="d605b-129">Evite mover el puntero del mouse sobre el gráfico o arrastrar ventanas u otros elementos sobre el gráfico.</span><span class="sxs-lookup"><span data-stu-id="d605b-129">Avoid moving the mouse pointer over the graphic, or dragging windows or other elements over the graphic.</span></span>
-   <span data-ttu-id="d605b-130">Usar una [*velocidad de fotogramas*](wmformat-glossary.md)más lenta.</span><span class="sxs-lookup"><span data-stu-id="d605b-130">Use a slower [*frame rate*](wmformat-glossary.md).</span></span> <span data-ttu-id="d605b-131">A menudo, las capturas de pantalla pueden ser eficaces a velocidades de fotogramas muy bajas (a veces, como mínimo, 4 o 5 fotogramas por segundo).</span><span class="sxs-lookup"><span data-stu-id="d605b-131">Screen captures can often be effective at very low frame rates (sometimes as low as 4 or 5 frames per second).</span></span>
-   <span data-ttu-id="d605b-132">Reduzca la velocidad de bits del audio que lo acompaña.</span><span class="sxs-lookup"><span data-stu-id="d605b-132">Reduce the bit rate of the accompanying audio.</span></span>

<span data-ttu-id="d605b-133">Además, el códec no admite el cambio de tamaño del rectángulo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d605b-133">Also, the codec does not support resizing of the video rectangle.</span></span> <span data-ttu-id="d605b-134">En otras palabras, si intenta usar el códec para codificar una pantalla de 800 x 600 en un rectángulo de vídeo de 640 x 480, el vídeo resultante tendrá artefactos significativos que pueden hacer que la gran parte del texto de la pantalla sea ilegible.</span><span class="sxs-lookup"><span data-stu-id="d605b-134">In other words, if you try to use the codec to encode a 800 x 600 screen down into to a 640 x 480 video rectangle, the resulting video will have significant artifacts that may make much of the text on the screen illegible.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d605b-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d605b-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d605b-136">**Configurar secuencias de captura de pantalla**</span><span class="sxs-lookup"><span data-stu-id="d605b-136">**Configuring Screen Capture Streams**</span></span>](configuring-screen-capture-streams.md)
</dt> <dt>

[<span data-ttu-id="d605b-137">**Configuración de secuencias**</span><span class="sxs-lookup"><span data-stu-id="d605b-137">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




