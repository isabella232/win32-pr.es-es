---
description: Escribir un proyecto en un archivo
ms.assetid: 84499e4f-4f45-4aa6-aa89-d95c3b6b47d0
title: Escribir un proyecto en un archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f63ddbc6a021362134d420220f7e25c662553f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687719"
---
# <a name="writing-a-project-to-a-file"></a><span data-ttu-id="ffee6-103">Escribir un proyecto en un archivo</span><span class="sxs-lookup"><span data-stu-id="ffee6-103">Writing a Project to a File</span></span>

<span data-ttu-id="ffee6-104">\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="ffee6-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="ffee6-105">En este artículo se describe cómo escribir un proyecto de [servicios de edición de DirectShow](directshow-editing-services.md) en un archivo.</span><span class="sxs-lookup"><span data-stu-id="ffee6-105">This article describes how to write a [DirectShow Editing Services](directshow-editing-services.md) project to a file.</span></span> <span data-ttu-id="ffee6-106">En primer lugar, se describe cómo escribir un archivo con el motor de representación básico.</span><span class="sxs-lookup"><span data-stu-id="ffee6-106">First it describes how to write a file with the basic render engine.</span></span> <span data-ttu-id="ffee6-107">A continuación, se describe la recompresión inteligente con el motor de representación inteligente.</span><span class="sxs-lookup"><span data-stu-id="ffee6-107">Then it describes smart recompression with the smart render engine.</span></span>

<span data-ttu-id="ffee6-108">Para obtener información general sobre cómo los servicios de edición de DirectShow representan proyectos, consulte [acerca de los motores de representación](about-the-render-engines.md).</span><span class="sxs-lookup"><span data-stu-id="ffee6-108">For an overview of how DirectShow Editing Services renders projects, see [About the Render Engines](about-the-render-engines.md).</span></span>

<span data-ttu-id="ffee6-109">**Usar el motor de representación básico**</span><span class="sxs-lookup"><span data-stu-id="ffee6-109">**Using the Basic Render Engine**</span></span>

<span data-ttu-id="ffee6-110">Empiece por crear el front-end del gráfico, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="ffee6-110">Start by building the front end of the graph, as follows:</span></span>

1.  <span data-ttu-id="ffee6-111">Cree el motor de representación.</span><span class="sxs-lookup"><span data-stu-id="ffee6-111">Create the render engine.</span></span>
2.  <span data-ttu-id="ffee6-112">Especifique la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="ffee6-112">Specify the timeline.</span></span>
3.  <span data-ttu-id="ffee6-113">Establezca el intervalo de representación.</span><span class="sxs-lookup"><span data-stu-id="ffee6-113">Set the render range.</span></span> <span data-ttu-id="ffee6-114">(Opcional)</span><span class="sxs-lookup"><span data-stu-id="ffee6-114">(Optional)</span></span>
4.  <span data-ttu-id="ffee6-115">Cree el front-end del gráfico.</span><span class="sxs-lookup"><span data-stu-id="ffee6-115">Build the front end of the graph.</span></span>

<span data-ttu-id="ffee6-116">En el ejemplo de código siguiente se muestran estos pasos.</span><span class="sxs-lookup"><span data-stu-id="ffee6-116">The following code example shows these steps.</span></span>


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC,
    IID_IRenderEngine, (void**) &pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd( );
