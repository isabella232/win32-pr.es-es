---
title: Filtro de lector ASF de WM (Windows Media Format 11 SDK)
description: Filtro de lector ASF de WM
ms.assetid: 3d5ca88a-86bd-4d84-b4f4-782564ced58d
keywords:
- SDK de Windows Media Format, lector ASF de WM
- DirectShow, lector ASF de WM
- Filtros QASF, lector ASF de WM
- Lector ASF de WM
- Advanced Systems Format (ASF), WM ASF Reader
- ASF (formato de sistemas avanzados), lector ASF de WM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e13b7944f45b850a158c9832e174ae5ec7dce4d6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800686"
---
# <a name="wm-asf-reader-filter-windows-media-format-11-sdk"></a><span data-ttu-id="dd565-109">Filtro de lector ASF de WM (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="dd565-109">WM ASF Reader Filter (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="dd565-110">Cuando se proporciona el nombre de un archivo ASF o una dirección URL, el lector ASF de WM lee el contenido comprimido, analiza los flujos y expone un PIN de salida para cada uno de ellos.</span><span class="sxs-lookup"><span data-stu-id="dd565-110">When given the name of an ASF file or a URL, the WM ASF Reader reads the compressed content, parses the streams, and exposes an output pin for each one.</span></span> <span data-ttu-id="dd565-111">Este filtro conecta el nivel inferior al Windows Media Audio o Windows Media Video DMOs, que realizan la descompresión.</span><span class="sxs-lookup"><span data-stu-id="dd565-111">This filter connects downstream to the Windows Media Audio or Windows Media Video DMOs, which do the decompression.</span></span> <span data-ttu-id="dd565-112">La búsqueda se admite si se puede buscar en el archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="dd565-112">Seeking is supported if the ASF file is seekable.</span></span> <span data-ttu-id="dd565-113">El lector ASF de WM aplica las marcas de tiempo a los ejemplos de medios en función de la marca de tiempo del archivo ASF, pero no modifica las marcas de tiempo de ningún modo.</span><span class="sxs-lookup"><span data-stu-id="dd565-113">The WM ASF Reader applies time stamps to the media samples based on the time stamp in the ASF file, but it does not modify the time stamps in any way.</span></span> <span data-ttu-id="dd565-114">Internamente, el filtro utiliza el objeto lector de formato de Windows Media para leer el contenido basado en Windows Media.</span><span class="sxs-lookup"><span data-stu-id="dd565-114">Internally, the filter uses the Windows Media Format reader object to read the Windows Media–based content.</span></span>

> [!Note]  
> <span data-ttu-id="dd565-115">En el SDK de DirectX, este filtro no es el filtro de origen predeterminado para los archivos ASF, por lo que con ese SDK no puede usar este filtro con el método **RenderFile** ; debe agregarlo explícitamente al gráfico de filtros mediante su identificador de clase (CLSID).</span><span class="sxs-lookup"><span data-stu-id="dd565-115">In the DirectX SDK, this filter is not the default source filter for ASF files, so with that SDK you cannot use this filter with the **RenderFile** method; you must explicitly add it to the filter graph by using its class identifier (CLSID).</span></span> <span data-ttu-id="dd565-116">Este comportamiento es diferente con el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="dd565-116">This behavior is different with the Windows Media Format SDK.</span></span> <span data-ttu-id="dd565-117">Al instalar las bibliotecas en tiempo de ejecución del SDK de Windows Media Format, el lector ASF de WM se registra como filtro predeterminado para los archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="dd565-117">When you install the Windows Media Format SDK runtime libraries, the WM ASF Reader is registered as the default filter for ASF files.</span></span>

 

<span data-ttu-id="dd565-118">La tabla siguiente contiene información sobre el filtro de lector ASF de WM, como las interfaces y los tipos de medios que admite.</span><span class="sxs-lookup"><span data-stu-id="dd565-118">The following table contains information about the WM ASF Reader filter, such as the interfaces and media types it supports.</span></span>



