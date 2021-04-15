---
title: Formatos de entrada de vídeo
description: Formatos de entrada de vídeo
ms.assetid: 0f1ec15d-328e-4c07-bf58-fd4ecb483549
keywords:
- SDK de Windows Media Format, formatos de entrada de vídeo
- Formato de sistemas avanzados (ASF), formatos de entrada de vídeo
- ASF (formato de sistemas avanzados), formatos de entrada de vídeo
- formatos de entrada de vídeo
- SDK de Windows Media Format, formatos de vídeo
- Formato de sistemas avanzados (ASF), formatos de vídeo
- ASF (formato de sistemas avanzados), formatos de vídeo
- formatos de vídeo
- Códec de Windows Media Video 9, formatos de entrada de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5113ee3cbd9c9235104f858968db20ebc29e3a
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "105695574"
---
# <a name="video-input-formats"></a><span data-ttu-id="3afbe-112">Formatos de entrada de vídeo</span><span class="sxs-lookup"><span data-stu-id="3afbe-112">Video Input Formats</span></span>

<span data-ttu-id="3afbe-113">El escritor acepta los siguientes formatos de vídeo como entrada para comprimirlos con el códec Windows Media Video 9:</span><span class="sxs-lookup"><span data-stu-id="3afbe-113">The writer accepts the following video formats as input to be compressed using the Windows Media Video 9 codec:</span></span>

-   <span data-ttu-id="3afbe-114">WMMEDIASUBTYPE \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="3afbe-114">WMMEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="3afbe-115">WMMEDIASUBTYPE \_ i420</span><span class="sxs-lookup"><span data-stu-id="3afbe-115">WMMEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="3afbe-116">WMMEDIASUBTYPE \_ YV12</span><span class="sxs-lookup"><span data-stu-id="3afbe-116">WMMEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="3afbe-117">WMMEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="3afbe-117">WMMEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="3afbe-118">WMMEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="3afbe-118">WMMEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="3afbe-119">WMMEDIASUBTYPE \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="3afbe-119">WMMEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="3afbe-120">WMMEDIASUBTYPE \_ YVU9</span><span class="sxs-lookup"><span data-stu-id="3afbe-120">WMMEDIASUBTYPE\_YVU9</span></span>
-   <span data-ttu-id="3afbe-121">WMMEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="3afbe-121">WMMEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="3afbe-122">WMMEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="3afbe-122">WMMEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="3afbe-123">WMMEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="3afbe-123">WMMEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="3afbe-124">WMMEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="3afbe-124">WMMEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="3afbe-125">WMMEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="3afbe-125">WMMEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="3afbe-126">Siempre debe usar [**IWMWriter:: GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount) y [**IWMWriter:: GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat) para enumerar los formatos de entrada disponibles y obtener el objeto de propiedades de medios de entrada para el formato deseado.</span><span class="sxs-lookup"><span data-stu-id="3afbe-126">You should always use [**IWMWriter::GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount) and [**IWMWriter::GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat) to enumerate the available input formats and to obtain the input media properties object for the desired format.</span></span> <span data-ttu-id="3afbe-127">Los objetos de las propiedades de los medios de entrada de vídeo deben cambiarse para reflejar el tamaño y la velocidad de fotogramas de los medios de entrada.</span><span class="sxs-lookup"><span data-stu-id="3afbe-127">Video input media properties objects must be changed to reflect the frame size and frame rate of your input media.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3afbe-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3afbe-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3afbe-129">**Identificadores de tipo de medio**</span><span class="sxs-lookup"><span data-stu-id="3afbe-129">**Media Type Identifiers**</span></span>](media-type-identifiers.md)
</dt> <dt>

[<span data-ttu-id="3afbe-130">**Tipos de medios**</span><span class="sxs-lookup"><span data-stu-id="3afbe-130">**Media Types**</span></span>](media-types.md)
</dt> </dl>

 

 