```



<span data-ttu-id="ffee6-117">A continuación, agregue filtros multiplexores y de escritura de archivos al gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="ffee6-117">Next, add multiplexer and file-writing filters to the filter graph.</span></span> <span data-ttu-id="ffee6-118">La forma más fácil de hacerlo es con el [generador de gráficos de captura](capture-graph-builder.md), un componente de DirectShow para crear gráficos de captura.</span><span class="sxs-lookup"><span data-stu-id="ffee6-118">The easiest way to do this is with the [Capture Graph Builder](capture-graph-builder.md), a DirectShow component for building capture graphs.</span></span> <span data-ttu-id="ffee6-119">El generador de gráficos de captura expone la interfaz [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) .</span><span class="sxs-lookup"><span data-stu-id="ffee6-119">The capture graph builder exposes the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface.</span></span> <span data-ttu-id="ffee6-120">Lleve a cabo los siguiente pasos:</span><span class="sxs-lookup"><span data-stu-id="ffee6-120">Perform the following steps:</span></span>

1.  <span data-ttu-id="ffee6-121">Cree una instancia del generador de gráficos de captura.</span><span class="sxs-lookup"><span data-stu-id="ffee6-121">Create an instance of the capture graph builder.</span></span>
2.  <span data-ttu-id="ffee6-122">Obtenga un puntero al gráfico y páselo al generador de gráficos.</span><span class="sxs-lookup"><span data-stu-id="ffee6-122">Obtain a pointer to the graph and pass it to the graph builder.</span></span>
3.  <span data-ttu-id="ffee6-123">Especifique el nombre y el tipo de medio del archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="ffee6-123">Specify the name and media type of the output file.</span></span> <span data-ttu-id="ffee6-124">Este paso también obtiene un puntero al filtro MUX, que es necesario más adelante.</span><span class="sxs-lookup"><span data-stu-id="ffee6-124">This step also obtains a pointer to the mux filter, which is required later.</span></span>

<span data-ttu-id="ffee6-125">En el ejemplo de código siguiente se muestran estos pasos.</span><span class="sxs-lookup"><span data-stu-id="ffee6-125">The following code example shows these steps.</span></span>


```C++
CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL, CLSCTX_INPROC, 
    IID_ICaptureGraphBuilder2, (void **)&pBuilder);

// Get a pointer to the graph front end.
IGraphBuilder *pGraph;
pRender->GetFilterGraph(&pGraph);
pBuilder->SetFiltergraph(pGraph);

// Create the file-writing section.
IBaseFilter *pMux;
pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("Output.avi"), &pMux, NULL);
```



<span data-ttu-id="ffee6-126">Por último, conecte los terminales de salida en el front-end al filtro Mux.</span><span class="sxs-lookup"><span data-stu-id="ffee6-126">Finally, connect the output pins on the front end to the mux filter.</span></span>

1.  <span data-ttu-id="ffee6-127">Recupere el número de grupos.</span><span class="sxs-lookup"><span data-stu-id="ffee6-127">Retrieve the number of groups.</span></span>
2.  <span data-ttu-id="ffee6-128">Para cada pin, obtenga un puntero al pin.</span><span class="sxs-lookup"><span data-stu-id="ffee6-128">For each pin, obtain a pointer to the pin.</span></span>
3.  <span data-ttu-id="ffee6-129">Opcionalmente, cree una instancia de un filtro de compresión para comprimir la secuencia.</span><span class="sxs-lookup"><span data-stu-id="ffee6-129">Optionally, create an instance of a compression filter to compress the stream.</span></span> <span data-ttu-id="ffee6-130">El tipo de compresor dependerá del tipo de medio del grupo.</span><span class="sxs-lookup"><span data-stu-id="ffee6-130">The type of compressor will depend on the media type of the group.</span></span> <span data-ttu-id="ffee6-131">Puede usar el [enumerador de dispositivos del sistema](system-device-enumerator.md) para enumerar los filtros de compresión disponibles.</span><span class="sxs-lookup"><span data-stu-id="ffee6-131">You can use the [System Device Enumerator](system-device-enumerator.md) to enumerate the available compression filters.</span></span> <span data-ttu-id="ffee6-132">Para obtener más información, vea [enumerar dispositivos y filtros](enumerating-devices-and-filters.md).</span><span class="sxs-lookup"><span data-stu-id="ffee6-132">For more information, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).</span></span>
4.  <span data-ttu-id="ffee6-133">Opcionalmente, establezca parámetros de compresión como la velocidad de fotogramas clave.</span><span class="sxs-lookup"><span data-stu-id="ffee6-133">Optionally, set compression parameters such as the key-frame rate.</span></span> <span data-ttu-id="ffee6-134">Este paso se describe en detalle más adelante en el artículo.</span><span class="sxs-lookup"><span data-stu-id="ffee6-134">This step is discussed in detail later in the article.</span></span>
5.  <span data-ttu-id="ffee6-135">Llame a [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream).</span><span class="sxs-lookup"><span data-stu-id="ffee6-135">Call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream).</span></span> <span data-ttu-id="ffee6-136">Este método toma punteros al pin, el filtro de compresión (si existe) y el multiplexor.</span><span class="sxs-lookup"><span data-stu-id="ffee6-136">This method takes pointers to the pin, the compression filter (if any), and the multiplexer.</span></span>

<span data-ttu-id="ffee6-137">En el ejemplo de código siguiente se muestra cómo conectar los pin de salida.</span><span class="sxs-lookup"><span data-stu-id="ffee6-137">The following code example shows how to connect the output pins.</span></span>


```C++
long NumGroups;
pTimeline->GetGroupCount(&NumGroups);

