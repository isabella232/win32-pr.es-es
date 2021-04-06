---
description: Asignador de superficie de VBI
ms.assetid: 51c73a25-1112-4fb4-a45f-967c6a1b5c55
title: Asignador de superficie de VBI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4edd698ed37c7b180bee27d0a99e95096080d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815259"
---
# <a name="vbi-surface-allocator"></a><span data-ttu-id="a0b90-103">Asignador de superficie de VBI</span><span class="sxs-lookup"><span data-stu-id="a0b90-103">VBI Surface Allocator</span></span>

<span data-ttu-id="a0b90-104">El asignador de superficie de VBI controla la asignación de búferes VBI en gráficos de televisión analógica con escenarios de captura de puerto de vídeo de hardware.</span><span class="sxs-lookup"><span data-stu-id="a0b90-104">The VBI Surface Allocator controls the allocation of VBI buffers in analog television graphs with hardware video port capture scenarios.</span></span> <span data-ttu-id="a0b90-105">Con dispositivos como el descodificador de Bt829, el búfer de fotogramas puede contener varios búferes de captura de VBI a los que se tiene acceso a través de un mecanismo propio basado en hardware conocido como un puerto de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a0b90-105">With devices such as the Bt829 decoder, the frame buffer may contain multiple VBI capture buffers that are accessed via a proprietary hardware-based mechanism known generically as a Video Port.</span></span> <span data-ttu-id="a0b90-106">El filtro de asignador de superficie de VBI conecta el nivel inferior del filtro de captura y no tiene ningún PIN de salida.</span><span class="sxs-lookup"><span data-stu-id="a0b90-106">The VBI Surface Allocator filter connects downstream from the capture filter and has no output pin.</span></span> <span data-ttu-id="a0b90-107">El filtro funciona en estrecha colaboración con el [mezclador de superposición](overlay-mixer-filter.md) (a través de DirectDraw) para realizar operaciones coordinadas en el puerto de vídeo de hardware, usando la misma memoria de búfer de fotogramas SVGA limitada.</span><span class="sxs-lookup"><span data-stu-id="a0b90-107">The filter works closely with the [Overlay Mixer](overlay-mixer-filter.md) (via DirectDraw) to perform coordinated operations on the hardware video port, utilizing the same limited SVGA frame buffer memory.</span></span>



|                                          |                                                                                     |
|------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a0b90-108">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="a0b90-108">Filter Interfaces</span></span>                        | [<span data-ttu-id="a0b90-109">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="a0b90-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                  |
| <span data-ttu-id="a0b90-110">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="a0b90-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="a0b90-111">\_Vídeo de MEDIATYPE, MEDIASUBTYPE \_ VPVBI</span><span class="sxs-lookup"><span data-stu-id="a0b90-111">MEDIATYPE\_Video, MEDIASUBTYPE\_VPVBI</span></span>                                               |
| <span data-ttu-id="a0b90-112">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="a0b90-112">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="a0b90-113">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="a0b90-113">**IKsPropertySet**</span></span>](ikspropertyset.md)                                            |
| <span data-ttu-id="a0b90-114">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="a0b90-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="a0b90-115">MEDIATYPE \_ null, MEDIASUBTYPE \_ null.</span><span class="sxs-lookup"><span data-stu-id="a0b90-115">MEDIATYPE\_NULL, MEDIASUBTYPE\_NULL.</span></span> <span data-ttu-id="a0b90-116">(Nunca se conecta a la clavija de salida).</span><span class="sxs-lookup"><span data-stu-id="a0b90-116">(Nothing is ever connected to the output pin.)</span></span> |
| <span data-ttu-id="a0b90-117">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="a0b90-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="a0b90-118">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="a0b90-118">Not applicable.</span></span>                                                                     |
| <span data-ttu-id="a0b90-119">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="a0b90-119">Filter CLSID</span></span>                             | <span data-ttu-id="a0b90-120">CLSID \_ VBISurfaces</span><span class="sxs-lookup"><span data-stu-id="a0b90-120">CLSID\_VBISurfaces</span></span>                                                                  |
| <span data-ttu-id="a0b90-121">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="a0b90-121">Property Page CLSID</span></span>                      | <span data-ttu-id="a0b90-122">Ninguna página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="a0b90-122">No property page.</span></span>                                                                   |
| <span data-ttu-id="a0b90-123">Executable</span><span class="sxs-lookup"><span data-stu-id="a0b90-123">Executable</span></span>                               | <span data-ttu-id="a0b90-124">vbisurf.ax</span><span class="sxs-lookup"><span data-stu-id="a0b90-124">vbisurf.ax</span></span>                                                                          |
| [<span data-ttu-id="a0b90-125">Fundament</span><span class="sxs-lookup"><span data-stu-id="a0b90-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="a0b90-126">MÉRITO \_ normal</span><span class="sxs-lookup"><span data-stu-id="a0b90-126">MERIT\_NORMAL</span></span>                                                                       |
| [<span data-ttu-id="a0b90-127">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="a0b90-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="a0b90-128">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="a0b90-128">CLSID\_LegacyAmFilterCategory</span></span>                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="a0b90-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a0b90-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0b90-130">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="a0b90-130">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



