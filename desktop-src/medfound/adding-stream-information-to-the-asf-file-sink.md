---
description: Obtenga información sobre cómo agregar información de flujo al receptor de archivos de ASF, que una aplicación puede usar para archivar datos multimedia de ASF en un archivo.
ms.assetid: 21cbde27-a2ca-4298-9197-43bcaf05588d
title: Agregar información de flujo al receptor de archivos de ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8202de8da5cb8e17534c334e3d39dddb3c4f99
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404367"
---
# <a name="adding-stream-information-to-the-asf-file-sink"></a><span data-ttu-id="67afb-103">Agregar información de flujo al receptor de archivos de ASF</span><span class="sxs-lookup"><span data-stu-id="67afb-103">Adding Stream Information to the ASF File Sink</span></span>

<span data-ttu-id="67afb-104">El receptor de archivos ASF es una implementación de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) proporcionada por Media Foundation que una aplicación puede usar para archivar datos multimedia de ASF en un archivo.</span><span class="sxs-lookup"><span data-stu-id="67afb-104">The ASF file sink is an implementation of [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) provided by Media Foundation that an application can use to archive ASF media data to a file.</span></span> <span data-ttu-id="67afb-105">Para obtener información sobre el modelo de objetos de los receptores de medios de ASF y el uso general, vea [Receptores de medios de ASF.](asf-media-sinks.md)</span><span class="sxs-lookup"><span data-stu-id="67afb-105">For information about ASF Media Sinks' object model and general usage, see [ASF Media Sinks](asf-media-sinks.md).</span></span>

<span data-ttu-id="67afb-106">Después de crear una instancia del receptor de archivos, debe configurarse antes de compilar la topología.</span><span class="sxs-lookup"><span data-stu-id="67afb-106">After instantiating the file sink, it must be configured before building the topology.</span></span> <span data-ttu-id="67afb-107">El receptor del archivo debe conocer los flujos del archivo de salida, la información del modo de codificación y los metadatos.</span><span class="sxs-lookup"><span data-stu-id="67afb-107">The file sink needs to know about the streams in the output file, the encoding mode information, and the metadata.</span></span> <span data-ttu-id="67afb-108">En este tema se describe el proceso de agregar secuencia en el receptor de archivos.</span><span class="sxs-lookup"><span data-stu-id="67afb-108">This topic describes the process of adding stream in the file sink.</span></span>

