---
description: El conjunto de todas las voces, con sus efectos contenidos y sus interconexiones, se conoce como el gráfico de procesamiento de audio.
ms.assetid: 4fa45dbf-3811-c91c-7561-3b896e9e1f03
title: Gráfico de audio de XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eb265bd6bc2547acd04ca41cceb58ad12896fbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279362"
---
# <a name="xaudio2-audio-graph"></a><span data-ttu-id="a8040-103">Gráfico de audio de XAudio2</span><span class="sxs-lookup"><span data-stu-id="a8040-103">XAudio2 Audio Graph</span></span>

<span data-ttu-id="a8040-104">El conjunto de todas las voces, con sus efectos contenidos y sus interconexiones, se conoce como el gráfico de procesamiento de audio.</span><span class="sxs-lookup"><span data-stu-id="a8040-104">The set of all voices, with their contained effects and their interconnections, is referred to as the audio processing graph.</span></span> <span data-ttu-id="a8040-105">El gráfico toma un conjunto de secuencias de audio del cliente como entrada, las procesa y entrega el resultado final a un dispositivo de audio.</span><span class="sxs-lookup"><span data-stu-id="a8040-105">The graph takes a set of audio streams from the client as input, processes them, and delivers the final result to an audio device.</span></span> <span data-ttu-id="a8040-106">Todo el procesamiento de audio se realiza en un subproceso independiente con una periodicidad definida por el cuanto del gráfico (actualmente, 10 milisegundos en Microsoft Windows y 5 1/3 milisegundos en Xbox 360).</span><span class="sxs-lookup"><span data-stu-id="a8040-106">All audio processing takes place in a separate thread with a periodicity defined by the graph's quantum (currently 10 milliseconds on Microsoft Windows, and 5 1/3 milliseconds on Xbox 360).</span></span> <span data-ttu-id="a8040-107">Cada Quantum milisegundos, el subproceso se reactiva y dispersa los milisegundos de los datos de audio a través del gráfico completo.</span><span class="sxs-lookup"><span data-stu-id="a8040-107">Every quantum milliseconds, the thread wakes up and disperses quantum milliseconds of audio data through the entire graph.</span></span> <span data-ttu-id="a8040-108">Para obtener un ejemplo de cómo crear un gráfico de audio básico, consulte Cómo: [compilar un gráfico básico de procesamiento de audio](how-to--build-a-basic-audio-processing-graph.md).</span><span class="sxs-lookup"><span data-stu-id="a8040-108">For an example of building a basic audio graph, see How to: [Build a Basic Audio Processing Graph](how-to--build-a-basic-audio-processing-graph.md).</span></span>

<span data-ttu-id="a8040-109">Un gráfico de audio simple:</span><span class="sxs-lookup"><span data-stu-id="a8040-109">A simple audio graph:</span></span>

![un gráfico de audio simple](images/xaudio2-audio-graph.png)

<span data-ttu-id="a8040-111">El cliente puede controlar el estado del gráfico dinámicamente mientras se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="a8040-111">The client can control the graph's state dynamically while it is running.</span></span> <span data-ttu-id="a8040-112">Las acciones de control pueden incluir la adición y eliminación de entradas y salidas, el cambio de los efectos internos y las interconexiones, el establecimiento de parámetros en los efectos, la habilitación y deshabilitación de partes del gráfico, etc.</span><span class="sxs-lookup"><span data-stu-id="a8040-112">Control actions might include adding and removing inputs and outputs, changing the internal effects and interconnections, setting parameters on the effects, enabling and disabling parts of the graph, and so on.</span></span> <span data-ttu-id="a8040-113">Para obtener un ejemplo de cómo cambiar dinámicamente un gráfico de audio, consulte [Cómo: agregar o quitar voces dinámicamente de un gráfico de audio](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md).</span><span class="sxs-lookup"><span data-stu-id="a8040-113">For an example of dynamically changing an audio graph, see [How to: Dynamically Add or Remove Voices From an Audio Graph](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md).</span></span>

## <a name="processing-the-graph"></a><span data-ttu-id="a8040-114">Procesar el gráfico</span><span class="sxs-lookup"><span data-stu-id="a8040-114">Processing the Graph</span></span>

<span data-ttu-id="a8040-115">Cualquier llamada al método que afecte a cualquier objeto del gráfico se considera que está afectando a un cambio de estado del gráfico.</span><span class="sxs-lookup"><span data-stu-id="a8040-115">Any method call that affects any object in the graph is considered to be effecting a graph state change.</span></span> <span data-ttu-id="a8040-116">Entre los cambios de estado del gráfico se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="a8040-116">Graph state changes include the following:</span></span>

