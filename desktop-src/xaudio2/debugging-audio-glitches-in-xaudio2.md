---
description: Se pueden producir problemas en XAudio2, en este tema se explica cómo se informan y algunos enfoques para corregirlos.
ms.assetid: 360d1c5a-82e7-c982-82ea-5b5c7d69bc25
title: Depurar problemas de audio en XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 749c2ff69888f3411d86e13f95b84509587f22a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911113"
---
# <a name="debugging-audio-glitches-in-xaudio2"></a><span data-ttu-id="cf966-103">Depurar problemas de audio en XAudio2</span><span class="sxs-lookup"><span data-stu-id="cf966-103">Debugging Audio Glitches in XAudio2</span></span>

<span data-ttu-id="cf966-104">Se pueden producir problemas en XAudio2, en este tema se explica cómo se informan y algunos enfoques para corregirlos.</span><span class="sxs-lookup"><span data-stu-id="cf966-104">Glitches can occur in XAudio2, this topic covers how they are reported and some approaches to fixing them.</span></span>

<span data-ttu-id="cf966-105">En esta información general se tratan los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="cf966-105">This overview covers the following topics:</span></span>

-   [<span data-ttu-id="cf966-106">Causas de problemas o problemas de salida de audio</span><span class="sxs-lookup"><span data-stu-id="cf966-106">Causes of audio output problems or glitches</span></span>](#causes-of-audio-output-problems-or-glitches)
-   [<span data-ttu-id="cf966-107">Cómo notifica XAudio2 los problemas</span><span class="sxs-lookup"><span data-stu-id="cf966-107">How XAudio2 reports problems</span></span>](#how-xaudio2-reports-problems)
-   [<span data-ttu-id="cf966-108">Enfoques para solucionar problemas</span><span class="sxs-lookup"><span data-stu-id="cf966-108">Approaches to fixing problems</span></span>](#approaches-to-fixing-problems)
-   [<span data-ttu-id="cf966-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cf966-109">Related topics</span></span>](#related-topics)

## <a name="causes-of-audio-output-problems-or-glitches"></a><span data-ttu-id="cf966-110">Causas de problemas o problemas de salida de audio</span><span class="sxs-lookup"><span data-stu-id="cf966-110">Causes of audio output problems or glitches</span></span>

<span data-ttu-id="cf966-111">Los problemas pueden producirse en la salida de XAudio2 por varios motivos.</span><span class="sxs-lookup"><span data-stu-id="cf966-111">Glitches can occur in XAudio2 output for several reasons.</span></span>

-   <span data-ttu-id="cf966-112">Se ha agotado una voz de origen de XAudio2.</span><span class="sxs-lookup"><span data-stu-id="cf966-112">An XAudio2 source voice is starved.</span></span> <span data-ttu-id="cf966-113">El cliente no envía un audio nuevo a él lo suficientemente rápido.</span><span class="sxs-lookup"><span data-stu-id="cf966-113">The client is not submitting fresh audio to it fast enough.</span></span> <span data-ttu-id="cf966-114">Obtiene el silencio porque no tiene datos para reproducir.</span><span class="sxs-lookup"><span data-stu-id="cf966-114">You get silence because it has no data to play.</span></span>
-   <span data-ttu-id="cf966-115">En conjunto, XAudio2 se sobrecarga.</span><span class="sxs-lookup"><span data-stu-id="cf966-115">XAudio2 as a whole is overburdened.</span></span> <span data-ttu-id="cf966-116">Tarda más de *x* MS en producir *x* MS de audio.</span><span class="sxs-lookup"><span data-stu-id="cf966-116">It takes longer than *X* ms to produce *X* ms of audio.</span></span> <span data-ttu-id="cf966-117">Obtiene las faltas porque XAudio2 no puede producir datos tan rápido como el dispositivo de audio lo necesita.</span><span class="sxs-lookup"><span data-stu-id="cf966-117">You get dropouts because XAudio2 can't produce data as fast as the audio device needs it.</span></span> <span data-ttu-id="cf966-118">Puede que esté ejecutando demasiadas voces o efectos a la vez, haciendo demasiado trabajo en las devoluciones de llamada de XAudio2 o realizando llamadas a la API de XAudio2 con demasiada frecuencia.</span><span class="sxs-lookup"><span data-stu-id="cf966-118">You might be running too many voices or effects at a time, doing too much work in XAudio2 callbacks, or making XAudio2 API calls too frequently.</span></span>
-   <span data-ttu-id="cf966-119">El subproceso de procesamiento de audio se está deteniendo porque la implementación del cliente de alguna devolución de llamada de XAudio2 está realizando cosas que pueden bloquear el subproceso.</span><span class="sxs-lookup"><span data-stu-id="cf966-119">The audio processing thread is stalling because the client's implementation of some XAudio2 callback is doing things that can block the thread.</span></span> <span data-ttu-id="cf966-120">Por ejemplo, podría tener acceso al disco, sincronizar con otros subprocesos o llamar a otras funciones que se puedan bloquear.</span><span class="sxs-lookup"><span data-stu-id="cf966-120">For example, it might be accessing the disk, synchronizing with other threads, or calling other functions that may block.</span></span> <span data-ttu-id="cf966-121">Utilice un subproceso en segundo plano de prioridad inferior que la devolución de llamada pueda señalizar para realizar dichas tareas.</span><span class="sxs-lookup"><span data-stu-id="cf966-121">Use a lower-priority background thread that the callback can signal to perform such tasks.</span></span>
-   <span data-ttu-id="cf966-122">El sistema en su conjunto está sobrecargado.</span><span class="sxs-lookup"><span data-stu-id="cf966-122">The system as a whole is overloaded.</span></span> <span data-ttu-id="cf966-123">Otros subprocesos que se ejecutan con la misma prioridad o mayor que XAudio2 están haciendo demasiado trabajo.</span><span class="sxs-lookup"><span data-stu-id="cf966-123">Other threads running at the same or higher priority than XAudio2 are doing too much work.</span></span> <span data-ttu-id="cf966-124">Compiten con el subproceso de audio para el tiempo de CPU.</span><span class="sxs-lookup"><span data-stu-id="cf966-124">They are competing with the audio thread for CPU time.</span></span>

## <a name="how-xaudio2-reports-problems"></a><span data-ttu-id="cf966-125">Cómo notifica XAudio2 los problemas</span><span class="sxs-lookup"><span data-stu-id="cf966-125">How XAudio2 reports problems</span></span>

<span data-ttu-id="cf966-126">XAudio2 puede comunicar los problemas de la compilación de depuración de varias maneras.</span><span class="sxs-lookup"><span data-stu-id="cf966-126">XAudio2 can communicate glitches in the debug build in several ways.</span></span>

-   <span data-ttu-id="cf966-127">Si se ha agotado una voz, XAudio2 muestra un mensaje en este formulario.</span><span class="sxs-lookup"><span data-stu-id="cf966-127">If a voice is being starved, XAudio2 shows a message in this form.</span></span>

    ``` syntax
    XAudio2: WARNING: Voice at 0xNNNNNNNN starved: no more source buffers are available, but no end-of-stream marker was received
    ```

-   <span data-ttu-id="cf966-128">Si el subproceso de audio se ejecuta durante demasiado tiempo, XAudio2 muestra un mensaje en este formulario.</span><span class="sxs-lookup"><span data-stu-id="cf966-128">If the audio thread runs for too long, XAudio2 shows a message in this form.</span></span>

    ``` syntax
    XAudio2: WARNING: Spent Xms in audio thread; XAudio2 possibly overloaded
    ```

    <span data-ttu-id="cf966-129">Normalmente, este mensaje aparece con el siguiente mensaje.</span><span class="sxs-lookup"><span data-stu-id="cf966-129">Typically, this message occurs with the next message.</span></span>

-   <span data-ttu-id="cf966-130">Si el controlador de audio no puede alimentar nuevos datos de audio en el tiempo, XAudio2 muestra un mensaje en este formulario.</span><span class="sxs-lookup"><span data-stu-id="cf966-130">If the audio driver can't be fed new audio data on time, XAudio2 shows a message in this form.</span></span>

    ``` syntax
    XAudio2: WARNING: Glitch at output sample X
    ```

-   <span data-ttu-id="cf966-131">La llamada a [**IXAudio2:: GetPerformanceData**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-getperformancedata) proporciona datos de rendimiento de XAudio2, incluido el número total de problemas desde que se inició el motor de xaudio2.</span><span class="sxs-lookup"><span data-stu-id="cf966-131">Calling [**IXAudio2::GetPerformanceData**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-getperformancedata) provides XAudio2 performance data, including the total number of glitches since the XAudio2 engine started.</span></span>

## <a name="approaches-to-fixing-problems"></a><span data-ttu-id="cf966-132">Enfoques para solucionar problemas</span><span class="sxs-lookup"><span data-stu-id="cf966-132">Approaches to fixing problems</span></span>

<span data-ttu-id="cf966-133">Las formas posibles de reducir los problemas de audio son las siguientes.</span><span class="sxs-lookup"><span data-stu-id="cf966-133">Possible ways to reduce audio glitches include the following.</span></span>

-   <span data-ttu-id="cf966-134">En el caso del agotamiento de la voz: aumente la cantidad de datos de audio que se ponen en cola en una voz.</span><span class="sxs-lookup"><span data-stu-id="cf966-134">In the voice starvation case: Increase the amount of audio data that is queued ahead on a voice.</span></span> <span data-ttu-id="cf966-135">Puede usar [**IXAudio2SourceVoice:: GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) para detectar el número de búferes en cola en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="cf966-135">You can use [**IXAudio2SourceVoice::GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) to discover the number of buffers queued at any moment.</span></span> <span data-ttu-id="cf966-136">Si sigue viendo errores de inanición de voz, pero no puede oír ningún problema, asegúrese de que está estableciendo el [**\_ búfer de XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**Marcas** para \_ el fin \_ de \_ la secuencia de XAUDIO2 en el búfer final de un sonido.</span><span class="sxs-lookup"><span data-stu-id="cf966-136">If you still see voice starvation errors, but can't hear any glitch, make sure you are setting [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer).**Flags** to XAUDIO2\_END\_OF\_STREAM on the final buffer of a sound.</span></span> <span data-ttu-id="cf966-137">Esto indica a XAudio2 que no espere que más búferes estén disponibles en cuanto se complete.</span><span class="sxs-lookup"><span data-stu-id="cf966-137">This tells XAudio2 not to expect any more buffers necessarily to be available as soon as this one completes.</span></span>

    <span data-ttu-id="cf966-138">En los demás casos:</span><span class="sxs-lookup"><span data-stu-id="cf966-138">In the other cases:</span></span>

    -   <span data-ttu-id="cf966-139">Reduzca el número de voces y efectos activos en el gráfico, especialmente efectos costosos como reverberación.</span><span class="sxs-lookup"><span data-stu-id="cf966-139">Reduce the number of active voices and effects in the graph, especially expensive effects like reverb.</span></span>
    -   <span data-ttu-id="cf966-140">Deshabilite las voces y los efectos que no esté usando.</span><span class="sxs-lookup"><span data-stu-id="cf966-140">Disable voices and effects you're not using.</span></span>
    -   <span data-ttu-id="cf966-141">Use las \_ \_ marcas de voz NOSRC y xaudio2 Voice \_ de xaudio2 \_ en [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="cf966-141">Use the XAUDIO2\_VOICE\_NOSRC and XAUDIO2\_VOICE\_NOPITCH flags in [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), whenever possible.</span></span> <span data-ttu-id="cf966-142">La conversión de la frecuencia de muestreo es costosa.</span><span class="sxs-lookup"><span data-stu-id="cf966-142">Sample rate conversion is costly.</span></span>
    -   <span data-ttu-id="cf966-143">Reduzca la velocidad de muestra de las voces individuales.</span><span class="sxs-lookup"><span data-stu-id="cf966-143">Reduce the sample rate of individual voices.</span></span> <span data-ttu-id="cf966-144">Por ejemplo, una voz de submezcla que hospeda un efecto de reverberación puede tener una velocidad de muestra menor que la voz de origen que envía a ella.</span><span class="sxs-lookup"><span data-stu-id="cf966-144">For example, a submix voice hosting a reverb effect can have a lower sample rate than the source voice sending to it.</span></span> <span data-ttu-id="cf966-145">Los sonidos como explosiones y gunshots que no necesitan alta fidelidad también se pueden grabar a velocidades de muestra inferiores.</span><span class="sxs-lookup"><span data-stu-id="cf966-145">Sounds such as explosions and gunshots that don't need high fidelity can also be recorded at lower sample rates.</span></span>
    -   <span data-ttu-id="cf966-146">Asegúrese de que las implementaciones de devolución de llamada hacen tan poco trabajo como sea posible y no bloqueen nunca.</span><span class="sxs-lookup"><span data-stu-id="cf966-146">Ensure that callback implementations do as little work as possible and never block.</span></span>
    -   <span data-ttu-id="cf966-147">Realice menos llamadas a XAudio2.</span><span class="sxs-lookup"><span data-stu-id="cf966-147">Make fewer calls to XAudio2.</span></span> <span data-ttu-id="cf966-148">Normalmente no es necesario actualizar los parámetros de audio para cada fotograma de vídeo.</span><span class="sxs-lookup"><span data-stu-id="cf966-148">Audio parameters usually don't need to be updated for every video frame.</span></span> <span data-ttu-id="cf966-149">Cada 30 ms es suficiente.</span><span class="sxs-lookup"><span data-stu-id="cf966-149">Every 30 ms or so is sufficient.</span></span> <span data-ttu-id="cf966-150">Debe eliminar las llamadas redundantes, como establecer el volumen varias veces en una sucesión rápida.</span><span class="sxs-lookup"><span data-stu-id="cf966-150">You should eliminate redundant calls, such as setting volume several times in quick succession.</span></span>
    -   <span data-ttu-id="cf966-151">Reduzca el uso general de la CPU del juego.</span><span class="sxs-lookup"><span data-stu-id="cf966-151">Reduce the game's overall CPU usage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf966-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cf966-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf966-153">Funciones de depuración</span><span class="sxs-lookup"><span data-stu-id="cf966-153">Debugging Facilities</span></span>](debugging-facilities.md)
</dt> <dt>

[<span data-ttu-id="cf966-154">Referencia de programación de XAudio2</span><span class="sxs-lookup"><span data-stu-id="cf966-154">XAudio2 Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 
