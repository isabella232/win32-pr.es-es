---
title: Trabajar con High-Resolution PCM audio
description: Trabajar con High-Resolution PCM audio
ms.assetid: 422a78f9-0f43-4edb-acaf-7f6e3f4a1cb8
keywords:
- Advanced Systems Format (ASF), audio PCM de alta resolución
- ASF (formato de sistemas avanzados), audio PCM de alta resolución
- perfiles, audio PCM de alta resolución
- códecs, audio PCM de alta resolución
- Advanced Systems Format (ASF), PCM audio
- ASF (formato de sistemas avanzados), audio PCM
- perfiles, audio PCM
- códecs, audio PCM
- audio PCM de alta resolución
- Audio PCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73a45904072307e915065ba3a5946d5ef774c73b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995370"
---
# <a name="working-with-high-resolution-pcm-audio"></a><span data-ttu-id="b93e3-113">Trabajar con High-Resolution PCM audio</span><span class="sxs-lookup"><span data-stu-id="b93e3-113">Working with High-Resolution PCM Audio</span></span>

<span data-ttu-id="b93e3-114">Algunos de los formatos de entrada para el códec Windows Media Audio 9 Professional y el códec Windows Media Audio 9 Lossless son formatos PCM de alta resolución.</span><span class="sxs-lookup"><span data-stu-id="b93e3-114">Some of the input formats for the Windows Media Audio 9 Professional codec and the Windows Media Audio 9 Lossless codec are high-resolution PCM formats.</span></span> <span data-ttu-id="b93e3-115">Se trata de formatos PCM que tienen más de dos canales o más de 16 bits por muestra (el audio con más de dos canales también se denomina audio multicanal).</span><span class="sxs-lookup"><span data-stu-id="b93e3-115">These are PCM formats that have more than two channels, or more than 16 bits per sample (audio with more than two channels is also called multichannel audio).</span></span>

<span data-ttu-id="b93e3-116">Estos formatos se configuran mediante una extensión estructurada de la estructura [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) , denominada [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b93e3-116">These formats are configured by using a structured extension of the [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) structure, called [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)).</span></span> <span data-ttu-id="b93e3-117">La estructura **WAVEFORMATEXTENSIBLE** incluye información sobre los canales incluidos en el audio.</span><span class="sxs-lookup"><span data-stu-id="b93e3-117">The **WAVEFORMATEXTENSIBLE** structure includes information about the channels included in the audio.</span></span> <span data-ttu-id="b93e3-118">Esta estructura es necesaria cuando se usa audio PCM de alta resolución, ya que algunas API de Windows no aceptarán estructuras **WAVEFORMATEX** que contengan valores de alta resolución.</span><span class="sxs-lookup"><span data-stu-id="b93e3-118">This structure is required when using high-resolution PCM audio, because some Windows APIs will not accept **WAVEFORMATEX** structures that contain high-resolution values.</span></span>

<span data-ttu-id="b93e3-119">Los formatos PCM de alta resolución tienen 22 bytes de datos extendidos, que se especifican en el miembro **cbSize** de la estructura **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="b93e3-119">High-resolution PCM formats have 22 bytes of extended data, which is specified in the **cbSize** member of the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="b93e3-120">Los formatos de audio de Windows Media de alta resolución no usan la estructura **WAVEFORMATEXTENSIBLE** , pero tienen datos extendidos anexados a la estructura **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="b93e3-120">High-resolution Windows Media audio formats do not use the **WAVEFORMATEXTENSIBLE** structure, but do have extended data appended to the **WAVEFORMATEX** structure.</span></span>

<span data-ttu-id="b93e3-121">Los códecs de audio de Windows Media solo admiten la descodificación de formatos PCM de alta resolución cuando la aplicación se ejecuta en Windows XP o posterior.</span><span class="sxs-lookup"><span data-stu-id="b93e3-121">The Windows Media audio codecs only support decoding to high-resolution PCM formats when the application is running on Windows XP or later.</span></span> <span data-ttu-id="b93e3-122">En versiones anteriores de Microsoft Windows, los códecs se descodifican en un formato con un máximo de 16 bits por muestra y 2 canales.</span><span class="sxs-lookup"><span data-stu-id="b93e3-122">On previous versions of Microsoft Windows, the codecs decode to a format with a maximum of 16 bits per sample and 2 channels.</span></span> <span data-ttu-id="b93e3-123">Además, debe especificar que desea que el códec descodifique en PCM de alta definición estableciendo el \_ valor de salida g wszEnableDiscreteOutput en **true** mediante el método [**IWMReaderAdvanced2:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) .</span><span class="sxs-lookup"><span data-stu-id="b93e3-123">In addition, you must specify that you want the codec to decode to high-definition PCM by setting the g\_wszEnableDiscreteOutput output setting to **TRUE** using the [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) method.</span></span> <span data-ttu-id="b93e3-124">Después de efectuar esta llamada, las salidas enumeradas por el lector incluirán formatos de alta definición.</span><span class="sxs-lookup"><span data-stu-id="b93e3-124">After making this call, the outputs enumerated by the reader will include high-definition formats.</span></span>

<span data-ttu-id="b93e3-125">El audio multicanal requiere más configuración.</span><span class="sxs-lookup"><span data-stu-id="b93e3-125">Multichannel audio requires more configuration.</span></span> <span data-ttu-id="b93e3-126">Para obtener más información, consulte [lectura de audio multicanal](reading-multichannel-audio.md).</span><span class="sxs-lookup"><span data-stu-id="b93e3-126">For more information, see [Reading Multichannel Audio](reading-multichannel-audio.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b93e3-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b93e3-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b93e3-128">**Trabajar con entradas**</span><span class="sxs-lookup"><span data-stu-id="b93e3-128">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> </dl>

 

 