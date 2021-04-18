---
description: Configuración de perfiles y otras propiedades de archivo ASF
ms.assetid: c43df556-9d8a-4010-9ed6-f84d8ac6d9bc
title: Configuración de perfiles y otras propiedades de archivo ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e26dcbb49cb5ff8309dccafc3f1d8d66397871
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422996"
---
# <a name="configuring-profiles-and-other-asf-file-properties"></a><span data-ttu-id="661f4-103">Configuración de perfiles y otras propiedades de archivo ASF</span><span class="sxs-lookup"><span data-stu-id="661f4-103">Configuring Profiles and Other ASF File Properties</span></span>

<span data-ttu-id="661f4-104">En los elementos siguientes se describe cómo realizar varias tareas relacionadas con la creación de archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="661f4-104">The following items describe how to perform various tasks related to the creation of ASF files.</span></span> <span data-ttu-id="661f4-105">Algunas de las interfaces mencionadas en este tema se documentan en la documentación del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="661f4-105">Some of the interfaces mentioned in this topic are documented in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="661f4-106">Creación de un perfil</span><span class="sxs-lookup"><span data-stu-id="661f4-106">Creating a Profile</span></span>

<span data-ttu-id="661f4-107">Los perfiles ASF se describen en detalle en el SDK de Windows Media Format; en esencia, describen los atributos de un archivo de formato de Windows Media, como la velocidad de bits, el número y el tipo de secuencias, y la calidad de la compresión.</span><span class="sxs-lookup"><span data-stu-id="661f4-107">ASF profiles are discussed in detail in the Windows Media Format SDK; essentially, they describe attributes of a Windows Media Format file such as bit rate, number and type of streams, and compression quality.</span></span> <span data-ttu-id="661f4-108">El filtro usa el perfil para determinar el tipo de archivo de formato de Windows Media que se va a escribir, el número de clavijas de entrada que debe configurar y los tipos de medios que pueden aceptar.</span><span class="sxs-lookup"><span data-stu-id="661f4-108">The filter uses the profile to determine what kind of Windows Media Format file to write, how many input pins it must set up, and what media types they can accept.</span></span>

<span data-ttu-id="661f4-109">Para crear un perfil personalizado, use el SDK de Windows Media Format directamente para crear un objeto de administrador de perfiles mediante la función **WMCreateProfileManager** .</span><span class="sxs-lookup"><span data-stu-id="661f4-109">To create a custom profile, use the Windows Media Format SDK directly to create a profile manager object by using the **WMCreateProfileManager** function.</span></span> <span data-ttu-id="661f4-110">A continuación, cree el perfil y páselo al escritor de [ASF de WM](wm-asf-writer-filter.md) mediante el método [**IConfigASFWriter:: ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) .</span><span class="sxs-lookup"><span data-stu-id="661f4-110">Next, create the profile, and pass it to the [WM ASF Writer](wm-asf-writer-filter.md) by using the [**IConfigASFWriter::ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) method.</span></span> <span data-ttu-id="661f4-111">Esta es la única manera de configurar el filtro con un perfil que use los códecs de la serie Windows Media Audio y vídeo 9.</span><span class="sxs-lookup"><span data-stu-id="661f4-111">This is the only way to configure the filter with a profile that uses the Windows Media Audio and Video 9 Series codecs.</span></span> <span data-ttu-id="661f4-112">Los perfiles de sistema para versiones anteriores de estos códecs se pueden agregar mediante el método [**IConfigASFWriter:: ConfigureFilterUsingProfileGuid**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofileguid) .</span><span class="sxs-lookup"><span data-stu-id="661f4-112">System profiles for earlier versions of these codecs can be added by using the [**IConfigASFWriter::ConfigureFilterUsingProfileGuid**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofileguid) method.</span></span>

