---
title: Filtro wm asf writer (Windows Media Format SDK 11)
description: Obtenga información sobre el filtro WM ASF Writer.
ms.assetid: a902c92e-836d-492c-b2d2-89c216125774
keywords:
- Windows Media Format SDK,WM ASF Writer
- DirectShow,WM ASF Writer
- Filtros QASF,WM ASF Writer
- WM ASF Writer,about
- Formato de sistemas avanzados (ASF),WM ASF Writer
- ASF (formato de sistemas avanzados),WM ASF Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0fbd6e36a8178f6ebd1943cdaac214597e0ba4e
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444706"
---
# <a name="wm-asf-writer-filter-windows-media-format-11-sdk"></a><span data-ttu-id="55800-109">Filtro wm asf writer (Windows Media Format SDK 11)</span><span class="sxs-lookup"><span data-stu-id="55800-109">WM ASF Writer Filter (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="55800-110">El filtro WM ASF Writer acepta un número variable de flujos de entrada y crea un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="55800-110">The WM ASF Writer filter accepts a variable number of input streams and creates an ASF file.</span></span> <span data-ttu-id="55800-111">El filtro controla toda la compresión y multiplexación (aunque se puede omitir el mecanismo de compresión).</span><span class="sxs-lookup"><span data-stu-id="55800-111">The filter handles all compression and multiplexing (although the compression mechanism can be bypassed).</span></span> <span data-ttu-id="55800-112">Puede usar el filtro WM ASF Writer en varios escenarios, como la captura de vídeo digital (DV), la re Audio-Video compresión de audio y la conversión de archivos multimedia digitales intercalados (AVI) o MPEG para streaming de red.</span><span class="sxs-lookup"><span data-stu-id="55800-112">You can use the WM ASF Writer filter in various scenarios including digital video (DV) capture, audio recompression, and conversion of Audio-Video Interleaved (AVI) or MPEG digital media files for network streaming.</span></span> <span data-ttu-id="55800-113">Este filtro proporciona la única manera de crear archivos Windows Media Audio Microsoft Windows Media Video en DirectShow.</span><span class="sxs-lookup"><span data-stu-id="55800-113">This filter provides the only way to create Microsoft Windows Media Audio and Windows Media Video files in DirectShow.</span></span>

<span data-ttu-id="55800-114">Para obtener más información, vea [Crear archivos ASF en DirectShow.](creating-asf-files-in-directshow.md)</span><span class="sxs-lookup"><span data-stu-id="55800-114">For more information, see [Creating ASF Files in DirectShow](creating-asf-files-in-directshow.md).</span></span>

<span data-ttu-id="55800-115">La tabla siguiente contiene información sobre el filtro WM ASF Writer, como las interfaces y los tipos de medios que admite.</span><span class="sxs-lookup"><span data-stu-id="55800-115">The following table contains information about the WM ASF Writer filter, such as the interfaces and media types it supports.</span></span>



