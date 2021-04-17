---
description: El filtro de representador NULL es un representador que descarta cada ejemplo que recibe, sin mostrar ni representar los datos de ejemplo.
ms.assetid: 2954762d-2ae6-4e38-ac88-5390a081897e
title: Filtro de representador nulo (QEDIT. h)
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
ms.openlocfilehash: 7ff6c728276ca3fd69c14e304780b1d70c563265
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690609"
---
# <a name="null-renderer-filter"></a><span data-ttu-id="5cf0c-103">Filtro de representador nulo</span><span class="sxs-lookup"><span data-stu-id="5cf0c-103">Null Renderer Filter</span></span>

> [!Note]  
> <span data-ttu-id="5cf0c-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="5cf0c-104">\[Deprecated.</span></span> <span data-ttu-id="5cf0c-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5cf0c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5cf0c-106">El filtro de representador NULL es un representador que descarta cada ejemplo que recibe, sin mostrar ni representar los datos de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="5cf0c-106">The Null Renderer filter is a renderer that discards every sample it receives, without displaying or rendering the sample data.</span></span>



|                                          |                                                                                                                      |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cf0c-107">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="5cf0c-107">Filter interfaces</span></span>                        | <span data-ttu-id="5cf0c-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span><span class="sxs-lookup"><span data-stu-id="5cf0c-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span></span> |
| <span data-ttu-id="5cf0c-109">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="5cf0c-109">Input pin media types</span></span>                    | <span data-ttu-id="5cf0c-110">Cualquier tipo de medio</span><span class="sxs-lookup"><span data-stu-id="5cf0c-110">Any media type</span></span>                                                                                                       |
| <span data-ttu-id="5cf0c-111">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="5cf0c-111">Input pin interfaces</span></span>                     | <span data-ttu-id="5cf0c-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="5cf0c-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>               |
| <span data-ttu-id="5cf0c-113">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="5cf0c-113">Output pin media types</span></span>                   | <span data-ttu-id="5cf0c-114">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="5cf0c-114">Not applicable.</span></span>                                                                                                      |
| <span data-ttu-id="5cf0c-115">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="5cf0c-115">Output pin interfaces</span></span>                    | <span data-ttu-id="5cf0c-116">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="5cf0c-116">Not applicable.</span></span>                                                                                                      |
| <span data-ttu-id="5cf0c-117">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="5cf0c-117">Filter CLSID</span></span>                             | <span data-ttu-id="5cf0c-118">CLSID \_ NullRenderer</span><span class="sxs-lookup"><span data-stu-id="5cf0c-118">CLSID\_NullRenderer</span></span>                                                                                                  |
| <span data-ttu-id="5cf0c-119">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="5cf0c-119">Property Page CLSID</span></span>                      | <span data-ttu-id="5cf0c-120">Ninguna página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="5cf0c-120">No property page.</span></span>                                                                                                    |
| <span data-ttu-id="5cf0c-121">Executable</span><span class="sxs-lookup"><span data-stu-id="5cf0c-121">Executable</span></span>                               | <span data-ttu-id="5cf0c-122">Qedit.dll</span><span class="sxs-lookup"><span data-stu-id="5cf0c-122">Qedit.dll</span></span>                                                                                                            |
| [<span data-ttu-id="5cf0c-123">Fundament</span><span class="sxs-lookup"><span data-stu-id="5cf0c-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="5cf0c-124">MÉRITO \_ \_ no se \_ usa</span><span class="sxs-lookup"><span data-stu-id="5cf0c-124">MERIT\_DO\_NOT\_USE</span></span>                                                                                                  |
| [<span data-ttu-id="5cf0c-125">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="5cf0c-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="5cf0c-126">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="5cf0c-126">CLSID\_LegacyAmFilterCategory</span></span>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="5cf0c-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5cf0c-127">Remarks</span></span>

<span data-ttu-id="5cf0c-128">Use este filtro cuando un PIN de salida en el gráfico requiera una conexión de nivel inferior, pero no desea representar los datos de ese pin.</span><span class="sxs-lookup"><span data-stu-id="5cf0c-128">Use this filter when an output pin in the graph requires a downstream connection, but you do not wish to render the data from that pin.</span></span> <span data-ttu-id="5cf0c-129">Al conectar el PIN de salida al representador nulo, se completa la conexión sin representar los datos.</span><span class="sxs-lookup"><span data-stu-id="5cf0c-129">By connecting the output pin to the Null Renderer, you complete the connection without rendering the data.</span></span>

<span data-ttu-id="5cf0c-130">Aunque este filtro no representa ningún ejemplo, espera el tiempo de presentación de cada ejemplo antes de descartar el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="5cf0c-130">Even though this filter does not render any samples, it does wait for each sample's presentation time before discarding the sample.</span></span> <span data-ttu-id="5cf0c-131">Por lo tanto, el gráfico se ejecutará a la velocidad normal.</span><span class="sxs-lookup"><span data-stu-id="5cf0c-131">Therefore, the graph will run at the normal rate.</span></span> <span data-ttu-id="5cf0c-132">Si desea que el gráfico se ejecute lo más rápido posible, establezca el reloj de referencia en **null**.</span><span class="sxs-lookup"><span data-stu-id="5cf0c-132">If you want the graph the run as quickly as possible, set the reference clock to **NULL**.</span></span> <span data-ttu-id="5cf0c-133">Para obtener más información, vea [establecer el reloj del gráfico](setting-the-graph-clock.md).</span><span class="sxs-lookup"><span data-stu-id="5cf0c-133">For more information, see [Setting the Graph Clock](setting-the-graph-clock.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5cf0c-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5cf0c-134">Requirements</span></span>



| <span data-ttu-id="5cf0c-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cf0c-135">Requirement</span></span> | <span data-ttu-id="5cf0c-136">Value</span><span class="sxs-lookup"><span data-stu-id="5cf0c-136">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5cf0c-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5cf0c-137">Header</span></span><br/> | <dl> <span data-ttu-id="5cf0c-138"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="5cf0c-138"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cf0c-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="5cf0c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cf0c-140">Objetos de servicios de edición de DirectShow</span><span class="sxs-lookup"><span data-stu-id="5cf0c-140">DirectShow Editing Services Objects</span></span>](directshow-editing-services-objects.md)
</dt> </dl>

 

 




