---
title: Configuración del escritor ASF de WM (QASF)
description: Configuración del escritor ASF de WM (QASF)
ms.assetid: 0f49ed5a-c228-456a-9551-8d277adccd0e
keywords:
- Windows Media Format SDK, configurar WM ASF Writer (QASF)
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, WM ASF Writer
- SDK de Windows Media Format, QASF
- Advanced Systems Format (ASF), configurar WM ASF Writer (QASF)
- ASF (Advanced Systems Format), configurar WM ASF Writer (QASF)
- Advanced Systems Format (ASF), WM ASF Writer
- ASF (formato de sistemas avanzados), escritor ASF de WM
- Advanced Systems Format (ASF), DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- Advanced Systems Format (ASF), QASF
- ASF (formato de sistemas avanzados), QASF
- DirectShow, configuración de WM ASF Writer (QASF)
- DirectShow, escritor ASF de WM
- DirectShow, QASF
- Escritor ASF de WM, configurar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72f954522c4acae89e6f6dd001561811088c2a9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149527"
---
# <a name="configuring-the-wm-asf-writer-qasf"></a><span data-ttu-id="b810b-119">Configuración del escritor ASF de WM (QASF)</span><span class="sxs-lookup"><span data-stu-id="b810b-119">Configuring the WM ASF Writer (QASF)</span></span>

<span data-ttu-id="b810b-120">Cuando se crea el filtro de [escritura ASF de WM](wm-asf-writer-filter.md) , se configura automáticamente con el \_ perfil WMProfile V80 \_ 256Video como valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b810b-120">When the [WM ASF Writer](wm-asf-writer-filter.md) filter is created, it is configured automatically with the WMProfile\_V80\_256Video profile as a default.</span></span> <span data-ttu-id="b810b-121">Dado que este perfil usa los códecs Windows Media Audio y Windows Media Video versión 8, se recomienda crear un perfil personalizado que use los códecs de la serie Windows Media 9 y, a continuación, pasar su puntero [**IWMProfile**](iwmprofile.md) al filtro mediante el método [**IConfigAsfWriter:: ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="b810b-121">Because this profile uses the Windows Media Audio and Windows Media Video version 8 codecs, it is recommended that you create a custom profile that uses the Windows Media 9 Series codecs, and then pass its [**IWMProfile**](iwmprofile.md) pointer to the filter using the [**IConfigAsfWriter::ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) method.</span></span> <span data-ttu-id="b810b-122">El filtro debe agregarse al gráfico antes de que se pueda configurar el filtro y debe configurarse antes de que se pueda conectar a los filtros de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="b810b-122">The filter must be added to the graph before the filter can be configured, and it must be configured before it can be connected to upstream filters.</span></span> <span data-ttu-id="b810b-123">El filtro usa el perfil para determinar el tipo de archivo de formato de Windows Media que se va a escribir, el número de clavijas de entrada que se configurarán y los tipos de medios que los pin pueden aceptar.</span><span class="sxs-lookup"><span data-stu-id="b810b-123">The filter uses the profile to determine what kind of Windows Media Format file to write, how many input pins to set up, and what media types the pins can accept.</span></span>

<span data-ttu-id="b810b-124">El filtro permite restablecer los perfiles mientras se conectan sus clavijas de entrada, siempre que el nuevo perfil no requiera ninguna clavija de entrada adicional.</span><span class="sxs-lookup"><span data-stu-id="b810b-124">The filter allows profiles to be reset while its input pins are connected, as long as the new profile does not require any additional input pins.</span></span> <span data-ttu-id="b810b-125">Por ejemplo, si cambia el perfil de un perfil de sólo audio de una entrada a un perfil de audio y vídeo de dos entradas, solo el PIN de audio será reconnectedAll los datos de entrada deben estar marcados con el tiempo y todos los pin de entrada deben estar conectados para poder ejecutar o pausar el filtro.</span><span class="sxs-lookup"><span data-stu-id="b810b-125">For example, if you change the profile from a one-input audio-only profile to a two-input audio and video profile, just the audio pin will be reconnectedAll input data must be time-stamped, and all input pins must be connected before the filter can be run or paused.</span></span> <span data-ttu-id="b810b-126">Esto significa que si configura el filtro con un perfil que tiene una secuencia de audio y una secuencia de vídeo, el filtro creará un PIN de entrada de audio y vídeo, y ambos PIN deben estar conectados para poder ejecutar el filtro.</span><span class="sxs-lookup"><span data-stu-id="b810b-126">This means that if you configure the filter with a profile that has an audio stream and a video stream, the filter will create an audio and a video input pin, and both pins must be connected before the filter can be run.</span></span>

