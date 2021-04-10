---
description: Filtro de divisor de AVI
ms.assetid: df3c7d11-7ecc-499a-af36-b74437e21999
title: Filtro de divisor de AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e61b9a60c4c42aafa875c166ae08ccdf337793c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152602"
---
# <a name="avi-splitter-filter"></a><span data-ttu-id="18e3d-103">Filtro de divisor de AVI</span><span class="sxs-lookup"><span data-stu-id="18e3d-103">AVI Splitter Filter</span></span>

<span data-ttu-id="18e3d-104">El filtro de divisor de AVI se usa para la reproducción de archivos AVI.</span><span class="sxs-lookup"><span data-stu-id="18e3d-104">The AVI Splitter Filter is used for playback of AVI files.</span></span> <span data-ttu-id="18e3d-105">Acepta los datos en formato AVI y los divide en sus flujos constituyentes para su procesamiento y/o representación.</span><span class="sxs-lookup"><span data-stu-id="18e3d-105">It accepts data in AVI format and splits it into its constituent streams for further processing and/or rendering.</span></span>



|                                          |                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18e3d-106">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="18e3d-106">Filter Interfaces</span></span>                        | <span data-ttu-id="18e3d-107">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)</span><span class="sxs-lookup"><span data-stu-id="18e3d-107">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)</span></span>                        |
| <span data-ttu-id="18e3d-108">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="18e3d-108">Input Pin Media Types</span></span>                    | <span data-ttu-id="18e3d-109">\_Secuencia MEDIATYPE, MEDIASUBTYPE \_ AVI</span><span class="sxs-lookup"><span data-stu-id="18e3d-109">MEDIATYPE\_Stream, MEDIASUBTYPE\_Avi</span></span>                                                                                                                                |
| <span data-ttu-id="18e3d-110">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="18e3d-110">Input Pin Interfaces</span></span>                     | <span data-ttu-id="18e3d-111">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="18e3d-111">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                    |
| <span data-ttu-id="18e3d-112">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="18e3d-112">Output Pin Media Types</span></span>                   | <span data-ttu-id="18e3d-113">Normalmente **, \_ vídeo** o **\_ audio de mediatype**.</span><span class="sxs-lookup"><span data-stu-id="18e3d-113">Typically **MEDIATYPE\_Video** or **MEDIATYPE\_Audio**.</span></span> <span data-ttu-id="18e3d-114">El tipo exacto depende del contenido del archivo, si el archivo está comprimido y qué códec se ha usado.</span><span class="sxs-lookup"><span data-stu-id="18e3d-114">The exact type depends on the content of the file, whether the file is compressed, and what codec was used.</span></span> |
| <span data-ttu-id="18e3d-115">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="18e3d-115">Output Pin Interfaces</span></span>                    | <span data-ttu-id="18e3d-116">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), IPropertyBag, [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="18e3d-116">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), IPropertyBag, [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>    |
| <span data-ttu-id="18e3d-117">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="18e3d-117">Filter CLSID</span></span>                             | <span data-ttu-id="18e3d-118">CLSID \_ AviSplitter</span><span class="sxs-lookup"><span data-stu-id="18e3d-118">CLSID\_AviSplitter</span></span>                                                                                                                                                  |
| <span data-ttu-id="18e3d-119">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="18e3d-119">Property Page CLSID</span></span>                      | <span data-ttu-id="18e3d-120">Ninguna página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="18e3d-120">No property page.</span></span>                                                                                                                                                   |
| <span data-ttu-id="18e3d-121">Executable</span><span class="sxs-lookup"><span data-stu-id="18e3d-121">Executable</span></span>                               | <span data-ttu-id="18e3d-122">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="18e3d-122">quartz.dll</span></span>                                                                                                                                                          |
| [<span data-ttu-id="18e3d-123">Fundament</span><span class="sxs-lookup"><span data-stu-id="18e3d-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="18e3d-124">MÉRITO \_ normal</span><span class="sxs-lookup"><span data-stu-id="18e3d-124">MERIT\_NORMAL</span></span>                                                                                                                                                       |
| [<span data-ttu-id="18e3d-125">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="18e3d-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="18e3d-126">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="18e3d-126">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="18e3d-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="18e3d-127">Remarks</span></span>

<span data-ttu-id="18e3d-128">Este filtro se conecta normalmente al filtro de [origen de archivo asincrónico](file-source--async--filter.md) en su PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="18e3d-128">This filter is typically connected to the [Async File Source](file-source--async--filter.md) filter on its input pin.</span></span> <span data-ttu-id="18e3d-129">Puede conectarse a cualquier filtro cuyo PIN de salida admita [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) y ofrezca el tipo de medio correcto al pin de entrada del filtro de divisor de AVI.</span><span class="sxs-lookup"><span data-stu-id="18e3d-129">It can connect to any filter whose output pin supports [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) and offers the correct media type to the AVI Splitter filter's input pin.</span></span>

<span data-ttu-id="18e3d-130">Los pin de salida del divisor de AVI admiten el método IPropertyBag:: Read para leer propiedades de flujos individuales.</span><span class="sxs-lookup"><span data-stu-id="18e3d-130">The output pins on the AVI Splitter support the IPropertyBag::Read method for reading properties from individual streams.</span></span> <span data-ttu-id="18e3d-131">Actualmente, se define la propiedad siguiente.</span><span class="sxs-lookup"><span data-stu-id="18e3d-131">Currently, the following property is defined.</span></span>



| <span data-ttu-id="18e3d-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="18e3d-132">Property</span></span> | <span data-ttu-id="18e3d-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="18e3d-133">Description</span></span>                                                                                                                                    |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18e3d-134">name</span><span class="sxs-lookup"><span data-stu-id="18e3d-134">name</span></span>     | <span data-ttu-id="18e3d-135">Devuelve el nombre de la secuencia, tomada del `'strn'` fragmento en el archivo AVI.</span><span class="sxs-lookup"><span data-stu-id="18e3d-135">Returns the name of the stream, taken from the `'strn'` chunk in the AVI file.</span></span> <span data-ttu-id="18e3d-136">Si este fragmento está ausente, el método Read devuelve E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="18e3d-136">If this chunk is absent, the Read method returns E\_INVALIDARG.</span></span> |



 

<span data-ttu-id="18e3d-137">El método IPropertyBag:: Write devuelve E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="18e3d-137">The IPropertyBag::Write method returns E\_FAIL.</span></span> <span data-ttu-id="18e3d-138">El filtro de [AVI MUX](avi-mux-filter.md) admite IPropertyBag:: Write para guardar las propiedades de la secuencia en un archivo AVI.</span><span class="sxs-lookup"><span data-stu-id="18e3d-138">The [AVI Mux](avi-mux-filter.md) filter supports IPropertyBag::Write for saving stream properties into an AVI file.</span></span>

<span data-ttu-id="18e3d-139">El divisor de AVI no permite que los filtros de nivel inferior utilicen su propio asignador.</span><span class="sxs-lookup"><span data-stu-id="18e3d-139">The AVI Splitter does not allow downstream filters to use their own allocator.</span></span>

<span data-ttu-id="18e3d-140">La duración de intercalación en el archivo determina la cantidad de memoria que el divisor de AVI asignará para procesarla.</span><span class="sxs-lookup"><span data-stu-id="18e3d-140">The interleaving duration in the file determines how much memory the AVI Splitter will allocate to process it.</span></span> <span data-ttu-id="18e3d-141">Un archivo intercalado en fragmentos de un segundo requerirá mucha más memoria para procesarse que un archivo cuya duración de intercalación está establecida en uno o dos fotogramas.</span><span class="sxs-lookup"><span data-stu-id="18e3d-141">A file that is interleaved in one second chunks will require much more memory to process than a file whose interleave duration is set to one or two frames.</span></span> <span data-ttu-id="18e3d-142">En los equipos modernos, este no suele ser un problema, a menos que se ejecuten varias instancias del divisor de AVI simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="18e3d-142">On modern computers, this is generally not an issue unless you are running multiple instances of the AVI Splitter simultaneously.</span></span>

### <a name="seeking"></a><span data-ttu-id="18e3d-143">Invoca</span><span class="sxs-lookup"><span data-stu-id="18e3d-143">Seeking</span></span>

<span data-ttu-id="18e3d-144">Si el archivo contiene una secuencia de vídeo, el divisor de AVI admite búsquedas por número de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="18e3d-144">If the file contains a video stream, the AVI Splitter supports seeking by frame number.</span></span> <span data-ttu-id="18e3d-145">Para habilitar la búsqueda basada en fotogramas, llame a [**IMediaSeeking:: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) en el [Administrador de gráficos de filtro](filter-graph-manager.md) con el **\_ \_ marco de formato de hora** de valor.</span><span class="sxs-lookup"><span data-stu-id="18e3d-145">To enable frame-based seeking, call [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) on the [Filter Graph Manager](filter-graph-manager.md) with the value **TIME\_FORMAT\_FRAME**.</span></span>

<span data-ttu-id="18e3d-146">Si el archivo contiene una secuencia de audio, el divisor de AVI admite búsquedas por número de muestra.</span><span class="sxs-lookup"><span data-stu-id="18e3d-146">If the file contains an audio stream, the AVI Splitter supports seeking by sample number.</span></span> <span data-ttu-id="18e3d-147">Para habilitar la búsqueda basada en el ejemplo, llame a [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) en el administrador de gráficos de filtro con el **ejemplo de \_ formato \_ de hora** de valor.</span><span class="sxs-lookup"><span data-stu-id="18e3d-147">To enable sample-based seeking, call [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) on the Filter Graph Manager with the value **TIME\_FORMAT\_SAMPLE**.</span></span>

<span data-ttu-id="18e3d-148">En ambos casos, el PIN de salida de esa secuencia debe estar conectado a un filtro de representador.</span><span class="sxs-lookup"><span data-stu-id="18e3d-148">In both cases, the output pin for that stream must be connected to a renderer filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="18e3d-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="18e3d-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18e3d-150">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="18e3d-150">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



