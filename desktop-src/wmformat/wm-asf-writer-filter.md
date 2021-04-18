---
title: Filtro del escritor ASF de WM (Windows Media Format 11 SDK)
description: Filtro de escritor ASF de WM
ms.assetid: a902c92e-836d-492c-b2d2-89c216125774
keywords:
- Windows Media Format SDK, WM ASF Writer
- DirectShow, escritor ASF de WM
- Filtros de QASF, escritor ASF de WM
- Escritor ASF de WM, acerca de
- Advanced Systems Format (ASF), WM ASF Writer
- ASF (formato de sistemas avanzados), escritor ASF de WM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d0de34bcf4b4047673f832d78f40377f98e94d6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105685816"
---
# <a name="wm-asf-writer-filter-windows-media-format-11-sdk"></a><span data-ttu-id="e3313-109">Filtro del escritor ASF de WM (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="e3313-109">WM ASF Writer Filter (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="e3313-110">El filtro de escritura ASF de WM acepta un número variable de flujos de entrada y crea un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="e3313-110">The WM ASF Writer filter accepts a variable number of input streams and creates an ASF file.</span></span> <span data-ttu-id="e3313-111">El filtro controla toda la compresión y multiplexación (aunque se puede omitir el mecanismo de compresión).</span><span class="sxs-lookup"><span data-stu-id="e3313-111">The filter handles all compression and multiplexing (although the compression mechanism can be bypassed).</span></span> <span data-ttu-id="e3313-112">Puede usar el filtro de escritor ASF de WM en varios escenarios, como la captura Audio-Video de vídeo digital (DV), la recompresión de audio y la conversión de archivos multimedia digitales intercalados (AVI) o MPEG para la transmisión por secuencias de la red.</span><span class="sxs-lookup"><span data-stu-id="e3313-112">You can use the WM ASF Writer filter in various scenarios including digital video (DV) capture, audio recompression, and conversion of Audio-Video Interleaved (AVI) or MPEG digital media files for network streaming.</span></span> <span data-ttu-id="e3313-113">Este filtro proporciona la única manera de crear archivos de Microsoft Windows Media Audio y Windows Media Video en DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e3313-113">This filter provides the only way to create Microsoft Windows Media Audio and Windows Media Video files in DirectShow.</span></span>

