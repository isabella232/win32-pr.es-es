---
description: El receptor de archivos ASF es una implementación de IMFMediaSink proporcionada por Media Foundation que una aplicación puede usar para archivar datos multimedia ASF en un archivo. Para obtener información sobre el modelo de objetos de los receptores de medios ASF y el uso general, consulte receptores multimedia ASF.
ms.assetid: 21cbde27-a2ca-4298-9197-43bcaf05588d
title: Agregar información de secuencias al receptor de archivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e08c6997d9c77836f379d4ca7b75720ddea245
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715089"
---
# <a name="adding-stream-information-to-the-asf-file-sink"></a><span data-ttu-id="2e808-104">Agregar información de secuencias al receptor de archivos ASF</span><span class="sxs-lookup"><span data-stu-id="2e808-104">Adding Stream Information to the ASF File Sink</span></span>

<span data-ttu-id="2e808-105">El receptor de archivos ASF es una implementación de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) proporcionada por Media Foundation que una aplicación puede usar para archivar datos multimedia ASF en un archivo.</span><span class="sxs-lookup"><span data-stu-id="2e808-105">The ASF file sink is an implementation of [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) provided by Media Foundation that an application can use to archive ASF media data to a file.</span></span> <span data-ttu-id="2e808-106">Para obtener información sobre el modelo de objetos y el uso general de los receptores de medios ASF, consulte [receptores de medios ASF](asf-media-sinks.md).</span><span class="sxs-lookup"><span data-stu-id="2e808-106">For information about ASF Media Sinks' object model and general usage, see [ASF Media Sinks](asf-media-sinks.md).</span></span>

<span data-ttu-id="2e808-107">Después de crear una instancia del receptor de archivos, debe configurarse antes de compilar la topología.</span><span class="sxs-lookup"><span data-stu-id="2e808-107">After instantiating the file sink, it must be configured before building the topology.</span></span> <span data-ttu-id="2e808-108">El receptor de archivos debe conocer las secuencias del archivo de salida, la información del modo de codificación y los metadatos.</span><span class="sxs-lookup"><span data-stu-id="2e808-108">The file sink needs to know about the streams in the output file, the encoding mode information, and the metadata.</span></span> <span data-ttu-id="2e808-109">En este tema se describe el proceso de agregar una secuencia en el receptor de archivos.</span><span class="sxs-lookup"><span data-stu-id="2e808-109">This topic describes the process of adding stream in the file sink.</span></span>

