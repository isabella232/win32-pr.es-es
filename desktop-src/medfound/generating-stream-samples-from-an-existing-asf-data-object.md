---
description: Generar ejemplos de secuencia a partir de un objeto de datos ASF existente
ms.assetid: eb27f122-d958-495d-98ea-8befd105a9a8
title: Generar ejemplos de secuencia a partir de un objeto de datos ASF existente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee612c9352e3295d6b4957922e385de40a9a1fa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153629"
---
# <a name="generating-stream-samples-from-an-existing-asf-data-object"></a><span data-ttu-id="c2658-103">Generar ejemplos de secuencia a partir de un objeto de datos ASF existente</span><span class="sxs-lookup"><span data-stu-id="c2658-103">Generating Stream Samples from an Existing ASF Data Object</span></span>

<span data-ttu-id="c2658-104">El objeto de *separador* ASF es un componente de nivel WMContainer que analiza el objeto de datos ASF de un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="c2658-104">The ASF *splitter* object is a WMContainer layer component that parses the ASF Data Object of an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="c2658-105">Antes de pasar paquetes de datos al divisor, la aplicación debe inicializar, configurar y seleccionar secuencias en el divisor para prepararlo para el proceso de análisis.</span><span class="sxs-lookup"><span data-stu-id="c2658-105">Before passing data packets to the splitter, the application must initialize, configure, and select streams on the splitter in order to prepare it for the parsing process.</span></span> <span data-ttu-id="c2658-106">Para obtener más información, vea [crear el objeto divisor de ASF](creating-the-asf-splitter-object.md) y [configurar el objeto divisor de ASF](configuring-the-asf-splitter-object.md).</span><span class="sxs-lookup"><span data-stu-id="c2658-106">For information, see [Creating the ASF Splitter Object](creating-the-asf-splitter-object.md) and [Configuring the ASF Splitter Object](configuring-the-asf-splitter-object.md).</span></span>

<span data-ttu-id="c2658-107">Los métodos necesarios para analizar el objeto de datos ASF son:</span><span class="sxs-lookup"><span data-stu-id="c2658-107">The methods required for parsing the ASF Data Object are:</span></span>

-   <span data-ttu-id="c2658-108">[**IMFASFSplitter::P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) que inicia el proceso de análisis insertando el búfer que contiene los paquetes de datos en el divisor.</span><span class="sxs-lookup"><span data-stu-id="c2658-108">[**IMFASFSplitter::ParseData**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) that starts the parsing process by pushing the buffer containing data packets to the splitter.</span></span>
-   <span data-ttu-id="c2658-109">[**IMFASFSplitter:: GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) que recopila ejemplos de secuencias generados a partir del búfer pasado al divisor.</span><span class="sxs-lookup"><span data-stu-id="c2658-109">[**IMFASFSplitter::GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) that collects stream samples that were generated from the buffer passed to splitter.</span></span>

## <a name="finding-the-data-offset"></a><span data-ttu-id="c2658-110">Buscar el desplazamiento de datos</span><span class="sxs-lookup"><span data-stu-id="c2658-110">Finding the Data Offset</span></span>

<span data-ttu-id="c2658-111">Antes de iniciar el proceso de análisis, la aplicación debe buscar el objeto de datos en el archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="c2658-111">Before starting the parsing process, the application must locate the Data Object within the ASF file.</span></span> <span data-ttu-id="c2658-112">Hay dos maneras de obtener el desplazamiento del objeto de datos desde el principio del archivo:</span><span class="sxs-lookup"><span data-stu-id="c2658-112">There are two ways to get the offset of the Data Object from the start of the file:</span></span>

