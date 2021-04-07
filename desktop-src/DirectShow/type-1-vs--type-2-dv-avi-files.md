---
description: Escriba-1 frente a
ms.assetid: 3f1cf981-f678-46a6-9784-ffb389438b6d
title: Archivos AVI de tipo 1 frente a-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0000b81e94e25749b5590287145a88a28280e16d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002153"
---
# <a name="type-1-vs-type-2-dv-avi-files"></a><span data-ttu-id="82774-103">Archivos AVI de tipo 1 frente a-2</span><span class="sxs-lookup"><span data-stu-id="82774-103">Type-1 vs. Type-2 DV AVI Files</span></span>

<span data-ttu-id="82774-104">Las cámaras DV producen audio y vídeo intercalados; cada fotograma de vídeo también contiene la información de audio.</span><span class="sxs-lookup"><span data-stu-id="82774-104">DV cameras produce interleaved audio-video; each frame of video also contains the audio information.</span></span> <span data-ttu-id="82774-105">Si guarda los datos de DV en un archivo AVI, tendrá una opción:</span><span class="sxs-lookup"><span data-stu-id="82774-105">If you save DV data to an AVI file, you have a choice:</span></span>

-   <span data-ttu-id="82774-106">Almacene los datos intercalados como una secuencia en el archivo AVI.</span><span class="sxs-lookup"><span data-stu-id="82774-106">Store the interleaved data as one stream in the AVI file.</span></span> <span data-ttu-id="82774-107">Esto se conoce como archivo de tipo 1.</span><span class="sxs-lookup"><span data-stu-id="82774-107">This is known as a type-1 file.</span></span>
-   <span data-ttu-id="82774-108">Divida los datos intercalados en secuencias de audio y vídeo independientes.</span><span class="sxs-lookup"><span data-stu-id="82774-108">Split the interleaved data into separate audio and video streams.</span></span> <span data-ttu-id="82774-109">Esto se conoce como archivo de tipo 2.</span><span class="sxs-lookup"><span data-stu-id="82774-109">This is known as a type-2 file.</span></span>

<span data-ttu-id="82774-110">Para la captura de vídeo, donde el rendimiento máximo es fundamental, es mejor usar un archivo de tipo 1, ya que los archivos de tipo 2 llevan datos de audio redundantes.</span><span class="sxs-lookup"><span data-stu-id="82774-110">For video capture, where maximum throughput is crucial, it is better to use a type-1 file, because type-2 files carry redundant audio data.</span></span> <span data-ttu-id="82774-111">(El flujo de vídeo todavía tiene los datos de audio.</span><span class="sxs-lookup"><span data-stu-id="82774-111">(The video stream still has the audio data.</span></span> <span data-ttu-id="82774-112">El audio se oculta simplemente mediante la etiqueta de la secuencia como vídeo.) Además, la escritura de un archivo de tipo 2 requiere tiempo adicional de procesador para dividir el flujo intercalado.</span><span class="sxs-lookup"><span data-stu-id="82774-112">The audio is simply hidden by labeling the stream as video.) Also, writing a type-2 file requires some additional processor time to split the interleaved stream.</span></span>

<span data-ttu-id="82774-113">Por otro lado, los archivos de tipo 1 son menos eficientes para la edición en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="82774-113">On the other hand, type-1 files are less efficient for real-time editing.</span></span> <span data-ttu-id="82774-114">La aplicación debe extraer el audio del flujo intercalado, realizar las modificaciones y volver a intercalar los datos.</span><span class="sxs-lookup"><span data-stu-id="82774-114">The application must extract the audio from the interleaved stream, make the edits, and interleave the data again.</span></span> <span data-ttu-id="82774-115">Además, el formato de tipo 1 no es compatible con Microsoft® vídeo para Windows® (VFW).</span><span class="sxs-lookup"><span data-stu-id="82774-115">Also, the type-1 format is not compatible with Microsoft® Video for Windows® (VFW).</span></span> <span data-ttu-id="82774-116">DirectShow puede controlar ambos tipos de archivos.</span><span class="sxs-lookup"><span data-stu-id="82774-116">DirectShow can handle both types of files.</span></span>

<span data-ttu-id="82774-117">Un archivo de tipo 2 se puede convertir al tipo-1 mediante el filtro [DV multiplexor](dv-muxer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="82774-117">A type-2 file can be converted to type-1 using the [DV Muxer](dv-muxer-filter.md) filter.</span></span> <span data-ttu-id="82774-118">Un archivo de tipo 1 se puede convertir al tipo 2 mediante el filtro de [divisor DV](dv-splitter-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="82774-118">A type-1 file can be converted to type-2 using the [DV Splitter](dv-splitter-filter.md) filter.</span></span> <span data-ttu-id="82774-119">En el diagrama siguiente se ilustra la diferencia entre los dos formatos.</span><span class="sxs-lookup"><span data-stu-id="82774-119">The following diagram illustrates the difference between the two formats.</span></span>

![conversión entre el tipo 1 y el tipo-2 DV](images/dv-filters3.png)

## <a name="related-topics"></a><span data-ttu-id="82774-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="82774-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82774-122">Vídeo digital en DirectShow</span><span class="sxs-lookup"><span data-stu-id="82774-122">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="82774-123">Datos de DV en el formato de archivo AVI</span><span class="sxs-lookup"><span data-stu-id="82774-123">DV Data in the AVI File Format</span></span>](dv-data-in-the-avi-file-format.md)
</dt> </dl>

 

 