| <span data-ttu-id="55800-116">Filtrar información</span><span class="sxs-lookup"><span data-stu-id="55800-116">Filter Information</span></span>                       |  <span data-ttu-id="55800-117">Tipos</span><span class="sxs-lookup"><span data-stu-id="55800-117">Types</span></span>                                                                                                                                                                                                                       |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55800-118">Interfaces de filtro</span><span class="sxs-lookup"><span data-stu-id="55800-118">Filter interfaces</span></span>      | <span data-ttu-id="55800-119">**IAMFilterMiscFlags,** **IBaseFilter,** **IConfigAsfWriter**, **IFileSinkFilter2,** IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="55800-119">**IAMFilterMiscFlags**, **IBaseFilter**, **IConfigAsfWriter**, **IFileSinkFilter2**, IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**</span></span> |
| <span data-ttu-id="55800-120">Tipos de medios de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="55800-120">Input pin media types</span></span>  | <span data-ttu-id="55800-121">Depende del perfil.</span><span class="sxs-lookup"><span data-stu-id="55800-121">Dependent on the profile.</span></span> <span data-ttu-id="55800-122">Normalmente, los tipos sin comprimir, como audio MEDIATYPE o vídeo MEDIATYPE, aunque se pueden aceptar tipos comprimidos si \_ \_ coinciden con el perfil</span><span class="sxs-lookup"><span data-stu-id="55800-122">Typically uncompressed types like MEDIATYPE\_Audio or MEDIATYPE\_Video, although compressed types can be accepted if they match the profile</span></span>                                                   |
| <span data-ttu-id="55800-123">Interfaces de pin de entrada</span><span class="sxs-lookup"><span data-stu-id="55800-123">Input pin interfaces</span></span>   | <span data-ttu-id="55800-124">**IPin,** **IMemInputPin,** **IAMStreamConfig,** **IServiceProvider**, **IAMWMBufferPass**, **IWMStreamConfig2** (a través **de IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="55800-124">**IPin**, **IMemInputPin**, **IAMStreamConfig**, **IServiceProvider**, **IAMWMBufferPass**, **IWMStreamConfig2** (through **IServiceProvider**)</span></span>                                                                         |
| <span data-ttu-id="55800-125">Tipos de medios de pin de salida</span><span class="sxs-lookup"><span data-stu-id="55800-125">Output pin media types</span></span> | <span data-ttu-id="55800-126">No aplicable</span><span class="sxs-lookup"><span data-stu-id="55800-126">Not applicable</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="55800-127">Interfaces de pin de salida</span><span class="sxs-lookup"><span data-stu-id="55800-127">Output pin interfaces</span></span>  | <span data-ttu-id="55800-128">No aplicable</span><span class="sxs-lookup"><span data-stu-id="55800-128">Not applicable</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="55800-129">Filtrar CLSID</span><span class="sxs-lookup"><span data-stu-id="55800-129">Filter CLSID</span></span>           | <span data-ttu-id="55800-130">CLSID \_ WMAsfWriter</span><span class="sxs-lookup"><span data-stu-id="55800-130">CLSID\_WMAsfWriter</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="55800-131">CLSID de la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="55800-131">Property page CLSID</span></span>    | <span data-ttu-id="55800-132">CLSID \_ WMAsfWriterProperties</span><span class="sxs-lookup"><span data-stu-id="55800-132">CLSID\_WMAsfWriterProperties</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="55800-133">Executable</span><span class="sxs-lookup"><span data-stu-id="55800-133">Executable</span></span>             | <span data-ttu-id="55800-134">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="55800-134">Qasf.dll</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="55800-135">Mérito</span><span class="sxs-lookup"><span data-stu-id="55800-135">Merit</span></span>                  | <span data-ttu-id="55800-136">NO \_ SE USA EL VALOR DE LUGAR DE \_ \_ SERVICIO</span><span class="sxs-lookup"><span data-stu-id="55800-136">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="55800-137">Categoría de filtro</span><span class="sxs-lookup"><span data-stu-id="55800-137">Filter Category</span></span>        | <span data-ttu-id="55800-138">No especificado</span><span class="sxs-lookup"><span data-stu-id="55800-138">Not specified</span></span>                                                                                                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="55800-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="55800-139">Remarks</span></span>

<span data-ttu-id="55800-140">El número de pines de entrada en el filtro depende del perfil que se pasa al filtro.</span><span class="sxs-lookup"><span data-stu-id="55800-140">The number of input pins on the filter depends on the profile that is passed to the filter.</span></span> <span data-ttu-id="55800-141">Se crea un pin del tipo de medio adecuado para cada secuencia definida en el perfil.</span><span class="sxs-lookup"><span data-stu-id="55800-141">One pin of the appropriate media type is created for each stream defined in the profile.</span></span>

<span data-ttu-id="55800-142">Las clavijas de entrada admiten un método de la **interfaz IAMStreamConfig:** **IAMStreamConfig::GetFormat**.</span><span class="sxs-lookup"><span data-stu-id="55800-142">The input pins support one method from the **IAMStreamConfig** interface: **IAMStreamConfig::GetFormat**.</span></span> <span data-ttu-id="55800-143">Todos los demás métodos devuelven E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="55800-143">All other methods return E\_NOTIMPL.</span></span> <span data-ttu-id="55800-144">Llame al **método GetFormat** para consultar el formato de compresión de destino del pin, definido por el perfil actual.</span><span class="sxs-lookup"><span data-stu-id="55800-144">Call the **GetFormat** method to query the pin's destination compression format, which is defined by the current profile.</span></span> <span data-ttu-id="55800-145">Use la [**interfaz IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) para establecer el perfil.</span><span class="sxs-lookup"><span data-stu-id="55800-145">Use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) interface to set the profile.</span></span>

<span data-ttu-id="55800-146">La interfaz **IServiceProvider** del filtro permite a las aplicaciones recuperar la interfaz [**IWMWriterAdvanced2,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) que se define en Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="55800-146">The filter's **IServiceProvider** interface enables applications to retrieve the [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) interface, which is defined in the Windows Media Format SDK.</span></span> <span data-ttu-id="55800-147">La **interfaz IWMWriterAdvanced2** controla el desinterlazado de [](wmformat-glossary.md) vídeo y es útil si la entrada es un origen entrelazado, como DV (vídeo digital).</span><span class="sxs-lookup"><span data-stu-id="55800-147">The **IWMWriterAdvanced2** interface controls video deinterlacing, and is useful if the input is an [*interlaced*](wmformat-glossary.md) source, such as DV (digital video).</span></span> <span data-ttu-id="55800-148">Use los **métodos GetInputSetting** **y SetInputSetting** para controlar el desinterlazado.</span><span class="sxs-lookup"><span data-stu-id="55800-148">Use the **GetInputSetting** and **SetInputSetting** methods to control deinterlacing.</span></span> <span data-ttu-id="55800-149">No se recomienda que los clientes usen ninguno de los otros métodos en esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="55800-149">It is not recommended that clients use any of the other methods on this interface.</span></span> <span data-ttu-id="55800-150">Esta interfaz solo se puede obtener después de agregar el filtro al gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="55800-150">This interface can only be obtained after the filter has been added to the filter graph.</span></span> <span data-ttu-id="55800-151">En el ejemplo siguiente se muestra cómo consultar esta interfaz:</span><span class="sxs-lookup"><span data-stu-id="55800-151">The following example shows how to query for this interface:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="55800-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="55800-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55800-153">**Referencia de QaSF de DirectShow**</span><span class="sxs-lookup"><span data-stu-id="55800-153">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> </dl>

 

 
