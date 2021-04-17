---
description: En esta información general se presentan algunos conceptos clave para usar XAudio2.
ms.assetid: 103e939f-7815-51c5-159a-c607da1e99ba
title: Conceptos clave de XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c2c0e173e2205070c9f94e8c25dcd9ce7e548c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720714"
---
# <a name="xaudio2-key-concepts"></a><span data-ttu-id="e1a4e-103">Conceptos clave de XAudio2</span><span class="sxs-lookup"><span data-stu-id="e1a4e-103">XAudio2 Key Concepts</span></span>

<span data-ttu-id="e1a4e-104">En esta información general se presentan algunos conceptos clave para usar XAudio2.</span><span class="sxs-lookup"><span data-stu-id="e1a4e-104">This overview introduces some key concepts for using XAudio2.</span></span>

-   [<span data-ttu-id="e1a4e-105">Motor de XAudio2</span><span class="sxs-lookup"><span data-stu-id="e1a4e-105">XAudio2 Engine</span></span>](#xaudio2-engine)
-   [<span data-ttu-id="e1a4e-106">Voces</span><span class="sxs-lookup"><span data-stu-id="e1a4e-106">Voices</span></span>](#voices)
-   [<span data-ttu-id="e1a4e-107">Gráfico de audio</span><span class="sxs-lookup"><span data-stu-id="e1a4e-107">Audio Graph</span></span>](#audio-graph)
-   [<span data-ttu-id="e1a4e-108">Devoluciones de llamada</span><span class="sxs-lookup"><span data-stu-id="e1a4e-108">Callbacks</span></span>](#callbacks)
-   [<span data-ttu-id="e1a4e-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e1a4e-109">Related Topics</span></span>](#related-topics)

## <a name="xaudio2-engine"></a><span data-ttu-id="e1a4e-110">Motor de XAudio2</span><span class="sxs-lookup"><span data-stu-id="e1a4e-110">XAudio2 Engine</span></span>

<span data-ttu-id="e1a4e-111">La interfaz [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) es el núcleo del motor XAudio2.</span><span class="sxs-lookup"><span data-stu-id="e1a4e-111">The [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) interface is the core of the XAudio2 engine.</span></span> <span data-ttu-id="e1a4e-112">La creación de una instancia de la interfaz **IXAudio2** permite al cliente enumerar los dispositivos de audio disponibles, configurar las propiedades globales de la API, crear voces y supervisar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="e1a4e-112">Creating an instance of the **IXAudio2** interface allows the client to enumerate the available audio devices, to configure global API properties, to create voices, and to monitor performance.</span></span> <span data-ttu-id="e1a4e-113">La función auxiliar [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) realiza las tareas de creación de instancias e inicialización de XAudio2.</span><span class="sxs-lookup"><span data-stu-id="e1a4e-113">The [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) helper function performs instantiation and initialization tasks for XAudio2.</span></span>

<span data-ttu-id="e1a4e-114">Puede crear instancias de XAudio2 varias veces en un único proceso.</span><span class="sxs-lookup"><span data-stu-id="e1a4e-114">You can create instances of XAudio2 multiple times within a single process.</span></span> <span data-ttu-id="e1a4e-115">Cada objeto XAudio2 funciona de forma independiente y tiene su propio subproceso de procesamiento de audio.</span><span class="sxs-lookup"><span data-stu-id="e1a4e-115">Each XAudio2 object operates independently, and has its own audio processing thread.</span></span> <span data-ttu-id="e1a4e-116">Solo se comparten los valores de Debug.</span><span class="sxs-lookup"><span data-stu-id="e1a4e-116">Only the debug settings are shared.</span></span> <span data-ttu-id="e1a4e-117">Esto es importante en Windows, donde pueden cargarse varios componentes diferentes en un único proceso.</span><span class="sxs-lookup"><span data-stu-id="e1a4e-117">This is important on Windows where several different components may be loaded in a single process.</span></span> <span data-ttu-id="e1a4e-118">Por ejemplo, Internet Explorer podría usar varios componentes de XAudio2 simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="e1a4e-118">For example, Internet Explorer might use multiple XAudio2 components simultaneously.</span></span> <span data-ttu-id="e1a4e-119">Aunque es posible crear varios objetos del motor de XAudio2 en una sola aplicación cliente, no se debe pasar información entre sus respectivos gráficos.</span><span class="sxs-lookup"><span data-stu-id="e1a4e-119">Although it is possible to create multiple XAudio2 engine objects within a single client application, you should not pass information between their respective graphs.</span></span>

<span data-ttu-id="e1a4e-120">Para obtener un ejemplo de cómo inicializar el motor de XAudio2, consulte [Cómo: inicializar xaudio2](how-to--initialize-xaudio2.md).</span><span class="sxs-lookup"><span data-stu-id="e1a4e-120">For an example of initializing the XAudio2 engine, see [How to: Initialize XAudio2](how-to--initialize-xaudio2.md).</span></span>

## <a name="voices"></a><span data-ttu-id="e1a4e-121">Voces</span><span class="sxs-lookup"><span data-stu-id="e1a4e-121">Voices</span></span>

<span data-ttu-id="e1a4e-122">Las voces son los objetos que usa XAudio2 para procesar, manipular y reproducir datos de audio.</span><span class="sxs-lookup"><span data-stu-id="e1a4e-122">Voices are the objects XAudio2 use to process, to manipulate, and to play audio data.</span></span> <span data-ttu-id="e1a4e-123">Hay tres tipos de voces en XAudio2.</span><span class="sxs-lookup"><span data-stu-id="e1a4e-123">There are three types of voices in XAudio2.</span></span>

-   [<span data-ttu-id="e1a4e-124">**Voces de origen**</span><span class="sxs-lookup"><span data-stu-id="e1a4e-124">**Source Voices**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)

    <span data-ttu-id="e1a4e-125">Las voces de origen representan un flujo de datos de audio.</span><span class="sxs-lookup"><span data-stu-id="e1a4e-125">Source voices represent a stream of audio data.</span></span> <span data-ttu-id="e1a4e-126">Las voces de origen envían sus datos a otros tipos de voces.</span><span class="sxs-lookup"><span data-stu-id="e1a4e-126">Source voices send their data to other types of voices.</span></span>

-   [<span data-ttu-id="e1a4e-127">**Voces de submezcla**</span><span class="sxs-lookup"><span data-stu-id="e1a4e-127">**Submix Voices**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)

    <span data-ttu-id="e1a4e-128">Las voces de submezcla realizan alguna manipulación de los datos de audio que reciben.</span><span class="sxs-lookup"><span data-stu-id="e1a4e-128">Submix voices perform some manipulation of audio data they receive.</span></span> <span data-ttu-id="e1a4e-129">Un ejemplo de manipulación de datos de audio podría ser la conversión de la frecuencia de muestreo.</span><span class="sxs-lookup"><span data-stu-id="e1a4e-129">One example of audio data manipulation might be sample rate conversion.</span></span> <span data-ttu-id="e1a4e-130">Después de que una voz de submezcla procese los datos, los pasa a otra voz de submezcla o a una voz maestra.</span><span class="sxs-lookup"><span data-stu-id="e1a4e-130">After a submix voice processes data, it passes that data to another submix voice or to a master voice.</span></span>

-   [<span data-ttu-id="e1a4e-131">**Voces de mastering**</span><span class="sxs-lookup"><span data-stu-id="e1a4e-131">**Mastering Voices**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)

    <span data-ttu-id="e1a4e-132">Las voces de Master reciben datos de voces de origen y voces de submezcla, y envían los datos al hardware de audio.</span><span class="sxs-lookup"><span data-stu-id="e1a4e-132">Mastering voices receive data from source voices and submix voices, and sends that data to the audio hardware.</span></span>

<span data-ttu-id="e1a4e-133">Consulte las [voces de xaudio2](voices.md) para obtener información general sobre las voces de xaudio2.</span><span class="sxs-lookup"><span data-stu-id="e1a4e-133">See [XAudio2 Voices](voices.md) for an overview of XAudio2 voices.</span></span>

## <a name="audio-graph"></a><span data-ttu-id="e1a4e-134">Gráfico de audio</span><span class="sxs-lookup"><span data-stu-id="e1a4e-134">Audio Graph</span></span>

<span data-ttu-id="e1a4e-135">Un gráfico de audio es una colección de voces de XAudio2.</span><span class="sxs-lookup"><span data-stu-id="e1a4e-135">An audio graph is a collection of XAudio2 voices.</span></span> <span data-ttu-id="e1a4e-136">El audio se inicia en un lado de un gráfico de audio en las voces de origen y, opcionalmente, pasa a través de una o más voces de la mezcla y finaliza en una voz de la maestra.</span><span class="sxs-lookup"><span data-stu-id="e1a4e-136">Audio starts at one side of an audio graph in source voices, optionally passes through one or more submix voices, and ends at a mastering voice.</span></span> <span data-ttu-id="e1a4e-137">Un gráfico de audio contendrá una voz de origen para cada sonido que se reproduce actualmente, cero o más voces de submezcla y una voz de maestro.</span><span class="sxs-lookup"><span data-stu-id="e1a4e-137">An audio graph will contain a source voice for each sound currently playing, zero or more submix voices, and one mastering voice.</span></span> <span data-ttu-id="e1a4e-138">El gráfico de audio más sencillo, y el mínimo necesario para crear un ruido en XAudio2, es una voz de origen única que se envía directamente a una voz de mastering.</span><span class="sxs-lookup"><span data-stu-id="e1a4e-138">The simplest audio graph, and the minimum needed to make a noise in XAudio2, is a single source voice outputting directly to a mastering voice.</span></span> <span data-ttu-id="e1a4e-139">Consulte [Cómo: reproducir un sonido con xaudio2](how-to--play-a-sound-with-xaudio2.md) para ver un ejemplo de los pasos mínimos necesarios para reproducir un sonido con xaudio2.</span><span class="sxs-lookup"><span data-stu-id="e1a4e-139">See [How to: Play a Sound with XAudio2](how-to--play-a-sound-with-xaudio2.md) for an example of the minimum steps need to play a sound with XAudio2.</span></span>

<span data-ttu-id="e1a4e-140">Consulte [gráfico de audio de xaudio2](audio-graphs.md) para obtener información general sobre los gráficos de audio de xaudio2.</span><span class="sxs-lookup"><span data-stu-id="e1a4e-140">See [XAudio2 Audio Graph](audio-graphs.md) for an overview of XAudio2 audio graphs.</span></span>

## <a name="callbacks"></a><span data-ttu-id="e1a4e-141">Devoluciones de llamada</span><span class="sxs-lookup"><span data-stu-id="e1a4e-141">Callbacks</span></span>

<span data-ttu-id="e1a4e-142">Las devoluciones de llamada son el mecanismo que usa XAudio2 para indicar al código de cliente que se ha producido algún evento en una voz o en el objeto de motor.</span><span class="sxs-lookup"><span data-stu-id="e1a4e-142">Callbacks are the mechanism XAudio2 uses to signal client code that some event has occurred in a voice or in the engine object.</span></span> <span data-ttu-id="e1a4e-143">Dado que la reproducción de audio es asincrónica en el motor de XAudio2, las devoluciones de llamada proporcionan la única manera de determinar cuándo finaliza la reproducción de un sonido.</span><span class="sxs-lookup"><span data-stu-id="e1a4e-143">Because audio playback is asynchronous in the XAudio2 engine, callbacks provide the only way to determine when a sound is finished playing.</span></span>

<span data-ttu-id="e1a4e-144">Consulte [devoluciones de llamada de xaudio2](callbacks.md) para obtener información general sobre las devoluciones de llamada de xaudio2.</span><span class="sxs-lookup"><span data-stu-id="e1a4e-144">See [XAudio2 Callbacks](callbacks.md) for an overview of XAudio2 callbacks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1a4e-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e1a4e-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1a4e-146">Introducción</span><span class="sxs-lookup"><span data-stu-id="e1a4e-146">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="e1a4e-147">Versiones de XAudio2</span><span class="sxs-lookup"><span data-stu-id="e1a4e-147">XAudio2 Versions</span></span>](xaudio2-versions.md)
</dt> <dt>

[<span data-ttu-id="e1a4e-148">Cómo: inicializar XAudio2</span><span class="sxs-lookup"><span data-stu-id="e1a4e-148">How to: Initialize XAudio2</span></span>](how-to--initialize-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="e1a4e-149">Cómo: reproducir un sonido con XAudio2</span><span class="sxs-lookup"><span data-stu-id="e1a4e-149">How to: Play a sound with XAudio2</span></span>](how-to--play-a-sound-with-xaudio2.md)
</dt> </dl>

 

 



