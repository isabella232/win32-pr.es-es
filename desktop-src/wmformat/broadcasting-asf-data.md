---
title: Difusión de datos de ASF
description: Difusión de datos de ASF
ms.assetid: 1b04f361-8147-4f6a-8c9d-d8eeed28550a
keywords:
- SDK de Windows Media Format, difundir datos ASF
- Advanced Systems Format (ASF), difundir datos
- ASF (formato de sistemas avanzados), difundir datos
- SDK de Windows Media Format, envío de datos ASF
- Advanced Systems Format (ASF), enviar datos
- ASF (formato de sistemas avanzados), enviar datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42339b4a3e60666c1ea0cb69a07dfdc836b19409
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/21/2020
ms.locfileid: "104077427"
---
# <a name="broadcasting-asf-data"></a><span data-ttu-id="479a5-109">Difusión de datos de ASF</span><span class="sxs-lookup"><span data-stu-id="479a5-109">Broadcasting ASF Data</span></span>

<span data-ttu-id="479a5-110">En este tema se describe cómo enviar datos ASF a través de una red mediante el protocolo HTTP.</span><span class="sxs-lookup"><span data-stu-id="479a5-110">This topic describes how to send ASF data across a network using the HTTP protocol.</span></span> <span data-ttu-id="479a5-111">El envío de archivos a través de una red requiere el uso del objeto escritor, por lo que debe tener una descripción general de este objeto antes de leer este tema.</span><span class="sxs-lookup"><span data-stu-id="479a5-111">Sending files over a network requires the use of the writer object, so you should have a general understanding of this object before reading this topic.</span></span> <span data-ttu-id="479a5-112">Para obtener más información, consulte [Writing ASF files](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="479a5-112">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>

<span data-ttu-id="479a5-113">Si está empezando con datos sin comprimir, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="479a5-113">If you are starting with uncompressed data, do the following:</span></span>

1.  <span data-ttu-id="479a5-114">Cree el objeto de escritor llamando a la función [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) .</span><span class="sxs-lookup"><span data-stu-id="479a5-114">Create the writer object by calling the [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) function.</span></span> <span data-ttu-id="479a5-115">Esta función devuelve un puntero **IWMWriter** .</span><span class="sxs-lookup"><span data-stu-id="479a5-115">This function returns an **IWMWriter** pointer.</span></span>
    ```C++
    IWMWriter *pWriter;
    hr = WMCreateWriter(NULL, &pWriter);
    ```

    

2.  <span data-ttu-id="479a5-116">Cree el objeto de receptor de red mediante una llamada a la función [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink) , que devuelve un puntero **IWMWriterNetworkSink** .</span><span class="sxs-lookup"><span data-stu-id="479a5-116">Create the network sink object by calling the [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink) function, which returns an **IWMWriterNetworkSink** pointer.</span></span>
    ```C++
    IWMWriterNetworkSink *pNetSink;
    hr = WMCreateWriterNetworkSink(&pNetSink);
    ```

    

3.  <span data-ttu-id="479a5-117">Llame a [**IWMWriterNetworkSink:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-open) en el receptor de red y especifique el número de puerto que se va a abrir; por ejemplo, 8080.</span><span class="sxs-lookup"><span data-stu-id="479a5-117">Call [**IWMWriterNetworkSink::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-open) on the network sink and specify the port number to open; for example, 8080.</span></span> <span data-ttu-id="479a5-118">Opcionalmente, llame a [**IWMWriterNetworkSink:: GetHostURL**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-gethosturl) para obtener la dirección URL del host.</span><span class="sxs-lookup"><span data-stu-id="479a5-118">Optionally, call [**IWMWriterNetworkSink::GetHostURL**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-gethosturl) to get the URL of the host.</span></span> <span data-ttu-id="479a5-119">Los clientes tendrán acceso al contenido desde esta dirección URL.</span><span class="sxs-lookup"><span data-stu-id="479a5-119">Clients will access the content from this URL.</span></span> <span data-ttu-id="479a5-120">También puede llamar a [**IWMWriterNetworkSink:: SetMaximumClients**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-setmaximumclients) para restringir el número de clientes.</span><span class="sxs-lookup"><span data-stu-id="479a5-120">You can also call [**IWMWriterNetworkSink::SetMaximumClients**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-setmaximumclients) to restrict the number of clients.</span></span>
    ```C++
    DWORD dwPortNum = 8080;
    hr = pNetSink->Open( &dwPortNum)
    ```

    

4.  <span data-ttu-id="479a5-121">Asocie el receptor de red al escritor mediante una llamada a [**IWMWriterAdvanced:: AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) en el escritor, con un puntero a la interfaz **IWMWriterNetworkSink** del receptor de la red.</span><span class="sxs-lookup"><span data-stu-id="479a5-121">Attach the network sink to the writer by calling [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) on the writer, with a pointer to the network sink's **IWMWriterNetworkSink** interface.</span></span>
    ```C++
    IWMWriterAdvanced *pWriterAdvanced;
    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced, ( void** ) pWriterAdvanced );
    if (SUCCEEDED(hr))
    {
        pWriterAdvanced->AddSink(pNetSink);
    }
    ```

    

5.  <span data-ttu-id="479a5-122">Establezca el perfil ASF llamando al método [**IWMWriter:: SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) en el objeto escritor con un puntero [**IWMProfile**](iwmprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="479a5-122">Set the ASF profile by calling the [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) method on the writer object, with an [**IWMProfile**](iwmprofile.md) pointer.</span></span> <span data-ttu-id="479a5-123">Para obtener información sobre cómo crear un perfil, consulte [trabajar con perfiles](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="479a5-123">For information about creating a profile, see [Working with Profiles](working-with-profiles.md).</span></span>
6.  <span data-ttu-id="479a5-124">Opcionalmente, especifique los metadatos mediante la interfaz [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) en el escritor.</span><span class="sxs-lookup"><span data-stu-id="479a5-124">Optionally, specify metadata using the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface on the writer.</span></span>
7.  <span data-ttu-id="479a5-125">Llame a [**IWMWriter:: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting) en el escritor.</span><span class="sxs-lookup"><span data-stu-id="479a5-125">Call [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting) on the writer.</span></span>
    ```C++
    hr = pWriter->BeginWriting();
    ```

    

8.  <span data-ttu-id="479a5-126">Para cada ejemplo, llame al método [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) .</span><span class="sxs-lookup"><span data-stu-id="479a5-126">For each sample, call the [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) method.</span></span> <span data-ttu-id="479a5-127">Especifique el número de secuencia, la hora de presentación, la duración de la muestra y un puntero al búfer de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="479a5-127">Specify the stream number, the presentation time, the duration of the sample, and a pointer to the sample buffer.</span></span> <span data-ttu-id="479a5-128">El método **WriteSample** comprime los ejemplos.</span><span class="sxs-lookup"><span data-stu-id="479a5-128">The **WriteSample** method compresses the samples.</span></span>
9.  <span data-ttu-id="479a5-129">Cuando haya terminado, llame a [**IWMWriter:: EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting) en el escritor.</span><span class="sxs-lookup"><span data-stu-id="479a5-129">When you are done, call [**IWMWriter::EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting) on the writer.</span></span>
    ```C++
    hr = pWriter->EndWriting();
    ```

    

10. <span data-ttu-id="479a5-130">Llame a [**IWMWriterAdvanced:: RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) en el escritor para desasociar el objeto de receptor de red.</span><span class="sxs-lookup"><span data-stu-id="479a5-130">Call [**IWMWriterAdvanced::RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) on the writer to detach the network sink object.</span></span>
    ```C++
    hr = pWriterAdvanced->RemoveSink(pNetSink);
    ```

    

11. <span data-ttu-id="479a5-131">Llame a [**IWMWriterNetworkSink:: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-close) en el receptor de red para liberar el puerto.</span><span class="sxs-lookup"><span data-stu-id="479a5-131">Call [**IWMWriterNetworkSink::Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-close) on the network sink to release the port.</span></span>
    ```C++
    hr = pNetSink->Close();
    ```

    

<span data-ttu-id="479a5-132">Otra manera de transmitir el contenido ASF a través de una red es leerlo desde un archivo ASF existente.</span><span class="sxs-lookup"><span data-stu-id="479a5-132">Another way to stream ASF content over a network is to read it from an existing ASF file.</span></span> <span data-ttu-id="479a5-133">En el ejemplo WMVNetWrite proporcionado en el SDK se muestra este enfoque.</span><span class="sxs-lookup"><span data-stu-id="479a5-133">The WMVNetWrite sample provided in the SDK demonstrates this approach.</span></span> <span data-ttu-id="479a5-134">Además de los pasos indicados anteriormente, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="479a5-134">In addition to the steps listed previously, do the following:</span></span>

1.  <span data-ttu-id="479a5-135">Cree un objeto de lector y llame al método **Open** con el nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="479a5-135">Create a reader object and call the **Open** method with the name of the file.</span></span>
2.  <span data-ttu-id="479a5-136">Llame a [**IWMReaderAdvanced:: SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection) en el objeto Reader con el valor **true**.</span><span class="sxs-lookup"><span data-stu-id="479a5-136">Call [**IWMReaderAdvanced::SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection) on the reader object, with the value **TRUE**.</span></span> <span data-ttu-id="479a5-137">Esto permite que la aplicación Lea todas las secuencias del archivo, incluidas las secuencias con exclusión mutua.</span><span class="sxs-lookup"><span data-stu-id="479a5-137">This enables the application to read every stream in the file, including streams with mutual exclusion.</span></span>
3.  <span data-ttu-id="479a5-138">Consulte al lector la interfaz [**IWMProfile**](iwmprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="479a5-138">Query the reader for the [**IWMProfile**](iwmprofile.md) interface.</span></span> <span data-ttu-id="479a5-139">Use este puntero cuando llame a [**IWMWriter:: SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) en el objeto de escritor (paso 5 en el procedimiento anterior).</span><span class="sxs-lookup"><span data-stu-id="479a5-139">Use this pointer when you call [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) on the writer object (step 5 in the previous procedure).</span></span>
4.  <span data-ttu-id="479a5-140">Para cada secuencia definida en el perfil, llame a [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) para obtener el número de secuencia.</span><span class="sxs-lookup"><span data-stu-id="479a5-140">For every stream defined in the profile, call [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) to get the stream number.</span></span> <span data-ttu-id="479a5-141">Pase este número de secuencia al método [**IWMReaderAdvanced:: SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples) del lector.</span><span class="sxs-lookup"><span data-stu-id="479a5-141">Pass this stream number to the reader's [**IWMReaderAdvanced::SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples) method.</span></span> <span data-ttu-id="479a5-142">Este método informa al lector de que entregue ejemplos comprimidos, en lugar de descodificarlos.</span><span class="sxs-lookup"><span data-stu-id="479a5-142">This method informs the reader to deliver compressed samples, rather than decoding them.</span></span> <span data-ttu-id="479a5-143">Los ejemplos se entregarán a la aplicación a través del método de devolución de llamada [**IWMReaderCallbackAdvanced:: OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="479a5-143">The samples will be delivered to the application through the application's [**IWMReaderCallbackAdvanced::OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) callback method.</span></span>

    <span data-ttu-id="479a5-144">Debe obtener información del códec para cada flujo que lea sin comprimir y agréguelo al encabezado antes de la difusión.</span><span class="sxs-lookup"><span data-stu-id="479a5-144">You must obtain codec information for every stream that you read uncompressed and add it to the header before broadcast.</span></span> <span data-ttu-id="479a5-145">Para obtener la información del códec, llame a [**IWMHeaderInfo2:: GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) y [**IWMHeaderInfo2:: GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) para enumerar los códecs asociados al archivo en el lector.</span><span class="sxs-lookup"><span data-stu-id="479a5-145">To obtain the codec information, call [**IWMHeaderInfo2::GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) and [**IWMHeaderInfo2::GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) to enumerate the codecs associated with the file in the reader.</span></span> <span data-ttu-id="479a5-146">Seleccione la información del códec que coincida con la configuración de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="479a5-146">Select the codec information that matches the stream configuration.</span></span> <span data-ttu-id="479a5-147">A continuación, establezca la información del códec en el escritor llamando a [**IWMHeaderInfo3:: AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), pasando la información obtenida del lector.</span><span class="sxs-lookup"><span data-stu-id="479a5-147">Then set the codec information in the writer by calling [**IWMHeaderInfo3::AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), passing the information obtained from the reader.</span></span>

5.  <span data-ttu-id="479a5-148">Después de establecer el perfil en el escritor, llame a [**IWMWriter:: GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount) en el escritor para obtener el número de entradas.</span><span class="sxs-lookup"><span data-stu-id="479a5-148">After you set the profile on the writer, call [**IWMWriter::GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount) on the writer to get the number of inputs.</span></span> <span data-ttu-id="479a5-149">Para cada entrada, llame a [**IWMWriter:: SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) con el valor **null**.</span><span class="sxs-lookup"><span data-stu-id="479a5-149">For each input, call [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) with the value **NULL**.</span></span> <span data-ttu-id="479a5-150">Esto indica al objeto del escritor que la aplicación proporcionará ejemplos comprimidos, por lo que el escritor no tiene que usar ningún códec para comprimir los datos.</span><span class="sxs-lookup"><span data-stu-id="479a5-150">This indicates to the writer object that the application will deliver compressed samples, so the writer does not have to use any codecs to compress the data.</span></span> <span data-ttu-id="479a5-151">Asegúrese de llamar a **SetInputProps** antes de llamar a **BeginWriting**.</span><span class="sxs-lookup"><span data-stu-id="479a5-151">Make sure to call **SetInputProps** before calling **BeginWriting**.</span></span>
6.  <span data-ttu-id="479a5-152">Opcionalmente, copie los atributos de metadatos del lector al escritor.</span><span class="sxs-lookup"><span data-stu-id="479a5-152">Optionally, copy the metadata attributes from the reader to the writer</span></span>
7.  <span data-ttu-id="479a5-153">Dado que los ejemplos del lector ya están comprimidos, use el método [**IWMWriterAdvanced:: WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) para escribir los ejemplos, en lugar del método **WriteSample** .</span><span class="sxs-lookup"><span data-stu-id="479a5-153">Because the samples from the reader are already compressed, use the [**IWMWriterAdvanced::WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) method to write the samples, instead of the **WriteSample** method.</span></span> <span data-ttu-id="479a5-154">El método **WriteStreamSample** omite los procedimientos de compresión habituales del objeto del escritor.</span><span class="sxs-lookup"><span data-stu-id="479a5-154">The **WriteStreamSample** method bypasses the writer object's usual compression procedures.</span></span>
8.  <span data-ttu-id="479a5-155">Cuando el lector alcanza el final del archivo, envía una \_ notificación de EOF de WMT a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="479a5-155">When the reader reaches the end of the file, it sends a WMT\_EOF notification to the application.</span></span>

<span data-ttu-id="479a5-156">Además, la aplicación debe controlar el reloj en el objeto lector, de modo que el lector extrae los datos del archivo lo más rápido posible.</span><span class="sxs-lookup"><span data-stu-id="479a5-156">In addition, the application should drive the clock on the reader object, so that the reader pulls data from the file as quickly as possible.</span></span> <span data-ttu-id="479a5-157">Para ello, llame al método [**IWMReaderAdvanced:: SetUserProvidedClock**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setuserprovidedclock) en el lector, con el valor **true**.</span><span class="sxs-lookup"><span data-stu-id="479a5-157">To do this, call the [**IWMReaderAdvanced::SetUserProvidedClock**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setuserprovidedclock) method on the reader, with the value **TRUE**.</span></span> <span data-ttu-id="479a5-158">Después de que el lector envíe la notificación de inicio de WMT \_ , llame a [**IWMReaderAdvanced::D elivertime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-delivertime) y especifique el intervalo de tiempo que el lector debe proporcionar.</span><span class="sxs-lookup"><span data-stu-id="479a5-158">After the reader sends the WMT\_STARTED notification, call [**IWMReaderAdvanced::DeliverTime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-delivertime) and specify the time interval that the reader should deliver.</span></span> <span data-ttu-id="479a5-159">Una vez que el lector ha terminado de leer este intervalo de tiempo, llama al método de devolución de llamada [**IWMReaderCallbackAdvanced:: altime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-ontime) de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="479a5-159">After the reader is done reading this time interval, it calls the application's [**IWMReaderCallbackAdvanced::OnTime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-ontime) callback method.</span></span> <span data-ttu-id="479a5-160">La aplicación debe volver a llamar a **DeliverTime** para leer el intervalo de tiempo siguiente.</span><span class="sxs-lookup"><span data-stu-id="479a5-160">The application should call **DeliverTime** again to read the next time interval.</span></span> <span data-ttu-id="479a5-161">Por ejemplo, para leer desde el archivo en intervalos de un segundo:</span><span class="sxs-lookup"><span data-stu-id="479a5-161">For example, to read from the file in one-second intervals:</span></span>


```C++
// Initial call to DeliverTime.
QWORD m_qwTime = 10000000; // 1 second.
hr = m_pReaderAdvanced->DeliverTime(m_qwTime);

// In the callback:
HRESULT CNetWrite::OnTime(QWORD cnsCurrentTime, void *pvContext)
{
    HRESULT hr = S_OK;
    // Continue calling DeliverTime until the end of the file.
    if(!m_bEOF)
    {
        m_qwTime += 10000000; // 1 second.
        hr = m_pReaderAdvanced->DeliverTime(m_qwTime);
    }
    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="479a5-162">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="479a5-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="479a5-163">**Envío de datos ASF a través de una red**</span><span class="sxs-lookup"><span data-stu-id="479a5-163">**Sending ASF Data Over a Network**</span></span>](sending-asf-data-over-a-network.md)
</dt> <dt>

[<span data-ttu-id="479a5-164">**Trabajar con receptores de escritor**</span><span class="sxs-lookup"><span data-stu-id="479a5-164">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