// Loop through the groups and get the output pins.
for (i = 0; i < NumGroups; i++)
{
    IPin *pPin;
    if (pRender->GetGroupOutputPin(i, &pPin) == S_OK) 
    {
        IBaseFilter *pCompressor;
        // Create a compressor filter. (Not shown.)
        // Set compression parameters. (Not shown.)

        // Connect the pin.
        pBuilder->RenderStream(NULL, NULL, pPin, pCompressor, pMux);
        pCompressor->Release();
        pPin->Release();
    }
}
```



<span data-ttu-id="ffee6-138">Para establecer los parámetros de compresión (el paso 4, anteriormente), use la interfaz [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) .</span><span class="sxs-lookup"><span data-stu-id="ffee6-138">To set compression parameters (step 4, previously), use the [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) interface.</span></span> <span data-ttu-id="ffee6-139">Esta interfaz se expone en las clavijas de salida de los filtros de compresión.</span><span class="sxs-lookup"><span data-stu-id="ffee6-139">This interface is exposed on the output pins of compression filters.</span></span> <span data-ttu-id="ffee6-140">Enumere los PIN del filtro de compresión y consulte cada pin de salida para **IAMVideoCompression**.</span><span class="sxs-lookup"><span data-stu-id="ffee6-140">Enumerate the compression filter's pins, and query each output pin for **IAMVideoCompression**.</span></span> <span data-ttu-id="ffee6-141">(Para obtener información sobre la enumeración de los pin, consulte [enumeración de PIN](enumerating-pins.md)). Asegúrese de liberar todos los punteros de interfaz obtenidos durante este paso.</span><span class="sxs-lookup"><span data-stu-id="ffee6-141">(For information about enumerating pins, see [Enumerating Pins](enumerating-pins.md).) Be sure to release all the interface pointers that you obtained during this step.</span></span>

<span data-ttu-id="ffee6-142">Después de compilar el gráfico de filtros, llame al método [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) en el administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="ffee6-142">After you build the filter graph, call the [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) method on the filter graph manager.</span></span> <span data-ttu-id="ffee6-143">A medida que se ejecuta el gráfico de filtros, escribe los datos en un archivo.</span><span class="sxs-lookup"><span data-stu-id="ffee6-143">As the filter graph runs, it writes the data to a file.</span></span> <span data-ttu-id="ffee6-144">Use la notificación de eventos para esperar a que se complete la reproducción.</span><span class="sxs-lookup"><span data-stu-id="ffee6-144">Use event notification to wait for playback to complete.</span></span> <span data-ttu-id="ffee6-145">(Consulte [responder a eventos](responding-to-events.md)). Cuando finalice la reproducción, debe llamar explícitamente a [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) para detener el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="ffee6-145">(See [Responding to Events](responding-to-events.md).) When playback finishes, you must explicitly call [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) to stop the filter graph.</span></span> <span data-ttu-id="ffee6-146">De lo contrario, el archivo no se escribe correctamente.</span><span class="sxs-lookup"><span data-stu-id="ffee6-146">Otherwise, the file is not written correctly.</span></span>

<span data-ttu-id="ffee6-147">**Usar el motor de representación inteligente**</span><span class="sxs-lookup"><span data-stu-id="ffee6-147">**Using the Smart Render Engine**</span></span>

<span data-ttu-id="ffee6-148">Para obtener las ventajas de la recompresión inteligente, utilice el motor de representación inteligente en lugar del motor de representación básico.</span><span class="sxs-lookup"><span data-stu-id="ffee6-148">To get the benefits of smart recompression, use the smart render engine in place of the basic render engine.</span></span> <span data-ttu-id="ffee6-149">Los pasos para generar el gráfico son prácticamente los mismos.</span><span class="sxs-lookup"><span data-stu-id="ffee6-149">The steps in building the graph are almost the same.</span></span> <span data-ttu-id="ffee6-150">La principal diferencia es que la compresión se controla en el front-end del gráfico, no en la sección de escritura de archivos.</span><span class="sxs-lookup"><span data-stu-id="ffee6-150">The major difference is that compression is handled in the front end of the graph, not in the file-writing section.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ffee6-151">No utilice el motor de representación inteligente para leer o escribir archivos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ffee6-151">Do not use the smart render engine to read or write Windows Media files.</span></span>

 

<span data-ttu-id="ffee6-152">Cada grupo de vídeos tiene una propiedad que especifica el formato de compresión para ese grupo.</span><span class="sxs-lookup"><span data-stu-id="ffee6-152">Each video group has a property that specifies the compression format for that group.</span></span> <span data-ttu-id="ffee6-153">El formato de compresión debe coincidir exactamente con el formato sin comprimir del grupo en el alto, el ancho, la profundidad de bits y la velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="ffee6-153">The compression format must exactly match the group's uncompressed format in height, width, bit depth, and frame rate.</span></span> <span data-ttu-id="ffee6-154">El motor de representación inteligente usa el formato de compresión al construir el gráfico.</span><span class="sxs-lookup"><span data-stu-id="ffee6-154">The smart render engine uses the compression format when it constructs the graph.</span></span> <span data-ttu-id="ffee6-155">Antes de establecer el formato de compresión, asegúrese de establecer el formato sin comprimir para ese grupo mediante una llamada a [**IAMTimelineGroup:: SetMediaType**](iamtimelinegroup-setmediatype.md).</span><span class="sxs-lookup"><span data-stu-id="ffee6-155">Before you set the compression format, make sure to set the uncompressed format for that group by calling [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md).</span></span>

<span data-ttu-id="ffee6-156">Para establecer el formato de compresión de un grupo, llame al método [**IAMTimelineGroup:: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) .</span><span class="sxs-lookup"><span data-stu-id="ffee6-156">To set a group's compression format, call the [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) method.</span></span> <span data-ttu-id="ffee6-157">Este método toma un puntero a una estructura [**SCompFmt0**](scompfmt0.md) .</span><span class="sxs-lookup"><span data-stu-id="ffee6-157">This method takes a pointer to an [**SCompFmt0**](scompfmt0.md) structure.</span></span> <span data-ttu-id="ffee6-158">La estructura **SCompFmt0** tiene dos miembros: **nFormatId**, que debe ser cero y **mediatype**, que es una estructura [**de \_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="ffee6-158">The **SCompFmt0** structure has two members: **nFormatId**, which must be zero, and **MediaType**, which is an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="ffee6-159">Inicialice la estructura de **\_ \_ tipo de medio am** con la información de formato.</span><span class="sxs-lookup"><span data-stu-id="ffee6-159">Initialize the **AM\_MEDIA\_TYPE** structure with the format information.</span></span>

> [!Note]  
> <span data-ttu-id="ffee6-160">Si desea que el proyecto final tenga el mismo formato que uno de los archivos de origen, puede obtener la \_ \_ estructura de tipo de medio am directamente desde el archivo de origen, mediante el detector de medios.</span><span class="sxs-lookup"><span data-stu-id="ffee6-160">If you want the final project to have the same format as one of your source files, you can get the AM\_MEDIA\_TYPE structure directly from the source file, using the media detector.</span></span> <span data-ttu-id="ffee6-161">Vea [**IMediaDet:: get \_ StreamMediaType**](imediadet-get-streammediatype.md).</span><span class="sxs-lookup"><span data-stu-id="ffee6-161">See [**IMediaDet::get\_StreamMediaType**](imediadet-get-streammediatype.md).</span></span>

 

<span data-ttu-id="ffee6-162">Convierta la variable [**SCompFmt0**](scompfmt0.md) en un puntero de tipo **Long**, tal como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="ffee6-162">Cast the [**SCompFmt0**](scompfmt0.md) variable to a pointer of type **long**, as shown in the following example.</span></span>


```C++
SCompFmt0 *pFormat = new SCompFmt0;
memset(pFormat, 0, sizeof(SCompFmt0));
pFormat->nFormatId = 0;

