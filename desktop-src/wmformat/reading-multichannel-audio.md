---
title: Lectura de audio multicanal
description: Lectura de audio multicanal
ms.assetid: 9d577c5c-7275-493e-8a77-318c264b59b3
keywords:
- SDK de Windows Media Format, lectura de audio multicanal
- Advanced Systems Format (ASF), lectura de audio multicanal
- ASF (formato de sistemas avanzados), lectura de audio multicanal
- Advanced Systems Format (ASF), audio multicanal
- ASF (formato de sistemas avanzados), audio multicanal
- códecs, leer audio multicanal
- audio multicanal, lectura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59da950eb4218ad87995ed80e22de4de302f8e42
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793240"
---
# <a name="reading-multichannel-audio"></a><span data-ttu-id="549c0-110">Lectura de audio multicanal</span><span class="sxs-lookup"><span data-stu-id="549c0-110">Reading Multichannel Audio</span></span>

<span data-ttu-id="549c0-111">El códec Windows Media Audio 9 Professional puede codificar audio multicanal (más de dos canales).</span><span class="sxs-lookup"><span data-stu-id="549c0-111">The Windows Media Audio 9 Professional codec can encode multichannel audio (more than two channels).</span></span> <span data-ttu-id="549c0-112">Al leer un archivo con audio multicanal, debe configurar el resultado correctamente o el audio se entregará con una calidad inferior y en estéreo.</span><span class="sxs-lookup"><span data-stu-id="549c0-112">When reading a file with multichannel audio, you must configure the output properly or the audio will be delivered at a lower quality and in stereo.</span></span> <span data-ttu-id="549c0-113">Para establecer una salida para la entrega de audio multicanal, debe establecer dos configuraciones de salida: g \_ wszEnableDiscreteOutput y g \_ wszSpeakerConfig.</span><span class="sxs-lookup"><span data-stu-id="549c0-113">To set an output for multichannel audio delivery, you must set two output settings: g\_wszEnableDiscreteOutput and g\_wszSpeakerConfig.</span></span>

<span data-ttu-id="549c0-114">Al establecer g \_ wszEnableDiscreteOutput en **true** , se establece el códec para proporcionar una salida de audio de alta definición.</span><span class="sxs-lookup"><span data-stu-id="549c0-114">Setting g\_wszEnableDiscreteOutput to **TRUE** sets the codec to deliver high-definition audio output.</span></span> <span data-ttu-id="549c0-115">El códec de Windows Media Audio 9 codifica el audio de alta definición con ejemplos de 24 bits en estéreo o en varios canales.</span><span class="sxs-lookup"><span data-stu-id="549c0-115">High-definition audio is encoded by the Windows Media Audio 9 codec with 24-bit samples in stereo or multiple channels.</span></span> <span data-ttu-id="549c0-116">Si este valor es **false**, solo se entregará la salida estéreo de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="549c0-116">If this setting is **FALSE**, only 16-bit stereo output will be delivered.</span></span>

<span data-ttu-id="549c0-117">El número de oradores en el equipo que se está configurando está establecido con g \_ wszSpeakerConfig.</span><span class="sxs-lookup"><span data-stu-id="549c0-117">The number of speakers on the playing computer is set with g\_wszSpeakerConfig.</span></span> <span data-ttu-id="549c0-118">Esta opción es un valor **DWORD** establecido en una de las constantes de altavoz de DirectSound que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="549c0-118">This setting is a **DWORD** value set to one of the DirectSound speaker constants listed in the following table.</span></span> <span data-ttu-id="549c0-119">Para resolver estos nombres de constantes para el compilador, debe incluir dsound. h.</span><span class="sxs-lookup"><span data-stu-id="549c0-119">To resolve these constant names for your compiler, you must include dsound.h.</span></span>



