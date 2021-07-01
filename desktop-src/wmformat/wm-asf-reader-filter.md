---
title: Filtro de lector DE ASF de WM (Windows Media Format SDK 11)
description: Obtenga información sobre el filtro wm asf reader para el SDK Windows Media Format 11. Revise la información del filtro y vea los temas relacionados.
ms.assetid: 3d5ca88a-86bd-4d84-b4f4-782564ced58d
keywords:
- Windows Media Format SDK,WM ASF Reader
- DirectShow,WM ASF Reader
- Filtros QASF, Lector DE ASF de WM
- Lector DE ASF de WM
- Formato de sistemas avanzados (ASF), lector DE ASF de WM
- ASF (formato de sistemas avanzados), LECTOR DE ASF de WM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26bde36b1b2cfa7644d6e75d8d1ff96260b2e457
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119650"
---
# <a name="wm-asf-reader-filter-windows-media-format-11-sdk"></a><span data-ttu-id="ca21f-110">Filtro de lector DE ASF de WM (Windows Media Format SDK 11)</span><span class="sxs-lookup"><span data-stu-id="ca21f-110">WM ASF Reader Filter (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="ca21f-111">Cuando se le da el nombre de un archivo ASF o una dirección URL, el lector DE ASF de WM lee el contenido comprimido, analiza las secuencias y expone un pin de salida para cada uno.</span><span class="sxs-lookup"><span data-stu-id="ca21f-111">When given the name of an ASF file or a URL, the WM ASF Reader reads the compressed content, parses the streams, and exposes an output pin for each one.</span></span> <span data-ttu-id="ca21f-112">Este filtro se conecta de bajada a la Windows Media Audio o Windows Media Video, que hacen la descompresión.</span><span class="sxs-lookup"><span data-stu-id="ca21f-112">This filter connects downstream to the Windows Media Audio or Windows Media Video DMOs, which do the decompression.</span></span> <span data-ttu-id="ca21f-113">Se admite la búsqueda si se puede buscar en el archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="ca21f-113">Seeking is supported if the ASF file is seekable.</span></span> <span data-ttu-id="ca21f-114">El lector DE ASF de WM aplica marcas de tiempo a los ejemplos multimedia en función de la marca de tiempo del archivo ASF, pero no modifica las marcas de tiempo de ninguna manera.</span><span class="sxs-lookup"><span data-stu-id="ca21f-114">The WM ASF Reader applies time stamps to the media samples based on the time stamp in the ASF file, but it does not modify the time stamps in any way.</span></span> <span data-ttu-id="ca21f-115">Internamente, el filtro usa el Windows Media Format lector para leer el contenido basado en Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ca21f-115">Internally, the filter uses the Windows Media Format reader object to read the Windows Media–based content.</span></span>

> [!Note]  
> <span data-ttu-id="ca21f-116">En el SDK de DirectX, este filtro no es el filtro de origen predeterminado para los archivos ASF, por lo que con ese SDK no se puede usar este filtro con el **método RenderFile;** debe agregarlo explícitamente al gráfico de filtros mediante su identificador de clase (CLSID).</span><span class="sxs-lookup"><span data-stu-id="ca21f-116">In the DirectX SDK, this filter is not the default source filter for ASF files, so with that SDK you cannot use this filter with the **RenderFile** method; you must explicitly add it to the filter graph by using its class identifier (CLSID).</span></span> <span data-ttu-id="ca21f-117">Este comportamiento es diferente con el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="ca21f-117">This behavior is different with the Windows Media Format SDK.</span></span> <span data-ttu-id="ca21f-118">Al instalar las bibliotecas Windows Media Format runtime del SDK, el lector de ASF de WM se registra como filtro predeterminado para los archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="ca21f-118">When you install the Windows Media Format SDK runtime libraries, the WM ASF Reader is registered as the default filter for ASF files.</span></span>

 

<span data-ttu-id="ca21f-119">La tabla siguiente contiene información sobre el filtro wm ASF Reader, como las interfaces y los tipos de medios que admite.</span><span class="sxs-lookup"><span data-stu-id="ca21f-119">The following table contains information about the WM ASF Reader filter, such as the interfaces and media types it supports.</span></span>



