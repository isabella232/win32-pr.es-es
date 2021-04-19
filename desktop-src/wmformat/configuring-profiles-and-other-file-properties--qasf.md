---
title: Configuración de perfiles y otras propiedades de archivo (QASF)
description: Configuración de perfiles y otras propiedades de archivo (QASF)
ms.assetid: a462fc8b-5a2e-4c93-828d-177d1965b734
keywords:
- Windows Media Format SDK, configurar perfiles (QASF)
- SDK de Windows Media Format, configurar las propiedades de archivo (QASF)
- SDK de Windows Media Format, metadatos (QASF)
- Advanced Systems Format (ASF), configurar perfiles (QASF)
- ASF (formato de sistemas avanzados), configurar perfiles (QASF)
- Advanced Systems Format (ASF), configurar las propiedades de archivo (QASF)
- ASF (formato de sistemas avanzados), configurar las propiedades de archivo (QASF)
- Advanced Systems Format (ASF), metadatos (QASF)
- ASF (formato de sistemas avanzados), metadatos (QASF)
- SDK de Windows Media Format, QASF
- Advanced Systems Format (ASF), QASF
- ASF (formato de sistemas avanzados), QASF
- metadatos, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ebb6afedfa00813e7447e5bcaefe1f251c02575
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488031"
---
# <a name="configuring-profiles-and-other-file-properties-qasf"></a><span data-ttu-id="ec631-116">Configuración de perfiles y otras propiedades de archivo (QASF)</span><span class="sxs-lookup"><span data-stu-id="ec631-116">Configuring Profiles and Other File Properties (QASF)</span></span>

<span data-ttu-id="ec631-117">En los elementos siguientes se describe cómo realizar varias tareas relacionadas con la creación de archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="ec631-117">The following items describe how to perform various tasks related to the creation of ASF files.</span></span>

## <a name="creating-a-profile-qasf"></a><span data-ttu-id="ec631-118">Creación de un perfil (QASF)</span><span class="sxs-lookup"><span data-stu-id="ec631-118">Creating a Profile (QASF)</span></span>

