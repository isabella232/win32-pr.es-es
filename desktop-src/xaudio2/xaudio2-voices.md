---
description: 'Hay tres tipos de objetos de voz de XAudio2: voces de origen, submezcla y maestra.'
ms.assetid: 3a4acc03-e47a-ff33-dee8-a374051f85f6
title: Voces de XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b11300cea770f59485e8a78b0d30110b5469befe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707123"
---
# <a name="xaudio2-voices"></a><span data-ttu-id="98a99-103">Voces de XAudio2</span><span class="sxs-lookup"><span data-stu-id="98a99-103">XAudio2 Voices</span></span>

<span data-ttu-id="98a99-104">Hay tres tipos de objetos de voz de XAudio2: voces de *origen*, *submezcla* y *maestra* .</span><span class="sxs-lookup"><span data-stu-id="98a99-104">There are three types of XAudio2 voice objects: *source*, *submix*, and *mastering* voices.</span></span> <span data-ttu-id="98a99-105">Las voces de origen operan en datos de audio proporcionados por el cliente.</span><span class="sxs-lookup"><span data-stu-id="98a99-105">Source voices operate on audio data provided by the client.</span></span> <span data-ttu-id="98a99-106">Las voces de origen y de submezcla envían su resultado a una o más voces de submezcla o de procesamiento.</span><span class="sxs-lookup"><span data-stu-id="98a99-106">Source and submix voices send their output to one or more submix or mastering voices.</span></span> <span data-ttu-id="98a99-107">Las voces de submezcla y de procesamiento mezclan el audio de todas las voces que les alimentan y trabajan con el resultado.</span><span class="sxs-lookup"><span data-stu-id="98a99-107">Submix and mastering voices mix the audio from all voices feeding them, and operate on the result.</span></span> <span data-ttu-id="98a99-108">Las voces de procesamiento escriben datos de audio en un dispositivo de audio.</span><span class="sxs-lookup"><span data-stu-id="98a99-108">Mastering voices write audio data to an audio device.</span></span>

## <a name="actions-performed-by-all-voices"></a><span data-ttu-id="98a99-109">Acciones realizadas por todas las voces</span><span class="sxs-lookup"><span data-stu-id="98a99-109">Actions Performed by All Voices</span></span>

<span data-ttu-id="98a99-110">Todas las voces realizan las siguientes acciones por orden en el audio que viaja.</span><span class="sxs-lookup"><span data-stu-id="98a99-110">All voices perform the following actions in order on the audio that travels though them.</span></span>

1.  <span data-ttu-id="98a99-111">Ajuste general del volumen, que afecta a todos los canales de audio.</span><span class="sxs-lookup"><span data-stu-id="98a99-111">Overall volume adjustment, affecting all audio channels.</span></span> <span data-ttu-id="98a99-112">Vea [**IXAudio2Voice:: SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume).</span><span class="sxs-lookup"><span data-stu-id="98a99-112">See [**IXAudio2Voice::SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume).</span></span>
2.  <span data-ttu-id="98a99-113">Cadena opcional especificada por el cliente de uno o más efectos de DSP, como la reverberación integrada o un efecto de usuario definido por la interfaz [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) .</span><span class="sxs-lookup"><span data-stu-id="98a99-113">An optional client-specified chain of one or more DSP effects, such as the built-in reverb or a user effect defined by the [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) interface.</span></span> <span data-ttu-id="98a99-114">Consulte [efectos de audio de XAudio2](xaudio2-audio-effects.md).</span><span class="sxs-lookup"><span data-stu-id="98a99-114">See [XAudio2 Audio Effects](xaudio2-audio-effects.md).</span></span>
3.  <span data-ttu-id="98a99-115">Ajuste del volumen de salida por canal.</span><span class="sxs-lookup"><span data-stu-id="98a99-115">Per-channel output volume adjustment.</span></span> <span data-ttu-id="98a99-116">Vea [**IXAudio2Voice:: SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes).</span><span class="sxs-lookup"><span data-stu-id="98a99-116">See [**IXAudio2Voice::SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes).</span></span>
4.  <span data-ttu-id="98a99-117">Combinación de matriz independiente en cada una de las voces de destino o en el dispositivo de salida de audio para la maestra de voces.</span><span class="sxs-lookup"><span data-stu-id="98a99-117">Separate matrix mix to each of the destination voices or to the audio output device for mastering voices.</span></span> <span data-ttu-id="98a99-118">Esta mezcla cambia el número de canales en el audio, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="98a99-118">This mix changes the number of channels in the audio, if necessary.</span></span>