|  <span data-ttu-id="ca21f-120">Filtrar información</span><span class="sxs-lookup"><span data-stu-id="ca21f-120">Filter Information</span></span>                      |  <span data-ttu-id="ca21f-121">Tipos</span><span class="sxs-lookup"><span data-stu-id="ca21f-121">Types</span></span>                                                                                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca21f-122">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="ca21f-122">Filter interfaces</span></span>      | <span data-ttu-id="ca21f-123">**IBaseFilter,** **IFileSourceFilter,** **IServiceProvider,** **IWMHeaderInfo,** **IWMReaderAdvanced** (parcialmente implementado.</span><span class="sxs-lookup"><span data-stu-id="ca21f-123">**IBaseFilter**, **IFileSourceFilter**, **IServiceProvider**, **IWMHeaderInfo**, **IWMReaderAdvanced** (partially implemented.</span></span> <span data-ttu-id="ca21f-124">Vea Remarks.), **IWMReaderAdvanced2** (parcialmente implementado), **IWMDRMReader** (a través **de IServiceProvider**).</span><span class="sxs-lookup"><span data-stu-id="ca21f-124">See Remarks.), **IWMReaderAdvanced2** (partially implemented), **IWMDRMReader** (through **IServiceProvider**)</span></span> |
| <span data-ttu-id="ca21f-125">Tipos de medios de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="ca21f-125">Input pin media types</span></span>  | <span data-ttu-id="ca21f-126">No aplicable</span><span class="sxs-lookup"><span data-stu-id="ca21f-126">Not applicable</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="ca21f-127">Interfaces de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="ca21f-127">Input pin interfaces</span></span>   | <span data-ttu-id="ca21f-128">No aplicable</span><span class="sxs-lookup"><span data-stu-id="ca21f-128">Not applicable</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="ca21f-129">Tipos de medios de pin de salida</span><span class="sxs-lookup"><span data-stu-id="ca21f-129">Output pin media types</span></span> | <span data-ttu-id="ca21f-130">MEDIATYPE \_ Video, MEDIATYPE \_ Audio, MEDIATYPE \_ ScriptCommand, MEDIATYPE \_ FileTransfer</span><span class="sxs-lookup"><span data-stu-id="ca21f-130">MEDIATYPE\_Video, MEDIATYPE\_Audio, MEDIATYPE\_ScriptCommand, MEDIATYPE\_FileTransfer</span></span>                                                                                                                                                         |
| <span data-ttu-id="ca21f-131">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="ca21f-131">Format type</span></span>            | <span data-ttu-id="ca21f-132">**VIDEOINFOHEADER2 si** el contenido está [*entrelazado; de*](wmformat-glossary.md)lo **contrario, VIDEOINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="ca21f-132">**VIDEOINFOHEADER2** if content is [*interlaced*](wmformat-glossary.md), otherwise **VIDEOINFOHEADER**</span></span>                                                                                                                    |
| <span data-ttu-id="ca21f-133">Interfaces de pin de salida</span><span class="sxs-lookup"><span data-stu-id="ca21f-133">Output pin interfaces</span></span>  | <span data-ttu-id="ca21f-134">**IMediaSeeking,** **IAMWMBufferPass,** **IServiceProvider**, **IWMStreamConfig2** (a través **de IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="ca21f-134">**IMediaSeeking**, **IAMWMBufferPass**, **IServiceProvider**, **IWMStreamConfig2** (through **IServiceProvider**)</span></span>                                                                                                                             |
| <span data-ttu-id="ca21f-135">Filtrar CLSID</span><span class="sxs-lookup"><span data-stu-id="ca21f-135">Filter CLSID</span></span>           | <span data-ttu-id="ca21f-136">CLSID \_ WMAsfReader</span><span class="sxs-lookup"><span data-stu-id="ca21f-136">CLSID\_WMAsfReader</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="ca21f-137">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="ca21f-137">Property Page CLSID</span></span>    | <span data-ttu-id="ca21f-138">Ninguna página de propiedades</span><span class="sxs-lookup"><span data-stu-id="ca21f-138">No property page</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="ca21f-139">Executable</span><span class="sxs-lookup"><span data-stu-id="ca21f-139">Executable</span></span>             | <span data-ttu-id="ca21f-140">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="ca21f-140">Qasf.dll</span></span>                                                                                                                                                                                                                                      |
| <span data-ttu-id="ca21f-141">Mérito</span><span class="sxs-lookup"><span data-stu-id="ca21f-141">Merit</span></span>                  | <span data-ttu-id="ca21f-142">NO ES \_ PROBABLE QUE SE PRODUZCAN</span><span class="sxs-lookup"><span data-stu-id="ca21f-142">MERIT\_UNLIKELY</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="ca21f-143">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="ca21f-143">Filter Category</span></span>        | <span data-ttu-id="ca21f-144">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="ca21f-144">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="ca21f-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ca21f-145">Remarks</span></span>

<span data-ttu-id="ca21f-146">El lector DE ASF de WM implementa parcialmente las interfaces **IWMReaderAdvanced** e **IWMReaderAdvanced2** con el fin de proporcionar a las aplicaciones acceso a los métodos informativos en el objeto de lector.</span><span class="sxs-lookup"><span data-stu-id="ca21f-146">The WM ASF Reader partially implements the **IWMReaderAdvanced** and **IWMReaderAdvanced2** interfaces in order to give applications access to the informational methods on the reader object.</span></span> <span data-ttu-id="ca21f-147">La implementación del filtro simplemente pasa las llamadas a través de a la interfaz en el objeto de lector.</span><span class="sxs-lookup"><span data-stu-id="ca21f-147">The filter's implementation simply passes the calls through to the interface on the reader object.</span></span> <span data-ttu-id="ca21f-148">Los métodos de streaming no se implementan porque el filtro debe tener un control completo sobre el proceso de streaming.</span><span class="sxs-lookup"><span data-stu-id="ca21f-148">The streaming methods are not implemented because the filter must have complete control over the streaming process.</span></span> <span data-ttu-id="ca21f-149">Se implementan los siguientes métodos **IWMReaderAdvanced** e **IWMReaderAdvanced2:**</span><span class="sxs-lookup"><span data-stu-id="ca21f-149">The following **IWMReaderAdvanced** and **IWMReaderAdvanced2** methods are implemented:</span></span>

-   [<span data-ttu-id="ca21f-150">**IWMReaderAdvanced::GetStatistics**</span><span class="sxs-lookup"><span data-stu-id="ca21f-150">**IWMReaderAdvanced::GetStatistics**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [<span data-ttu-id="ca21f-151">**IWMReaderAdvanced::SetClientInfo**</span><span class="sxs-lookup"><span data-stu-id="ca21f-151">**IWMReaderAdvanced::SetClientInfo**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [<span data-ttu-id="ca21f-152">**IWMReaderAdvanced2::GetBufferProgress**</span><span class="sxs-lookup"><span data-stu-id="ca21f-152">**IWMReaderAdvanced2::GetBufferProgress**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [<span data-ttu-id="ca21f-153">**IWMReaderAdvanced2::GetDownloadProgress**</span><span class="sxs-lookup"><span data-stu-id="ca21f-153">**IWMReaderAdvanced2::GetDownloadProgress**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [<span data-ttu-id="ca21f-154">**IWMReaderAdvanced2::GetPlayMode**</span><span class="sxs-lookup"><span data-stu-id="ca21f-154">**IWMReaderAdvanced2::GetPlayMode**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [<span data-ttu-id="ca21f-155">**IWMReaderAdvanced2::GetProtocolName**</span><span class="sxs-lookup"><span data-stu-id="ca21f-155">**IWMReaderAdvanced2::GetProtocolName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [<span data-ttu-id="ca21f-156">**IWMReaderAdvanced2::SetLogClientID**</span><span class="sxs-lookup"><span data-stu-id="ca21f-156">**IWMReaderAdvanced2::SetLogClientID**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [<span data-ttu-id="ca21f-157">**IWMReaderAdvanced2::SetPlayMode**</span><span class="sxs-lookup"><span data-stu-id="ca21f-157">**IWMReaderAdvanced2::SetPlayMode**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a><span data-ttu-id="ca21f-158">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ca21f-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca21f-159">**Referencia de QaSF de DirectShow**</span><span class="sxs-lookup"><span data-stu-id="ca21f-159">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> <dt>

[<span data-ttu-id="ca21f-160">**Lectura de archivos ASF en DirectShow**</span><span class="sxs-lookup"><span data-stu-id="ca21f-160">**Reading ASF Files in DirectShow**</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 