<span data-ttu-id="661f4-113">Puede restablecer el perfil mientras los pines de entrada del filtro están conectados, siempre que el nuevo perfil no requiera ninguna clavija de entrada adicional.</span><span class="sxs-lookup"><span data-stu-id="661f4-113">You can reset the profile while the filter's input pins are connected, as long as the new profile does not require any additional input pins.</span></span> <span data-ttu-id="661f4-114">Por ejemplo, si cambia el perfil de un perfil de sólo audio de una entrada a un perfil de audio y vídeo de dos entradas, solo se volverá a conectar el PIN de audio y no se creará ningún PIN nuevo para la secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="661f4-114">For example, if you change the profile from a one-input audio-only profile to a two-input audio and video profile, just the audio pin will be reconnected and no new pin will be created for the video stream.</span></span>

<span data-ttu-id="661f4-115">Agregar metadatos</span><span class="sxs-lookup"><span data-stu-id="661f4-115">Adding Metadata</span></span>

<span data-ttu-id="661f4-116">Para agregar metadatos a un archivo, consulte el filtro de [escritor ASF de WM](wm-asf-writer-filter.md) para la interfaz **IWMHeaderInfo** .</span><span class="sxs-lookup"><span data-stu-id="661f4-116">To add metadata to a file, query the [WM ASF Writer](wm-asf-writer-filter.md) filter for the **IWMHeaderInfo** interface.</span></span> <span data-ttu-id="661f4-117">Una vez que se ha dado un perfil al filtro, use los métodos de la interfaz **IWMHeaderInfo** para escribir los metadatos.</span><span class="sxs-lookup"><span data-stu-id="661f4-117">After the filter has been given a profile, use the **IWMHeaderInfo** interface methods to write the metadata.</span></span>

<span data-ttu-id="661f4-118">Indexación de un archivo</span><span class="sxs-lookup"><span data-stu-id="661f4-118">Indexing a File</span></span>

<span data-ttu-id="661f4-119">De manera predeterminada, el escritor ASF de WM crea archivos indizados de forma temporal.</span><span class="sxs-lookup"><span data-stu-id="661f4-119">The WM ASF Writer creates temporally indexed files by default.</span></span> <span data-ttu-id="661f4-120">Para crear un archivo indexado mediante Marcos, use el método [**IConfigAsfWriter:: SetIndexMode**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-setindexmode) para deshabilitar toda la indexación y, a continuación, cree el archivo.</span><span class="sxs-lookup"><span data-stu-id="661f4-120">To create a frame-indexed file, use the [**IConfigAsfWriter::SetIndexMode**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-setindexmode) method to disable all indexing, then create the file.</span></span> <span data-ttu-id="661f4-121">Cuando haya finalizado, use el SDK de Windows Media Format directamente para crear un índice basado en marco para el archivo.</span><span class="sxs-lookup"><span data-stu-id="661f4-121">When it is complete, use the Windows Media Format SDK directly to create a frame-based index for the file.</span></span>

<span data-ttu-id="661f4-122">Codificación de Two-Pass</span><span class="sxs-lookup"><span data-stu-id="661f4-122">Two-Pass Encoding</span></span>

<span data-ttu-id="661f4-123">La codificación de dos pasos solo se admite en códecs de Windows Media de la versión 8 y posteriores.</span><span class="sxs-lookup"><span data-stu-id="661f4-123">Two-pass encoding is supported only on Windows Media codecs of version 8 and later.</span></span> <span data-ttu-id="661f4-124">Coloque el escritor ASF de WM en modo de preprocesamiento llamando a [**IConfigAsfWriter2:: SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) y especificando AM \_ CONFIGASFWRITER \_ param \_ Multipass en el parámetro *DwParam* y **true** en el parámetro *dwParam1* .</span><span class="sxs-lookup"><span data-stu-id="661f4-124">Put the WM ASF Writer into preprocess mode by calling [**IConfigAsfWriter2::SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) and specifying AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS in the *dwParam* parameter and **TRUE** in the *dwParam1* parameter.</span></span>