## <a name="source-voices"></a><span data-ttu-id="98a99-119">Voces de origen</span><span class="sxs-lookup"><span data-stu-id="98a99-119">Source Voices</span></span>

<span data-ttu-id="98a99-120">Use las voces de origen para enviar datos de audio a la canalización de procesamiento de XAudio2.</span><span class="sxs-lookup"><span data-stu-id="98a99-120">Use source voices to submit audio data into the XAudio2 processing pipeline.</span></span> <span data-ttu-id="98a99-121">Son los puntos de entrada en el [gráfico de audio de XAudio2](xaudio2-audio-graph.md).</span><span class="sxs-lookup"><span data-stu-id="98a99-121">They are the entry points into the [XAudio2 Audio Graph](xaudio2-audio-graph.md).</span></span> <span data-ttu-id="98a99-122">Debe enviar datos de voz a una voz de patrón para que se escuche, ya sea directamente o a través de voces de submezcla intermedias.</span><span class="sxs-lookup"><span data-stu-id="98a99-122">You must send voice data to a mastering voice to be heard, either directly or through intermediate submix voices.</span></span>

<span data-ttu-id="98a99-123">Además de las acciones realizadas por todas las voces, las voces de origen realizan las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="98a99-123">In addition to the actions performed by all voices, source voices perform the following actions.</span></span>

-   <span data-ttu-id="98a99-124">Si es necesario, un descodificador se ejecuta primero para convertir los datos de origen codificados en modulación por pulsos de código (PCM).</span><span class="sxs-lookup"><span data-stu-id="98a99-124">If necessary, a decoder runs first to convert encoded source data to Pulse Code Modulation (PCM).</span></span>
-   <span data-ttu-id="98a99-125">Una conversión de frecuencia de muestreo de velocidad variable (SRC) convierte los datos de audio de origen de la voz a la velocidad de muestra esperada por las voces de destino, si es necesario, y también admite cambios de paso dinámicos.</span><span class="sxs-lookup"><span data-stu-id="98a99-125">A variable-rate sample rate conversion (SRC) converts the voice's source audio data to the sample rate expected by its destination voices, if necessary, and also supports dynamic pitch changes.</span></span>
-   <span data-ttu-id="98a99-126">Se puede usar un filtro opcional de variable de estado para colorear el sonido de varias maneras.</span><span class="sxs-lookup"><span data-stu-id="98a99-126">An optional state-variable filter can be used to color the sound in various ways.</span></span> <span data-ttu-id="98a99-127">Vea [**IXAudio2Voice:: SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).</span><span class="sxs-lookup"><span data-stu-id="98a99-127">See [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).</span></span>
-   <span data-ttu-id="98a99-128">Se puede aplicar un filtro opcional a las salidas de la voz.</span><span class="sxs-lookup"><span data-stu-id="98a99-128">An optional filter can be applied to the voice's outputs.</span></span> <span data-ttu-id="98a99-129">Vea [**IXAudio2Voice:: SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).</span><span class="sxs-lookup"><span data-stu-id="98a99-129">See [**IXAudio2Voice::SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).</span></span>

## <a name="submix-voices"></a><span data-ttu-id="98a99-130">Voces de submezcla</span><span class="sxs-lookup"><span data-stu-id="98a99-130">Submix Voices</span></span>

<span data-ttu-id="98a99-131">Una voz de submezcla se usa principalmente para mejorar el rendimiento y el procesamiento de efectos.</span><span class="sxs-lookup"><span data-stu-id="98a99-131">A submix voice is used primarily for performance improvements and effects processing.</span></span> <span data-ttu-id="98a99-132">No se pueden enviar búferes de datos directamente a voces de submezcla.</span><span class="sxs-lookup"><span data-stu-id="98a99-132">You cannot submit data buffers directly to submix voices.</span></span> <span data-ttu-id="98a99-133">No será audible a menos que lo envíe a una voz de maestro.</span><span class="sxs-lookup"><span data-stu-id="98a99-133">It will not be audible unless you submit it to a mastering voice.</span></span> <span data-ttu-id="98a99-134">Puede utilizar una voz de submezcla para asegurarse de que un conjunto determinado de datos de voz se convierte en el mismo formato y de que una cadena de efectos determinada se procese en el resultado colectivo.</span><span class="sxs-lookup"><span data-stu-id="98a99-134">You can use a submix voice to ensure that a particular set of voice data is converted to the same format and to have a particular effect chain processed on the collective result.</span></span>

