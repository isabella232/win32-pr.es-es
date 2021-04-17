---
description: Usar el códec de pantalla de Windows Media Video 9
ms.assetid: d88d5f5e-0935-4bbe-8abf-72cc536f9b40
title: Usar el códec de pantalla de Windows Media Video 9 (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b825e053c4c732481c8d1ca5d4dc972f804f262a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105689618"
---
# <a name="using-the-windows-media-video-9-screen-codec-microsoft-media-foundation"></a><span data-ttu-id="4a66f-103">Usar el códec de pantalla de Windows Media Video 9 (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="4a66f-103">Using the Windows Media Video 9 Screen Codec (Microsoft Media Foundation)</span></span>

<span data-ttu-id="4a66f-104">El códec de pantalla de Windows Media Video 9 está optimizado para comprimir el vídeo de la *aplicación*, que consta de capturas de pantalla consecutivas para una pantalla del equipo.</span><span class="sxs-lookup"><span data-stu-id="4a66f-104">The Windows Media Video 9 Screen codec is optimized for compressing *application video*, which consists of consecutive screen shots for a computer display.</span></span> <span data-ttu-id="4a66f-105">El códec aprovecha la simplicidad de imagen típica (relativamente pocos colores, muchas líneas rectas, etc.) y la falta de movimiento relativo para lograr una relación de compresión muy alta.</span><span class="sxs-lookup"><span data-stu-id="4a66f-105">The codec takes advantage of the typical image simplicity (relatively few colors, lots of straight lines, and so on) and relative lack of motion to achieve a very high compression ratio.</span></span> <span data-ttu-id="4a66f-106">El inconveniente de esta optimización es que el vídeo que no se ajusta a las características esperadas del vídeo de la aplicación puede ser difícil de comprimir con un nivel de calidad aceptable.</span><span class="sxs-lookup"><span data-stu-id="4a66f-106">The disadvantage of this optimization is that video that doesn't conform to the expected characteristics of application video can be difficult to compress with an acceptable level of quality.</span></span>

<span data-ttu-id="4a66f-107">El codificador de pantalla de Windows Media Video 9 se identifica mediante el identificador de clase CLSID \_ CMSSEncMediaObject2 y el descodificador identifica el identificador de clase CLSID \_ CMSSDecMediaObject.</span><span class="sxs-lookup"><span data-stu-id="4a66f-107">The Windows Media Video 9 Screen encoder is identified by the class identifier CLSID\_CMSSEncMediaObject2, and the decoder is identified the class identifier CLSID\_CMSSDecMediaObject.</span></span> <span data-ttu-id="4a66f-108">El valor FOURCC para los tipos de medios que usan este códec es "MSS2".</span><span class="sxs-lookup"><span data-stu-id="4a66f-108">The FOURCC value for media types using this codec is "MSS2".</span></span>

## <a name="configuring-the-encoder"></a><span data-ttu-id="4a66f-109">Configurar el codificador</span><span class="sxs-lookup"><span data-stu-id="4a66f-109">Configuring the Encoder</span></span>

<span data-ttu-id="4a66f-110">El codificador del códec de pantalla de Windows Media Video 9 se configura de la misma manera que el descodificador de vídeo estándar.</span><span class="sxs-lookup"><span data-stu-id="4a66f-110">The encoder of the Windows Media Video 9 Screen codec is configured in the same way as the standard video decoder.</span></span>

> [!Note]  
> <span data-ttu-id="4a66f-111">El codificador de pantalla solo admite la codificación de un paso.</span><span class="sxs-lookup"><span data-stu-id="4a66f-111">The screen encoder supports only one-pass encoding.</span></span> <span data-ttu-id="4a66f-112">Puede establecer la propiedad [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) en 2 y procesar las entradas dos veces sin errores, pero no hay ninguna ventaja para hacerlo.</span><span class="sxs-lookup"><span data-stu-id="4a66f-112">You can set the [MFPKEY\_PASSESUSED](mfpkey-passesusedproperty.md) property to 2 and process the inputs twice without error, but there is no benefit to doing so.</span></span> <span data-ttu-id="4a66f-113">Se trata de un problema conocido y puede corregirse en futuras versiones.</span><span class="sxs-lookup"><span data-stu-id="4a66f-113">This is a known issue and may be corrected in future releases.</span></span>

 

## <a name="getting-the-best-results"></a><span data-ttu-id="4a66f-114">Obtener los mejores resultados</span><span class="sxs-lookup"><span data-stu-id="4a66f-114">Getting the Best Results</span></span>

<span data-ttu-id="4a66f-115">Si descubre que la calidad que desea en el contenido de captura de pantalla requiere una velocidad de bits superior a la que puede usar para el escenario de entrega, puede probar las siguientes técnicas para obtener una mayor eficacia del códec:</span><span class="sxs-lookup"><span data-stu-id="4a66f-115">If you discover that the quality you want in your screen capture content requires a higher bit rate than you can use for your delivery scenario, you can try the following techniques to get more efficiency from the codec:</span></span>

-   <span data-ttu-id="4a66f-116">Use una resolución más pequeña para la captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="4a66f-116">Use a smaller resolution for the screen capture.</span></span> <span data-ttu-id="4a66f-117">La captura de una resolución de pantalla mayor que la necesaria puede confundir al visor presentando información innecesaria.</span><span class="sxs-lookup"><span data-stu-id="4a66f-117">Capturing a larger screen resolution than needed can confuse the viewer by presenting unnecessary information.</span></span>
-   <span data-ttu-id="4a66f-118">Usar una velocidad de fotogramas más lenta.</span><span class="sxs-lookup"><span data-stu-id="4a66f-118">Use a slower frame rate.</span></span> <span data-ttu-id="4a66f-119">A menudo, las capturas de pantalla pueden ser eficaces a velocidades de fotogramas muy bajas (a veces, como mínimo, 4 o 5 fotogramas por segundo).</span><span class="sxs-lookup"><span data-stu-id="4a66f-119">Screen captures can often be effective at very low frame rates (sometimes as low as 4 or 5 frames per second).</span></span>
-   <span data-ttu-id="4a66f-120">Use menos gráficos en la captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="4a66f-120">Use fewer graphics in the screen capture.</span></span> <span data-ttu-id="4a66f-121">El códec de pantalla de Windows Media Video 9 está optimizado para codificar texto y primitivas de Windows con alta calidad.</span><span class="sxs-lookup"><span data-stu-id="4a66f-121">The Windows Media Video 9 Screen codec is optimized to encode Windows primitives and text with high quality.</span></span> <span data-ttu-id="4a66f-122">Normalmente, los problemas se producen debido a los gráficos de mapa Dete, que a menudo contienen miles de colores individuales.</span><span class="sxs-lookup"><span data-stu-id="4a66f-122">Usually problems occur because of bitmapped graphics, which often contain thousands of individual colors.</span></span> <span data-ttu-id="4a66f-123">Cuantos menos mapas de bits haya en la pantalla al capturar, mejor serán los resultados.</span><span class="sxs-lookup"><span data-stu-id="4a66f-123">The fewer bitmaps that are on the screen when you capture, the better your results will be.</span></span> <span data-ttu-id="4a66f-124">Si no puede eliminar gráficos de la captura de pantalla, hay varias maneras de minimizar el impacto que tiene un mapa de bits en la calidad de la imagen:</span><span class="sxs-lookup"><span data-stu-id="4a66f-124">If you cannot eliminate graphics from your screen capture, there are several ways to minimize the impact that a bitmap has on image quality:</span></span>
    -   <span data-ttu-id="4a66f-125">Reduzca el tamaño del gráfico.</span><span class="sxs-lookup"><span data-stu-id="4a66f-125">Reduce the size of the graphic.</span></span>
    -   <span data-ttu-id="4a66f-126">Reducir el número de gráficos individuales que aparecen en la pantalla al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="4a66f-126">Reduce the number of individual graphics that appear on the screen at the same time.</span></span>
    -   <span data-ttu-id="4a66f-127">Reduzca la cantidad de movimiento del gráfico.</span><span class="sxs-lookup"><span data-stu-id="4a66f-127">Reduce the amount of movement of the graphic.</span></span> <span data-ttu-id="4a66f-128">Por ejemplo, si el gráfico está en una ventana, mantenga la ventana como estacional como sea posible.</span><span class="sxs-lookup"><span data-stu-id="4a66f-128">For example, if the graphic is in a window, keep the window as stationary as possible.</span></span>
    -   <span data-ttu-id="4a66f-129">Evite mover el puntero del mouse sobre el gráfico o arrastrar ventanas u otros elementos sobre el gráfico.</span><span class="sxs-lookup"><span data-stu-id="4a66f-129">Avoid moving the mouse pointer over the graphic, or dragging windows or other elements over the graphic.</span></span>

## <a name="decoding"></a><span data-ttu-id="4a66f-130">Descodificación</span><span class="sxs-lookup"><span data-stu-id="4a66f-130">Decoding</span></span>

<span data-ttu-id="4a66f-131">No hay ningún requisito especial para descodificar el vídeo de captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="4a66f-131">There are no special requirements for decoding screen capture video.</span></span> <span data-ttu-id="4a66f-132">Sin embargo, al igual que con todos los códecs de Windows Media Video 9, el descodificador de captura de pantalla no puede descomprimir correctamente el contenido codificado sin los datos privados del códec.</span><span class="sxs-lookup"><span data-stu-id="4a66f-132">However, as with all Windows Media Video 9 codecs, the screen capture decoder cannot properly decompress the encoded content without the codec private data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a66f-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4a66f-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a66f-134">Configuración de la codificación de vídeo</span><span class="sxs-lookup"><span data-stu-id="4a66f-134">Configuring Video Encoding</span></span>](configuringvideoencoding.md)
</dt> <dt>

[<span data-ttu-id="4a66f-135">Uso de datos privados de códecs de vídeo</span><span class="sxs-lookup"><span data-stu-id="4a66f-135">Using Video Codec Private Data</span></span>](usingvideocodecprivatedata.md)
</dt> <dt>

[<span data-ttu-id="4a66f-136">Codificador de pantalla de Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="4a66f-136">Windows Media Video 9 Screen Encoder</span></span>](windowsmediavideo9screenencoder.md)
</dt> <dt>

[<span data-ttu-id="4a66f-137">Trabajar con vídeo</span><span class="sxs-lookup"><span data-stu-id="4a66f-137">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