<span data-ttu-id="661f4-125">A continuación, ejecute el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="661f4-125">Then run the filter graph.</span></span> <span data-ttu-id="661f4-126">Cuando se realizan todos los pasos de preprocesamiento (normalmente solo se realizará un paso de preprocesamiento), la aplicación recibirá un evento de [**\_ \_ finalización de preprocesamiento de EC**](ec-preprocess-complete.md) del filtro.</span><span class="sxs-lookup"><span data-stu-id="661f4-126">When all the preprocessing passes are done (typically only one preprocessing pass will be performed), the application will receive an [**EC\_PREPROCESS\_COMPLETE**](ec-preprocess-complete.md) event from the filter.</span></span> <span data-ttu-id="661f4-127">Cuando se reciba este evento, use [**IMediaSeeking:: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) para restablecer el puntero de secuencia de nuevo al principio y vuelva a ejecutar el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="661f4-127">When this event is received, use [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) to reset the stream pointer back to the beginning, and run the filter graph again.</span></span> <span data-ttu-id="661f4-128">Después del último paso (normalmente el segundo paso), la aplicación recibirá un evento de [**\_ finalización de EC**](ec-complete.md) para indicar que se ha completado el proceso de codificación.</span><span class="sxs-lookup"><span data-stu-id="661f4-128">After the last pass (typically the second pass), the application will receive an [**EC\_COMPLETE**](ec-complete.md) event to signify that the encoding process is complete.</span></span> <span data-ttu-id="661f4-129">Si se cancela un paso de preprocesamiento antes de que se reciba el evento de **\_ \_ finalización** previa al preprocesamiento, llame a [**IConfigAsfWriter2:: ResetMultiPassState**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-resetmultipassstate) para restablecer el filtro antes de intentar otra ejecución de preprocesamiento.</span><span class="sxs-lookup"><span data-stu-id="661f4-129">If a preprocessing pass is canceled before the **EC\_PREPROCESS\_COMPLETE** event is received, call [**IConfigAsfWriter2::ResetMultiPassState**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-resetmultipassstate) to reset the filter before attempting another preprocessing run.</span></span>

<span data-ttu-id="661f4-130">Solo es necesario establecer el \_ parámetro AM CONFIGASFWRITER \_ param \_ Multipass en **false** si desea dejar por completo el filtro del modo de preprocesamiento.</span><span class="sxs-lookup"><span data-stu-id="661f4-130">It is only necessary to set the AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS parameter to **FALSE** if you want to put the filter out of preprocessing mode completely.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="661f4-131">Es responsabilidad de la aplicación habilitar el modo de preprocesamiento basado en el perfil que se utilizará para la codificación.</span><span class="sxs-lookup"><span data-stu-id="661f4-131">It is the application's responsibility to enable the preprocessing mode based on the profile that will be used for encoding.</span></span> <span data-ttu-id="661f4-132">Algunos perfiles requieren codificación de dos pasos; Si intenta codificar un archivo con este tipo de perfil y no establece AM \_ CONFIGASFWRITER \_ param \_ Multipass en **true**, se producirá un error de [**\_ USERABORT de EC**](ec-userabort.md) .</span><span class="sxs-lookup"><span data-stu-id="661f4-132">Some profiles require two-pass encoding; if you attempt to encode a file with such a profile, and do not set AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS to **TRUE**, an [**EC\_USERABORT**](ec-userabort.md) error will result.</span></span> <span data-ttu-id="661f4-133">Para obtener más información, consulte la documentación del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="661f4-133">For more information, see the Windows Media Format SDK documentation.</span></span>

 

<span data-ttu-id="661f4-134">Obtener y establecer propiedades de búfer en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="661f4-134">Getting and Setting Buffer Properties at Run Time</span></span>