-   [<span data-ttu-id="2e808-110">Agregar secuencias en el receptor de archivos ASF</span><span class="sxs-lookup"><span data-stu-id="2e808-110">Adding Streams in the ASF File Sink</span></span>](#adding-streams-in-the-asf-file-sink)
-   [<span data-ttu-id="2e808-111">Enumerar receptores de secuencia</span><span class="sxs-lookup"><span data-stu-id="2e808-111">Enumerating Stream Sinks</span></span>](#enumerating-stream-sinks)
-   [<span data-ttu-id="2e808-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2e808-112">Related topics</span></span>](#related-topics)

## <a name="adding-streams-in-the-asf-file-sink"></a><span data-ttu-id="2e808-113">Agregar secuencias en el receptor de archivos ASF</span><span class="sxs-lookup"><span data-stu-id="2e808-113">Adding Streams in the ASF File Sink</span></span>

<span data-ttu-id="2e808-114">El receptor de archivos debe conocer los flujos de salida y sus propiedades para que pueda generar ejemplos de salida en consecuencia y agregarlos al archivo ASF de salida.</span><span class="sxs-lookup"><span data-stu-id="2e808-114">The file sink must know of the output streams and their properties so that it can generate output samples accordingly and add them to the output ASF file.</span></span> <span data-ttu-id="2e808-115">Esta configuración se escribe en el objeto de encabezado ASF final.</span><span class="sxs-lookup"><span data-stu-id="2e808-115">These settings are written to the final ASF Header Object.</span></span>

<span data-ttu-id="2e808-116">Para establecer la información de la secuencia, debe tener una referencia al objeto ContentInfo ASF del receptor de archivo.</span><span class="sxs-lookup"><span data-stu-id="2e808-116">To set stream information, you must have a reference to the file sink's ASF ContentInfo object.</span></span> <span data-ttu-id="2e808-117">Para obtener información, consulte [crear el receptor de archivos ASF](creating-the-asf-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="2e808-117">For information, see [Creating the ASF File Sink](creating-the-asf-file-sink.md).</span></span>

<span data-ttu-id="2e808-118">En el procedimiento siguiente se resumen los pasos generales para configurar Stream mediante el uso del objeto de perfil ASF.</span><span class="sxs-lookup"><span data-stu-id="2e808-118">The following procedure summarizes the general steps for configuring stream by using the ASF profile object.</span></span>

<span data-ttu-id="2e808-119">**Para configurar la información de la secuencia en el receptor de archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="2e808-119">**To configure stream information in the ASF file sink**</span></span>

1.  <span data-ttu-id="2e808-120">Cree un objeto de perfil ASF llamando a [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile).</span><span class="sxs-lookup"><span data-stu-id="2e808-120">Create an ASF profile object by calling [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile).</span></span>
2.  <span data-ttu-id="2e808-121">Para cada secuencia del archivo de salida, cree un tipo de medio para la secuencia de destino que se va a agregar al receptor de archivos.</span><span class="sxs-lookup"><span data-stu-id="2e808-121">For each stream in the output file, create a media type for the target stream to be added in the file sink.</span></span> <span data-ttu-id="2e808-122">El tipo de medio debe ser compatible con los tipos de salida admitidos por los codificadores de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2e808-122">The media type must be compatible with the output types supported by the Windows Media encoders.</span></span>

    <span data-ttu-id="2e808-123">Para obtener información acerca de cómo agregar secuencias de audio al perfil, consulte crear secuencias de audio para la codificación ASF.</span><span class="sxs-lookup"><span data-stu-id="2e808-123">For information about adding audio streams to the profile, see Creating Audio Streams for ASF Encoding.</span></span>

    <span data-ttu-id="2e808-124">Para obtener información acerca de cómo agregar secuencias de vídeo al perfil, consulte crear secuencias de vídeo para la codificación ASF.</span><span class="sxs-lookup"><span data-stu-id="2e808-124">For information about adding video streams to the profile, see Creating Video Streams for ASF Encoding.</span></span>

3.  <span data-ttu-id="2e808-125">Cree secuencias basadas en los tipos de medios creados en el paso 2 llamando a [**IMFASFProfile:: CreateStream (**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream).</span><span class="sxs-lookup"><span data-stu-id="2e808-125">Create streams based on the media types created in step 2 by calling [**IMFASFProfile::CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream).</span></span>
4.  <span data-ttu-id="2e808-126">Asigne un número de secuencia para la secuencia recién creada mediante una llamada al puntero de la interfaz [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) recibido en el paso 3.</span><span class="sxs-lookup"><span data-stu-id="2e808-126">Assign a stream number for the newly created stream by calling [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface pointer received in step 3.</span></span>
5.  <span data-ttu-id="2e808-127">Opcionalmente, configure la secuencia con la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="2e808-127">Optionally configure the stream with the following information:</span></span>
    -   <span data-ttu-id="2e808-128">Parámetros de depósito con fugas estableciendo los atributos: [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) o [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="2e808-128">Leaky bucket parameters by setting the attributes: [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) or [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)</span></span>
    -   <span data-ttu-id="2e808-129">Extensión de carga, exclusión mutua mediante una llamada a métodos [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .</span><span class="sxs-lookup"><span data-stu-id="2e808-129">Payload extension, mutual exclusion by calling [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) methods.</span></span>
6.  <span data-ttu-id="2e808-130">Opcionalmente, puede establecer el tamaño de los paquetes de datos para el perfil estableciendo los atributos [**MF \_ ASFPROFILE \_ MINPACKETSIZE**](mf-asfprofile-minpacketsize-attribute.md) y [**MF \_ ASFPROFILE \_ MAXPACKETSIZE**](mf-asfprofile-maxpacketsize-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="2e808-130">Optionally set data packet size for the profile by setting [**MF\_ASFPROFILE\_MINPACKETSIZE**](mf-asfprofile-minpacketsize-attribute.md) and [**MF\_ASFPROFILE\_MAXPACKETSIZE**](mf-asfprofile-maxpacketsize-attribute.md) attributes.</span></span> <span data-ttu-id="2e808-131">El perfil ASF expone la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , a la que una aplicación puede obtener referencia llamando a **IMFASFProfile:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="2e808-131">The ASF profile exposes the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface, which an application can get reference to by calling **IMFASFProfile::QueryInterface**.</span></span>
7.  <span data-ttu-id="2e808-132">Establezca la información de codificación de la secuencia en el receptor de archivos.</span><span class="sxs-lookup"><span data-stu-id="2e808-132">Set encoding information for the stream in the file sink.</span></span> <span data-ttu-id="2e808-133">Se describe en [configuración de las propiedades del receptor de archivos](setting-properties-in-the-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="2e808-133">Discussed in [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span>
8.  <span data-ttu-id="2e808-134">Agregue la secuencia al perfil llamando a [**IMFASFProfile:: SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream).</span><span class="sxs-lookup"><span data-stu-id="2e808-134">Add the stream to the profile by calling [**IMFASFProfile::SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream).</span></span>
9.  <span data-ttu-id="2e808-135">Asocie el perfil con el objeto ContentInfo llamando a [**IMFASFContentInfo:: SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).</span><span class="sxs-lookup"><span data-stu-id="2e808-135">Associate the profile with the ContentInfo object by calling [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).</span></span>

<span data-ttu-id="2e808-136">Para modificar una secuencia existente, la aplicación puede obtener una referencia a la interfaz [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) del flujo y volver a configurarla según los requisitos.</span><span class="sxs-lookup"><span data-stu-id="2e808-136">To modify an existing stream, the application can get a reference to the stream's [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface and reconfigure it according to the requirements.</span></span> <span data-ttu-id="2e808-137">Para agregar o quitar secuencias, la aplicación debe llamar a [**IMFASFProfile:: RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream).</span><span class="sxs-lookup"><span data-stu-id="2e808-137">To add or remove streams, the application must call [**IMFASFProfile::RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream).</span></span> <span data-ttu-id="2e808-138">Para aplicar estos cambios, las modificaciones o la eliminación de secuencias, debe volver a establecer el perfil en el objeto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="2e808-138">To apply these changes, stream modifications or removal, you must set the profile again in the ContentInfo object.</span></span> <span data-ttu-id="2e808-139">Esto sobrescribe el perfil existente que ya está asociado al objeto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="2e808-139">This overwrites the existing profile that is already associated with the ContentInfo object.</span></span>


```C++
//-------------------------------------------------------------------
//  CreateVideoStream
//  Create an video stream and add it to the profile.
//
//  pProfile: A pointer to the ASF profile.
//  wStreamNumber: Stream number to assign for the new stream.
//    pType: A pointer to the source's video media type.
//-------------------------------------------------------------------

HRESULT CreateVideoStream(IMFASFProfile* pProfile, WORD wStreamNumber, IMFMediaType* pType)
{
    if (!pProfile)
    {
        return E_INVALIDARG;
    }
    if (wStreamNumber < 1 || wStreamNumber > 127 )
    {
        return MF_E_INVALIDSTREAMNUMBER;
    }

    HRESULT hr = S_OK;

    
    IMFMediaType* pVideoType = NULL;
    IMFASFStreamConfig* pVideoStream = NULL;

    UINT32 dwBitRate = 0;
        
    //Create a new video type from the source type
    hr = CreateCompressedVideoType(pType, &pVideoType);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create a new stream with the video type
    hr = pProfile->CreateStream(pVideoType, &pVideoStream);
    if (FAILED(hr))
    {
        goto done;
    }
    

    //Set a valid stream number
    hr = pVideoStream->SetStreamNumber(wStreamNumber);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the stream to the profile
    hr = pProfile->SetStream(pVideoStream);
    if (FAILED(hr))
    {
        goto done;
    }

    wprintf_s(L"Video Stream created. Stream Number: %d .\n", wStreamNumber);

done:

    SafeRelease(&pVideoStream);
    SafeRelease(&pVideoType);

    return hr;
}
```



## <a name="enumerating-stream-sinks"></a><span data-ttu-id="2e808-140">Enumerar receptores de secuencia</span><span class="sxs-lookup"><span data-stu-id="2e808-140">Enumerating Stream Sinks</span></span>

<span data-ttu-id="2e808-141">Para cada secuencia del perfil que sea consciente del objeto ContentInfo, el receptor de archivos ASF crea y agrega un receptor de flujo que contiene todas las propiedades de la secuencia codificada.</span><span class="sxs-lookup"><span data-stu-id="2e808-141">For each stream in the profile that the ContentInfo object is aware of, the ASF file sink creates and adds a stream sink that contains all the properties of the encoded stream.</span></span> <span data-ttu-id="2e808-142">El receptor de archivos ASF está diseñado para contener secuencias fijas.</span><span class="sxs-lookup"><span data-stu-id="2e808-142">The ASF file sink is designed to contain fixed streams.</span></span> <span data-ttu-id="2e808-143">Esto significa que no puede Agregar o quitar secuencias mediante una llamada a [**IMFMediaSink:: AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink) o [**IMFMediaSink:: RemoveStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink).</span><span class="sxs-lookup"><span data-stu-id="2e808-143">This means that you cannot add or remove streams by calling [**IMFMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink) or [**IMFMediaSink::RemoveStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink).</span></span> <span data-ttu-id="2e808-144">Estas llamadas en el receptor de archivo dan error con \_ el \_ código de error fijo MF E STREAMSINKS \_ .</span><span class="sxs-lookup"><span data-stu-id="2e808-144">These calls on the file sink fail with the MF\_E\_STREAMSINKS\_FIXED error code.</span></span> <span data-ttu-id="2e808-145">La adición o eliminación de secuencias en el perfil no agrega ni quita automáticamente los receptores de la secuencia en el receptor de archivos.</span><span class="sxs-lookup"><span data-stu-id="2e808-145">Adding or removing streams in the profile does not automatically add or remove the stream sinks in the file sink.</span></span> <span data-ttu-id="2e808-146">Debe descartar la instancia existente del archivo y volver a crearla con la nueva información de la secuencia si han cambiado las secuencias en el perfil.</span><span class="sxs-lookup"><span data-stu-id="2e808-146">You must discard the existing instance of the file and recreate it with new stream information if your streams in the profile have changed.</span></span>

<span data-ttu-id="2e808-147">El procedimiento siguiente resume los pasos generales para enumerar los receptores de secuencias en el receptor de archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="2e808-147">The following procedure summarizes the general steps for enumerating stream sinks in the ASF file sink.</span></span>

<span data-ttu-id="2e808-148">**Para enumerar los receptores de la secuencia**</span><span class="sxs-lookup"><span data-stu-id="2e808-148">**To enumerate stream sinks**</span></span>

1.  <span data-ttu-id="2e808-149">Llame a [**IMFMediaSink:: GetStreamSinkCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkcount) para obtener el número total de receptores de flujo en el receptor de archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="2e808-149">Call [**IMFMediaSink::GetStreamSinkCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkcount) to get the total number of stream sinks in the ASF file sink.</span></span>
2.  <span data-ttu-id="2e808-150">Recorrer los receptores de flujo Ang obtener una referencia a la interfaz [**GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) del receptor de flujo.</span><span class="sxs-lookup"><span data-stu-id="2e808-150">Loop through the stream sinks ang get a reference to the stream sink's [**GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) interface.</span></span>

    <span data-ttu-id="2e808-151">O bien</span><span class="sxs-lookup"><span data-stu-id="2e808-151">-or-</span></span>

    <span data-ttu-id="2e808-152">Llame a [**IMFMediaSink:: GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) para obtener el receptor de flujo especificando el número de secuencia.</span><span class="sxs-lookup"><span data-stu-id="2e808-152">Call [**IMFMediaSink::GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) to get the stream sink by specifying the stream number.</span></span> <span data-ttu-id="2e808-153">Cada receptor de flujo se identifica con el número de secuencia que estableció al crear la secuencia en el perfil.</span><span class="sxs-lookup"><span data-stu-id="2e808-153">Each stream sink is identified with the stream number you set while creating the stream in the profile.</span></span>

<span data-ttu-id="2e808-154">Si va a crear una topología parcial para codificar un archivo multimedia, debe agregar el receptor de archivos a la topología como un nodo de topología de salida.</span><span class="sxs-lookup"><span data-stu-id="2e808-154">If you are building a partial topology for encoding a media file, you must add the file sink to the topology as an output topology node.</span></span> <span data-ttu-id="2e808-155">Puede hacerlo especificando cada receptor de vapor en el receptor de archivos o estableciendo el objeto de activación del receptor de archivos y los identificadores del receptor de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="2e808-155">You can do so either by specifying each steam sink in the file sink or by setting the file sink activation object and the stream sink identifiers.</span></span> <span data-ttu-id="2e808-156">Para obtener más información y ejemplos de código, vea [crear nodos de salida](creating-output-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="2e808-156">For more information and code example, see [Creating Output Nodes](creating-output-nodes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e808-157">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2e808-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e808-158">Receptores de medios ASF</span><span class="sxs-lookup"><span data-stu-id="2e808-158">ASF Media Sinks</span></span>](asf-media-sinks.md)
</dt> <dt>

[<span data-ttu-id="2e808-159">Compatibilidad con ASF en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2e808-159">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



