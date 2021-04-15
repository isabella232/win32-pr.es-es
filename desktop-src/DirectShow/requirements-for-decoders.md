---
description: Requisitos para descodificadores
ms.assetid: 149aea20-0d37-4b1c-a098-8446c4088ce1
title: Requisitos para descodificadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461120bec88636e4c015c2e319d855571e8ac1b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494842"
---
# <a name="requirements-for-decoders"></a><span data-ttu-id="0aebd-103">Requisitos para descodificadores</span><span class="sxs-lookup"><span data-stu-id="0aebd-103">Requirements for Decoders</span></span>

<span data-ttu-id="0aebd-104">Los descodificadores que proporcionan ejemplos a la VMR deben observar las siguientes reglas:</span><span class="sxs-lookup"><span data-stu-id="0aebd-104">Decoders that deliver samples to the VMR must observe the following rules:</span></span>

-   <span data-ttu-id="0aebd-105">Debe haber un fotograma de subimagen entregado al VMR para cada fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0aebd-105">There should be one subpicture frame delivered to the VMR for each video frame.</span></span> <span data-ttu-id="0aebd-106">Los dos fotogramas deben tener las mismas marcas de tiempo.</span><span class="sxs-lookup"><span data-stu-id="0aebd-106">The two frames should have the same time stamps.</span></span>
-   <span data-ttu-id="0aebd-107">Si la subimagen no ha cambiado, use la \_ marca AM GBF \_ NOTASYNCPOINT en el método [**IMemAllocator:: getBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) para obligar al asignador a que devuelva un búfer que contenga el último fotograma entregado a VMR.</span><span class="sxs-lookup"><span data-stu-id="0aebd-107">If the subpicture has not changed, use the AM\_GBF\_NOTASYNCPOINT flag in the [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) method to force the allocator to return a buffer containing the last frame delivered to the VMR.</span></span> <span data-ttu-id="0aebd-108">Simplemente coloque una nueva marca de tiempo en el ejemplo y entréguela de nuevo a la VMR.</span><span class="sxs-lookup"><span data-stu-id="0aebd-108">Just put a new time stamp on the sample and deliver it to the VMR again.</span></span> <span data-ttu-id="0aebd-109">Si la fama de la subimagen está en blanco, debe proporcionarla.</span><span class="sxs-lookup"><span data-stu-id="0aebd-109">If the subpicture fame is blank, you should still deliver it.</span></span> <span data-ttu-id="0aebd-110">VMR detectará el fotograma vacío y no lo combinará con el vídeo.</span><span class="sxs-lookup"><span data-stu-id="0aebd-110">The VMR will detect the empty frame and not blend it with the video.</span></span> <span data-ttu-id="0aebd-111">Esta prueba se realiza mediante el chip VGA y no afecta al rendimiento de la reproducción.</span><span class="sxs-lookup"><span data-stu-id="0aebd-111">This test is performed by the VGA chip and does not affect the playback performance.</span></span>
-   <span data-ttu-id="0aebd-112">Todos los ejemplos, a excepción de las secuencias en directo, deben tener marcas de tiempo de inicio y detención válidas adjuntas.</span><span class="sxs-lookup"><span data-stu-id="0aebd-112">All samples, except for live streams, must have valid start and stop time stamps attached.</span></span> <span data-ttu-id="0aebd-113">(El DVD no es una secuencia en directo).</span><span class="sxs-lookup"><span data-stu-id="0aebd-113">(DVD is not a live stream.)</span></span>
-   <span data-ttu-id="0aebd-114">Las marcas de tiempo de ejemplo multimedia deben ser contiguas</span><span class="sxs-lookup"><span data-stu-id="0aebd-114">The media sample time stamps must be contiguous</span></span>
-   <span data-ttu-id="0aebd-115">El descodificador debe identificarse como compatible con VMR para su uso por los generadores de gráficos.</span><span class="sxs-lookup"><span data-stu-id="0aebd-115">The decoder must identify itself as VMR-capable for use by graph builders.</span></span>
-   <span data-ttu-id="0aebd-116">La secuencia de subimagen ahora debe contener valores alfa por píxel incrustados.</span><span class="sxs-lookup"><span data-stu-id="0aebd-116">The subpicture stream should now contain embedded per-pixel alpha values.</span></span> <span data-ttu-id="0aebd-117">El tipo de superficie ARGB4444 es ideal para las subimágenes.</span><span class="sxs-lookup"><span data-stu-id="0aebd-117">The ARGB4444 surface type is ideal for subpictures.</span></span>
-   <span data-ttu-id="0aebd-118">No suponga que el paso de la subimagen es el mismo que el ancho de la superficie.</span><span class="sxs-lookup"><span data-stu-id="0aebd-118">Do not assume that the stride of the subpicture is the same as the surface width.</span></span> <span data-ttu-id="0aebd-119">Este no es siempre el caso de la VMR.</span><span class="sxs-lookup"><span data-stu-id="0aebd-119">This is not always the case with the VMR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0aebd-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0aebd-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0aebd-121">Aceleración de vídeo sobre DirectX</span><span class="sxs-lookup"><span data-stu-id="0aebd-121">About DirectX Video Acceleration</span></span>](about-directx-video-acceleration.md)
</dt> </dl>

 

 