<span data-ttu-id="661f4-135">En algunos escenarios, por ejemplo, si desea forzar la inserción de fotogramas clave al escribir un archivo, es posible que una aplicación necesite obtener o establecer información sobre un búfer de Windows Media en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="661f4-135">In some scenarios, for example if you want to force key-frame insertion when writing a file, an application may need to get or set information about a Windows Media buffer at run time.</span></span> <span data-ttu-id="661f4-136">Los filtros del [lector ASF de WM](wm-asf-reader-filter.md) y del [escritor ASF de WM](wm-asf-writer-filter.md) admiten un mecanismo de devolución de llamada que permite a una aplicación tener acceso a la interfaz **INSSBuffer3** en cada búfer multimedia individual durante la lectura o escritura de archivos.</span><span class="sxs-lookup"><span data-stu-id="661f4-136">The [WM ASF Reader](wm-asf-reader-filter.md) and [WM ASF Writer](wm-asf-writer-filter.md) filters both support a callback mechanism that enables an application to access the **INSSBuffer3** interface on each individual media buffer during file reading or file writing.</span></span> <span data-ttu-id="661f4-137">Las aplicaciones pueden usar esta interfaz para designar ejemplos específicos como fotogramas clave, establecer códigos de tiempo SMPTE, especificar la configuración de entrelazado o agregar cualquier tipo de datos privados a un flujo.</span><span class="sxs-lookup"><span data-stu-id="661f4-137">Applications can use this interface to designate specific samples as key frames, set SMPTE time codes, specify interlace settings, or add any type of private data to a stream.</span></span>

<span data-ttu-id="661f4-138">Use la interfaz [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass) para registrar las devoluciones de llamada del PIN que está controlando la secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="661f4-138">Use the [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass) interface to register for callbacks from the pin that is handling the video stream.</span></span> <span data-ttu-id="661f4-139">El PIN llamará al método [**IAMWMBufferPassCallback:: Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) para cada búfer.</span><span class="sxs-lookup"><span data-stu-id="661f4-139">The pin will call your [**IAMWMBufferPassCallback::Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) method for each buffer.</span></span>

<span data-ttu-id="661f4-140">Píxeles no cuadrados</span><span class="sxs-lookup"><span data-stu-id="661f4-140">Non-Square Pixels</span></span>

<span data-ttu-id="661f4-141">El escritor ASF de WM se conecta a un filtro de nivel superior, como el descodificador DV, que genera información de relación de aspecto de píxeles.</span><span class="sxs-lookup"><span data-stu-id="661f4-141">The WM ASF Writer connects to an upstream filter, such as the DV Decoder, that outputs pixel aspect ratio information.</span></span> <span data-ttu-id="661f4-142">El escritor ASF de WM escribirá esta información como extensiones de unidad de datos para cada muestra del archivo.</span><span class="sxs-lookup"><span data-stu-id="661f4-142">The WM ASF Writer will write this information as data unit extensions for every sample in the file.</span></span>

<span data-ttu-id="661f4-143">Cuando el lector ASF de WM encuentra información de relación de aspecto de píxeles en el encabezado de archivo o en las extensiones de unidad de datos para los ejemplos, ofrecerá un formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) como primera opción en el PIN de salida.</span><span class="sxs-lookup"><span data-stu-id="661f4-143">When the WM ASF Reader encounters pixel aspect ratio information in the file header or in data unit extensions for the samples, it will offer a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format as a first choice on its output pin.</span></span> <span data-ttu-id="661f4-144">Los miembros **dwPictAspectRatioX** y **dwPictAspectRatioY** de la estructura, que describen la relación de aspecto del rectángulo de vídeo, se ajustarán correctamente para tener en cuenta la relación de aspecto de píxeles.</span><span class="sxs-lookup"><span data-stu-id="661f4-144">The **dwPictAspectRatioX** and **dwPictAspectRatioY** members of the structure, which describe the video rectangle's aspect ratio, will be correctly adjusted to account for the pixel aspect ratio.</span></span>

<span data-ttu-id="661f4-145">Mantener el formato entrelazado</span><span class="sxs-lookup"><span data-stu-id="661f4-145">Maintaining Interlaced Format</span></span>

