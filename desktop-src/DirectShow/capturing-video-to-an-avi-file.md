---
description: Capturar vídeo en un archivo AVI
ms.assetid: 0f5f4a82-4a2e-4c48-b201-bda641cb8619
title: Capturar vídeo en un archivo AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86504e9ce149f495e1ea31664f56382340d33887
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104558888"
---
# <a name="capturing-video-to-an-avi-file"></a><span data-ttu-id="1cfb8-103">Capturar vídeo en un archivo AVI</span><span class="sxs-lookup"><span data-stu-id="1cfb8-103">Capturing Video to an AVI File</span></span>

<span data-ttu-id="1cfb8-104">En la ilustración siguiente se muestra el gráfico más sencillo posible para capturar vídeo en un archivo AVI.</span><span class="sxs-lookup"><span data-stu-id="1cfb8-104">The following illustration shows the simplest possible graph for capturing video to an AVI file.</span></span>

![gráfico de captura de vídeo AVI](images/vidcap02.png)

<span data-ttu-id="1cfb8-106">El filtro de [AVI-MUX](avi-mux-filter.md) toma el flujo de vídeo del PIN de captura y lo empaqueta en una secuencia AVI.</span><span class="sxs-lookup"><span data-stu-id="1cfb8-106">The [AVI Mux](avi-mux-filter.md) filter takes the video stream from the capture pin and packages it into an AVI stream.</span></span> <span data-ttu-id="1cfb8-107">También se puede conectar una secuencia de audio al filtro de AVI, en cuyo caso el MUX intercalaría las dos secuencias.</span><span class="sxs-lookup"><span data-stu-id="1cfb8-107">An audio stream could also be connected to the AVI Mux filter, in which case the mux would interleave the two streams.</span></span> <span data-ttu-id="1cfb8-108">El filtro del [escritor de archivos](file-writer-filter.md) escribe el flujo AVI en el disco.</span><span class="sxs-lookup"><span data-stu-id="1cfb8-108">The [File Writer](file-writer-filter.md) filter writes the AVI stream to disk.</span></span>

<span data-ttu-id="1cfb8-109">Para compilar el gráfico, empiece por llamar al método [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) , como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="1cfb8-109">To build the graph, start by calling the [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) method, as follows:</span></span>


```C++
IBaseFilter *pMux;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Avi,  // Specifies AVI for the target file.
    L"C:\\Example.avi", // File name.
    &pMux,              // Receives a pointer to the mux.
    NULL);              // (Optional) Receives a pointer to the file sink.
```



<span data-ttu-id="1cfb8-110">El primer parámetro especifica el tipo de archivo; en este caso, AVI.</span><span class="sxs-lookup"><span data-stu-id="1cfb8-110">The first parameter specifies the file type — in this case, AVI.</span></span> <span data-ttu-id="1cfb8-111">El segundo parámetro proporciona el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="1cfb8-111">The second parameter gives the file name.</span></span> <span data-ttu-id="1cfb8-112">Para AVI, el método SetOutputFileName crea el filtro de AVI y el filtro de escritor de archivos y los agrega al gráfico.</span><span class="sxs-lookup"><span data-stu-id="1cfb8-112">For AVI, the SetOutputFileName method cocreates the AVI Mux filter and the File Writer filter and adds them to the graph.</span></span> <span data-ttu-id="1cfb8-113">También establece el nombre de archivo en el filtro del escritor de archivos, llamando al método [**IFileSinkFilter:: SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) y conecta los dos filtros.</span><span class="sxs-lookup"><span data-stu-id="1cfb8-113">It also sets the file name on the File Writer filter, by calling the [**IFileSinkFilter::SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) method, and connects the two filters.</span></span> <span data-ttu-id="1cfb8-114">El método devuelve un puntero a AVI MUX en el tercer parámetro.</span><span class="sxs-lookup"><span data-stu-id="1cfb8-114">The method returns a pointer to the AVI Mux in the third parameter.</span></span> <span data-ttu-id="1cfb8-115">Opcionalmente, devuelve un puntero a la interfaz [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) en el cuarto parámetro.</span><span class="sxs-lookup"><span data-stu-id="1cfb8-115">Optionally, it returns a pointer to the [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) interface in the fourth parameter.</span></span> <span data-ttu-id="1cfb8-116">Si no necesita esta interfaz, puede establecer este parámetro en **null**, como se muestra en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="1cfb8-116">If you don't need this interface, you can set this parameter to **NULL**, as shown in the previous example.</span></span>