<span data-ttu-id="b810b-127">Agregar extensiones de unidad de datos</span><span class="sxs-lookup"><span data-stu-id="b810b-127">Adding Data Unit Extensions</span></span>

<span data-ttu-id="b810b-128">Puede configurar una secuencia de perfil para las extensiones de unidad de datos, como los códigos de tiempo SMPTE, antes o después de que se conecte el filtro, siempre que siga este orden de operaciones:</span><span class="sxs-lookup"><span data-stu-id="b810b-128">You can configure a profile stream for data unit extensions, such as SMPTE time codes, either before or after the filter is connected, as long as you follow this order of operations:</span></span>

1.  <span data-ttu-id="b810b-129">Agregue una o más extensiones de unidad de datos a la secuencia mediante [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension).</span><span class="sxs-lookup"><span data-stu-id="b810b-129">Add one or more data unit extensions to the stream using [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension).</span></span>
2.  <span data-ttu-id="b810b-130">Llame a [**WMProfile:: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) para actualizar el perfil.</span><span class="sxs-lookup"><span data-stu-id="b810b-130">Call [**WMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) to update the profile.</span></span>
3.  <span data-ttu-id="b810b-131">Llame a [**IConfigAsfWriter:: ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) con el objeto de perfil actualizado.</span><span class="sxs-lookup"><span data-stu-id="b810b-131">Call [**IConfigAsfWriter::ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) with the updated profile object.</span></span>
4.  <span data-ttu-id="b810b-132">Busque el PIN de entrada de vídeo y llame a su método [**IAMWMBufferPass:: SetNotify**](iamwmbufferpass-setnotify.md) para registrar la interfaz [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b810b-132">Find the video input pin, and call its [**IAMWMBufferPass::SetNotify**](iamwmbufferpass-setnotify.md) method to register your application-defined [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) interface.</span></span>

<span data-ttu-id="b810b-133">Cuando se ejecute el gráfico, se llamará al método [**IAMWMBufferPassCallback:: Notify**](iamwmbufferpasscallback-notify.md) para cada fotograma y podrá obtener y establecer propiedades en el ejemplo mediante sus métodos de interfaz [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) .</span><span class="sxs-lookup"><span data-stu-id="b810b-133">When the graph runs, your [**IAMWMBufferPassCallback::Notify**](iamwmbufferpasscallback-notify.md) method will be called for each frame, and you will be able to get and set properties on the sample using its [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface methods.</span></span>

> [!Note]  
> <span data-ttu-id="b810b-134">En algunos escenarios de uso intensivo del procesador, como el Telecine inverso, el escritor ASF de WM puede requerir más búferes de salida de los que pueden admitir algunos filtros de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="b810b-134">In some processor-intensive scenarios such as inverse telecine, the WM ASF Writer may require more output buffers than some downstream filters can support.</span></span> <span data-ttu-id="b810b-135">Por ejemplo, el descodificador de DV no aceptará más de un búfer para su PIN de salida y se aplica lo mismo para el descompresor de AVI en determinadas condiciones.</span><span class="sxs-lookup"><span data-stu-id="b810b-135">The DV Decoder, for example, will not accept more than one buffer for its output pin and the same is true for the AVI Decompressor in certain conditions.</span></span> <span data-ttu-id="b810b-136">Si surgen problemas al intentar conectarse a estos filtros o, posiblemente, al ejecutar el gráfico, puede que sea necesario escribir un filtro intermediario que acepte cualquier número de búferes en su PIN de salida.</span><span class="sxs-lookup"><span data-stu-id="b810b-136">If you encounter problems when attempting to connect to these filters, or possibly when running the graph, it may be necessary to write an intermediary filter that accepts any number of buffers on its output pin.</span></span>

 

 

 