<span data-ttu-id="e3313-114">Para obtener más información, vea [crear archivos ASF en DirectShow](creating-asf-files-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="e3313-114">For more information, see [Creating ASF Files in DirectShow](creating-asf-files-in-directshow.md).</span></span>

<span data-ttu-id="e3313-115">La tabla siguiente contiene información sobre el filtro del escritor ASF de WM, como las interfaces y los tipos de medios que admite.</span><span class="sxs-lookup"><span data-stu-id="e3313-115">The following table contains information about the WM ASF Writer filter, such as the interfaces and media types it supports.</span></span>



|                        |                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3313-116">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="e3313-116">Filter interfaces</span></span>      | <span data-ttu-id="e3313-117">**IAMFilterMiscFlags**, **IBaseFilter**, **IConfigAsfWriter**, **IFileSinkFilter2**, IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="e3313-117">**IAMFilterMiscFlags**, **IBaseFilter**, **IConfigAsfWriter**, **IFileSinkFilter2**, IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**</span></span> |
| <span data-ttu-id="e3313-118">Tipos de medios de anclaje de entrada</span><span class="sxs-lookup"><span data-stu-id="e3313-118">Input pin media types</span></span>  | <span data-ttu-id="e3313-119">Depende del perfil.</span><span class="sxs-lookup"><span data-stu-id="e3313-119">Dependent on the profile.</span></span> <span data-ttu-id="e3313-120">Normalmente tipos sin comprimir como \_ el vídeo de tipo mediatype audio o mediatype \_ , aunque se pueden aceptar tipos comprimidos si coinciden con el perfil</span><span class="sxs-lookup"><span data-stu-id="e3313-120">Typically uncompressed types like MEDIATYPE\_Audio or MEDIATYPE\_Video, although compressed types can be accepted if they match the profile</span></span>                                                   |
| <span data-ttu-id="e3313-121">Interfaces de PIN de entrada</span><span class="sxs-lookup"><span data-stu-id="e3313-121">Input pin interfaces</span></span>   | <span data-ttu-id="e3313-122">**IPin**, **IMemInputPin**, **IAMStreamConfig**, **IServiceProvider**, **IAMWMBufferPass**, **IWMStreamConfig2** (a través de **IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="e3313-122">**IPin**, **IMemInputPin**, **IAMStreamConfig**, **IServiceProvider**, **IAMWMBufferPass**, **IWMStreamConfig2** (through **IServiceProvider**)</span></span>                                                                         |
| <span data-ttu-id="e3313-123">Tipos de medios de anclaje de salida</span><span class="sxs-lookup"><span data-stu-id="e3313-123">Output pin media types</span></span> | <span data-ttu-id="e3313-124">No aplicable</span><span class="sxs-lookup"><span data-stu-id="e3313-124">Not applicable</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="e3313-125">Interfaces de clavija de salida</span><span class="sxs-lookup"><span data-stu-id="e3313-125">Output pin interfaces</span></span>  | <span data-ttu-id="e3313-126">No aplicable</span><span class="sxs-lookup"><span data-stu-id="e3313-126">Not applicable</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="e3313-127">Identificador CLSID</span><span class="sxs-lookup"><span data-stu-id="e3313-127">Filter CLSID</span></span>           | <span data-ttu-id="e3313-128">CLSID \_ WMAsfWriter</span><span class="sxs-lookup"><span data-stu-id="e3313-128">CLSID\_WMAsfWriter</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="e3313-129">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="e3313-129">Property page CLSID</span></span>    | <span data-ttu-id="e3313-130">CLSID \_ WMAsfWriterProperties</span><span class="sxs-lookup"><span data-stu-id="e3313-130">CLSID\_WMAsfWriterProperties</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="e3313-131">Executable</span><span class="sxs-lookup"><span data-stu-id="e3313-131">Executable</span></span>             | <span data-ttu-id="e3313-132">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="e3313-132">Qasf.dll</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="e3313-133">Fundament</span><span class="sxs-lookup"><span data-stu-id="e3313-133">Merit</span></span>                  | <span data-ttu-id="e3313-134">MÉRITO \_ \_ no se \_ usa</span><span class="sxs-lookup"><span data-stu-id="e3313-134">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="e3313-135">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="e3313-135">Filter Category</span></span>        | <span data-ttu-id="e3313-136">No especificado</span><span class="sxs-lookup"><span data-stu-id="e3313-136">Not specified</span></span>                                                                                                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="e3313-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e3313-137">Remarks</span></span>

<span data-ttu-id="e3313-138">El número de clavijas de entrada en el filtro depende del perfil que se pasa al filtro.</span><span class="sxs-lookup"><span data-stu-id="e3313-138">The number of input pins on the filter depends on the profile that is passed to the filter.</span></span> <span data-ttu-id="e3313-139">Se crea un PIN del tipo de medio adecuado para cada flujo definido en el perfil.</span><span class="sxs-lookup"><span data-stu-id="e3313-139">One pin of the appropriate media type is created for each stream defined in the profile.</span></span>

<span data-ttu-id="e3313-140">Los pin de entrada admiten un método de la interfaz **IAMStreamConfig** : **IAMStreamConfig:: GetFormat**.</span><span class="sxs-lookup"><span data-stu-id="e3313-140">The input pins support one method from the **IAMStreamConfig** interface: **IAMStreamConfig::GetFormat**.</span></span> <span data-ttu-id="e3313-141">Todos los demás métodos devuelven E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="e3313-141">All other methods return E\_NOTIMPL.</span></span> <span data-ttu-id="e3313-142">Llame al método **GetFormat** para consultar el formato de compresión de destino del PIN, definido por el perfil actual.</span><span class="sxs-lookup"><span data-stu-id="e3313-142">Call the **GetFormat** method to query the pin's destination compression format, which is defined by the current profile.</span></span> <span data-ttu-id="e3313-143">Use la interfaz [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) para establecer el perfil.</span><span class="sxs-lookup"><span data-stu-id="e3313-143">Use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) interface to set the profile.</span></span>

<span data-ttu-id="e3313-144">La interfaz **IServiceProvider** del filtro permite a las aplicaciones recuperar la interfaz [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) , que se define en el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="e3313-144">The filter's **IServiceProvider** interface enables applications to retrieve the [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) interface, which is defined in the Windows Media Format SDK.</span></span> <span data-ttu-id="e3313-145">La interfaz **IWMWriterAdvanced2** controla el desentrelazado de vídeo y es útil si la entrada es un origen [*entrelazado*](wmformat-glossary.md) , como DV (vídeo digital).</span><span class="sxs-lookup"><span data-stu-id="e3313-145">The **IWMWriterAdvanced2** interface controls video deinterlacing, and is useful if the input is an [*interlaced*](wmformat-glossary.md) source, such as DV (digital video).</span></span> <span data-ttu-id="e3313-146">Use los métodos **GetInputSetting** y **SetInputSetting** para controlar el desentrelazado.</span><span class="sxs-lookup"><span data-stu-id="e3313-146">Use the **GetInputSetting** and **SetInputSetting** methods to control deinterlacing.</span></span> <span data-ttu-id="e3313-147">No se recomienda que los clientes usen ninguno de los otros métodos de esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="e3313-147">It is not recommended that clients use any of the other methods on this interface.</span></span> <span data-ttu-id="e3313-148">Esta interfaz solo se puede obtener una vez que se ha agregado el filtro al gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="e3313-148">This interface can only be obtained after the filter has been added to the filter graph.</span></span> <span data-ttu-id="e3313-149">En el ejemplo siguiente se muestra cómo consultar esta interfaz:</span><span class="sxs-lookup"><span data-stu-id="e3313-149">The following example shows how to query for this interface:</span></span>


```C++
// Assume that m_pGraph is a valid IGraphBuilder interface pointer,
// and that pAsfWriter points to the IBaseFilter interface
// on the WM ASF Writer filter.

IServiceProvider *pProvider = NULL;
IWMWriterAdvanced2 *pWMWA2 = NULL;

hr = m_pGraph->AddFilter(pAsfWriter, L"WM ASF Writer");
...
hr = pAsfWriter->QueryInterface(IID_IServiceProvider, (void**)&pProvider)
if (SUCCEEDED(hr))
{
    hr = pProvider->QueryService(IID_IWMWriterAdvanced2,
        IID_IWMWriterAdvanced2, (void**)&pWMWA2);
    pProvider->Release();
}

```



## <a name="related-topics"></a><span data-ttu-id="e3313-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e3313-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3313-151">**Referencia de QASF de DirectShow**</span><span class="sxs-lookup"><span data-stu-id="e3313-151">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> </dl>

 

 