| <span data-ttu-id="549c0-120">Constante</span><span class="sxs-lookup"><span data-stu-id="549c0-120">Constant</span></span>             | <span data-ttu-id="549c0-121">Value</span><span class="sxs-lookup"><span data-stu-id="549c0-121">Value</span></span>      | <span data-ttu-id="549c0-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="549c0-122">Description</span></span>                                                                  |
|----------------------|------------|------------------------------------------------------------------------------|
| <span data-ttu-id="549c0-123">DSSPEAKER \_ DIRECTOUT</span><span class="sxs-lookup"><span data-stu-id="549c0-123">DSSPEAKER\_DIRECTOUT</span></span> | <span data-ttu-id="549c0-124">0x00000000</span><span class="sxs-lookup"><span data-stu-id="549c0-124">0x00000000</span></span> | <span data-ttu-id="549c0-125">El audio se pasa directamente, sin tener que configurarse para los altavoces.</span><span class="sxs-lookup"><span data-stu-id="549c0-125">The audio is passed through directly, without being configured for speakers.</span></span> |
| <span data-ttu-id="549c0-126">\_auriculares DSSPEAKER</span><span class="sxs-lookup"><span data-stu-id="549c0-126">DSSPEAKER\_HEADPHONE</span></span> | <span data-ttu-id="549c0-127">0x00000001</span><span class="sxs-lookup"><span data-stu-id="549c0-127">0x00000001</span></span> | <span data-ttu-id="549c0-128">El equipo cliente está equipado con auriculares.</span><span class="sxs-lookup"><span data-stu-id="549c0-128">The client computer is equipped with headphones.</span></span>                             |
| <span data-ttu-id="549c0-129">\_mono DSSPEAKER</span><span class="sxs-lookup"><span data-stu-id="549c0-129">DSSPEAKER\_MONO</span></span>      | <span data-ttu-id="549c0-130">0x00000002</span><span class="sxs-lookup"><span data-stu-id="549c0-130">0x00000002</span></span> | <span data-ttu-id="549c0-131">El equipo cliente está equipado con un altavoz monoaural.</span><span class="sxs-lookup"><span data-stu-id="549c0-131">The client computer is equipped with a monaural speaker.</span></span>                     |
| <span data-ttu-id="549c0-132">DSSPEAKER \_ cuádruple</span><span class="sxs-lookup"><span data-stu-id="549c0-132">DSSPEAKER\_QUAD</span></span>      | <span data-ttu-id="549c0-133">0x00000003</span><span class="sxs-lookup"><span data-stu-id="549c0-133">0x00000003</span></span> | <span data-ttu-id="549c0-134">El equipo cliente está equipado con altavoces quadraphonic.</span><span class="sxs-lookup"><span data-stu-id="549c0-134">The client computer is equipped with quadraphonic speakers.</span></span>                  |
| <span data-ttu-id="549c0-135">\_estéreo DSSPEAKER</span><span class="sxs-lookup"><span data-stu-id="549c0-135">DSSPEAKER\_STEREO</span></span>    | <span data-ttu-id="549c0-136">0x00000004</span><span class="sxs-lookup"><span data-stu-id="549c0-136">0x00000004</span></span> | <span data-ttu-id="549c0-137">El equipo cliente está equipado con altavoces estéreo.</span><span class="sxs-lookup"><span data-stu-id="549c0-137">The client computer is equipped with stereo speakers.</span></span>                        |
| <span data-ttu-id="549c0-138">\_envolvente DSSPEAKER</span><span class="sxs-lookup"><span data-stu-id="549c0-138">DSSPEAKER\_SURROUND</span></span>  | <span data-ttu-id="549c0-139">0x00000005</span><span class="sxs-lookup"><span data-stu-id="549c0-139">0x00000005</span></span> | <span data-ttu-id="549c0-140">El equipo cliente está equipado con altavoces con sonido envolvente de cuatro canales.</span><span class="sxs-lookup"><span data-stu-id="549c0-140">The client computer is equipped with four-channel surround-sound speakers.</span></span>   |
| <span data-ttu-id="549c0-141">DSSPEAKER \_ 5POINT1</span><span class="sxs-lookup"><span data-stu-id="549c0-141">DSSPEAKER\_5POINT1</span></span>   | <span data-ttu-id="549c0-142">0x00000006</span><span class="sxs-lookup"><span data-stu-id="549c0-142">0x00000006</span></span> | <span data-ttu-id="549c0-143">El equipo cliente está equipado con cinco altavoces y un subwoofer.</span><span class="sxs-lookup"><span data-stu-id="549c0-143">The client computer is equipped with five speakers and a subwoofer.</span></span>          |
| <span data-ttu-id="549c0-144">DSSPEAKER \_ 7POINT1</span><span class="sxs-lookup"><span data-stu-id="549c0-144">DSSPEAKER\_7POINT1</span></span>   | <span data-ttu-id="549c0-145">0x00000007</span><span class="sxs-lookup"><span data-stu-id="549c0-145">0x00000007</span></span> | <span data-ttu-id="549c0-146">El equipo cliente está equipado con siete altavoces y un subwoofer.</span><span class="sxs-lookup"><span data-stu-id="549c0-146">The client computer is equipped with seven speakers and a subwoofer.</span></span>         |



 

