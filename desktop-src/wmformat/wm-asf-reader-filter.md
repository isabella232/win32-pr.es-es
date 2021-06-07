---
title: Filtro de lector de ASF de WM (Windows Media Format SDK 11)
description: Obtenga información sobre el filtro wm asf Reader.
ms.assetid: 3d5ca88a-86bd-4d84-b4f4-782564ced58d
keywords:
- Windows Media Format SDK,WM ASF Reader
- DirectShow,WM ASF Reader
- Filtros QASF, Lector DE ASF de WM
- Lector de ASF de WM
- Advanced Systems Format (ASF),WM ASF Reader
- ASF (formato de sistemas avanzados), LECTOR DE ASF de WM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 421ab634a0d68837b22961b37005c5670d73e5fa
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444286"
---
# <a name="wm-asf-reader-filter-windows-media-format-11-sdk"></a><span data-ttu-id="4ffd3-109">Filtro de lector de ASF de WM (Windows Media Format SDK 11)</span><span class="sxs-lookup"><span data-stu-id="4ffd3-109">WM ASF Reader Filter (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="4ffd3-110">Cuando se le da el nombre de un archivo ASF o una dirección URL, el lector de ASF wm lee el contenido comprimido, analiza las secuencias y expone un pin de salida para cada uno.</span><span class="sxs-lookup"><span data-stu-id="4ffd3-110">When given the name of an ASF file or a URL, the WM ASF Reader reads the compressed content, parses the streams, and exposes an output pin for each one.</span></span> <span data-ttu-id="4ffd3-111">Este filtro se conecta de bajada a la Windows Media Audio o Windows Media Video, que hacen la descompresión.</span><span class="sxs-lookup"><span data-stu-id="4ffd3-111">This filter connects downstream to the Windows Media Audio or Windows Media Video DMOs, which do the decompression.</span></span> <span data-ttu-id="4ffd3-112">Se admite la búsqueda si se puede buscar en el archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="4ffd3-112">Seeking is supported if the ASF file is seekable.</span></span> <span data-ttu-id="4ffd3-113">El lector de ASF de WM aplica marcas de tiempo a los ejemplos de medios en función de la marca de tiempo del archivo ASF, pero no modifica las marcas de tiempo de ninguna manera.</span><span class="sxs-lookup"><span data-stu-id="4ffd3-113">The WM ASF Reader applies time stamps to the media samples based on the time stamp in the ASF file, but it does not modify the time stamps in any way.</span></span> <span data-ttu-id="4ffd3-114">Internamente, el filtro usa el Windows Media Format lector para leer el contenido basado en Windows Media.</span><span class="sxs-lookup"><span data-stu-id="4ffd3-114">Internally, the filter uses the Windows Media Format reader object to read the Windows Media–based content.</span></span>

> [!Note]  
> <span data-ttu-id="4ffd3-115">En el SDK de DirectX, este filtro no es el filtro de origen predeterminado para los archivos ASF, por lo que con ese SDK no se puede usar este filtro con el **método RenderFile.** debe agregarlo explícitamente al gráfico de filtros mediante su identificador de clase (CLSID).</span><span class="sxs-lookup"><span data-stu-id="4ffd3-115">In the DirectX SDK, this filter is not the default source filter for ASF files, so with that SDK you cannot use this filter with the **RenderFile** method; you must explicitly add it to the filter graph by using its class identifier (CLSID).</span></span> <span data-ttu-id="4ffd3-116">Este comportamiento es diferente con Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="4ffd3-116">This behavior is different with the Windows Media Format SDK.</span></span> <span data-ttu-id="4ffd3-117">Al instalar las bibliotecas en tiempo de Windows Media Format SDK, el lector de ASF de WM se registra como filtro predeterminado para los archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="4ffd3-117">When you install the Windows Media Format SDK runtime libraries, the WM ASF Reader is registered as the default filter for ASF files.</span></span>

 

<span data-ttu-id="4ffd3-118">La tabla siguiente contiene información sobre el filtro lector de ASF de WM, como las interfaces y los tipos de medios que admite.</span><span class="sxs-lookup"><span data-stu-id="4ffd3-118">The following table contains information about the WM ASF Reader filter, such as the interfaces and media types it supports.</span></span>



