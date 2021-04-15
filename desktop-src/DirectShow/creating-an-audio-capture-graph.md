---
description: Creación de un gráfico de captura de audio
ms.assetid: 2302bb40-a5db-473a-afeb-71905ac41f47
title: Creación de un gráfico de captura de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd3c731a7dc498fcb7180bc56ae6a7f94dbec6d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105666150"
---
# <a name="creating-an-audio-capture-graph"></a><span data-ttu-id="654cc-103">Creación de un gráfico de captura de audio</span><span class="sxs-lookup"><span data-stu-id="654cc-103">Creating an Audio Capture Graph</span></span>

<span data-ttu-id="654cc-104">El primer paso para una aplicación de captura de audio es crear un gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="654cc-104">The first step for an audio capture application is to build a filter graph.</span></span> <span data-ttu-id="654cc-105">La configuración del gráfico depende del tipo de archivo que desea crear.</span><span class="sxs-lookup"><span data-stu-id="654cc-105">The configuration of the graph depends on the type of file that you want to create.</span></span>

-   <span data-ttu-id="654cc-106">Archivo AVI de solo audio: filtro de captura de audio para filtro de [AVI de AVI](avi-mux-filter.md) y filtro de AVI MUX al [escritor de archivos](file-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="654cc-106">Audio-only AVI file: Audio Capture Filter to [AVI Mux](avi-mux-filter.md) filter, and AVI Mux to [File Writer](file-writer-filter.md) filter.</span></span>
-   <span data-ttu-id="654cc-107">Archivo WAV: filtro de captura de audio en el [ejemplo de filtro de WavDest](wavdest-filter-sample.md) al filtro de escritura de archivos</span><span class="sxs-lookup"><span data-stu-id="654cc-107">WAV file: Audio Capture Filter to [WavDest Filter Sample](wavdest-filter-sample.md) to File Writer Filter</span></span>
-   <span data-ttu-id="654cc-108">Archivo de Windows Media Audio (. WMA): filtro de captura de audio para el filtro del [escritor ASF de WM](wm-asf-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="654cc-108">Windows Media Audio (.wma) file: Audio Capture Filter to [WM ASF Writer](wm-asf-writer-filter.md) filter.</span></span>

<span data-ttu-id="654cc-109">El filtro WavDest se proporciona como un ejemplo de SDK.</span><span class="sxs-lookup"><span data-stu-id="654cc-109">The WavDest filter is provided as an SDK sample.</span></span> <span data-ttu-id="654cc-110">Para usarlo, debe compilar y registrar el filtro.</span><span class="sxs-lookup"><span data-stu-id="654cc-110">To use it, you must build and register the filter.</span></span>

<span data-ttu-id="654cc-111">Para usar el filtro del escritor ASF, debe instalar el SDK de Windows Media y obtener una clave de software para desbloquear el filtro.</span><span class="sxs-lookup"><span data-stu-id="654cc-111">To use the ASF Writer filter, you must install the Windows Media SDK and obtain a software key to unlock the filter.</span></span> <span data-ttu-id="654cc-112">Para obtener más información, vea [usar Windows Media en DirectShow](using-windows-media-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="654cc-112">For more information, see [Using Windows Media in DirectShow](using-windows-media-in-directshow.md).</span></span>

<span data-ttu-id="654cc-113">Puede compilar el gráfico de filtro mediante el objeto [generador de gráficos de captura](capture-graph-builder.md) o puede compilar el gráfico "manualmente". es decir, hacer que la aplicación agregue y conecte mediante programación cada filtro.</span><span class="sxs-lookup"><span data-stu-id="654cc-113">You can build the filter graph using the [Capture Graph Builder](capture-graph-builder.md) object, or you can build the graph "manually"; that is, have the application programmatically add and connect each filter.</span></span> <span data-ttu-id="654cc-114">En este artículo se describe el enfoque manual.</span><span class="sxs-lookup"><span data-stu-id="654cc-114">This article describes the manual approach.</span></span> <span data-ttu-id="654cc-115">Para obtener más información sobre cómo usar el generador de gráficos de captura, consulte [captura de vídeo](video-capture.md).</span><span class="sxs-lookup"><span data-stu-id="654cc-115">For more information about using the Capture Graph Builder, see [Video Capture](video-capture.md).</span></span> <span data-ttu-id="654cc-116">Gran parte de la información de ese artículo se aplica a los gráficos de solo audio.</span><span class="sxs-lookup"><span data-stu-id="654cc-116">Much of the information in that article applies to audio-only graphs.</span></span>

<span data-ttu-id="654cc-117">Agregar el dispositivo de captura de audio</span><span class="sxs-lookup"><span data-stu-id="654cc-117">Adding the Audio Capture Device</span></span>

<span data-ttu-id="654cc-118">Dado que el filtro de captura de audio se comunica con un dispositivo de hardware específico, no se puede llamar simplemente a **CoCreateInstance** para crear el filtro.</span><span class="sxs-lookup"><span data-stu-id="654cc-118">Because the Audio Capture Filter communicates with a specific hardware device, you cannot simply call **CoCreateInstance** to create the filter.</span></span> <span data-ttu-id="654cc-119">En su lugar, use el [enumerador de dispositivos del sistema](system-device-enumerator.md) para enumerar todos los dispositivos de la categoría "orígenes de captura de audio", que se identifica mediante el identificador de clase CLSID \_ AudioInputDeviceCategory.</span><span class="sxs-lookup"><span data-stu-id="654cc-119">Instead, use the [System Device Enumerator](system-device-enumerator.md) to enumerate all of the devices in the "Audio Capture Sources" category, which is identified by the class identifier CLSID\_AudioInputDeviceCategory.</span></span>

<span data-ttu-id="654cc-120">El enumerador de dispositivos del sistema devuelve una lista de monikers para los dispositivos; el nombre descriptivo de cada moniker corresponde al nombre del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="654cc-120">The System Device Enumerator returns a list of monikers for the devices; each moniker's friendly name corresponds to the name of the device.</span></span> <span data-ttu-id="654cc-121">Elija uno de los monikers devueltos y úselo para crear una instancia del filtro de captura de audio para ese dispositivo.</span><span class="sxs-lookup"><span data-stu-id="654cc-121">Choose one of the returned monikers and use it to create an instance of the Audio Capture Filter for that device.</span></span> <span data-ttu-id="654cc-122">Agregue el filtro al gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="654cc-122">Add the filter to the filter graph.</span></span> <span data-ttu-id="654cc-123">El dispositivo de grabación de audio preferido del usuario aparece en primer lugar en la lista de moniker.</span><span class="sxs-lookup"><span data-stu-id="654cc-123">The user's preferred audio recording device appears first in the moniker list.</span></span> <span data-ttu-id="654cc-124">(El usuario selecciona un dispositivo preferido haciendo clic en sonidos y multimedia en el panel de control).</span><span class="sxs-lookup"><span data-stu-id="654cc-124">(The user selects a preferred device by clicking Sounds and Multimedia in Control Panel.)</span></span>

<span data-ttu-id="654cc-125">Para obtener más información, vea [usar el enumerador de dispositivos del sistema](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="654cc-125">For more information, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

<span data-ttu-id="654cc-126">Para especificar la entrada que se va a capturar, obtenga la interfaz [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) del filtro de captura de audio y llame al método **Put \_ enable** para especificar la entrada.</span><span class="sxs-lookup"><span data-stu-id="654cc-126">To specify which input to capture from, obtain the [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) interface from the Audio Capture filter and call the **put\_Enable** method to specify the input.</span></span> <span data-ttu-id="654cc-127">Sin embargo, una limitación de este método es que distintos dispositivos de hardware pueden usar cadenas diferentes para identificar sus entradas.</span><span class="sxs-lookup"><span data-stu-id="654cc-127">One limitation of this method, however, is that different hardware devices may use different strings to identify their inputs.</span></span> <span data-ttu-id="654cc-128">Por ejemplo, una tarjeta puede usar "micrófono" para identificar la entrada del micrófono y otra tarjeta puede usar "MIC".</span><span class="sxs-lookup"><span data-stu-id="654cc-128">For example, one card may use "Microphone" to identify the microphone input and another card may use "Mic".</span></span> <span data-ttu-id="654cc-129">Para determinar el identificador de cadena de una entrada determinada, use las funciones multimedia de Windows [**waveOutOpen**](/previous-versions//dd743866(v=vs.85)), [**mixerOpen**](/previous-versions//dd757308(v=vs.85))y [**mixerGetLineInfo**](/previous-versions//dd757303(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="654cc-129">To determine the string identifier for a given input, use the Windows Multimedia functions [**waveOutOpen**](/previous-versions//dd743866(v=vs.85)), [**mixerOpen**](/previous-versions//dd757308(v=vs.85)), and [**mixerGetLineInfo**](/previous-versions//dd757303(v=vs.85)).</span></span> <span data-ttu-id="654cc-130">Vea el tema de MSDN [consultas de dispositivo](/windows/desktop/Multimedia/mixer-device-queries) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="654cc-130">See the MSDN topic [Mixer Device Queries](/windows/desktop/Multimedia/mixer-device-queries) for more information.</span></span>

<span data-ttu-id="654cc-131">Adición del multiplexor y del escritor de archivos</span><span class="sxs-lookup"><span data-stu-id="654cc-131">Adding the Multiplexer and the File Writer</span></span>

<span data-ttu-id="654cc-132">Un gráfico de captura de audio debe contener un multiplexor y un escritor de archivos.</span><span class="sxs-lookup"><span data-stu-id="654cc-132">An audio capture graph must contain a multiplexer and a file writer.</span></span>

<span data-ttu-id="654cc-133">Un *multiplexor* es un filtro que combina uno o varios flujos en un solo flujo con un formato determinado.</span><span class="sxs-lookup"><span data-stu-id="654cc-133">A *multiplexer* is a filter that combines one or more streams into a single stream with a particular format.</span></span> <span data-ttu-id="654cc-134">Por ejemplo, el filtro de AVI MUX combina secuencias de audio y vídeo en una secuencia AVI intercalada.</span><span class="sxs-lookup"><span data-stu-id="654cc-134">For example, the AVI Mux filter combines audio and video streams into an interleaved AVI stream.</span></span> <span data-ttu-id="654cc-135">Para la captura de audio, normalmente solo hay una única secuencia de audio, pero los datos de audio se deben empaquetar en un formato que se pueda guardar en el disco, lo que requiere un multiplexor.</span><span class="sxs-lookup"><span data-stu-id="654cc-135">For audio capture, there is typically only a single audio stream, but the audio data must still be packaged into a format that can be saved to disk, which requires a multiplexer.</span></span> <span data-ttu-id="654cc-136">La elección del multiplexor depende del formato de destino:</span><span class="sxs-lookup"><span data-stu-id="654cc-136">The choice of multiplexer depends on the target format:</span></span>

-   <span data-ttu-id="654cc-137">AVI: multiplexor de AVI</span><span class="sxs-lookup"><span data-stu-id="654cc-137">AVI: AVI Multiplexer</span></span>
-   <span data-ttu-id="654cc-138">WAV: WavDest</span><span class="sxs-lookup"><span data-stu-id="654cc-138">WAV: WavDest</span></span>
-   <span data-ttu-id="654cc-139">WMA: ASF Writer</span><span class="sxs-lookup"><span data-stu-id="654cc-139">WMA: ASF Writer</span></span>

<span data-ttu-id="654cc-140">Un *escritor de archivos* es un filtro que escribe los datos entrantes en un archivo.</span><span class="sxs-lookup"><span data-stu-id="654cc-140">A *file writer* is a filter that writes incoming data to a file.</span></span> <span data-ttu-id="654cc-141">En el caso de archivos AVI o WAV, use el [filtro de escritura de archivo](file-writer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="654cc-141">For AVI or WAV files, use the [File Writer Filter](file-writer-filter.md).</span></span> <span data-ttu-id="654cc-142">En el caso de los archivos WMA, el escritor ASF actúa como multiplexor y escritor de archivos.</span><span class="sxs-lookup"><span data-stu-id="654cc-142">For WMA files, the ASF Writer acts as both multiplexer and file writer.</span></span>

<span data-ttu-id="654cc-143">Después de crear los filtros y agregarlos al gráfico, conecte el PIN de salida del filtro de captura de audio al pin de entrada del multiplexor y conecte el PIN de salida del multiplexor al pin de entrada del escritor del filtro (suponiendo que se trata de filtros independientes).</span><span class="sxs-lookup"><span data-stu-id="654cc-143">After you create the filters and add them to the graph, connect the Audio Capture Filter's output pin to the multiplexer's input pin, and connect the multiplexer's output pin to the filter writer's input pin (assuming these are separate filters).</span></span> <span data-ttu-id="654cc-144">Para especificar el nombre de archivo, consulte el escritor de archivos para la interfaz [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) y llame al método [**IFileSinkFilter:: SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) .</span><span class="sxs-lookup"><span data-stu-id="654cc-144">To specify the file name, query the file writer for the [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) interface and call the [**IFileSinkFilter::SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) method.</span></span>

### <a name="example-code"></a><span data-ttu-id="654cc-145">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="654cc-145">Example Code</span></span>

<span data-ttu-id="654cc-146">En el ejemplo siguiente se muestra cómo crear un gráfico de captura de audio mediante el filtro WavDest.</span><span class="sxs-lookup"><span data-stu-id="654cc-146">The following example shows how to build an audio capture graph using the WavDest filter.</span></span> <span data-ttu-id="654cc-147">Los mismos principios se aplican a los demás tipos de archivo.</span><span class="sxs-lookup"><span data-stu-id="654cc-147">The same principles apply for the other file types.</span></span>


```C++
IBaseFilter *pSrc = NULL, *pWaveDest = NULL, *pWriter = NULL;
IFileSinkFilter *pSink= NULL;
IGraphBuilder *pGraph;

// Create the Filter Graph Manager.
hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER,
    IID_IGraphBuilder, (void**)&pGraph);

// This example omits error handling.

// Not shown: Use the System Device Enumerator to create the 
// audio capture filter.

// Add the audio capture filter to the filter graph. 
hr = pGraph->AddFilter(pSrc, L"Capture");

// Add the WavDest and the File Writer.
hr = AddFilterByCLSID(pGraph, CLSID_WavDest, L"WavDest", &pWaveDest);
hr = AddFilterByCLSID(pGraph, CLSID_FileWriter, L"File Writer", &pWriter);

// Set the file name.
hr = pWriter->QueryInterface(IID_IFileSinkFilter, (void**)&pSink);
hr = pSink->SetFileName(L"C:\\MyWavFile.wav", NULL);

// Connect the filters.
hr = ConnectFilters(pGraph, pSrc, pWaveDest);
hr = ConnectFilters(pGraph, pWaveDest, pWriter);

// Not shown: Release interface pointers.

```



<span data-ttu-id="654cc-148">En este ejemplo se usa la `AddFilterByCLSID` función descrita en [Agregar un filtro por CLSID](add-a-filter-by-clsid.md)y la `ConnectFilters` función descrita en [conectar dos filtros](connect-two-filters.md).</span><span class="sxs-lookup"><span data-stu-id="654cc-148">This example uses the `AddFilterByCLSID` function described in [Add a Filter by CLSID](add-a-filter-by-clsid.md), and the `ConnectFilters` function described in [Connect Two Filters](connect-two-filters.md).</span></span> <span data-ttu-id="654cc-149">Ninguno de ellos es una API de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="654cc-149">Neither of these is a DirectShow API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="654cc-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="654cc-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="654cc-151">Captura de audio</span><span class="sxs-lookup"><span data-stu-id="654cc-151">Audio Capture</span></span>](audio-capture.md)
</dt> </dl>

 

 
