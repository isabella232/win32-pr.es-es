---
description: El filtro Representador nulo es un representador que descarta cada muestra que recibe, sin mostrar ni representar los datos de ejemplo.
ms.assetid: 2954762d-2ae6-4e38-ac88-5390a081897e
title: Filtro de representador null (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Null Renderer Filter
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 64647cbcbcc836c400890fb173a29c76f8723029
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908813"
---
# <a name="null-renderer-filter"></a><span data-ttu-id="52ae1-103">Filtro de representador null</span><span class="sxs-lookup"><span data-stu-id="52ae1-103">Null Renderer Filter</span></span>

> [!Note]  
> <span data-ttu-id="52ae1-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="52ae1-104">\[Deprecated.</span></span> <span data-ttu-id="52ae1-105">Esta API puede quitarse de futuras versiones de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="52ae1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="52ae1-106">El filtro Representador nulo es un representador que descarta cada muestra que recibe, sin mostrar ni representar los datos de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="52ae1-106">The Null Renderer filter is a renderer that discards every sample it receives, without displaying or rendering the sample data.</span></span>



| <span data-ttu-id="52ae1-107">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="52ae1-107">Label</span></span> | <span data-ttu-id="52ae1-108">Value</span><span class="sxs-lookup"><span data-stu-id="52ae1-108">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52ae1-109">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="52ae1-109">Filter interfaces</span></span>                        | <span data-ttu-id="52ae1-110">[**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span><span class="sxs-lookup"><span data-stu-id="52ae1-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span></span> |
| <span data-ttu-id="52ae1-111">Tipos de medios de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="52ae1-111">Input pin media types</span></span>                    | <span data-ttu-id="52ae1-112">Cualquier tipo de medio</span><span class="sxs-lookup"><span data-stu-id="52ae1-112">Any media type</span></span>                                                                                                       |
| <span data-ttu-id="52ae1-113">Interfaces de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="52ae1-113">Input pin interfaces</span></span>                     | <span data-ttu-id="52ae1-114">[**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="52ae1-114">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>               |
| <span data-ttu-id="52ae1-115">Tipos de medios de pin de salida</span><span class="sxs-lookup"><span data-stu-id="52ae1-115">Output pin media types</span></span>                   | <span data-ttu-id="52ae1-116">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="52ae1-116">Not applicable.</span></span>                                                                                                      |
| <span data-ttu-id="52ae1-117">Interfaces de pin de salida</span><span class="sxs-lookup"><span data-stu-id="52ae1-117">Output pin interfaces</span></span>                    | <span data-ttu-id="52ae1-118">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="52ae1-118">Not applicable.</span></span>                                                                                                      |
| <span data-ttu-id="52ae1-119">Filtrar CLSID</span><span class="sxs-lookup"><span data-stu-id="52ae1-119">Filter CLSID</span></span>                             | <span data-ttu-id="52ae1-120">CLSID \_ NullRenderer</span><span class="sxs-lookup"><span data-stu-id="52ae1-120">CLSID\_NullRenderer</span></span>                                                                                                  |
| <span data-ttu-id="52ae1-121">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="52ae1-121">Property Page CLSID</span></span>                      | <span data-ttu-id="52ae1-122">No hay ninguna página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="52ae1-122">No property page.</span></span>                                                                                                    |
| <span data-ttu-id="52ae1-123">Executable</span><span class="sxs-lookup"><span data-stu-id="52ae1-123">Executable</span></span>                               | <span data-ttu-id="52ae1-124">Qedit.dll</span><span class="sxs-lookup"><span data-stu-id="52ae1-124">Qedit.dll</span></span>                                                                                                            |
| [<span data-ttu-id="52ae1-125">Mérito</span><span class="sxs-lookup"><span data-stu-id="52ae1-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="52ae1-126">NO USE LA OPCIÓN DE \_ \_ NO \_ USAR.</span><span class="sxs-lookup"><span data-stu-id="52ae1-126">MERIT\_DO\_NOT\_USE</span></span>                                                                                                  |
| [<span data-ttu-id="52ae1-127">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="52ae1-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="52ae1-128">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="52ae1-128">CLSID\_LegacyAmFilterCategory</span></span>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="52ae1-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="52ae1-129">Remarks</span></span>

<span data-ttu-id="52ae1-130">Use este filtro cuando un pin de salida en el gráfico requiera una conexión de bajada, pero no desea representar los datos de ese pin.</span><span class="sxs-lookup"><span data-stu-id="52ae1-130">Use this filter when an output pin in the graph requires a downstream connection, but you do not wish to render the data from that pin.</span></span> <span data-ttu-id="52ae1-131">Al conectar el pin de salida al representador null, se completa la conexión sin representar los datos.</span><span class="sxs-lookup"><span data-stu-id="52ae1-131">By connecting the output pin to the Null Renderer, you complete the connection without rendering the data.</span></span>

<span data-ttu-id="52ae1-132">Aunque este filtro no representa ninguna muestra, espera el tiempo de presentación de cada muestra antes de descartarla.</span><span class="sxs-lookup"><span data-stu-id="52ae1-132">Even though this filter does not render any samples, it does wait for each sample's presentation time before discarding the sample.</span></span> <span data-ttu-id="52ae1-133">Por lo tanto, el gráfico se ejecutará a la velocidad normal.</span><span class="sxs-lookup"><span data-stu-id="52ae1-133">Therefore, the graph will run at the normal rate.</span></span> <span data-ttu-id="52ae1-134">Si desea que el gráfico se ejecute lo más rápido posible, establezca el reloj de referencia en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="52ae1-134">If you want the graph the run as quickly as possible, set the reference clock to **NULL**.</span></span> <span data-ttu-id="52ae1-135">Para obtener más información, vea [Establecer el reloj del gráfico.](setting-the-graph-clock.md)</span><span class="sxs-lookup"><span data-stu-id="52ae1-135">For more information, see [Setting the Graph Clock](setting-the-graph-clock.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="52ae1-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52ae1-136">Requirements</span></span>



| <span data-ttu-id="52ae1-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="52ae1-137">Requirement</span></span> | <span data-ttu-id="52ae1-138">Value</span><span class="sxs-lookup"><span data-stu-id="52ae1-138">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="52ae1-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52ae1-139">Header</span></span><br/> | <dl> <span data-ttu-id="52ae1-140"><dt>Qedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="52ae1-140"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52ae1-141">Consulte también</span><span class="sxs-lookup"><span data-stu-id="52ae1-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52ae1-142">Objetos de Servicios de edición de DirectShow</span><span class="sxs-lookup"><span data-stu-id="52ae1-142">DirectShow Editing Services Objects</span></span>](directshow-editing-services-objects.md)
</dt> </dl>

 

 