-   <span data-ttu-id="c2658-113">Antes de inicializar el objeto ContentInfo, puede llamar al método [**IMFASFContentInfo:: GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) .</span><span class="sxs-lookup"><span data-stu-id="c2658-113">Before you have initialized the ContentInfo object, you can call the [**IMFASFContentInfo::GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) method.</span></span> <span data-ttu-id="c2658-114">Este método requiere un búfer que contenga los primeros 30 bytes del encabezado ASF.</span><span class="sxs-lookup"><span data-stu-id="c2658-114">This method requires a buffer that contains the first 30 bytes of the ASF header.</span></span> <span data-ttu-id="c2658-115">Devuelve el tamaño del encabezado completo que indica el desplazamiento al primer paquete de datos.</span><span class="sxs-lookup"><span data-stu-id="c2658-115">It returns the size of the entire header that indicates the offset to the first data packet.</span></span> <span data-ttu-id="c2658-116">Este valor también incluye el tamaño del encabezado del objeto de datos de 50 bytes.</span><span class="sxs-lookup"><span data-stu-id="c2658-116">This value also includes the Data Object header size of 50 bytes.</span></span>
-   <span data-ttu-id="c2658-117">Después de inicializar el objeto ContentInfo, puede obtener el descriptor de presentación llamando a [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)y, a continuación, consultando el descriptor de presentación para el atributo de [**desplazamiento de \_ \_ \_ \_ Inicio \_ de datos ASF de MF PD**](mf-pd-asf-data-start-offset-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="c2658-117">After you have initialized the ContentInfo object, you can get the presentation descriptor by calling [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor), and then querying the presentation descriptor for the [**MF\_PD\_ASF\_DATA\_START\_OFFSET**](mf-pd-asf-data-start-offset-attribute.md) attribute.</span></span> <span data-ttu-id="c2658-118">El valor de este atributo es el tamaño del encabezado.</span><span class="sxs-lookup"><span data-stu-id="c2658-118">The value of this attribute is the header size.</span></span>
    > [!Note]  
    > <span data-ttu-id="c2658-119">El atributo de [**\_ \_ \_ \_ longitud de datos ASF de MF**](mf-pd-asf-data-length-attribute.md) en el descriptor de presentación especifica la longitud del objeto de datos ASF.</span><span class="sxs-lookup"><span data-stu-id="c2658-119">The [**MF\_PD\_ASF\_DATA\_LENGTH**](mf-pd-asf-data-length-attribute.md) attribute on the presentation descriptor specifies the length of the ASF Data Object.</span></span>

     

<span data-ttu-id="c2658-120">En ambos casos, el valor devuelto es el tamaño del objeto de encabezado más el tamaño de la sección de encabezado del objeto de datos.</span><span class="sxs-lookup"><span data-stu-id="c2658-120">In both cases, the returned value is the size of the Header Object plus the size of the header section of the Data Object.</span></span> <span data-ttu-id="c2658-121">Por lo tanto, el valor resultante es el desplazamiento al inicio de los paquetes de datos en el objeto de datos ASF.</span><span class="sxs-lookup"><span data-stu-id="c2658-121">Therefore, the resulting value is the offset to the start of the data packets in the ASF Data Object.</span></span> <span data-ttu-id="c2658-122">Cuando empiece a enviar datos al divisor, los datos deben comenzar en este desplazamiento desde el principio del archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="c2658-122">When you begin sending data to the splitter, the data must start at this offset from the beginning of the ASF file.</span></span>

<span data-ttu-id="c2658-123">El valor de desplazamiento se pasa como un parámetro a **ParseData** que inicia el proceso de análisis.</span><span class="sxs-lookup"><span data-stu-id="c2658-123">The offset value is passed as a parameter to **ParseData** that starts the parsing process.</span></span>

<span data-ttu-id="c2658-124">El objeto de datos se divide en paquetes de datos.</span><span class="sxs-lookup"><span data-stu-id="c2658-124">The Data Object is divided into data packets.</span></span> <span data-ttu-id="c2658-125">Cada paquete de datos contiene un encabezado de paquete de datos que proporciona información de análisis de paquetes y los datos de carga, los datos de medios digitales reales.</span><span class="sxs-lookup"><span data-stu-id="c2658-125">Each data packet contains a data packet header that provides packet parsing information and the payload data—the actual digital media data.</span></span> <span data-ttu-id="c2658-126">En un escenario de búsqueda, la aplicación podría querer que el divisor iniciara el análisis en un paquete de datos determinado.</span><span class="sxs-lookup"><span data-stu-id="c2658-126">In a seeking scenario, the application might want the splitter to start parsing at a particular data packet.</span></span> <span data-ttu-id="c2658-127">Para ello, puede usar el indizador ASF para recuperar el desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="c2658-127">To do this, you can use the ASF Indexer is used to retrieve the offset.</span></span> <span data-ttu-id="c2658-128">El indexador devuelve un valor de desplazamiento que comienza en el límite del paquete.</span><span class="sxs-lookup"><span data-stu-id="c2658-128">The indexer returns an offset value that starts at the packet boundary.</span></span> <span data-ttu-id="c2658-129">Si no usa el indexador, asegúrese de que el desplazamiento comienza al principio del encabezado del paquete de datos.</span><span class="sxs-lookup"><span data-stu-id="c2658-129">If you are not using the indexer, make sure that the offset starts at the start of the data packet header.</span></span> <span data-ttu-id="c2658-130">Si se pasa un desplazamiento no válido al divisor, como el valor no apunta al límite del paquete, las llamadas a **ParseHeader** y **GetNextSample** se realizan correctamente pero **GetNextSample** no recupera ningún ejemplo y se recibe **null** en el parámetro *pSample* .</span><span class="sxs-lookup"><span data-stu-id="c2658-130">If an invalid offset is passed to the splitter, such as the value does not point at the packet boundary, **ParseHeader** and **GetNextSample** calls succeed but **GetNextSample** does not retrieve any samples and **NULL** is received in the *pSample* parameter.</span></span>

<span data-ttu-id="c2658-131">Si el divisor está configurado para analizar en dirección inversa, el divisor siempre comienza el análisis al final del búfer de medios que se pasa a **ParseData**.</span><span class="sxs-lookup"><span data-stu-id="c2658-131">If the splitter is configured to parse in the reverse direction, then the splitter always starts parsing at the end of the media buffer that is passed to **ParseData**.</span></span> <span data-ttu-id="c2658-132">Por lo tanto, para el análisis inverso en la llamada a **ParseData**, pase el desplazamiento en el parámetro *cbLength* , que especifica la longitud de los datos y establece *cbBufferOffset* en cero.</span><span class="sxs-lookup"><span data-stu-id="c2658-132">Therefore, for reverse parsing in the call to **ParseData**, pass the offset in the *cbLength* parameter, which specifies the length of the data and set *cbBufferOffset* to zero.</span></span>

## <a name="generating-samples-for-asf-data-packets"></a><span data-ttu-id="c2658-133">Generar ejemplos para paquetes de datos ASF</span><span class="sxs-lookup"><span data-stu-id="c2658-133">Generating Samples for ASF Data Packets</span></span>

<span data-ttu-id="c2658-134">Una aplicación inicia el proceso de análisis pasando los paquetes de datos al divisor.</span><span class="sxs-lookup"><span data-stu-id="c2658-134">An application starts the parsing process by passing the data packets to the splitter.</span></span> <span data-ttu-id="c2658-135">La entrada del divisor es una serie de búferes multimedia que contienen los fragmentos completos del objeto de datos.</span><span class="sxs-lookup"><span data-stu-id="c2658-135">The input to the splitter is a series of media buffers that contain the entire or fragments of the Data Object.</span></span> <span data-ttu-id="c2658-136">La salida del divisor es una serie de ejemplos de medios que contienen los datos del paquete.</span><span class="sxs-lookup"><span data-stu-id="c2658-136">The output from the splitter is a series of media samples that contain the packet data.</span></span>

<span data-ttu-id="c2658-137">Para pasar datos de entrada al divisor, cree un búfer de medios y rellénelo con los datos de la sección del objeto de datos del archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="c2658-137">To pass input data to the splitter, create a media buffer and fill it with data from the Data Object section of the ASF file.</span></span> <span data-ttu-id="c2658-138">(Para obtener más información sobre los búferes multimedia, consulte [búferes multimedia](media-buffers.md)). A continuación, pase el búfer multimedia al método [**IMFASFSplitter::P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) .</span><span class="sxs-lookup"><span data-stu-id="c2658-138">(For more information about media buffers, see [Media Buffers](media-buffers.md).) Then, pass the media buffer to the [**IMFASFSplitter::ParseData**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) method.</span></span> <span data-ttu-id="c2658-139">También puede especificar:</span><span class="sxs-lookup"><span data-stu-id="c2658-139">You can also specify:</span></span>

-   <span data-ttu-id="c2658-140">Desplazamiento en el búfer donde el divisor debe empezar a analizar.</span><span class="sxs-lookup"><span data-stu-id="c2658-140">The offset into the buffer where the splitter should start parsing.</span></span> <span data-ttu-id="c2658-141">Si el desplazamiento es cero, el análisis comienza en el inicio del búfer.</span><span class="sxs-lookup"><span data-stu-id="c2658-141">If the offset is zero, parsing begins at the start of the buffer.</span></span> <span data-ttu-id="c2658-142">Para obtener información acerca de cómo establecer el desplazamiento de datos, vea la sección "buscar el desplazamiento de datos" de este tema.</span><span class="sxs-lookup"><span data-stu-id="c2658-142">For information about setting the data offset, see the "Finding the Data Offset" section in this topic.</span></span>
-   <span data-ttu-id="c2658-143">La cantidad de datos que se van a analizar.</span><span class="sxs-lookup"><span data-stu-id="c2658-143">The amount of data to parse.</span></span> <span data-ttu-id="c2658-144">Si este valor es cero, el divisor se analiza hasta que alcanza el final del búfer, tal y como se especifica en el método [**IMFMediaBuffer:: GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) .</span><span class="sxs-lookup"><span data-stu-id="c2658-144">If this value is zero, the splitter parses until it reaches the end of the buffer, as specified by the [**IMFMediaBuffer::GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) method.</span></span>

<span data-ttu-id="c2658-145">El divisor genera ejemplos de medios haciendo referencia a los datos de los búferes multimedia.</span><span class="sxs-lookup"><span data-stu-id="c2658-145">The splitter generates media samples by referencing the data in the media buffers.</span></span> <span data-ttu-id="c2658-146">El cliente puede recuperar los ejemplos de salida llamando a [**IMFASFSplitter:: GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) en un bucle hasta que no haya más datos para analizar.</span><span class="sxs-lookup"><span data-stu-id="c2658-146">The client can retrieve the output samples by calling [**IMFASFSplitter::GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) in a loop until there is no more data to parse.</span></span> <span data-ttu-id="c2658-147">Si **GetNextSample** devuelve la \_ \_ marca de ASF STATUSFLAGS incompleta en el parámetro *pdwStatusFlags* , significa que hay más ejemplos para recuperar y la aplicación puede volver a llamar a **GetNextSample** .</span><span class="sxs-lookup"><span data-stu-id="c2658-147">If **GetNextSample** returns the ASF\_STATUSFLAGS\_INCOMPLETE flag in the *pdwStatusFlags* parameter, it means there are more samples to retrieve, and the application can call **GetNextSample** again.</span></span> <span data-ttu-id="c2658-148">De lo contrario, llame a **ParseData** para pasar más datos al divisor.</span><span class="sxs-lookup"><span data-stu-id="c2658-148">Otherwise, call **ParseData** to pass more data to the splitter.</span></span> <span data-ttu-id="c2658-149">En el caso de los ejemplos generados, el divisor establece la información siguiente:</span><span class="sxs-lookup"><span data-stu-id="c2658-149">For the generated samples, the splitter sets the following information:</span></span>

-   <span data-ttu-id="c2658-150">El divisor establece una marca de tiempo en todos los ejemplos que genera.</span><span class="sxs-lookup"><span data-stu-id="c2658-150">The splitter sets a time stamp on all the samples that it generates.</span></span> <span data-ttu-id="c2658-151">La hora de muestra representa el tiempo de presentación y no incluye el tiempo de preestación.</span><span class="sxs-lookup"><span data-stu-id="c2658-151">The sample time represents the presentation time and does not include the preroll time.</span></span> <span data-ttu-id="c2658-152">La aplicación puede llamar a [**IMFSample:: GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) para obtener el tiempo de presentación, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="c2658-152">The application can call [**IMFSample::GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) to get the presentation time, in 100-nanosecond units.</span></span>
-   <span data-ttu-id="c2658-153">Si se produce una interrupción durante la generación del ejemplo, el divisor establece el atributo [**\_ discontinuidad MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) en el primer ejemplo después de la discontinuidad.</span><span class="sxs-lookup"><span data-stu-id="c2658-153">If a break occurs during sample generation, the splitter sets the [**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute on the first sample after the discontinuity.</span></span> <span data-ttu-id="c2658-154">Las discontinuidades suelen deberse a la pérdida de paquetes en una conexión de red, a datos de archivos dañados o a la conmutación de divisores de un flujo de origen a otro.</span><span class="sxs-lookup"><span data-stu-id="c2658-154">Discontinuities are usually caused by dropped packets on a network connection, corrupt file data, or the splitter switching from one source stream to another.</span></span>
-   <span data-ttu-id="c2658-155">En el caso de vídeo, el divisor comprueba si el ejemplo contiene un fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="c2658-155">For video, the splitter checks whether the sample contains a key frame.</span></span> <span data-ttu-id="c2658-156">Si lo hace, el divisor establece el atributo [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c2658-156">If it does, the splitter sets the [**MFSampleExtension\_CleanPoint**](mfsampleextension-cleanpoint-attribute.md) attribute on the sample.</span></span>

<span data-ttu-id="c2658-157">Si el divisor analiza los paquetes de datos que se reciben de un servidor multimedia, es posible que la longitud del paquete sea variable.</span><span class="sxs-lookup"><span data-stu-id="c2658-157">If the splitter is parsing data packets that are received from a media server, it is possible that the packet length is variable.</span></span> <span data-ttu-id="c2658-158">En este caso, el cliente debe llamar a **ParseData** para cada paquete y establecer el atributo de [**\_ \_ límite de paquetes MFASFSPLITTER**](mfasfsplitter-packet-boundary-attribute.md) en cada búfer que se envía al divisor.</span><span class="sxs-lookup"><span data-stu-id="c2658-158">In this case, the client must call **ParseData** for each packet and set the [**MFASFSPLITTER\_PACKET\_BOUNDARY**](mfasfsplitter-packet-boundary-attribute.md) attribute on each buffer that is sent to the splitter.</span></span> <span data-ttu-id="c2658-159">Este atributo indica al divisor si el búfer multimedia contiene el inicio de un paquete ASF.</span><span class="sxs-lookup"><span data-stu-id="c2658-159">This attribute indicates to the splitter whether the media buffer contains the start of an ASF packet.</span></span> <span data-ttu-id="c2658-160">Establezca el atributo en **true** si el búfer contiene el inicio de un nuevo paquete.</span><span class="sxs-lookup"><span data-stu-id="c2658-160">Set the attribute to **TRUE** if the buffer contains the start of a new packet.</span></span> <span data-ttu-id="c2658-161">Si el búfer contiene una continuación del paquete anterior, establezca el atributo en **false**.</span><span class="sxs-lookup"><span data-stu-id="c2658-161">If the buffer contains a continuation of the previous packet, set the attribute to **FALSE**.</span></span> <span data-ttu-id="c2658-162">Los búferes no pueden abarcar varios paquetes.</span><span class="sxs-lookup"><span data-stu-id="c2658-162">The buffers cannot span multiple packets.</span></span>

<span data-ttu-id="c2658-163">Antes de pasar nuevos búferes multimedia al divisor, la aplicación debe llamar a [**IMFASFSplitter:: Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-flush).</span><span class="sxs-lookup"><span data-stu-id="c2658-163">Before passing new media buffers to the splitter, the application must call [**IMFASFSplitter::Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-flush).</span></span> <span data-ttu-id="c2658-164">Este método restablece el divisor y borra cualquier fotograma parcial que esté a la espera de que se complete.</span><span class="sxs-lookup"><span data-stu-id="c2658-164">This method resets the splitter and clears any partial frame that is waiting to be completed.</span></span> <span data-ttu-id="c2658-165">Esto resulta útil en un escenario de búsqueda en el que el desplazamiento está en una ubicación diferente.</span><span class="sxs-lookup"><span data-stu-id="c2658-165">This is useful in a seeking scenario where the offset is at a different location.</span></span>

### <a name="example"></a><span data-ttu-id="c2658-166">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c2658-166">Example</span></span>

<span data-ttu-id="c2658-167">En el ejemplo de código siguiente se muestra cómo analizar paquetes de datos.</span><span class="sxs-lookup"><span data-stu-id="c2658-167">The following code example shows how to parse data packets.</span></span> <span data-ttu-id="c2658-168">En este ejemplo se analiza desde el principio del objeto de datos hasta el final de la secuencia y se muestra información acerca de los ejemplos que contienen fotogramas clave.</span><span class="sxs-lookup"><span data-stu-id="c2658-168">This example parses from the beginning of the Data Object to the end of the stream and displays information about the samples that contain key frames.</span></span> <span data-ttu-id="c2658-169">Para obtener un ejemplo completo que usa este código, vea [Tutorial: leer un archivo ASF](tutorial--reading-an-asf-file.md).</span><span class="sxs-lookup"><span data-stu-id="c2658-169">For a complete example that uses this code, see [Tutorial: Reading an ASF File](tutorial--reading-an-asf-file.md).</span></span>


```C++
// Parse the video stream and display information about the video samples.
//
// The current read position of the byte stream must be at the start of the ASF
// Data Object.

HRESULT DisplayKeyFrames(IMFByteStream *pStream, IMFASFSplitter *pSplitter)
{
    const DWORD cbReadSize = 2048;  // Read size (arbitrary value)

    IMFMediaBuffer *pBuffer = NULL;
    IMFSample *pSample = NULL;

    HRESULT hr = S_OK;
    while (SUCCEEDED(hr))
    {
        // The parser must get a newly allocated buffer each time.
        hr = MFCreateMemoryBuffer(cbReadSize, &pBuffer);
        if (FAILED(hr))
        {
            break;
        }

        // Read data into the buffer.
        hr = ReadFromByteStream(pStream, pBuffer, cbReadSize);
        if (FAILED(hr)) 
        {
            break; 
        }

        // Get the amound of data that was read.
        DWORD cbData;
        hr = pBuffer->GetCurrentLength(&cbData);
        if (FAILED(hr)) 
        { 
            break; 
        }

        if (cbData == 0)
        {
            break; // End of file.
        }

        // Send the data to the ASF splitter.
        hr = pSplitter->ParseData(pBuffer, 0, 0);
        SafeRelease(&pBuffer);
        if (FAILED(hr)) 
        { 
            break; 
        }

        // Pull samples from the splitter.
        DWORD parsingStatus = 0;
        do
        {
            WORD streamID;
            hr = pSplitter->GetNextSample(&parsingStatus, &streamID, &pSample);
            if (FAILED(hr)) 
            { 
                break; 
            }
            if (pSample == NULL)
            {
                // No samples yet. Parse more data.
                break;
            }
            if (IsRandomAccessPoint(pSample))
            {
                DisplayKeyFrame(pSample);
            }
            SafeRelease(&pSample);
            
        } while (parsingStatus & ASF_STATUSFLAGS_INCOMPLETE);
    }
    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="c2658-170">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c2658-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2658-171">Divisor ASF</span><span class="sxs-lookup"><span data-stu-id="c2658-171">ASF Splitter</span></span>](asf-splitter.md)
</dt> </dl>

 

 



