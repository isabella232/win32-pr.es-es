---
description: Filtro de AVI-MUX
ms.assetid: 31d30c91-fc6a-45ec-a2e0-34e6a1e902a4
title: Filtro de AVI-MUX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3755a4d5f63e824ae08eb736a5999dcac3d7ab32
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906826"
---
# <a name="avi-mux-filter"></a><span data-ttu-id="1e1c9-103">Filtro de AVI-MUX</span><span class="sxs-lookup"><span data-stu-id="1e1c9-103">AVI Mux Filter</span></span>

<span data-ttu-id="1e1c9-104">El filtro de AVI-MUX acepta varios flujos de entrada y los intercala en formato AVI.</span><span class="sxs-lookup"><span data-stu-id="1e1c9-104">The AVI Mux filter accepts multiple input streams and interleaves them into AVI format.</span></span> <span data-ttu-id="1e1c9-105">El filtro utiliza clavijas de entrada independientes para cada flujo de entrada y un PIN de salida para el flujo AVI.</span><span class="sxs-lookup"><span data-stu-id="1e1c9-105">The filter uses separate input pins for each input stream, and one output pin for the AVI stream.</span></span>

<span data-ttu-id="1e1c9-106">Las aplicaciones de captura de vídeo o de creación pueden utilizar este filtro para guardar archivos en el disco en formato AVI.</span><span class="sxs-lookup"><span data-stu-id="1e1c9-106">Video capture or authoring applications can use this filter to save files to disk in AVI format.</span></span> <span data-ttu-id="1e1c9-107">Normalmente, el filtro se conecta al filtro del [escritor de archivos](file-writer-filter.md) , pero puede conectarse a cualquier filtro cuyo PIN de entrada admita las interfaces IStream e [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .</span><span class="sxs-lookup"><span data-stu-id="1e1c9-107">The filter is typically connected to the [File Writer](file-writer-filter.md) filter, but it can connect to any filter whose input pin supports the IStream and [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interfaces.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e1c9-108">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="1e1c9-108">Filter Interfaces</span></span></td>
<td><span data-ttu-id="1e1c9-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfigavimux"><strong>IConfigAviMux</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving"><strong>IConfigInterleaving</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a>, ISpecifyPropertyPages</span><span class="sxs-lookup"><span data-stu-id="1e1c9-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfigavimux"><strong>IConfigAviMux</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving"><strong>IConfigInterleaving</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a>, ISpecifyPropertyPages</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e1c9-110">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="1e1c9-110">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="1e1c9-111">Cualquier tipo principal que se corresponda con un FOURCC de estilo antiguo o MEDIATYPE_AUXLine21Data.</span><span class="sxs-lookup"><span data-stu-id="1e1c9-111">Any major type that corresponds to an old-style FOURCC, or MEDIATYPE_AUXLine21Data.</span></span> <span data-ttu-id="1e1c9-112">(Para obtener más información, vea <a href="fourccmap.md"><strong>clase FOURCCMap</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="1e1c9-112">(For more information, see <a href="fourccmap.md"><strong>FOURCCMap Class</strong></a>.)</span></span>
<ul>
<li><span data-ttu-id="1e1c9-113">Si el tipo principal es MEDIATYPE_Audio, el formato debe ser FORMAT_WaveFormatEx.</span><span class="sxs-lookup"><span data-stu-id="1e1c9-113">If the major type is MEDIATYPE_Audio, the format must be FORMAT_WaveFormatEx.</span></span></li>
<li><span data-ttu-id="1e1c9-114">Si el tipo principal es MEDIATYPE_Video, el formato debe ser FORMAT_VideoInfo o FORMAT_DvInfo.</span><span class="sxs-lookup"><span data-stu-id="1e1c9-114">If the major type is MEDIATYPE_Video, the format must be FORMAT_VideoInfo or FORMAT_DvInfo.</span></span></li>
<li><span data-ttu-id="1e1c9-115">Si el tipo principal es MEDIATYPE_Interleaved, el formato debe ser FORMAT_DvInfo.</span><span class="sxs-lookup"><span data-stu-id="1e1c9-115">If the major type is MEDIATYPE_Interleaved, the format must be FORMAT_DvInfo.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e1c9-116">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="1e1c9-116">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="1e1c9-117"><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol"><strong>IAMStreamControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, IPropertyBag, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e1c9-117"><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol"><strong>IAMStreamControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, IPropertyBag, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e1c9-118">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="1e1c9-118">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="1e1c9-119">MEDIATYPE_Stream, MEDIASUBTYPE_Avi</span><span class="sxs-lookup"><span data-stu-id="1e1c9-119">MEDIATYPE_Stream, MEDIASUBTYPE_Avi</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e1c9-120">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="1e1c9-120">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="1e1c9-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="1e1c9-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e1c9-122">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="1e1c9-122">Filter CLSID</span></span></td>
<td><span data-ttu-id="1e1c9-123">CLSID_AviDest</span><span class="sxs-lookup"><span data-stu-id="1e1c9-123">CLSID_AviDest</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e1c9-124">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="1e1c9-124">Property Page CLSID</span></span></td>
<td><span data-ttu-id="1e1c9-125">CLSID_AviMuxProptyPage, CLSID_AviMuxProptyPage1</span><span class="sxs-lookup"><span data-stu-id="1e1c9-125">CLSID_AviMuxProptyPage, CLSID_AviMuxProptyPage1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e1c9-126">Executable</span><span class="sxs-lookup"><span data-stu-id="1e1c9-126">Executable</span></span></td>
<td><span data-ttu-id="1e1c9-127">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="1e1c9-127">qcap.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e1c9-128"><a href="merit.md">Fundament</a></span><span class="sxs-lookup"><span data-stu-id="1e1c9-128"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="1e1c9-129">MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="1e1c9-129">MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e1c9-130"><a href="filter-categories.md">Categoría de filtro</a></span><span class="sxs-lookup"><span data-stu-id="1e1c9-130"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="1e1c9-131">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="1e1c9-131">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="remarks"></a><span data-ttu-id="1e1c9-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1e1c9-132">Remarks</span></span>

<span data-ttu-id="1e1c9-133">En los comentarios siguientes se describen diversos aspectos de la funcionalidad del filtro de AVI.</span><span class="sxs-lookup"><span data-stu-id="1e1c9-133">The following remarks describe various aspects of the AVI Mux filter's functionality.</span></span>

<span data-ttu-id="1e1c9-134">Chinchetas</span><span class="sxs-lookup"><span data-stu-id="1e1c9-134">Pins</span></span>

<span data-ttu-id="1e1c9-135">Cuando se crea el filtro de AVI, tiene un PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="1e1c9-135">When the AVI Mux filter is created, it has one input pin.</span></span> <span data-ttu-id="1e1c9-136">A medida que cada pin de entrada está conectado, el filtro crea un nuevo PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="1e1c9-136">As each input pin is connected, the filter creates a new input pin.</span></span>

<span data-ttu-id="1e1c9-137">Propiedades de la secuencia</span><span class="sxs-lookup"><span data-stu-id="1e1c9-137">Stream Properties</span></span>

<span data-ttu-id="1e1c9-138">Los pin de entrada admiten la interfaz IPropertyBag para establecer propiedades en flujos individuales.</span><span class="sxs-lookup"><span data-stu-id="1e1c9-138">The input pins support the IPropertyBag interface for setting properties on individual streams.</span></span> <span data-ttu-id="1e1c9-139">Actualmente, se define la propiedad siguiente:</span><span class="sxs-lookup"><span data-stu-id="1e1c9-139">Currently, the following property is defined:</span></span>



| <span data-ttu-id="1e1c9-140">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1e1c9-140">Property</span></span> | <span data-ttu-id="1e1c9-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e1c9-141">Description</span></span>                                                           |
|----------|-----------------------------------------------------------------------|
| <span data-ttu-id="1e1c9-142">name</span><span class="sxs-lookup"><span data-stu-id="1e1c9-142">name</span></span>     | <span data-ttu-id="1e1c9-143">El nombre del flujo.</span><span class="sxs-lookup"><span data-stu-id="1e1c9-143">The name of the stream.</span></span> <span data-ttu-id="1e1c9-144">Esta propiedad se escribe como un `'strn'` fragmento.</span><span class="sxs-lookup"><span data-stu-id="1e1c9-144">This property is written as a `'strn'` chunk.</span></span> |



 

<span data-ttu-id="1e1c9-145">Si el filtro se está ejecutando o está en pausa, el método IPropertyBag:: Write devuelve el \_ Estado VFW E \_ incorrecto \_ .</span><span class="sxs-lookup"><span data-stu-id="1e1c9-145">If the filter is running or paused, the IPropertyBag::Write method returns VFW\_E\_WRONG\_STATE.</span></span>

<span data-ttu-id="1e1c9-146">Velocidades de fotogramas</span><span class="sxs-lookup"><span data-stu-id="1e1c9-146">Frame Rates</span></span>

<span data-ttu-id="1e1c9-147">Si el filtro de nivel superior no especifica una velocidad de fotogramas en el miembro **AvgTimePerFrame** de la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , el MUX de AVI usa las marcas de tiempo en el primer fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1e1c9-147">If the upstream filter does not specify a frame rate in the **AvgTimePerFrame** member of the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure, the AVI Mux uses the time stamps on the first video frame.</span></span> <span data-ttu-id="1e1c9-148">El formato de archivo AVI no admite velocidades de fotogramas variables.</span><span class="sxs-lookup"><span data-stu-id="1e1c9-148">The AVI file format does not support variable frame rates.</span></span>

<span data-ttu-id="1e1c9-149">Fotogramas quitados</span><span class="sxs-lookup"><span data-stu-id="1e1c9-149">Dropped Frames</span></span>

<span data-ttu-id="1e1c9-150">El filtro de AVI de AVI calcula los fotogramas quitados según las horas de los medios de cada ejemplo, si están disponibles, o bien las marcas de tiempo del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="1e1c9-150">The AVI Mux filter calculates dropped frames based on each sample's media times, if available, or else the sample's time stamps.</span></span> <span data-ttu-id="1e1c9-151">Escribe una entrada de índice de longitud cero para cada fotograma quitado.</span><span class="sxs-lookup"><span data-stu-id="1e1c9-151">It writes a zero-length index entry for every dropped frame.</span></span>

<span data-ttu-id="1e1c9-152">IMediaSeeking</span><span class="sxs-lookup"><span data-stu-id="1e1c9-152">IMediaSeeking</span></span>

<span data-ttu-id="1e1c9-153">El filtro de AVI-MUX implementa la interfaz [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="1e1c9-153">The AVI Mux filter implements the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface as follows:</span></span>

-   <span data-ttu-id="1e1c9-154">El método [**GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) devuelve el progreso actual de la multiplexación.</span><span class="sxs-lookup"><span data-stu-id="1e1c9-154">The [**GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) method returns the current progress of the multiplexing.</span></span> <span data-ttu-id="1e1c9-155">Si va a transcodificar un archivo (más lento que en tiempo real), este valor es más preciso que el valor devuelto por el administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="1e1c9-155">If you are transcoding a file (slower than real time), this value is more accurate than the value returned by the Filter Graph Manager.</span></span> <span data-ttu-id="1e1c9-156">Para obtener más información, vea la sección Comentarios de la página de referencia de GetCurrentPosition.</span><span class="sxs-lookup"><span data-stu-id="1e1c9-156">For more information, see the Remarks section of the GetCurrentPosition reference page.</span></span>
-   <span data-ttu-id="1e1c9-157">El método [**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) consulta cada filtro de nivel superior y devuelve la duración de la secuencia más larga.</span><span class="sxs-lookup"><span data-stu-id="1e1c9-157">The [**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method queries each upstream filter and returns the duration of the longest stream.</span></span> <span data-ttu-id="1e1c9-158">Si alguno de estos filtros produce un error en la llamada a GetDuration (o no admite IMediaSeeking), el MUX de AVI devuelve un código de error y rellena el parámetro *pDuration* con la duración más larga encontrada.</span><span class="sxs-lookup"><span data-stu-id="1e1c9-158">If any of these filters fails the GetDuration call (or does not support IMediaSeeking), the AVI Mux returns a failure code and fills in the *pDuration* parameter with the longest duration found.</span></span> <span data-ttu-id="1e1c9-159">Sin embargo, el valor de *pDuration* en este caso no es necesariamente la longitud del flujo de entrada más largo.</span><span class="sxs-lookup"><span data-stu-id="1e1c9-159">However, the value of *pDuration* in this case is not necessarily the length of the longest input stream.</span></span>
-   <span data-ttu-id="1e1c9-160">AVI MUX no implementa los métodos GetStopPosition, GetPositions, GetAvailable, GetRate o GetPreroll. tampoco implementa ningún \* método Set para realizar búsquedas.</span><span class="sxs-lookup"><span data-stu-id="1e1c9-160">The AVI Mux does not implement the GetStopPosition, GetPositions, GetAvailable, GetRate, or GetPreroll methods; nor does it implement any Set\* methods for seeking.</span></span>

<span data-ttu-id="1e1c9-161">Extensiones de formato de archivo AVI 2,0</span><span class="sxs-lookup"><span data-stu-id="1e1c9-161">AVI 2.0 File Format Extensions</span></span>

<span data-ttu-id="1e1c9-162">DirectShow actualmente admite las siguientes extensiones de formato de archivo AVI 2,0:</span><span class="sxs-lookup"><span data-stu-id="1e1c9-162">DirectShow currently supports the following AVI 2.0 file format extensions:</span></span>

-   <span data-ttu-id="1e1c9-163">Aumento del tamaño de archivo AVI (más de 1 GB)</span><span class="sxs-lookup"><span data-stu-id="1e1c9-163">Increased AVI file size (greater than 1 GB)</span></span>
-   <span data-ttu-id="1e1c9-164">Indexación jerárquica</span><span class="sxs-lookup"><span data-stu-id="1e1c9-164">Hierarchical indexing</span></span>

<span data-ttu-id="1e1c9-165">Para obtener más información, consulte la versión 1,02 de las "extensiones de formato de archivo AVI de OpenDML" publicada por el Subcomité formato de archivo AVI OpenDML AVI-JPEG.</span><span class="sxs-lookup"><span data-stu-id="1e1c9-165">For more information, see version 1.02 of the "OpenDML AVI File Format Extensions" published by the OpenDML AVI M-JPEG File Format Subcommittee.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e1c9-166">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1e1c9-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e1c9-167">Filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="1e1c9-167">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