-   <span data-ttu-id="a8040-117">Crear y destruir voces</span><span class="sxs-lookup"><span data-stu-id="a8040-117">Creating and destroying voices</span></span>
-   <span data-ttu-id="a8040-118">Inicio o detención de voces</span><span class="sxs-lookup"><span data-stu-id="a8040-118">Starting or stopping voices</span></span>
-   <span data-ttu-id="a8040-119">Cambiar los destinos de una voz</span><span class="sxs-lookup"><span data-stu-id="a8040-119">Changing the destinations of a voice</span></span>
-   <span data-ttu-id="a8040-120">Modificar cadenas de efectos</span><span class="sxs-lookup"><span data-stu-id="a8040-120">Modifying effect chains</span></span>
-   <span data-ttu-id="a8040-121">Habilitar o deshabilitar efectos</span><span class="sxs-lookup"><span data-stu-id="a8040-121">Enabling or disabling effects</span></span>
-   <span data-ttu-id="a8040-122">Establecer parámetros en los efectos o en los SRCs, filtros, volúmenes y mezcladores integrados</span><span class="sxs-lookup"><span data-stu-id="a8040-122">Setting parameters on the effects or on the built-in SRCs, filters, volumes, and mixers</span></span>

<span data-ttu-id="a8040-123">Cualquier conjunto de cambios de estado del gráfico se puede combinar y realizar como una transacción atómica.</span><span class="sxs-lookup"><span data-stu-id="a8040-123">Any set of graph state changes can be combined and performed as an atomic transaction.</span></span> <span data-ttu-id="a8040-124">Estas operaciones atómicas se conocen como conjuntos de operaciones.</span><span class="sxs-lookup"><span data-stu-id="a8040-124">These atomic operations are known as operation sets.</span></span> <span data-ttu-id="a8040-125">Se describen en la introducción a los [conjuntos de operaciones de XAudio2](xaudio2-operation-sets.md) .</span><span class="sxs-lookup"><span data-stu-id="a8040-125">They are discussed in the [XAudio2 Operation Sets](xaudio2-operation-sets.md) overview.</span></span>

## <a name="internal-data-representation"></a><span data-ttu-id="a8040-126">Representación de datos internos</span><span class="sxs-lookup"><span data-stu-id="a8040-126">Internal Data Representation</span></span>

<span data-ttu-id="a8040-127">Los datos de audio dentro del gráfico de XAudio2 siempre se almacenan y procesan en formato PCM de punto flotante de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a8040-127">Audio data within the XAudio2 graph is always stored and processed in 32-bit floating-point PCM form.</span></span> <span data-ttu-id="a8040-128">Sin embargo, el número de canales y la velocidad de muestreo pueden variar dentro del gráfico.</span><span class="sxs-lookup"><span data-stu-id="a8040-128">However, the channel count and sample rate can vary within the graph.</span></span> <span data-ttu-id="a8040-129">El formato en el que una voz determinada procesa audio viene determinado por el tipo de voz y los parámetros que se usan para crear la voz.</span><span class="sxs-lookup"><span data-stu-id="a8040-129">The format in which a given voice processes audio is determined by the voice type and parameters used to create the voice.</span></span>



| <span data-ttu-id="a8040-130">Tipo de voz</span><span class="sxs-lookup"><span data-stu-id="a8040-130">Voice Type</span></span>                                                                                                      | <span data-ttu-id="a8040-131">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8040-131">Parameters</span></span>                                                                                     |
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8040-132">**IXAudio2SourceVoice**</span><span class="sxs-lookup"><span data-stu-id="a8040-132">**IXAudio2SourceVoice**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)                                                              | <span data-ttu-id="a8040-133">El número de canales y la velocidad de muestreo de las voces a las que la voz de origen envía audio.</span><span class="sxs-lookup"><span data-stu-id="a8040-133">The channel count and sample rate of the voices to which the source voice sends audio.</span></span>         |
| <span data-ttu-id="a8040-134">[**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) y [ **IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)</span><span class="sxs-lookup"><span data-stu-id="a8040-134">[**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) and [**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)</span></span> | <span data-ttu-id="a8040-135">Los argumentos *InputChannels* y *InputSampleRate* usados para crear la voz de submezcla o de creación de registro.</span><span class="sxs-lookup"><span data-stu-id="a8040-135">The *InputChannels* and *InputSampleRate* arguments used to create the submix/mastering voice.</span></span> |



 

