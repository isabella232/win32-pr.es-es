---
description: Filtro divisor avi
ms.assetid: df3c7d11-7ecc-499a-af36-b74437e21999
title: Filtro de divisor AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24335511e9b7b866c85792c2036a4d4b6d089f2a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909663"
---
# <a name="avi-splitter-filter"></a><span data-ttu-id="25363-103">Filtro de divisor AVI</span><span class="sxs-lookup"><span data-stu-id="25363-103">AVI Splitter Filter</span></span>

<span data-ttu-id="25363-104">El filtro divisor de AVI se usa para la reproducción de archivos AVI.</span><span class="sxs-lookup"><span data-stu-id="25363-104">The AVI Splitter Filter is used for playback of AVI files.</span></span> <span data-ttu-id="25363-105">Acepta datos en formato AVI y los divide en sus flujos constituyentes para su posterior procesamiento o representación.</span><span class="sxs-lookup"><span data-stu-id="25363-105">It accepts data in AVI format and splits it into its constituent streams for further processing and/or rendering.</span></span>



| <span data-ttu-id="25363-106">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="25363-106">Label</span></span> | <span data-ttu-id="25363-107">Value</span><span class="sxs-lookup"><span data-stu-id="25363-107">Value</span></span> |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25363-108">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="25363-108">Filter Interfaces</span></span>                        | <span data-ttu-id="25363-109">[**IAMMediaContent,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)</span><span class="sxs-lookup"><span data-stu-id="25363-109">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)</span></span>                        |
| <span data-ttu-id="25363-110">Tipos de medios de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="25363-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="25363-111">MEDIATYPE \_ Stream, MEDIASUBTYPE \_ Avi</span><span class="sxs-lookup"><span data-stu-id="25363-111">MEDIATYPE\_Stream, MEDIASUBTYPE\_Avi</span></span>                                                                                                                                |
| <span data-ttu-id="25363-112">Interfaces de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="25363-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="25363-113">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="25363-113">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                    |
| <span data-ttu-id="25363-114">Tipos de medios de pin de salida</span><span class="sxs-lookup"><span data-stu-id="25363-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="25363-115">Normalmente, **vídeo MEDIATYPE \_** o **\_ audio MEDIATYPE**.</span><span class="sxs-lookup"><span data-stu-id="25363-115">Typically **MEDIATYPE\_Video** or **MEDIATYPE\_Audio**.</span></span> <span data-ttu-id="25363-116">El tipo exacto depende del contenido del archivo, de si el archivo está comprimido y del códec que se usó.</span><span class="sxs-lookup"><span data-stu-id="25363-116">The exact type depends on the content of the file, whether the file is compressed, and what codec was used.</span></span> |
| <span data-ttu-id="25363-117">Interfaces de pin de salida</span><span class="sxs-lookup"><span data-stu-id="25363-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="25363-118">[**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin)IPropertyBag, [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="25363-118">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), IPropertyBag, [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>    |
| <span data-ttu-id="25363-119">Filtrar CLSID</span><span class="sxs-lookup"><span data-stu-id="25363-119">Filter CLSID</span></span>                             | <span data-ttu-id="25363-120">CLSID \_ AviSplitter</span><span class="sxs-lookup"><span data-stu-id="25363-120">CLSID\_AviSplitter</span></span>                                                                                                                                                  |
| <span data-ttu-id="25363-121">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="25363-121">Property Page CLSID</span></span>                      | <span data-ttu-id="25363-122">No hay ninguna página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="25363-122">No property page.</span></span>                                                                                                                                                   |
| <span data-ttu-id="25363-123">Executable</span><span class="sxs-lookup"><span data-stu-id="25363-123">Executable</span></span>                               | <span data-ttu-id="25363-124">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="25363-124">quartz.dll</span></span>                                                                                                                                                          |
| [<span data-ttu-id="25363-125">Mérito</span><span class="sxs-lookup"><span data-stu-id="25363-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="25363-126">PROCEDIMIENTO \_ NORMAL</span><span class="sxs-lookup"><span data-stu-id="25363-126">MERIT\_NORMAL</span></span>                                                                                                                                                       |
| [<span data-ttu-id="25363-127">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="25363-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="25363-128">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="25363-128">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="25363-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="25363-129">Remarks</span></span>

<span data-ttu-id="25363-130">Este filtro normalmente está conectado al filtro [Async File Source](file-source--async--filter.md) (Origen de archivo asincrónico) en su pin de entrada.</span><span class="sxs-lookup"><span data-stu-id="25363-130">This filter is typically connected to the [Async File Source](file-source--async--filter.md) filter on its input pin.</span></span> <span data-ttu-id="25363-131">Puede conectarse a cualquier filtro cuyo pin de salida admita [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) y ofrece el tipo de medio correcto al pin de entrada del filtro del divisor AVI.</span><span class="sxs-lookup"><span data-stu-id="25363-131">It can connect to any filter whose output pin supports [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) and offers the correct media type to the AVI Splitter filter's input pin.</span></span>

<span data-ttu-id="25363-132">Los pines de salida del divisor AVI admiten el método IPropertyBag::Read para leer propiedades de secuencias individuales.</span><span class="sxs-lookup"><span data-stu-id="25363-132">The output pins on the AVI Splitter support the IPropertyBag::Read method for reading properties from individual streams.</span></span> <span data-ttu-id="25363-133">Actualmente, se define la siguiente propiedad.</span><span class="sxs-lookup"><span data-stu-id="25363-133">Currently, the following property is defined.</span></span>



| <span data-ttu-id="25363-134">Propiedad</span><span class="sxs-lookup"><span data-stu-id="25363-134">Property</span></span> | <span data-ttu-id="25363-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="25363-135">Description</span></span>                                                                                                                                    |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25363-136">name</span><span class="sxs-lookup"><span data-stu-id="25363-136">name</span></span>     | <span data-ttu-id="25363-137">Devuelve el nombre de la secuencia, tomado del `'strn'` fragmento del archivo AVI.</span><span class="sxs-lookup"><span data-stu-id="25363-137">Returns the name of the stream, taken from the `'strn'` chunk in the AVI file.</span></span> <span data-ttu-id="25363-138">Si este fragmento no está presente, el método Read devuelve E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="25363-138">If this chunk is absent, the Read method returns E\_INVALIDARG.</span></span> |



 

<span data-ttu-id="25363-139">El método IPropertyBag::Write devuelve E \_ FAIL.</span><span class="sxs-lookup"><span data-stu-id="25363-139">The IPropertyBag::Write method returns E\_FAIL.</span></span> <span data-ttu-id="25363-140">El [filtro AVI Mux](avi-mux-filter.md) admite IPropertyBag::Write para guardar las propiedades de flujo en un archivo AVI.</span><span class="sxs-lookup"><span data-stu-id="25363-140">The [AVI Mux](avi-mux-filter.md) filter supports IPropertyBag::Write for saving stream properties into an AVI file.</span></span>

<span data-ttu-id="25363-141">El divisor AVI no permite que los filtros de nivel inferior usen su propio asignador.</span><span class="sxs-lookup"><span data-stu-id="25363-141">The AVI Splitter does not allow downstream filters to use their own allocator.</span></span>

<span data-ttu-id="25363-142">La duración de intercalación en el archivo determina la cantidad de memoria que asignará el divisor AVI para procesarlo.</span><span class="sxs-lookup"><span data-stu-id="25363-142">The interleaving duration in the file determines how much memory the AVI Splitter will allocate to process it.</span></span> <span data-ttu-id="25363-143">Un archivo intercalado en fragmentos de un segundo requerirá mucho más memoria para procesar que un archivo cuya duración de intercalación se establece en uno o dos fotogramas.</span><span class="sxs-lookup"><span data-stu-id="25363-143">A file that is interleaved in one second chunks will require much more memory to process than a file whose interleave duration is set to one or two frames.</span></span> <span data-ttu-id="25363-144">En equipos modernos, esto no suele ser un problema a menos que ejecute varias instancias del divisor AVI simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="25363-144">On modern computers, this is generally not an issue unless you are running multiple instances of the AVI Splitter simultaneously.</span></span>

### <a name="seeking"></a><span data-ttu-id="25363-145">Buscando</span><span class="sxs-lookup"><span data-stu-id="25363-145">Seeking</span></span>

<span data-ttu-id="25363-146">Si el archivo contiene una secuencia de vídeo, el divisor AVI admite la búsqueda por número de fotograma.</span><span class="sxs-lookup"><span data-stu-id="25363-146">If the file contains a video stream, the AVI Splitter supports seeking by frame number.</span></span> <span data-ttu-id="25363-147">Para habilitar la búsqueda basada en fotogramas, llame a [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) en el Administrador de [gráficos](filter-graph-manager.md) de filtros con el valor **TIME FORMAT \_ \_ FRAME**.</span><span class="sxs-lookup"><span data-stu-id="25363-147">To enable frame-based seeking, call [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) on the [Filter Graph Manager](filter-graph-manager.md) with the value **TIME\_FORMAT\_FRAME**.</span></span>

<span data-ttu-id="25363-148">Si el archivo contiene una secuencia de audio, el divisor AVI admite la búsqueda por número de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="25363-148">If the file contains an audio stream, the AVI Splitter supports seeking by sample number.</span></span> <span data-ttu-id="25363-149">Para habilitar la búsqueda basada en muestras, llame [**a SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) en el Administrador de gráficos de filtros con el valor **TIME FORMAT \_ \_ SAMPLE**.</span><span class="sxs-lookup"><span data-stu-id="25363-149">To enable sample-based seeking, call [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) on the Filter Graph Manager with the value **TIME\_FORMAT\_SAMPLE**.</span></span>

<span data-ttu-id="25363-150">En ambos casos, la patilla de salida de esa secuencia debe estar conectada a un filtro de representador.</span><span class="sxs-lookup"><span data-stu-id="25363-150">In both cases, the output pin for that stream must be connected to a renderer filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="25363-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="25363-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25363-152">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="25363-152">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



