---
description: Trabajar con fotogramas de vídeo
ms.assetid: a5ad74dd-abfd-4810-a512-42e4b98a6c59
title: Trabajar con fotogramas de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ead597fac5a28befc9c9868485840d03b46e5185
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687720"
---
# <a name="working-with-video-frames"></a><span data-ttu-id="e6e02-103">Trabajar con fotogramas de vídeo</span><span class="sxs-lookup"><span data-stu-id="e6e02-103">Working with Video Frames</span></span>

<span data-ttu-id="e6e02-104">El vídeo sin comprimir es una secuencia de mapas de bits que se reproducen en una sucesión rápida, normalmente a una velocidad de aproximadamente 30 fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="e6e02-104">Uncompressed video is a sequence of bitmaps played in rapid succession, typically at a rate of about 30 frames per second.</span></span> <span data-ttu-id="e6e02-105">Dado que la mayoría del vídeo entra en un gráfico de filtros de DirectShow en formato comprimido, el flujo de vídeo suele pasar por un descodificador para la descompresión.</span><span class="sxs-lookup"><span data-stu-id="e6e02-105">Because most video enters a DirectShow filter graph in a compressed format, the video stream generally goes through a decoder for decompression.</span></span> <span data-ttu-id="e6e02-106">Muchos descodificadores generan datos en formato YUV y dejan la conversión final a RGB para el hardware de vídeo justo antes de la representación.</span><span class="sxs-lookup"><span data-stu-id="e6e02-106">Many decoders output data in a YUV format and leave the final conversion to RGB for the video hardware just prior to rendering.</span></span> <span data-ttu-id="e6e02-107">Si un descodificador usa la aceleración de vídeo de DirectX, el hardware de vídeo realiza el trabajo adicional para descodificar la imagen.</span><span class="sxs-lookup"><span data-stu-id="e6e02-107">If a decoder uses DirectX Video Acceleration, the video hardware performs additional work to decode the image.</span></span> <span data-ttu-id="e6e02-108">Por lo tanto, es posible que no se realice la descompresión final de los mapas de bits hasta que los datos lleguen al hardware de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e6e02-108">Thus, final decompression of the bitmaps may not be performed until the data reaches the video hardware.</span></span>

<span data-ttu-id="e6e02-109">Pero para realizar muchos tipos de análisis, procesamiento o edición de vídeo, a menudo es necesario trabajar en mapas de bits sin comprimir en algún tipo de formato RGB o YUV antes de que se representen o se escriban en el archivo.</span><span class="sxs-lookup"><span data-stu-id="e6e02-109">But to perform many types of video analysis, processing, or editing, it is often necessary to work on uncompressed bitmaps in some type of RGB or YUV format before they are rendered or written to file.</span></span> <span data-ttu-id="e6e02-110">Este trabajo se realiza normalmente en un filtro de transformación basado en la clase base [**CTransformFilter**](ctransformfilter.md) , específicamente en el método **Transform** .</span><span class="sxs-lookup"><span data-stu-id="e6e02-110">This work is typically done within a transform filter based on the [**CTransformFilter**](ctransformfilter.md) base class, specifically in the **Transform** method.</span></span> <span data-ttu-id="e6e02-111">Este método recibe un puntero a un objeto [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) que encapsula los datos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e6e02-111">This method receives a pointer to an [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) object that encapsulates the video data.</span></span> <span data-ttu-id="e6e02-112">El método **IMediaSample:: GetPointer** devuelve un puntero al primer byte de los datos sin procesar.</span><span class="sxs-lookup"><span data-stu-id="e6e02-112">The **IMediaSample::GetPointer** method returns a pointer to the first byte of the raw data.</span></span> <span data-ttu-id="e6e02-113">En el caso de los marcos sin comprimir, estos datos se componen de píxeles a los que el filtro puede tener acceso o modificar directamente.</span><span class="sxs-lookup"><span data-stu-id="e6e02-113">For uncompressed frames, this data consists of pixels that can be accessed or modified directly by the filter.</span></span> <span data-ttu-id="e6e02-114">En las secciones siguientes se proporciona información general que le ayudará a trabajar de forma eficaz con los datos DIB de esta manera.</span><span class="sxs-lookup"><span data-stu-id="e6e02-114">The following sections provide background information that will help you work effectively with DIB data in this manner.</span></span>

> [!Note]  
> <span data-ttu-id="e6e02-115">También puede modificar los bits mediante las funciones GDI, GDI+, DirectDraw o Direct3D, pero estas técnicas quedan fuera del ámbito de este artículo.</span><span class="sxs-lookup"><span data-stu-id="e6e02-115">You can also modify the bits by using GDI, GDI+, DirectDraw or Direct3D functions, but these techniques are beyond the scope of this article.</span></span>

 

<span data-ttu-id="e6e02-116">Esta sección contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="e6e02-116">This section contains the following topics:</span></span>

-   [<span data-ttu-id="e6e02-117">De arriba abajo y Bottom-Up DIB</span><span class="sxs-lookup"><span data-stu-id="e6e02-117">Top-Down vs. Bottom-Up DIBs</span></span>](top-down-vs--bottom-up-dibs.md)
-   [<span data-ttu-id="e6e02-118">Trabajar con RGB de 16 bits</span><span class="sxs-lookup"><span data-stu-id="e6e02-118">Working with 16-bit RGB</span></span>](working-with-16-bit-rgb.md)

 

 