<span data-ttu-id="ec631-119">Para crear un perfil personalizado, use el SDK de Windows Media Format directamente para crear un objeto de administrador de perfiles mediante la función [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="ec631-119">To create a custom profile, use the Windows Media Format SDK directly to create a profile manager object by using the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span> <span data-ttu-id="ec631-120">A continuación, cree el perfil y páselo al escritor de [ASF de WM](wm-asf-writer-filter.md) mediante el método [**IConfigASFWriter:: ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="ec631-120">Next, create the profile, and pass it to the [WM ASF Writer](wm-asf-writer-filter.md) by using the [**IConfigASFWriter::ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) method.</span></span> <span data-ttu-id="ec631-121">Esta es la única manera de configurar el filtro con un perfil que use los códecs de la serie Windows Media Audio y vídeo 9.</span><span class="sxs-lookup"><span data-stu-id="ec631-121">This is the only way to configure the filter with a profile that uses the Windows Media Audio and Video 9 Series codecs.</span></span> <span data-ttu-id="ec631-122">Los perfiles de sistema para versiones anteriores de estos códecs se pueden agregar mediante el método [**IConfigASFWriter:: ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md) .</span><span class="sxs-lookup"><span data-stu-id="ec631-122">System profiles for earlier versions of these codecs can be added by using the [**IConfigASFWriter::ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md) method.</span></span>

## <a name="adding-metadata-qasf"></a><span data-ttu-id="ec631-123">Agregar metadatos (QASF)</span><span class="sxs-lookup"><span data-stu-id="ec631-123">Adding Metadata (QASF)</span></span>

<span data-ttu-id="ec631-124">Para agregar metadatos a un archivo, llame a **QueryInterface** desde la interfaz **IBASEFILTER** del [escritor ASF de WM](wm-asf-writer-filter.md) para recuperar la interfaz [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) .</span><span class="sxs-lookup"><span data-stu-id="ec631-124">To add metadata to a file, call **QueryInterface** from the **IBaseFilter** interface on the [WM ASF Writer](wm-asf-writer-filter.md) to retrieve the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface.</span></span> <span data-ttu-id="ec631-125">Una vez que se ha dado un perfil al filtro, use los métodos de la interfaz **IWMHeaderInfo** para escribir los metadatos.</span><span class="sxs-lookup"><span data-stu-id="ec631-125">After the filter has been given a profile, use the **IWMHeaderInfo** interface methods to write the metadata.</span></span>

## <a name="indexing-a-file-qasf"></a><span data-ttu-id="ec631-126">Indexación de un archivo (QASF)</span><span class="sxs-lookup"><span data-stu-id="ec631-126">Indexing a File (QASF)</span></span>

<span data-ttu-id="ec631-127">De manera predeterminada, el escritor ASF de WM crea archivos indizados de forma temporal.</span><span class="sxs-lookup"><span data-stu-id="ec631-127">The WM ASF Writer creates temporally indexed files by default.</span></span> <span data-ttu-id="ec631-128">Para crear un archivo indexado mediante Marcos, use el método [**IConfigAsfWriter:: SetIndexMode**](iconfigasfwriter-setindexmode.md) para deshabilitar toda la indexación y, a continuación, cree el archivo.</span><span class="sxs-lookup"><span data-stu-id="ec631-128">To create a frame-indexed file, use the [**IConfigAsfWriter::SetIndexMode**](iconfigasfwriter-setindexmode.md) method to disable all indexing, then create the file.</span></span> <span data-ttu-id="ec631-129">Cuando haya finalizado, use el SDK de Windows Media Format directamente para crear un índice basado en marco para el archivo.</span><span class="sxs-lookup"><span data-stu-id="ec631-129">When it is complete, use the Windows Media Format SDK directly to create a frame-based index for the file.</span></span>

## <a name="performing-two-pass-encoding-qasf"></a><span data-ttu-id="ec631-130">Realización de la codificación de Two-Pass (QASF)</span><span class="sxs-lookup"><span data-stu-id="ec631-130">Performing Two-Pass Encoding (QASF)</span></span>

<span data-ttu-id="ec631-131">La codificación de dos pasos solo se admite en códecs de Windows Media de la versión 8 y posteriores.</span><span class="sxs-lookup"><span data-stu-id="ec631-131">Two-pass encoding is supported only on Windows Media codecs of version 8 and later.</span></span> <span data-ttu-id="ec631-132">Coloque el escritor ASF de WM en modo de preprocesamiento llamando a [**IConfigAsfWriter2:: SetParam**](iconfigasfwriter2-setparam.md) y especificando AM \_ CONFIGASFWRITER \_ param \_ Multipass en el parámetro *DwParam* y **true** en el parámetro *dwParam1* .</span><span class="sxs-lookup"><span data-stu-id="ec631-132">Put the WM ASF Writer into preprocess mode by calling [**IConfigAsfWriter2::SetParam**](iconfigasfwriter2-setparam.md) and specifying AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS in the *dwParam* parameter and **TRUE** in the *dwParam1* parameter.</span></span>

<span data-ttu-id="ec631-133">A continuación, ejecute el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="ec631-133">Then run the filter graph.</span></span> <span data-ttu-id="ec631-134">Cuando se realizan todos los pasos de preprocesamiento (normalmente solo se realizará un paso de preprocesamiento), la aplicación recibirá un evento de **\_ \_ finalización de preprocesamiento de EC** del filtro.</span><span class="sxs-lookup"><span data-stu-id="ec631-134">When all the preprocessing passes are done (typically only one preprocessing pass will be performed), the application will receive an **EC\_PREPROCESS\_COMPLETE** event from the filter.</span></span> <span data-ttu-id="ec631-135">Cuando se reciba este evento, use **IMediaSeeking:: SetPositions** para restablecer el puntero de secuencia de nuevo al principio y vuelva a ejecutar el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="ec631-135">When this event is received, use **IMediaSeeking::SetPositions** to reset the stream pointer back to the beginning, and run the filter graph again.</span></span> <span data-ttu-id="ec631-136">Después del último paso (normalmente el segundo paso), la aplicación recibirá un evento de **\_ finalización de EC** para indicar que se ha completado el proceso de codificación.</span><span class="sxs-lookup"><span data-stu-id="ec631-136">After the last pass (typically the second pass), the application will receive an **EC\_COMPLETE** event to signify that the encoding process is complete.</span></span> <span data-ttu-id="ec631-137">Si se cancela un paso de preprocesamiento antes de que se reciba el evento de **\_ \_ finalización** previa al preprocesamiento, llame a [**IConfigAsfWriter2:: ResetMultiPassState**](iconfigasfwriter2-resetmultipassstate.md) para restablecer el filtro antes de intentar otra ejecución de preprocesamiento.</span><span class="sxs-lookup"><span data-stu-id="ec631-137">If a preprocessing pass is canceled before the **EC\_PREPROCESS\_COMPLETE** event is received, call [**IConfigAsfWriter2::ResetMultiPassState**](iconfigasfwriter2-resetmultipassstate.md) to reset the filter before attempting another preprocessing run.</span></span>

<span data-ttu-id="ec631-138">Solo es necesario llamar a **IConfigAsfWriter:: SetParam**(AM \_ CONFIGASFWRITER \_ param \_ Multipass, **false**) Si desea poner el filtro fuera del modo de preprocesamiento por completo.</span><span class="sxs-lookup"><span data-stu-id="ec631-138">It is only necessary to call **IConfigAsfWriter::SetParam**(AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS, **FALSE**) if you want to put the filter out of preprocessing mode completely.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ec631-139">Es responsabilidad de la aplicación habilitar el modo de preprocesamiento según el perfil que se usará para la codificación.</span><span class="sxs-lookup"><span data-stu-id="ec631-139">It is the application's responsibility to enable preprocessing mode based on the profile that will be used for encoding.</span></span> <span data-ttu-id="ec631-140">Algunos perfiles requieren codificación de dos pasos; Si intenta codificar un archivo con este tipo de perfil y no establece AM \_ CONFIGASFWRITER \_ param \_ Multipass en **true**, se producirá un error de USERABORT de EC \_ .</span><span class="sxs-lookup"><span data-stu-id="ec631-140">Some profiles require two-pass encoding; if you attempt to encode a file with such a profile, and do not set AM\_CONFIGASFWRITER\_PARAM\_MULTIPASS to **TRUE**, an EC\_USERABORT error will result.</span></span> <span data-ttu-id="ec631-141">Para obtener más información sobre cómo determinar si un perfil determinado requiere codificación de dos pasos, vea [usar la codificación de Two-Pass](using-two-pass-encoding.md) o [escribir secuencias de velocidad de bits variable](writing-variable-bit-rate-streams.md).</span><span class="sxs-lookup"><span data-stu-id="ec631-141">For more information on how to determine whether a given profile requires two-pass encoding, see [Using Two-Pass Encoding](using-two-pass-encoding.md) or [Writing Variable Bit Rate Streams](writing-variable-bit-rate-streams.md).</span></span>

 

## <a name="getting-and-setting-buffer-properties-at-run-time-qasf"></a><span data-ttu-id="ec631-142">Obtener y establecer propiedades de búfer en tiempo de ejecución (QASF)</span><span class="sxs-lookup"><span data-stu-id="ec631-142">Getting and Setting Buffer Properties at Run Time (QASF)</span></span>

<span data-ttu-id="ec631-143">En algunos escenarios, por ejemplo, si desea forzar la inserción de fotogramas clave al escribir un archivo, es posible que una aplicación necesite obtener o establecer información sobre un búfer de Windows Media en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="ec631-143">In some scenarios, for example if you want to force key-frame insertion when writing a file, an application may need to get or set information about a Windows Media buffer at run time.</span></span> <span data-ttu-id="ec631-144">Los filtros del [lector ASF de WM](wm-asf-reader-filter.md) y del [escritor ASF de WM](wm-asf-writer-filter.md) admiten un mecanismo de devolución de llamada que permite a una aplicación tener acceso a la interfaz [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) en cada búfer multimedia individual durante la lectura o escritura de archivos.</span><span class="sxs-lookup"><span data-stu-id="ec631-144">The [WM ASF Reader](wm-asf-reader-filter.md) and [WM ASF Writer](wm-asf-writer-filter.md) filters both support a callback mechanism that enables an application to access the [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface on each individual media buffer during file reading or file writing.</span></span> <span data-ttu-id="ec631-145">Las aplicaciones pueden usar esta interfaz para designar ejemplos específicos como fotogramas clave, o [*cleanpoints*](wmformat-glossary.md), para establecer códigos de tiempo de SMPTE, para especificar la configuración de entrelazado o para agregar cualquier tipo de datos privados a un flujo.</span><span class="sxs-lookup"><span data-stu-id="ec631-145">Applications can use this interface to designate specific samples as key frames, or [*cleanpoints*](wmformat-glossary.md), to set SMPTE time codes, to specify interlace settings, or add any type of private data to a stream.</span></span>

<span data-ttu-id="ec631-146">Use la interfaz [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass) para registrar las devoluciones de llamada del PIN que está controlando la secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ec631-146">Use the [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass) interface to register for callbacks from the pin that is handling the video stream.</span></span> <span data-ttu-id="ec631-147">Cuando el PIN llama al método [**IAMWMBufferPassCallback:: Notify**](iamwmbufferpasscallback-notify.md) , examine las marcas de tiempo en el búfer y, si es necesario, llame a [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) para establecer la propiedad de **WM \_ SampleExtensionGUID \_ OutputCleanPoint** en el búfer en **true**.</span><span class="sxs-lookup"><span data-stu-id="ec631-147">When the pin calls your [**IAMWMBufferPassCallback::Notify**](iamwmbufferpasscallback-notify.md) method, examine the time stamps on the buffer and, if appropriate, call [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) to set the **WM\_SampleExtensionGUID\_OutputCleanPoint** property on the buffer to **TRUE**.</span></span>

## <a name="non-square-pixel-support-qasf"></a><span data-ttu-id="ec631-148">Compatibilidad con píxeles no cuadrados (QASF)</span><span class="sxs-lookup"><span data-stu-id="ec631-148">Non-Square Pixel Support (QASF)</span></span>

<span data-ttu-id="ec631-149">El escritor ASF de WM se conecta a un filtro de nivel superior, como el descodificador DV, que genera información de relación de aspecto de píxeles.</span><span class="sxs-lookup"><span data-stu-id="ec631-149">The WM ASF Writer connects to an upstream filter, such as the DV Decoder, that outputs pixel aspect ratio information.</span></span> <span data-ttu-id="ec631-150">El escritor ASF de WM escribirá esta información como extensiones de unidad de datos para cada muestra del archivo.</span><span class="sxs-lookup"><span data-stu-id="ec631-150">The WM ASF Writer will write this information as data unit extensions for every sample in the file.</span></span>

<span data-ttu-id="ec631-151">Cuando el lector ASF de WM encuentra información de relación de aspecto de píxeles en el encabezado de archivo o en las extensiones de unidad de datos para los ejemplos, ofrecerá un tipo de medio **VIDEOINFOHEADER2** como primera opción en el PIN de salida.</span><span class="sxs-lookup"><span data-stu-id="ec631-151">When the WM ASF Reader encounters pixel aspect ratio information in the file header or in data unit extensions for the samples, it will offer a **VIDEOINFOHEADER2** media type as a first choice on its output pin.</span></span> <span data-ttu-id="ec631-152">Los miembros **dwPictAspectRatioX** y **dwPictAspectRatioY** de la estructura, que describen la relación de aspecto del rectángulo de vídeo, se ajustarán correctamente para tener en cuenta la relación de aspecto de píxeles.</span><span class="sxs-lookup"><span data-stu-id="ec631-152">The **dwPictAspectRatioX** and **dwPictAspectRatioY** members of the structure, which describe the video rectangle's aspect ratio, will be correctly adjusted to account for the pixel aspect ratio.</span></span>

## <a name="maintaining-interlaced-format"></a><span data-ttu-id="ec631-153">Mantener el formato entrelazado</span><span class="sxs-lookup"><span data-stu-id="ec631-153">Maintaining Interlaced Format</span></span>

<span data-ttu-id="ec631-154">Si captura vídeo entrelazado de una cámara de televisión o DV, es posible que desee conservar el vídeo original como campos independientes si espera que el archivo codificado se reproduzca en un televisor u otro dispositivo de pantalla entrelazada.</span><span class="sxs-lookup"><span data-stu-id="ec631-154">If you capture interlaced video from a television or a DV camera, you might wish to preserve the original video as independent fields if you expect the encoded file to be played back on a television or other interlaced display device.</span></span> <span data-ttu-id="ec631-155">(Los monitores de equipos son dispositivos de digitalización progresiva). Si desentrelaza un vídeo y, a continuación, lo reentrelaza para su reproducción en un televisor, se producirá una pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="ec631-155">(Computer monitors are progressive scanning devices.) If you deinterlace a video, and then reinterlace it for playback on a television, some loss of data will be incurred.</span></span> <span data-ttu-id="ec631-156">En un archivo ASF, la información de entrelazado se almacena como extensiones de unidad de datos que la aplicación aplica a cada ejemplo mediante el método **IAMWMBufferPassCallback** descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ec631-156">In an ASF file, interlacing information is stored as data unit extensions that the application applies to each sample using the **IAMWMBufferPassCallback** method described previously.</span></span> <span data-ttu-id="ec631-157">Para codificar un archivo que conserva la configuración de entrelazado original, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="ec631-157">To encode a file that preserves the original interlace settings, follow these steps:</span></span>

-   <span data-ttu-id="ec631-158">Implemente una clase que admita **IAMWMBufferPassCallback** y escriba una función Notify que establezca las marcas de entrelazado para cada ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ec631-158">Implement a class that supports **IAMWMBufferPassCallback** and write a Notify function that sets the interlace flags for each sample.</span></span> <span data-ttu-id="ec631-159">El escritor ASF de WM llamará a esta función antes de procesar cada ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ec631-159">This function will be called by the WM ASF Writer before it processes each sample.</span></span>


```C++
// Set to WM_CT_TOP_FIELD_FIRST if that is your format.
BYTE flag = WM_CT_INTERLACED | WM_CT_BOTTOM_FIELD_FIRST;
            HRESULT hr = pNSSBuffer3->SetProperty(WM_SampleExtensionGUID_ContentType, (void*) &flag, WM_SampleExtension_ContentType_Size);
           
```



-   <span data-ttu-id="ec631-160">Establezca las extensiones de unidad de datos en el perfil antes de pasar el perfil al filtro.</span><span class="sxs-lookup"><span data-stu-id="ec631-160">Set the data unit extensions on the profile before you pass the profile to the filter.</span></span>


```C++
hr = pWMStreamConfig2->AddDataUnitExtension( WM_SampleExtensionGUID_ContentType, WM_SampleExtension_ContentType_Size, NULL, 0 );
```



-   <span data-ttu-id="ec631-161">Después de configurar el filtro con el perfil, obtenga la interfaz **IWMWriterAdvanced2** del escritor ASF de WM y llame al método **SetInputSettings** .</span><span class="sxs-lookup"><span data-stu-id="ec631-161">After you configure the filter with the profile, obtain the **IWMWriterAdvanced2** interface from the WM ASF Writer and call the **SetInputSettings** method.</span></span>

`// Must do this first.`

`hr = pConfigAsfWriter2->ConfigureFilterUsingProfile(pProfile);`


```C++
  
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



 

 