// Initialize pFormat->MediaType. (Not shown.)

pGroup->SetSmartRecompressFormat( (long*) pFormat );
```



<span data-ttu-id="ffee6-163">El motor de representación inteligente busca automáticamente un filtro de compresión compatible.</span><span class="sxs-lookup"><span data-stu-id="ffee6-163">The smart render engine automatically searches for a compatible compression filter.</span></span> <span data-ttu-id="ffee6-164">También puede especificar un filtro de compresión para un grupo mediante una llamada a [**ISmartRenderEngine:: SetGroupCompressor**](ismartrenderengine-setgroupcompressor.md).</span><span class="sxs-lookup"><span data-stu-id="ffee6-164">You can also specify a compression filter for a group by calling [**ISmartRenderEngine::SetGroupCompressor**](ismartrenderengine-setgroupcompressor.md).</span></span>

<span data-ttu-id="ffee6-165">Para compilar el gráfico, siga los mismos pasos descritos para el motor de representación básico en la sección anterior.</span><span class="sxs-lookup"><span data-stu-id="ffee6-165">To build the graph, use the same steps that were described for the Basic Render Engine in the previous section.</span></span> <span data-ttu-id="ffee6-166">Las únicas diferencias son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="ffee6-166">The only differences are the following:</span></span>

-   <span data-ttu-id="ffee6-167">Use el motor de representación inteligente, no el motor de representación básico.</span><span class="sxs-lookup"><span data-stu-id="ffee6-167">Use the smart render engine, not the basic render engine.</span></span> <span data-ttu-id="ffee6-168">El identificador de clase es CLSID \_ SmartRenderEngine.</span><span class="sxs-lookup"><span data-stu-id="ffee6-168">The class identifier is CLSID\_SmartRenderEngine.</span></span>
-   <span data-ttu-id="ffee6-169">Establezca los parámetros de compresión después de compilar el front-end, pero antes de representar los pines de salida.</span><span class="sxs-lookup"><span data-stu-id="ffee6-169">Set compression parameters after you build the front end but before you render the output pins.</span></span> <span data-ttu-id="ffee6-170">Llame al método [**ISmartRenderEngine:: GetGroupCompressor**](ismartrenderengine-getgroupcompressor.md) para obtener un puntero al filtro de compresión de un grupo.</span><span class="sxs-lookup"><span data-stu-id="ffee6-170">Call the [**ISmartRenderEngine::GetGroupCompressor**](ismartrenderengine-getgroupcompressor.md) method to obtain a pointer to a group's compression filter.</span></span> <span data-ttu-id="ffee6-171">A continuación, consulte la interfaz [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) , tal y como se describió anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ffee6-171">Then query for the [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) interface, as described previously.</span></span>
-   <span data-ttu-id="ffee6-172">Al representar los pines de salida, no es necesario insertar un filtro de compresión.</span><span class="sxs-lookup"><span data-stu-id="ffee6-172">When you render the output pins, there is no need to insert a compression filter.</span></span> <span data-ttu-id="ffee6-173">La secuencia ya está comprimida.</span><span class="sxs-lookup"><span data-stu-id="ffee6-173">The stream is already compressed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ffee6-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ffee6-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffee6-175">Representar un proyecto</span><span class="sxs-lookup"><span data-stu-id="ffee6-175">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 