<span data-ttu-id="98a99-135">Además de las acciones realizadas por todas las voces, las voces de submezcla realizan las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="98a99-135">In addition to the actions performed by all voices, submix voices perform the following actions.</span></span>

-   <span data-ttu-id="98a99-136">Un SRC de velocidad fija se ejecuta en la salida de la voz, si es necesario, para convertir el audio a la velocidad de muestra esperada por sus voces de destino.</span><span class="sxs-lookup"><span data-stu-id="98a99-136">A fixed-rate SRC runs on the voice's output, if necessary, to convert the audio to the sample rate expected by its destination voices.</span></span>
-   <span data-ttu-id="98a99-137">Se puede usar un filtro opcional de variable de estado para colorear el sonido de varias maneras.</span><span class="sxs-lookup"><span data-stu-id="98a99-137">An optional state-variable filter can be used to color the sound in various ways.</span></span> <span data-ttu-id="98a99-138">Vea [**IXAudio2Voice:: SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).</span><span class="sxs-lookup"><span data-stu-id="98a99-138">See [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).</span></span>
-   <span data-ttu-id="98a99-139">Se puede aplicar un filtro opcional a las salidas de la voz.</span><span class="sxs-lookup"><span data-stu-id="98a99-139">An optional filter can be applied to the voice's outputs.</span></span> <span data-ttu-id="98a99-140">Vea [**IXAudio2Voice:: SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).</span><span class="sxs-lookup"><span data-stu-id="98a99-140">See [**IXAudio2Voice::SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).</span></span>

## <a name="mastering-voices"></a><span data-ttu-id="98a99-141">Voces de mastering</span><span class="sxs-lookup"><span data-stu-id="98a99-141">Mastering Voices</span></span>

<span data-ttu-id="98a99-142">Use una voz de maestro para representar el dispositivo de salida de audio.</span><span class="sxs-lookup"><span data-stu-id="98a99-142">Use a mastering voice to represent the audio output device.</span></span> <span data-ttu-id="98a99-143">Los búferes de datos no se pueden enviar directamente a las voces de la maestra, pero los datos enviados a otros tipos de voces deben dirigirse a una voz de patrón para que se escuche.</span><span class="sxs-lookup"><span data-stu-id="98a99-143">You cannot submit data buffers directly to mastering voices, but data submitted to other types of voices must go to a mastering voice to be heard.</span></span>

<span data-ttu-id="98a99-144">Además de las acciones realizadas por todas las voces, las voces de Master realizan las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="98a99-144">In addition to the actions performed by all voices, mastering voices perform the following actions.</span></span>

-   <span data-ttu-id="98a99-145">Si crea la voz de masterización con un valor de *InputSampleRate* explícito que no es compatible con el dispositivo de audio, se usa un src de velocidad fija para realizar la conversión a la velocidad de muestra más cercana admitida por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="98a99-145">If you create the mastering voice with an explicit *InputSampleRate* value that is not supported by the audio device, a fixed-rate SRC is used to convert to the closest sample rate supported by the device.</span></span>
-   <span data-ttu-id="98a99-146">Recorte el audio de salida final, si lo requiere el dispositivo de salida.</span><span class="sxs-lookup"><span data-stu-id="98a99-146">Clip the final output audio, if it is required by the output device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="98a99-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="98a99-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98a99-148">Voces</span><span class="sxs-lookup"><span data-stu-id="98a99-148">Voices</span></span>](voices.md)
</dt> <dt>

[<span data-ttu-id="98a99-149">Guía de programación de XAudio2</span><span class="sxs-lookup"><span data-stu-id="98a99-149">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="98a99-150">**IXAudio2SourceVoice**</span><span class="sxs-lookup"><span data-stu-id="98a99-150">**IXAudio2SourceVoice**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)
</dt> <dt>

[<span data-ttu-id="98a99-151">**IXAudio2SubmixVoice**</span><span class="sxs-lookup"><span data-stu-id="98a99-151">**IXAudio2SubmixVoice**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)
</dt> <dt>

[<span data-ttu-id="98a99-152">**IXAudio2MasteringVoice**</span><span class="sxs-lookup"><span data-stu-id="98a99-152">**IXAudio2MasteringVoice**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)
</dt> </dl>

 

 
