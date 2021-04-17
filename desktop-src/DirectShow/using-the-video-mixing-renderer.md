---
description: Usar el representador de mezcla de vídeo
ms.assetid: 3d0fdfac-ec7e-4e02-886b-2039c607dac7
title: Usar el representador de mezcla de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5baf7d559eed0d3111876924520952b55c6da2e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667848"
---
# <a name="using-the-video-mixing-renderer"></a><span data-ttu-id="47d3c-103">Usar el representador de mezcla de vídeo</span><span class="sxs-lookup"><span data-stu-id="47d3c-103">Using the Video Mixing Renderer</span></span>

<span data-ttu-id="47d3c-104">En cuanto a rendimiento y amplitud de características, el filtro de representador de mezcla de vídeo (VMR) representa la siguiente generación en la representación de vídeo en la plataforma Windows.</span><span class="sxs-lookup"><span data-stu-id="47d3c-104">In terms of both performance and breadth of features, the Video Mixing Renderer (VMR) filter represents the next generation in video rendering on the Windows platform.</span></span> <span data-ttu-id="47d3c-105">VMR reemplaza al [representador de vídeo](video-renderer-filter.md)y [mezclador de superposición](overlay-mixer-filter.md) y agrega muchas características nuevas de mezcla.</span><span class="sxs-lookup"><span data-stu-id="47d3c-105">The VMR replaces the [Overlay Mixer](overlay-mixer-filter.md) and [Video Renderer](video-renderer-filter.md), and adds many new mixing features.</span></span>

<span data-ttu-id="47d3c-106">Hay dos versiones de VMR:</span><span class="sxs-lookup"><span data-stu-id="47d3c-106">There are two versions of the VMR:</span></span>

-   <span data-ttu-id="47d3c-107">VMR-7, que usa DirectDraw 7 para la representación.</span><span class="sxs-lookup"><span data-stu-id="47d3c-107">The VMR-7, which uses DirectDraw 7 for rendering.</span></span>
-   <span data-ttu-id="47d3c-108">VMR-9, que usa Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="47d3c-108">The VMR-9, which uses Direct3D 9.</span></span>

<span data-ttu-id="47d3c-109">VMR-7 está disponible en Windows XP y versiones posteriores, pero no está disponible para su redistribución.</span><span class="sxs-lookup"><span data-stu-id="47d3c-109">The VMR-7 is available on Windows XP and later, but is not available for redistribution.</span></span> <span data-ttu-id="47d3c-110">VMR-9 está disponible para la redistribución en todas las plataformas compatibles con DirectX 9.</span><span class="sxs-lookup"><span data-stu-id="47d3c-110">The VMR-9 is available for redistribution on all platforms supported by DirectX 9.</span></span> <span data-ttu-id="47d3c-111">Los dos filtros VMR son muy similares en su implementación de y las interfaces que exponen.</span><span class="sxs-lookup"><span data-stu-id="47d3c-111">The two VMR filters are very similar in their implementation and the interfaces that they expose.</span></span>

<span data-ttu-id="47d3c-112">VMR-9 tiene su propio CLSID y su propio conjunto de interfaces, estructuras y tipos de enumeración que no siempre son idénticos a los tipos de datos correspondientes para VMR-7, debido a las diferencias subyacentes entre DirectDraw 7 y Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="47d3c-112">The VMR-9 has its own CLSID and its own set of interfaces, structures and enumeration types which are not always identical to the corresponding data types for the VMR-7, due to the underlying differences between DirectDraw 7 and Direct3D 9.</span></span> <span data-ttu-id="47d3c-113">Las interfaces VMR-9 terminan con "9", por ejemplo **IVMRStreamConfig9**, y las estructuras y los tipos de enumeración tienen "VMR9" en su nombre para distinguirlos de los tipos de datos que se usan con VMR-7.</span><span class="sxs-lookup"><span data-stu-id="47d3c-113">The VMR-9 interfaces all end with "9", for example **IVMRStreamConfig9**, and the structures and enumeration types all have "VMR9" in their name to distinguish them from the data types used with the VMR-7.</span></span>

<span data-ttu-id="47d3c-114">Para garantizar la compatibilidad con versiones anteriores, VMR-9 no es el representador predeterminado en ningún sistema.</span><span class="sxs-lookup"><span data-stu-id="47d3c-114">To ensure backward-compatibility, the VMR-9 is not the default renderer on any system.</span></span> <span data-ttu-id="47d3c-115">Para usar VMR-9, debe agregarlo explícitamente al gráfico de filtros mediante el método [**IFilterGraph:: addFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) y configurarlo antes de conectarlo a los filtros de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="47d3c-115">To use the VMR-9, you must explicitly add it to the filter graph using the [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) method, and configure it before connecting it to any upstream filters.</span></span>

<span data-ttu-id="47d3c-116">Este artículo contiene las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="47d3c-116">This article contains the following sections.</span></span> <span data-ttu-id="47d3c-117">Excepto donde se indique lo contrario, la información de estas secciones se aplica a los filtros VMR-7 y VMR-9.</span><span class="sxs-lookup"><span data-stu-id="47d3c-117">Except where noted, the information in these sections applies to both the VMR-7 and the VMR-9 filters.</span></span>

-   [<span data-ttu-id="47d3c-118">Acerca de la presentación de la combinación de vídeo</span><span class="sxs-lookup"><span data-stu-id="47d3c-118">About the Video Mixing Render</span></span>](about-the-video-mixing-render.md)
-   [<span data-ttu-id="47d3c-119">Modos de funcionamiento de VMR</span><span class="sxs-lookup"><span data-stu-id="47d3c-119">VMR Modes of Operation</span></span>](vmr-modes-of-operation.md)
-   [<span data-ttu-id="47d3c-120">Creación de un gráfico de filtros VMR-9</span><span class="sxs-lookup"><span data-stu-id="47d3c-120">Building a VMR-9 Filter Graph</span></span>](building-a-vmr-9-filter-graph.md)
-   [<span data-ttu-id="47d3c-121">Usar el modo de mezcla de VMR</span><span class="sxs-lookup"><span data-stu-id="47d3c-121">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
-   [<span data-ttu-id="47d3c-122">Establecer preferencias de desentrelazado</span><span class="sxs-lookup"><span data-stu-id="47d3c-122">Setting Deinterlace Preferences</span></span>](setting-deinterlace-preferences.md)
-   [<span data-ttu-id="47d3c-123">Usar la VMR para desarrolladores de filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="47d3c-123">Using the VMR for DirectShow Filter Developers</span></span>](using-the-vmr-for-directshow-filter-developers.md)
-   [<span data-ttu-id="47d3c-124">Uso del Protocolo de protección de la salida certificada (COPP)</span><span class="sxs-lookup"><span data-stu-id="47d3c-124">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)

## <a name="related-topics"></a><span data-ttu-id="47d3c-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="47d3c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47d3c-126">Filtro de representador de mezcla de vídeo 7</span><span class="sxs-lookup"><span data-stu-id="47d3c-126">Video Mixing Renderer Filter 7</span></span>](video-mixing-renderer-filter-7.md)
</dt> <dt>

[<span data-ttu-id="47d3c-127">Filtro de representador de mezcla de vídeo 9</span><span class="sxs-lookup"><span data-stu-id="47d3c-127">Video Mixing Renderer Filter 9</span></span>](video-mixing-renderer-filter-9.md)
</dt> </dl>

 

 



