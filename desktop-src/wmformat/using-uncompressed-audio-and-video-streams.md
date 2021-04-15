---
title: Uso de secuencias de audio y vídeo sin comprimir
description: Uso de secuencias de audio y vídeo sin comprimir
ms.assetid: 1a8fe604-bd99-4ba1-878f-8e1fd89483b3
keywords:
- flujos, configurar secuencias de audio y vídeo sin comprimir
- códecs, configurar secuencias de audio y vídeo sin comprimir
- secuencias de vídeo, sin comprimir
- secuencias de audio sin comprimir
- secuencias de audio y vídeo sin comprimir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00d81bd0a9f8c53751e404a0cfb0e55d57d4242
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105714333"
---
# <a name="using-uncompressed-audio-and-video-streams"></a><span data-ttu-id="5696b-108">Uso de secuencias de audio y vídeo sin comprimir</span><span class="sxs-lookup"><span data-stu-id="5696b-108">Using Uncompressed Audio and Video Streams</span></span>

<span data-ttu-id="5696b-109">En la mayoría de los casos, el medio sin comprimir tiene requisitos de almacenamiento y entrega muy elevados, pero en algunos escenarios de reproducción local, el nivel de calidad es lo suficientemente importante como para garantizar que no se use la compresión.</span><span class="sxs-lookup"><span data-stu-id="5696b-109">Under most circumstances, uncompressed media has prohibitively large storage and delivery requirements, but for some local playback scenarios, the quality level is important enough to warrant not using compression..</span></span>

<span data-ttu-id="5696b-110">La configuración de una secuencia de medios sin comprimir debe reflejar la configuración de los medios de origen.</span><span class="sxs-lookup"><span data-stu-id="5696b-110">The settings for an uncompressed media stream should reflect the settings of the source media.</span></span> <span data-ttu-id="5696b-111">Al configurar una secuencia sin comprimir, debe calcular la velocidad de bits del medio y establecer la secuencia de forma adecuada llamando a [**IWMStreamConfig:: SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate).</span><span class="sxs-lookup"><span data-stu-id="5696b-111">When configuring an uncompressed stream, you must calculate the bit rate of the media and set the stream appropriately by calling [**IWMStreamConfig::SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate).</span></span> <span data-ttu-id="5696b-112">Dado que las secuencias sin comprimir no son viables para la transmisión por secuencias, siempre debe establecer en cero la ventana de búfer de los flujos de medios sin comprimir llamando a [**IWMStreamConfig:: SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow).</span><span class="sxs-lookup"><span data-stu-id="5696b-112">Because uncompressed streams are not viable for streaming, you should always set the buffer window for uncompressed media streams to zero by calling [**IWMStreamConfig::SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow).</span></span>

<span data-ttu-id="5696b-113">Se admiten los siguientes formatos de píxel para las secuencias de vídeo sin comprimir:</span><span class="sxs-lookup"><span data-stu-id="5696b-113">The following pixel formats are supported for uncompressed video streams:</span></span>

-   <span data-ttu-id="5696b-114">WMMEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="5696b-114">WMMEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="5696b-115">WMMEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="5696b-115">WMMEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="5696b-116">WMMEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="5696b-116">WMMEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="5696b-117">WMMEDIASUBTYPE \_ i420</span><span class="sxs-lookup"><span data-stu-id="5696b-117">WMMEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="5696b-118">WMMEDIASUBTYPE \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="5696b-118">WMMEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="5696b-119">WMMEDIASUBTYPE \_ YV12</span><span class="sxs-lookup"><span data-stu-id="5696b-119">WMMEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="5696b-120">WMMEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="5696b-120">WMMEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="5696b-121">WMMEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="5696b-121">WMMEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="5696b-122">WMMEDIASUBTYPE \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="5696b-122">WMMEDIASUBTYPE\_YVYU</span></span>

## <a name="related-topics"></a><span data-ttu-id="5696b-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5696b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5696b-124">**Configuración común para todos los flujos**</span><span class="sxs-lookup"><span data-stu-id="5696b-124">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="5696b-125">**Configuración de secuencias de audio**</span><span class="sxs-lookup"><span data-stu-id="5696b-125">**Configuring Audio Streams**</span></span>](configuring-audio-streams.md)
</dt> <dt>

[<span data-ttu-id="5696b-126">**Configuración de secuencias**</span><span class="sxs-lookup"><span data-stu-id="5696b-126">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="5696b-127">**Configuración de secuencias de vídeo**</span><span class="sxs-lookup"><span data-stu-id="5696b-127">**Configuring Video Streams**</span></span>](configuring-video-streams.md)
</dt> </dl>

 

 