-   [<span data-ttu-id="67afb-109">Adición de secuencias en el receptor de archivos de ASF</span><span class="sxs-lookup"><span data-stu-id="67afb-109">Adding Streams in the ASF File Sink</span></span>](#adding-streams-in-the-asf-file-sink)
-   [<span data-ttu-id="67afb-110">Enumeración de receptores de flujo</span><span class="sxs-lookup"><span data-stu-id="67afb-110">Enumerating Stream Sinks</span></span>](#enumerating-stream-sinks)
-   [<span data-ttu-id="67afb-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="67afb-111">Related topics</span></span>](#related-topics)

## <a name="adding-streams-in-the-asf-file-sink"></a><span data-ttu-id="67afb-112">Adición de secuencias en el receptor de archivos de ASF</span><span class="sxs-lookup"><span data-stu-id="67afb-112">Adding Streams in the ASF File Sink</span></span>

<span data-ttu-id="67afb-113">El receptor del archivo debe conocer los flujos de salida y sus propiedades para que pueda generar ejemplos de salida en consecuencia y agregarlos al archivo ASF de salida.</span><span class="sxs-lookup"><span data-stu-id="67afb-113">The file sink must know of the output streams and their properties so that it can generate output samples accordingly and add them to the output ASF file.</span></span> <span data-ttu-id="67afb-114">Esta configuración se escribe en el objeto de encabezado asf final.</span><span class="sxs-lookup"><span data-stu-id="67afb-114">These settings are written to the final ASF Header Object.</span></span>

<span data-ttu-id="67afb-115">Para establecer la información de flujo, debe tener una referencia al objeto ContentInfo de ASF del receptor de archivos.</span><span class="sxs-lookup"><span data-stu-id="67afb-115">To set stream information, you must have a reference to the file sink's ASF ContentInfo object.</span></span> <span data-ttu-id="67afb-116">Para obtener información, vea [Creating the ASF File Sink](creating-the-asf-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="67afb-116">For information, see [Creating the ASF File Sink](creating-the-asf-file-sink.md).</span></span>

<span data-ttu-id="67afb-117">En el procedimiento siguiente se resumen los pasos generales para configurar la secuencia mediante el objeto de perfil de ASF.</span><span class="sxs-lookup"><span data-stu-id="67afb-117">The following procedure summarizes the general steps for configuring stream by using the ASF profile object.</span></span>

<span data-ttu-id="67afb-118">**Para configurar la información de flujo en el receptor de archivos de ASF**</span><span class="sxs-lookup"><span data-stu-id="67afb-118">**To configure stream information in the ASF file sink**</span></span>

1.  <span data-ttu-id="67afb-119">Cree un objeto de perfil de ASF mediante una llamada [**a MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile).</span><span class="sxs-lookup"><span data-stu-id="67afb-119">Create an ASF profile object by calling [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile).</span></span>
2.  <span data-ttu-id="67afb-120">Para cada secuencia del archivo de salida, cree un tipo de medio para la secuencia de destino que se va a agregar en el receptor del archivo.</span><span class="sxs-lookup"><span data-stu-id="67afb-120">For each stream in the output file, create a media type for the target stream to be added in the file sink.</span></span> <span data-ttu-id="67afb-121">El tipo de medio debe ser compatible con los tipos de salida admitidos por los codificadores de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="67afb-121">The media type must be compatible with the output types supported by the Windows Media encoders.</span></span>

    <span data-ttu-id="67afb-122">Para obtener información sobre cómo agregar secuencias de audio al perfil, vea Crear secuencias de audio para codificación ASF.</span><span class="sxs-lookup"><span data-stu-id="67afb-122">For information about adding audio streams to the profile, see Creating Audio Streams for ASF Encoding.</span></span>

    <span data-ttu-id="67afb-123">Para obtener información sobre cómo agregar secuencias de vídeo al perfil, consulte Creación de secuencias de vídeo para la codificación ASF.</span><span class="sxs-lookup"><span data-stu-id="67afb-123">For information about adding video streams to the profile, see Creating Video Streams for ASF Encoding.</span></span>

3.  <span data-ttu-id="67afb-124">Cree secuencias basadas en los tipos de medios creados en el paso 2 mediante una llamada [**a IMFASFProfile::CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream).</span><span class="sxs-lookup"><span data-stu-id="67afb-124">Create streams based on the media types created in step 2 by calling [**IMFASFProfile::CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream).</span></span>
4.  <span data-ttu-id="67afb-125">Asigne un número de secuencia para la secuencia recién creada mediante una llamada al puntero de interfaz [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) recibido en el paso 3.</span><span class="sxs-lookup"><span data-stu-id="67afb-125">Assign a stream number for the newly created stream by calling [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface pointer received in step 3.</span></span>
5.  <span data-ttu-id="67afb-126">Opcionalmente, configure la secuencia con la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="67afb-126">Optionally configure the stream with the following information:</span></span>
    -   <span data-ttu-id="67afb-127">Parámetros de cubo de pérdida estableciendo los atributos: [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) o [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="67afb-127">Leaky bucket parameters by setting the attributes: [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) or [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)</span></span>
    -   <span data-ttu-id="67afb-128">Extensión de carga, exclusión mutua mediante una llamada [**a los métodos DE TIPO IMFASFStreamConfig.**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig)</span><span class="sxs-lookup"><span data-stu-id="67afb-128">Payload extension, mutual exclusion by calling [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) methods.</span></span>
6.  <span data-ttu-id="67afb-129">Opcionalmente, establezca el tamaño del paquete de datos para el perfil estableciendo los atributos [**MF \_ ASFPROFILE \_ MINPACKETSIZE**](mf-asfprofile-minpacketsize-attribute.md) y [**MF \_ ASFPROFILE \_ MAXPACKETSIZE.**](mf-asfprofile-maxpacketsize-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="67afb-129">Optionally set data packet size for the profile by setting [**MF\_ASFPROFILE\_MINPACKETSIZE**](mf-asfprofile-minpacketsize-attribute.md) and [**MF\_ASFPROFILE\_MAXPACKETSIZE**](mf-asfprofile-maxpacketsize-attribute.md) attributes.</span></span> <span data-ttu-id="67afb-130">El perfil de ASF expone la interfaz [**IMFAttributes,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) a la que una aplicación puede obtener referencia mediante una llamada a **IMFASFProfile::QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="67afb-130">The ASF profile exposes the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface, which an application can get reference to by calling **IMFASFProfile::QueryInterface**.</span></span>
7.  <span data-ttu-id="67afb-131">Establezca la información de codificación de la secuencia en el receptor del archivo.</span><span class="sxs-lookup"><span data-stu-id="67afb-131">Set encoding information for the stream in the file sink.</span></span> <span data-ttu-id="67afb-132">Se describe en [Establecer propiedades en el receptor de archivos](setting-properties-in-the-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="67afb-132">Discussed in [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span>
8.  <span data-ttu-id="67afb-133">Agregue la secuencia al perfil mediante una llamada [**a IMFASFProfile::SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream).</span><span class="sxs-lookup"><span data-stu-id="67afb-133">Add the stream to the profile by calling [**IMFASFProfile::SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream).</span></span>
9.  <span data-ttu-id="67afb-134">Asocie el perfil al objeto ContentInfo llamando a [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).</span><span class="sxs-lookup"><span data-stu-id="67afb-134">Associate the profile with the ContentInfo object by calling [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).</span></span>

<span data-ttu-id="67afb-135">Para modificar una secuencia existente, la aplicación puede obtener una referencia a la interfaz [**DEFSTREAMConfig DE LA SECUENCIA**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) Y volver a configurarla según los requisitos.</span><span class="sxs-lookup"><span data-stu-id="67afb-135">To modify an existing stream, the application can get a reference to the stream's [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface and reconfigure it according to the requirements.</span></span> <span data-ttu-id="67afb-136">Para agregar o quitar secuencias, la aplicación debe llamar a [**IMFASFProfile::RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream).</span><span class="sxs-lookup"><span data-stu-id="67afb-136">To add or remove streams, the application must call [**IMFASFProfile::RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream).</span></span> <span data-ttu-id="67afb-137">Para aplicar estos cambios, modificaciones de secuencias o eliminación, debe volver a establecer el perfil en el objeto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="67afb-137">To apply these changes, stream modifications or removal, you must set the profile again in the ContentInfo object.</span></span> <span data-ttu-id="67afb-138">Esto sobrescribe el perfil existente que ya está asociado al objeto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="67afb-138">This overwrites the existing profile that is already associated with the ContentInfo object.</span></span>


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



## <a name="enumerating-stream-sinks"></a><span data-ttu-id="67afb-139">Enumeración de receptores de flujo</span><span class="sxs-lookup"><span data-stu-id="67afb-139">Enumerating Stream Sinks</span></span>

<span data-ttu-id="67afb-140">Para cada secuencia del perfil de la que el objeto ContentInfo es consciente, el receptor del archivo ASF crea y agrega un receptor de flujo que contiene todas las propiedades de la secuencia codificada.</span><span class="sxs-lookup"><span data-stu-id="67afb-140">For each stream in the profile that the ContentInfo object is aware of, the ASF file sink creates and adds a stream sink that contains all the properties of the encoded stream.</span></span> <span data-ttu-id="67afb-141">El receptor de archivos asf está diseñado para contener secuencias fijas.</span><span class="sxs-lookup"><span data-stu-id="67afb-141">The ASF file sink is designed to contain fixed streams.</span></span> <span data-ttu-id="67afb-142">Esto significa que no se pueden agregar ni quitar secuencias llamando a [**IMFMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink) o [**IMFMediaSink::RemoveStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink).</span><span class="sxs-lookup"><span data-stu-id="67afb-142">This means that you cannot add or remove streams by calling [**IMFMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink) or [**IMFMediaSink::RemoveStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink).</span></span> <span data-ttu-id="67afb-143">Estas llamadas en el receptor de archivos producirán un error con el código \_ de error CORREGIDO MF E \_ STREAMSINKS. \_</span><span class="sxs-lookup"><span data-stu-id="67afb-143">These calls on the file sink fail with the MF\_E\_STREAMSINKS\_FIXED error code.</span></span> <span data-ttu-id="67afb-144">La adición o eliminación de secuencias en el perfil no agrega ni quita automáticamente los receptores de flujo en el receptor de archivos.</span><span class="sxs-lookup"><span data-stu-id="67afb-144">Adding or removing streams in the profile does not automatically add or remove the stream sinks in the file sink.</span></span> <span data-ttu-id="67afb-145">Debe descartar la instancia existente del archivo y volver a crearla con nueva información de secuencia si las secuencias del perfil han cambiado.</span><span class="sxs-lookup"><span data-stu-id="67afb-145">You must discard the existing instance of the file and recreate it with new stream information if your streams in the profile have changed.</span></span>

<span data-ttu-id="67afb-146">En el procedimiento siguiente se resumen los pasos generales para enumerar los receptores de flujo en el receptor de archivos de ASF.</span><span class="sxs-lookup"><span data-stu-id="67afb-146">The following procedure summarizes the general steps for enumerating stream sinks in the ASF file sink.</span></span>

<span data-ttu-id="67afb-147">**Para enumerar los receptores de flujo**</span><span class="sxs-lookup"><span data-stu-id="67afb-147">**To enumerate stream sinks**</span></span>

1.  <span data-ttu-id="67afb-148">Llame [**a IMFMediaSink::GetStreamSinkCount para**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkcount) obtener el número total de receptores de flujo en el receptor de archivos asf.</span><span class="sxs-lookup"><span data-stu-id="67afb-148">Call [**IMFMediaSink::GetStreamSinkCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkcount) to get the total number of stream sinks in the ASF file sink.</span></span>
2.  <span data-ttu-id="67afb-149">Recorrer en bucle los receptores de flujo para obtener una referencia a la interfaz [**GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) del receptor de secuencias.</span><span class="sxs-lookup"><span data-stu-id="67afb-149">Loop through the stream sinks ang get a reference to the stream sink's [**GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) interface.</span></span>

    <span data-ttu-id="67afb-150">O bien</span><span class="sxs-lookup"><span data-stu-id="67afb-150">-or-</span></span>

    <span data-ttu-id="67afb-151">Llame [**a IMFMediaSink::GetStreamSinkById para**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) obtener el receptor del flujo especificando el número de secuencia.</span><span class="sxs-lookup"><span data-stu-id="67afb-151">Call [**IMFMediaSink::GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) to get the stream sink by specifying the stream number.</span></span> <span data-ttu-id="67afb-152">Cada receptor de flujo se identifica con el número de secuencia que estableció al crear la secuencia en el perfil.</span><span class="sxs-lookup"><span data-stu-id="67afb-152">Each stream sink is identified with the stream number you set while creating the stream in the profile.</span></span>

<span data-ttu-id="67afb-153">Si va a crear una topología parcial para codificar un archivo multimedia, debe agregar el receptor de archivos a la topología como nodo de topología de salida.</span><span class="sxs-lookup"><span data-stu-id="67afb-153">If you are building a partial topology for encoding a media file, you must add the file sink to the topology as an output topology node.</span></span> <span data-ttu-id="67afb-154">Puede hacerlo especificando cada receptor de flujo en el receptor de archivos o estableciendo el objeto de activación del receptor de archivos y los identificadores del receptor del flujo.</span><span class="sxs-lookup"><span data-stu-id="67afb-154">You can do so either by specifying each steam sink in the file sink or by setting the file sink activation object and the stream sink identifiers.</span></span> <span data-ttu-id="67afb-155">Para obtener más información y ejemplo de código, vea [Crear nodos de salida.](creating-output-nodes.md)</span><span class="sxs-lookup"><span data-stu-id="67afb-155">For more information and code example, see [Creating Output Nodes](creating-output-nodes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="67afb-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="67afb-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67afb-157">Receptores de medios de ASF</span><span class="sxs-lookup"><span data-stu-id="67afb-157">ASF Media Sinks</span></span>](asf-media-sinks.md)
</dt> <dt>

[<span data-ttu-id="67afb-158">Compatibilidad con ASF en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="67afb-158">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