<span data-ttu-id="661f4-146">Si captura vídeo entrelazado de una cámara de televisión o DV, es posible que desee conservar el vídeo original como campos independientes si espera que el archivo codificado se reproduzca en un televisor u otro dispositivo de pantalla entrelazada.</span><span class="sxs-lookup"><span data-stu-id="661f4-146">If you capture interlaced video from a television or a DV camera, you might wish to preserve the original video as independent fields if you expect the encoded file to be played back on a television or other interlaced display device.</span></span> <span data-ttu-id="661f4-147">(Los monitores de equipos son dispositivos de digitalización progresiva). Si desentrelaza un vídeo y, a continuación, lo reentrelaza para su reproducción en un televisor, se producirá una pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="661f4-147">(Computer monitors are progressive scanning devices.) If you deinterlace a video, and then reinterlace it for playback on a television, some loss of data will be incurred.</span></span> <span data-ttu-id="661f4-148">En un archivo ASF, la información de entrelazado se almacena como extensiones de unidad de datos que la aplicación aplica a cada ejemplo mediante el método [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="661f4-148">In an ASF file, interlacing information is stored as data unit extensions that the application applies to each sample using the [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) method described previously.</span></span> <span data-ttu-id="661f4-149">Para codificar un archivo que conserva la configuración de entrelazado original, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="661f4-149">To encode a file that preserves the original interlace settings, follow these steps:</span></span>

1.  <span data-ttu-id="661f4-150">Implemente una clase que admita **IAMWMBufferPassCallback** y escriba una función Notify que establezca las marcas de entrelazado para cada ejemplo.</span><span class="sxs-lookup"><span data-stu-id="661f4-150">Implement a class that supports **IAMWMBufferPassCallback** and write a Notify function that sets the interlace flags for each sample.</span></span> <span data-ttu-id="661f4-151">El escritor ASF de WM llamará a esta función antes de procesar cada ejemplo.</span><span class="sxs-lookup"><span data-stu-id="661f4-151">This function will be called by the WM ASF Writer before it processes each sample.</span></span>
    ```C++
    // Set to WM_CT_TOP_FIELD_FIRST if that is your format.
    BYTE flag = WM_CT_INTERLACED | WM_CT_BOTTOM_FIELD_FIRST;
    HRESULT hr = S_OK;

    hr = pNSSBuffer3->SetProperty(
        WM_SampleExtensionGUID_ContentType, 
        (void*) &flag, 
        WM_SampleExtension_ContentType_Size
        );         
    ```

    

2.  <span data-ttu-id="661f4-152">Establezca las extensiones de unidad de datos en el perfil antes de pasar el perfil al filtro.</span><span class="sxs-lookup"><span data-stu-id="661f4-152">Set the data unit extensions on the profile before you pass the profile to the filter.</span></span>
    ```C++
    hr = pWMStreamConfig2->AddDataUnitExtension(
        WM_SampleExtensionGUID_ContentType, 
        WM_SampleExtension_ContentType_Size, 
        NULL, 
        0 
        );
    ```

    

3.  <span data-ttu-id="661f4-153">Después de configurar el filtro con el perfil, obtenga la interfaz **IWMWriterAdvanced2** del escritor ASF de WM y llame al método **SetInputSettings** .</span><span class="sxs-lookup"><span data-stu-id="661f4-153">After you configure the filter with the profile, obtain the **IWMWriterAdvanced2** interface from the WM ASF Writer and call the **SetInputSettings** method.</span></span>

    ``

    ``

    ```C++
    // Must do this first.
    hr = pConfigAsfWriter2->ConfigureFilterUsingProfile(pProfile);
      
    CComPtr<IServiceProvider> pProvider;
    CComPtr<IWMWriterAdvanced2> pWMWA2;

    hr = pConfigAsfWriter2->QueryInterface( __uuidof(IServiceProvider),
                                             (void**)&pProvider);
    if (SUCCEEDED(hr))
    {
        hr = pProvider->QueryService(IID_IWMWriterAdvanced2,
            IID_IWMWriterAdvanced2,
            (void**)&pWMWA2);
    }

    BOOL pValue = TRUE;

    // Set the first parameter to your actual input number.
    hr = pWMWA2->SetInputSetting(0, g_wszInterlacedCoding,
        WMT_TYPE_BOOL, (BYTE*) &pValue, sizeof(WMT_TYPE_BOOL));
                
    ```

    

## <a name="related-topics"></a><span data-ttu-id="661f4-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="661f4-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="661f4-155">Crear archivos ASF en DirectShow</span><span class="sxs-lookup"><span data-stu-id="661f4-155">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