<span data-ttu-id="1cfb8-117">A continuación, llame al método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) para conectar el filtro de captura a AVI MUX, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="1cfb8-117">Next, call the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method to connect the capture filter to the AVI Mux, as follows:</span></span>


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_CAPTURE, // Pin category.
    &MEDIATYPE_Video,      // Media type.
    pCap,                  // Capture filter.
    NULL,                  // Intermediate filter (optional).
    pMux);                 // Mux or file sink filter.

// Release the mux filter.
pMux->Release();
```



<span data-ttu-id="1cfb8-118">El primer parámetro proporciona la categoría PIN, que es la \_ \_ captura de categoría PIN para la captura.</span><span class="sxs-lookup"><span data-stu-id="1cfb8-118">The first parameter gives the pin category, which is PIN\_CATEGORY\_CAPTURE for capture.</span></span> <span data-ttu-id="1cfb8-119">El segundo parámetro proporciona el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="1cfb8-119">The second parameter gives the media type.</span></span> <span data-ttu-id="1cfb8-120">El tercer parámetro es un puntero a la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="1cfb8-120">The third parameter is a pointer to the capture filter's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span> <span data-ttu-id="1cfb8-121">El cuarto parámetro es opcional. permite enrutar el flujo de vídeo a través de un filtro intermedio, como un codificador, antes de pasarlo al filtro Mux.</span><span class="sxs-lookup"><span data-stu-id="1cfb8-121">The fourth parameter is optional; it lets you route the video stream through an intermediate filter, such as an encoder, before passing it to the mux filter.</span></span> <span data-ttu-id="1cfb8-122">De lo contrario, establezca este parámetro en **null**, como se muestra en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="1cfb8-122">Otherwise, set this parameter to **NULL**, as shown in the previous example.</span></span> <span data-ttu-id="1cfb8-123">El quinto parámetro es el puntero al filtro Mux.</span><span class="sxs-lookup"><span data-stu-id="1cfb8-123">The fifth parameter is the pointer to the mux filter.</span></span> <span data-ttu-id="1cfb8-124">Este puntero se obtiene llamando al método SetOutputFileName.</span><span class="sxs-lookup"><span data-stu-id="1cfb8-124">This pointer is obtained by calling the SetOutputFileName method.</span></span>

<span data-ttu-id="1cfb8-125">Para capturar audio, llame a RenderStream con el tipo de archivo multimedia MEDIATYPE \_ audio.</span><span class="sxs-lookup"><span data-stu-id="1cfb8-125">To capture audio, call RenderStream with the media type MEDIATYPE\_Audio.</span></span> <span data-ttu-id="1cfb8-126">Si va a capturar audio y vídeo desde dos dispositivos independientes, es una buena idea convertir la secuencia de audio en la secuencia maestra.</span><span class="sxs-lookup"><span data-stu-id="1cfb8-126">If you are capturing audio and video from two separate devices, it is a good idea to make the audio stream the master stream.</span></span> <span data-ttu-id="1cfb8-127">Esto ayuda a evitar el desplazamiento entre los dos flujos, ya que el filtro de AVI MUX ajusta la velocidad de reproducción en el flujo de vídeo para que coincida con la secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="1cfb8-127">This helps to prevent drift between the two streams, because the AVI Mux filter adjust the playback rate on the video stream to match the audio stream.</span></span> <span data-ttu-id="1cfb8-128">Para establecer la secuencia maestra, llame al método [**IConfigAviMux:: SetMasterStream**](/windows/desktop/api/Strmif/nf-strmif-iconfigavimux-setmasterstream) en el filtro de AVI MUX:</span><span class="sxs-lookup"><span data-stu-id="1cfb8-128">To set the master stream, call the [**IConfigAviMux::SetMasterStream**](/windows/desktop/api/Strmif/nf-strmif-iconfigavimux-setmasterstream) method on the AVI Mux filter:</span></span>


```C++
IConfigAviMux *pConfigMux = NULL;
hr = pMux->QueryInterface(IID_IConfigAviMux, (void**)&pConfigMux);
if (SUCCEEDED(hr))
{
    pConfigMux->SetMasterStream(1);
    pConfigMux->Release();
}
```



<span data-ttu-id="1cfb8-129">El parámetro para SetMasterStream es el número de secuencia, que viene determinado por el orden en el que se llama a RenderStream.</span><span class="sxs-lookup"><span data-stu-id="1cfb8-129">The parameter to SetMasterStream is the stream number, which is determined by the order in which you call RenderStream.</span></span> <span data-ttu-id="1cfb8-130">Por ejemplo, si llama primero a RenderStream para el vídeo y luego para audio, el vídeo es el flujo 0 y el audio es el flujo 1.</span><span class="sxs-lookup"><span data-stu-id="1cfb8-130">For example, if you call RenderStream first for video and then for audio, the video is stream 0 and the audio is stream 1.</span></span>

<span data-ttu-id="1cfb8-131">También puede establecer el modo en que el filtro de AVI MUX intercala las secuencias de audio y vídeo, llamando al método [**IConfigInterleaving::p \_ UT**](/windows/desktop/api/Strmif/nf-strmif-iconfiginterleaving-put_mode) .</span><span class="sxs-lookup"><span data-stu-id="1cfb8-131">You may also want to set how the AVI Mux filter interleaves the audio and video streams, by calling the [**IConfigInterleaving::put\_Mode**](/windows/desktop/api/Strmif/nf-strmif-iconfiginterleaving-put_mode) method.</span></span>


```C++
IConfigInterleaving *pInterleave = NULL;
hr = pMux->QueryInterface(IID_IConfigInterleaving, (void**)&pInterleave);
if (SUCCEEDED(hr))
{
    pInterleave->put_Mode(INTERLEAVE_CAPTURE);
    pInterleave->Release();
}
```



<span data-ttu-id="1cfb8-132">Con la marca de captura de intercalación \_ , AVI MUX realiza la intercalación a una velocidad adecuada para la captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1cfb8-132">With the INTERLEAVE\_CAPTURE flag, the AVI Mux performs interleaving at a rate that is suitable for video capture.</span></span> <span data-ttu-id="1cfb8-133">También puede usar la intercalación \_ None, lo que significa que no hay intercalación: AVI MUX simplemente escribirá los datos en el orden en que llegan.</span><span class="sxs-lookup"><span data-stu-id="1cfb8-133">You can also use INTERLEAVE\_NONE, which means no interleaving — the AVI Mux will simply write the data in the order that it arrives.</span></span> <span data-ttu-id="1cfb8-134">La marca de intercalación \_ completa significa que AVI MUX realiza una intercalación completa; sin embargo, este modo es menos adecuado para la captura de vídeo porque requiere el mayor nivel de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="1cfb8-134">The INTERLEAVE\_FULL flag means the AVI Mux performs full interleaving; however, this mode is less suitable for video capture because it requires the most overheard.</span></span>

<span data-ttu-id="1cfb8-135">Codificar la secuencia de vídeo</span><span class="sxs-lookup"><span data-stu-id="1cfb8-135">Encoding the Video Stream</span></span>

<span data-ttu-id="1cfb8-136">Puede codificar el flujo de vídeo insertando un filtro de codificador entre el filtro de captura y el filtro de AVI.</span><span class="sxs-lookup"><span data-stu-id="1cfb8-136">You can encode the video stream by inserting an encoder filter between the capture filter and the AVI Mux filter.</span></span> <span data-ttu-id="1cfb8-137">Use el [enumerador de dispositivos del sistema](system-device-enumerator.md) o el [asignador de filtros](filter-mapper.md) para seleccionar un filtro de codificador.</span><span class="sxs-lookup"><span data-stu-id="1cfb8-137">Use the [System Device Enumerator](system-device-enumerator.md) or the [Filter Mapper](filter-mapper.md) to select an encoder filter.</span></span> <span data-ttu-id="1cfb8-138">(Para obtener más información, consulte [enumeración de dispositivos y filtros](enumerating-devices-and-filters.md)).</span><span class="sxs-lookup"><span data-stu-id="1cfb8-138">(For more information, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).)</span></span>

<span data-ttu-id="1cfb8-139">Especifique el filtro del codificador como cuarto parámetro en RenderStream, que se muestra en negrita en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="1cfb8-139">Specify the encoder filter as the fourth parameter to RenderStream, shown in bold in the following example:</span></span>


```C++
IBaseFilter *pEncoder;
/* Create the encoder filter (not shown). */
// Add it to the filter graph.
pGraph->AddFilter(pEncoder, L"Encoder");

/* Call SetOutputFileName as shown previously. */

// Render the stream.
hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, 
    pCap, 
pEncoder, pMux);
pEncoder->Release();
```



<span data-ttu-id="1cfb8-140">El filtro del codificador podría admitir [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) u otras interfaces para establecer los parámetros de codificación.</span><span class="sxs-lookup"><span data-stu-id="1cfb8-140">The encoder filter might support [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) or other interfaces for setting the encoding parameters.</span></span> <span data-ttu-id="1cfb8-141">Para obtener una lista de interfaces posibles, vea [interfaces de codificación y descodificación de archivos](file-encoding-and-decoding-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="1cfb8-141">For a list of possible interfaces, see [File Encoding and Decoding Interfaces](file-encoding-and-decoding-interfaces.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1cfb8-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1cfb8-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1cfb8-143">Capturar vídeo en un archivo</span><span class="sxs-lookup"><span data-stu-id="1cfb8-143">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 