|  <span data-ttu-id="4ffd3-119">Filtrar información</span><span class="sxs-lookup"><span data-stu-id="4ffd3-119">Filter Information</span></span>                      |  <span data-ttu-id="4ffd3-120">Tipos</span><span class="sxs-lookup"><span data-stu-id="4ffd3-120">Types</span></span>                                                                                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ffd3-121">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="4ffd3-121">Filter interfaces</span></span>      | <span data-ttu-id="4ffd3-122">**IBaseFilter,** **IFileSourceFilter,** **IServiceProvider**, **IWMHeaderInfo**, **IWMReaderAdvanced** (implementado parcialmente.</span><span class="sxs-lookup"><span data-stu-id="4ffd3-122">**IBaseFilter**, **IFileSourceFilter**, **IServiceProvider**, **IWMHeaderInfo**, **IWMReaderAdvanced** (partially implemented.</span></span> <span data-ttu-id="4ffd3-123">Vea Remarks.), **IWMReaderAdvanced2** (parcialmente implementado), **IWMDRMReader** (a través **de IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="4ffd3-123">See Remarks.), **IWMReaderAdvanced2** (partially implemented), **IWMDRMReader** (through **IServiceProvider**)</span></span> |
| <span data-ttu-id="4ffd3-124">Tipos de medios de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="4ffd3-124">Input pin media types</span></span>  | <span data-ttu-id="4ffd3-125">No aplicable</span><span class="sxs-lookup"><span data-stu-id="4ffd3-125">Not applicable</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="4ffd3-126">Interfaces de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="4ffd3-126">Input pin interfaces</span></span>   | <span data-ttu-id="4ffd3-127">No aplicable</span><span class="sxs-lookup"><span data-stu-id="4ffd3-127">Not applicable</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="4ffd3-128">Tipos de medios de pin de salida</span><span class="sxs-lookup"><span data-stu-id="4ffd3-128">Output pin media types</span></span> | <span data-ttu-id="4ffd3-129">MEDIATYPE \_ Video, MEDIATYPE \_ Audio, MEDIATYPE \_ ScriptCommand, MEDIATYPE \_ FileTransfer</span><span class="sxs-lookup"><span data-stu-id="4ffd3-129">MEDIATYPE\_Video, MEDIATYPE\_Audio, MEDIATYPE\_ScriptCommand, MEDIATYPE\_FileTransfer</span></span>                                                                                                                                                         |
| <span data-ttu-id="4ffd3-130">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="4ffd3-130">Format type</span></span>            | <span data-ttu-id="4ffd3-131">**VIDEOINFOHEADER2 si** el contenido está [*entrelazado; de*](wmformat-glossary.md)lo **contrario, VIDEOINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="4ffd3-131">**VIDEOINFOHEADER2** if content is [*interlaced*](wmformat-glossary.md), otherwise **VIDEOINFOHEADER**</span></span>                                                                                                                    |
| <span data-ttu-id="4ffd3-132">Interfaces de pin de salida</span><span class="sxs-lookup"><span data-stu-id="4ffd3-132">Output pin interfaces</span></span>  | <span data-ttu-id="4ffd3-133">**IMediaSeeking**, **IAMWMBufferPass**, **IServiceProvider**, **IWMStreamConfig2** (a **través de IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="4ffd3-133">**IMediaSeeking**, **IAMWMBufferPass**, **IServiceProvider**, **IWMStreamConfig2** (through **IServiceProvider**)</span></span>                                                                                                                             |
| <span data-ttu-id="4ffd3-134">Filtrar CLSID</span><span class="sxs-lookup"><span data-stu-id="4ffd3-134">Filter CLSID</span></span>           | <span data-ttu-id="4ffd3-135">CLSID \_ WMAsfReader</span><span class="sxs-lookup"><span data-stu-id="4ffd3-135">CLSID\_WMAsfReader</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="4ffd3-136">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="4ffd3-136">Property Page CLSID</span></span>    | <span data-ttu-id="4ffd3-137">Ninguna página de propiedades</span><span class="sxs-lookup"><span data-stu-id="4ffd3-137">No property page</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="4ffd3-138">Executable</span><span class="sxs-lookup"><span data-stu-id="4ffd3-138">Executable</span></span>             | <span data-ttu-id="4ffd3-139">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="4ffd3-139">Qasf.dll</span></span>                                                                                                                                                                                                                                      |
| <span data-ttu-id="4ffd3-140">Mérito</span><span class="sxs-lookup"><span data-stu-id="4ffd3-140">Merit</span></span>                  | <span data-ttu-id="4ffd3-141">NO PROBABLE \_ QUE SE PRODUZCAN LOS CASO</span><span class="sxs-lookup"><span data-stu-id="4ffd3-141">MERIT\_UNLIKELY</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="4ffd3-142">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="4ffd3-142">Filter Category</span></span>        | <span data-ttu-id="4ffd3-143">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="4ffd3-143">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="4ffd3-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4ffd3-144">Remarks</span></span>

<span data-ttu-id="4ffd3-145">El Lector de ASF de WM implementa parcialmente las interfaces **IWMReaderAdvanced** e **IWMReaderAdvanced2** con el fin de proporcionar a las aplicaciones acceso a los métodos informativos en el objeto de lector.</span><span class="sxs-lookup"><span data-stu-id="4ffd3-145">The WM ASF Reader partially implements the **IWMReaderAdvanced** and **IWMReaderAdvanced2** interfaces in order to give applications access to the informational methods on the reader object.</span></span> <span data-ttu-id="4ffd3-146">La implementación del filtro simplemente pasa las llamadas a través de a la interfaz en el objeto de lector.</span><span class="sxs-lookup"><span data-stu-id="4ffd3-146">The filter's implementation simply passes the calls through to the interface on the reader object.</span></span> <span data-ttu-id="4ffd3-147">Los métodos de streaming no se implementan porque el filtro debe tener un control completo sobre el proceso de streaming.</span><span class="sxs-lookup"><span data-stu-id="4ffd3-147">The streaming methods are not implemented because the filter must have complete control over the streaming process.</span></span> <span data-ttu-id="4ffd3-148">Se implementan **los métodos IWMReaderAdvanced** e **IWMReaderAdvanced2** siguientes:</span><span class="sxs-lookup"><span data-stu-id="4ffd3-148">The following **IWMReaderAdvanced** and **IWMReaderAdvanced2** methods are implemented:</span></span>

-   [<span data-ttu-id="4ffd3-149">**IWMReaderAdvanced::GetStatistics**</span><span class="sxs-lookup"><span data-stu-id="4ffd3-149">**IWMReaderAdvanced::GetStatistics**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [<span data-ttu-id="4ffd3-150">**IWMReaderAdvanced::SetClientInfo**</span><span class="sxs-lookup"><span data-stu-id="4ffd3-150">**IWMReaderAdvanced::SetClientInfo**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [<span data-ttu-id="4ffd3-151">**IWMReaderAdvanced2::GetBufferProgress**</span><span class="sxs-lookup"><span data-stu-id="4ffd3-151">**IWMReaderAdvanced2::GetBufferProgress**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [<span data-ttu-id="4ffd3-152">**IWMReaderAdvanced2::GetDownloadProgress**</span><span class="sxs-lookup"><span data-stu-id="4ffd3-152">**IWMReaderAdvanced2::GetDownloadProgress**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [<span data-ttu-id="4ffd3-153">**IWMReaderAdvanced2::GetPlayMode**</span><span class="sxs-lookup"><span data-stu-id="4ffd3-153">**IWMReaderAdvanced2::GetPlayMode**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [<span data-ttu-id="4ffd3-154">**IWMReaderAdvanced2::GetProtocolName**</span><span class="sxs-lookup"><span data-stu-id="4ffd3-154">**IWMReaderAdvanced2::GetProtocolName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [<span data-ttu-id="4ffd3-155">**IWMReaderAdvanced2::SetLogClientID**</span><span class="sxs-lookup"><span data-stu-id="4ffd3-155">**IWMReaderAdvanced2::SetLogClientID**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [<span data-ttu-id="4ffd3-156">**IWMReaderAdvanced2::SetPlayMode**</span><span class="sxs-lookup"><span data-stu-id="4ffd3-156">**IWMReaderAdvanced2::SetPlayMode**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a><span data-ttu-id="4ffd3-157">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4ffd3-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ffd3-158">**Referencia de DirectShow QASF**</span><span class="sxs-lookup"><span data-stu-id="4ffd3-158">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> <dt>

[<span data-ttu-id="4ffd3-159">**Lectura de archivos ASF en DirectShow**</span><span class="sxs-lookup"><span data-stu-id="4ffd3-159">**Reading ASF Files in DirectShow**</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 