## <a name="format-conversion"></a><span data-ttu-id="a8040-136">Conversión de formato</span><span class="sxs-lookup"><span data-stu-id="a8040-136">Format Conversion</span></span>

<span data-ttu-id="a8040-137">XAudio2 controla cualquier conversión de canal o velocidad de muestra que se requiera a medida que el audio viaja de una voz a otra, con las siguientes limitaciones:</span><span class="sxs-lookup"><span data-stu-id="a8040-137">XAudio2 handles any sample rate or channel conversions that are required as audio travels from one voice to another, with the following limitations:</span></span>

-   <span data-ttu-id="a8040-138">Todas las voces de destino de una voz determinada deben ejecutarse con la misma velocidad de muestra</span><span class="sxs-lookup"><span data-stu-id="a8040-138">All destination voices for a particular voice must be running at the same sample rate</span></span>
-   <span data-ttu-id="a8040-139">Los efectos de una cadena de efectos pueden cambiar el número de canales del audio, pero no su velocidad de muestra</span><span class="sxs-lookup"><span data-stu-id="a8040-139">Effects in an effect chain can change the audio's channel count, but not its sample rate</span></span>
-   <span data-ttu-id="a8040-140">El número de canales de salida de una cadena de efectos debe coincidir con el de las voces a las que envía</span><span class="sxs-lookup"><span data-stu-id="a8040-140">An effect chain's output channel count must match that of the voices to which it sends</span></span>
-   <span data-ttu-id="a8040-141">No se puede realizar ningún cambio de gráfico dinámico, lo que interrumpiría las reglas anteriores</span><span class="sxs-lookup"><span data-stu-id="a8040-141">No dynamic graph change can be made which would break the rules above</span></span>

<span data-ttu-id="a8040-142">En el lado de entrada, las voces de origen pueden leer datos en cualquier formato PCM válido o en cualquiera de los formatos comprimidos compatibles con XAudio2.</span><span class="sxs-lookup"><span data-stu-id="a8040-142">On the input side, source voices can read data in any valid PCM format, or in any of the compressed formats supported by XAudio2.</span></span> <span data-ttu-id="a8040-143">Si se comprimen los datos de entrada, se descodifican en PCM de punto flotante antes de que se realice cualquier otro procesamiento.</span><span class="sxs-lookup"><span data-stu-id="a8040-143">If the input data is compressed, it is decoded to floating-point PCM before any further processing is done.</span></span>

<span data-ttu-id="a8040-144">En el lado de salida, las voces de masterización solo pueden generar datos PCM.</span><span class="sxs-lookup"><span data-stu-id="a8040-144">On the output side, mastering voices can only produce PCM data.</span></span> <span data-ttu-id="a8040-145">Estos datos siempre satisfarán las mismas restricciones descritas anteriormente para los datos PCM entrantes.</span><span class="sxs-lookup"><span data-stu-id="a8040-145">This data will always satisfy the same restrictions described above for input PCM data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8040-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a8040-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8040-147">Gráficos de audio</span><span class="sxs-lookup"><span data-stu-id="a8040-147">Audio Graphs</span></span>](audio-graphs.md)
</dt> <dt>

[<span data-ttu-id="a8040-148">Guía de programación de XAudio2</span><span class="sxs-lookup"><span data-stu-id="a8040-148">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="a8040-149">Cómo: crear un gráfico de procesamiento de audio básico</span><span class="sxs-lookup"><span data-stu-id="a8040-149">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="a8040-150">Cómo: agregar o quitar voces de un gráfico de audio dinámicamente</span><span class="sxs-lookup"><span data-stu-id="a8040-150">How to: Dynamically Add or Remove Voices From an Audio Graph</span></span>](how-to--dynamically-add-or-remove-voices-from-an-audio-graph.md)
</dt> <dt>

[<span data-ttu-id="a8040-151">Cómo: usar voces de submezcla</span><span class="sxs-lookup"><span data-stu-id="a8040-151">How to: Use Submix Voices</span></span>](how-to--use-submix-voices.md)
</dt> <dt>

[<span data-ttu-id="a8040-152">Cómo: crear un efecto en cadena</span><span class="sxs-lookup"><span data-stu-id="a8040-152">How to: Create an Effect Chain</span></span>](how-to--create-an-effect-chain.md)
</dt> </dl>

 

 