<span data-ttu-id="549c0-147">Para establecer esta configuración, use [**IWMReaderAdvanced2:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting).</span><span class="sxs-lookup"><span data-stu-id="549c0-147">To set these settings, use [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting).</span></span>

<span data-ttu-id="549c0-148">Por último, para que los canales se generen de manera discreta y no se despliegan en estéreo, debe establecer el tipo de medio correcto en la salida siguiendo estos pasos:</span><span class="sxs-lookup"><span data-stu-id="549c0-148">Finally, for the channels to be output discretely, with no fold-down to stereo, you must set the correct media type on the output by following these steps:</span></span>

1.  <span data-ttu-id="549c0-149">Llame a [**IWMReader:: GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) para obtener el número de formatos admitidos para la salida de audio pertinente.</span><span class="sxs-lookup"><span data-stu-id="549c0-149">Call [**IWMReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) to get the number of supported formats for the relevant audio output.</span></span> <span data-ttu-id="549c0-150">Los índices de formato de salida son de base cero.</span><span class="sxs-lookup"><span data-stu-id="549c0-150">Output format indexes are zero-based.</span></span>
2.  <span data-ttu-id="549c0-151">Para cada formato admitido, llame a [**IWMReader:: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) para recuperar la interfaz [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) en el objeto de propiedades de los medios de salida.</span><span class="sxs-lookup"><span data-stu-id="549c0-151">For each supported format, call [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) to retrieve the [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) interface on the output media properties object.</span></span>
3.  <span data-ttu-id="549c0-152">Llame a [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype) para recuperar el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="549c0-152">Call [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype) to retrieve the media type.</span></span>
4.  <span data-ttu-id="549c0-153">Si el tipo de medio recuperado es el tipo multicanal deseado, establézcalo llamando a [**IWMReader:: SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops).</span><span class="sxs-lookup"><span data-stu-id="549c0-153">If the retrieved media type is the desired multichannel type, then set it by calling [**IWMReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops).</span></span>

<span data-ttu-id="549c0-154">Una vez que haya establecido la salida discreta y la configuración de los altavoces, los formatos de salida enumerados por el lector deben incluir formatos multicanal que utilicen la estructura [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="549c0-154">After you have set discrete output and the speaker configuration, the output formats enumerated by the reader should include multichannel formats that use the [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)) structure.</span></span> <span data-ttu-id="549c0-155">Si enumera los formatos de salida antes de establecer las propiedades, se incluirán solo los formatos con 1 o 2 canales y un máximo de 16 bits por canal.</span><span class="sxs-lookup"><span data-stu-id="549c0-155">If you enumerate the output formats before setting the properties, only formats with 1 or 2 channels and a maximum of 16 bits per channel will be included.</span></span> <span data-ttu-id="549c0-156">Al igual que con otros formatos de audio, solo debe usar los formatos enumerados por el lector; no configure el suyo propio.</span><span class="sxs-lookup"><span data-stu-id="549c0-156">As with other audio formats, you should use only the formats enumerated by the reader; do not configure your own.</span></span>

> [!Note]  
> <span data-ttu-id="549c0-157">Puede generar audio multicanal solo si la aplicación se ejecuta en Microsoft Windows XP o en una versión posterior de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="549c0-157">You can output multichannel audio only if your application is running on Microsoft Windows XP or a later version of Microsoft Windows.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="549c0-158">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="549c0-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="549c0-159">**Entradas, secuencias y salidas**</span><span class="sxs-lookup"><span data-stu-id="549c0-159">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="549c0-160">**Leer archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="549c0-160">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="549c0-161">**Configuración de salida**</span><span class="sxs-lookup"><span data-stu-id="549c0-161">**Output Settings**</span></span>](output-settings.md)
</dt> <dt>

[<span data-ttu-id="549c0-162">**Trabajar con High-Resolution PCM audio**</span><span class="sxs-lookup"><span data-stu-id="549c0-162">**Working with High-Resolution PCM Audio**</span></span>](working-with-high-resolution-pcm-audio.md)
</dt> </dl>

 

 