|                        |                                                                                                                                                                                                                                               |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd565-119">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="dd565-119">Filter interfaces</span></span>      | <span data-ttu-id="dd565-120">**IBaseFilter**, **IFileSourceFilter**, **IServiceProvider**, **IWMHeaderInfo**, **IWMReaderAdvanced** (implementado parcialmente).</span><span class="sxs-lookup"><span data-stu-id="dd565-120">**IBaseFilter**, **IFileSourceFilter**, **IServiceProvider**, **IWMHeaderInfo**, **IWMReaderAdvanced** (partially implemented.</span></span> <span data-ttu-id="dd565-121">Vea la sección Comentarios.), **IWMReaderAdvanced2** (parcialmente implementado), **IWMDRMReader** (a través de **IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="dd565-121">See Remarks.), **IWMReaderAdvanced2** (partially implemented), **IWMDRMReader** (through **IServiceProvider**)</span></span> |
| <span data-ttu-id="dd565-122">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="dd565-122">Input pin media types</span></span>  | <span data-ttu-id="dd565-123">No aplicable</span><span class="sxs-lookup"><span data-stu-id="dd565-123">Not applicable</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="dd565-124">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="dd565-124">Input pin interfaces</span></span>   | <span data-ttu-id="dd565-125">No aplicable</span><span class="sxs-lookup"><span data-stu-id="dd565-125">Not applicable</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="dd565-126">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="dd565-126">Output pin media types</span></span> | <span data-ttu-id="dd565-127">MEDIATYPE \_ vídeo, mediatype \_ audio, mediatype \_ comando, mediatype \_ FileTransfer</span><span class="sxs-lookup"><span data-stu-id="dd565-127">MEDIATYPE\_Video, MEDIATYPE\_Audio, MEDIATYPE\_ScriptCommand, MEDIATYPE\_FileTransfer</span></span>                                                                                                                                                         |
| <span data-ttu-id="dd565-128">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="dd565-128">Format type</span></span>            | <span data-ttu-id="dd565-129">**VIDEOINFOHEADER2** si el contenido está [*entrelazado*](wmformat-glossary.md); de lo contrario, **VIDEOINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="dd565-129">**VIDEOINFOHEADER2** if content is [*interlaced*](wmformat-glossary.md), otherwise **VIDEOINFOHEADER**</span></span>                                                                                                                    |
| <span data-ttu-id="dd565-130">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="dd565-130">Output pin interfaces</span></span>  | <span data-ttu-id="dd565-131">**IMediaSeeking**, **IAMWMBufferPass**, **IServiceProvider**, **IWMStreamConfig2** (a través de **IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="dd565-131">**IMediaSeeking**, **IAMWMBufferPass**, **IServiceProvider**, **IWMStreamConfig2** (through **IServiceProvider**)</span></span>                                                                                                                             |
| <span data-ttu-id="dd565-132">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="dd565-132">Filter CLSID</span></span>           | <span data-ttu-id="dd565-133">CLSID \_ WMAsfReader</span><span class="sxs-lookup"><span data-stu-id="dd565-133">CLSID\_WMAsfReader</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="dd565-134">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="dd565-134">Property Page CLSID</span></span>    | <span data-ttu-id="dd565-135">Ninguna página de propiedades</span><span class="sxs-lookup"><span data-stu-id="dd565-135">No property page</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="dd565-136">Executable</span><span class="sxs-lookup"><span data-stu-id="dd565-136">Executable</span></span>             | <span data-ttu-id="dd565-137">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="dd565-137">Qasf.dll</span></span>                                                                                                                                                                                                                                      |
| <span data-ttu-id="dd565-138">Fundament</span><span class="sxs-lookup"><span data-stu-id="dd565-138">Merit</span></span>                  | <span data-ttu-id="dd565-139">MÉRITO \_ improbable</span><span class="sxs-lookup"><span data-stu-id="dd565-139">MERIT\_UNLIKELY</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="dd565-140">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="dd565-140">Filter Category</span></span>        | <span data-ttu-id="dd565-141">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="dd565-141">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="dd565-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dd565-142">Remarks</span></span>

<span data-ttu-id="dd565-143">El lector ASF de WM implementa parcialmente las interfaces **IWMReaderAdvanced** y **IWMReaderAdvanced2** para proporcionar a las aplicaciones acceso a los métodos informativos del objeto lector.</span><span class="sxs-lookup"><span data-stu-id="dd565-143">The WM ASF Reader partially implements the **IWMReaderAdvanced** and **IWMReaderAdvanced2** interfaces in order to give applications access to the informational methods on the reader object.</span></span> <span data-ttu-id="dd565-144">La implementación del filtro simplemente pasa las llamadas a la interfaz en el objeto del lector.</span><span class="sxs-lookup"><span data-stu-id="dd565-144">The filter's implementation simply passes the calls through to the interface on the reader object.</span></span> <span data-ttu-id="dd565-145">Los métodos de transmisión por secuencias no se implementan porque el filtro debe tener control total sobre el proceso de streaming.</span><span class="sxs-lookup"><span data-stu-id="dd565-145">The streaming methods are not implemented because the filter must have complete control over the streaming process.</span></span> <span data-ttu-id="dd565-146">Se implementan los siguientes métodos **IWMReaderAdvanced** y **IWMReaderAdvanced2** :</span><span class="sxs-lookup"><span data-stu-id="dd565-146">The following **IWMReaderAdvanced** and **IWMReaderAdvanced2** methods are implemented:</span></span>

-   [<span data-ttu-id="dd565-147">**IWMReaderAdvanced::GetStatistics**</span><span class="sxs-lookup"><span data-stu-id="dd565-147">**IWMReaderAdvanced::GetStatistics**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [<span data-ttu-id="dd565-148">**IWMReaderAdvanced:: SetClientInfo**</span><span class="sxs-lookup"><span data-stu-id="dd565-148">**IWMReaderAdvanced::SetClientInfo**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [<span data-ttu-id="dd565-149">**IWMReaderAdvanced2::GetBufferProgress**</span><span class="sxs-lookup"><span data-stu-id="dd565-149">**IWMReaderAdvanced2::GetBufferProgress**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [<span data-ttu-id="dd565-150">**IWMReaderAdvanced2::GetDownloadProgress**</span><span class="sxs-lookup"><span data-stu-id="dd565-150">**IWMReaderAdvanced2::GetDownloadProgress**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [<span data-ttu-id="dd565-151">**IWMReaderAdvanced2::GetPlayMode**</span><span class="sxs-lookup"><span data-stu-id="dd565-151">**IWMReaderAdvanced2::GetPlayMode**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [<span data-ttu-id="dd565-152">**IWMReaderAdvanced2::GetProtocolName**</span><span class="sxs-lookup"><span data-stu-id="dd565-152">**IWMReaderAdvanced2::GetProtocolName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [<span data-ttu-id="dd565-153">**IWMReaderAdvanced2::SetLogClientID**</span><span class="sxs-lookup"><span data-stu-id="dd565-153">**IWMReaderAdvanced2::SetLogClientID**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [<span data-ttu-id="dd565-154">**IWMReaderAdvanced2::SetPlayMode**</span><span class="sxs-lookup"><span data-stu-id="dd565-154">**IWMReaderAdvanced2::SetPlayMode**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a><span data-ttu-id="dd565-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dd565-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd565-156">**Referencia de QASF de DirectShow**</span><span class="sxs-lookup"><span data-stu-id="dd565-156">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> <dt>

[<span data-ttu-id="dd565-157">**Leer archivos ASF en DirectShow**</span><span class="sxs-lookup"><span data-stu-id="dd565-157">**Reading ASF Files in DirectShow**</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 




