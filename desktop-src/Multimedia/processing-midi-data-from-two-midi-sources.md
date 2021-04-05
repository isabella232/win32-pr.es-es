---
title: Procesamiento de datos MIDI de dos orígenes MIDI
description: Procesamiento de datos MIDI de dos orígenes MIDI
ms.assetid: d8b605d9-a12a-4830-8f29-ea700aefb41d
keywords:
- Windows multimedia, procesamiento de datos MIDI de dos orígenes
- multimedia, procesamiento de datos MIDI de dos orígenes
- audio multimedia, procesamiento de datos MIDI de dos orígenes
- audio, procesamiento de datos MIDI de dos orígenes
- Interfaz digital de instrumentos musicales (MIDI), procesamiento de datos de dos orígenes
- MIDI (interfaz digital de instrumentos musicales), procesamiento de datos de dos orígenes
- procesamiento de datos MIDI de dos orígenes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513dcd16036f6f833aec6813f75c6c082925f666
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077686"
---
# <a name="processing-midi-data-from-two-midi-sources"></a><span data-ttu-id="438b5-110">Procesamiento de datos MIDI de dos orígenes MIDI</span><span class="sxs-lookup"><span data-stu-id="438b5-110">Processing MIDI Data from Two MIDI Sources</span></span>

<span data-ttu-id="438b5-111">El subsistema MIDI puede enrutar los mensajes MIDI de dos orígenes de datos a un solo dispositivo de salida MIDI para la reproducción simultánea.</span><span class="sxs-lookup"><span data-stu-id="438b5-111">The MIDI subsystem can route MIDI messages from two data sources to a single MIDI output device for concurrent playback.</span></span> <span data-ttu-id="438b5-112">Por ejemplo, un origen puede ser música de fondo o una línea de graves que se ha grabado previamente y se ha almacenado en un archivo.</span><span class="sxs-lookup"><span data-stu-id="438b5-112">For example, one source can be background music or a bass line that has been pre-recorded and stored in a file.</span></span> <span data-ttu-id="438b5-113">El segundo origen puede ser datos activos de un instrumento MIDI, como un teclado o guitarra.</span><span class="sxs-lookup"><span data-stu-id="438b5-113">The second source can be live data from a MIDI instrument, such as a keyboard or guitar.</span></span>

<span data-ttu-id="438b5-114">Ambos orígenes de datos envían datos MIDI a un único dispositivo MIDI que se identifica con un identificador.</span><span class="sxs-lookup"><span data-stu-id="438b5-114">Both data sources send MIDI data to a single MIDI device that is identified with one handle.</span></span> <span data-ttu-id="438b5-115">Envíe un flujo de datos mediante la función [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) y uno o más búferes de secuencia.</span><span class="sxs-lookup"><span data-stu-id="438b5-115">Send one data stream by using the [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) function and one or more stream buffers.</span></span> <span data-ttu-id="438b5-116">Normalmente, este flujo de datos contiene datos grabados como datos empaquetados en el búfer.</span><span class="sxs-lookup"><span data-stu-id="438b5-116">This data stream typically contains prerecorded data that is packed into the buffer.</span></span>

<span data-ttu-id="438b5-117">Envíe el segundo flujo de datos (normalmente desde un instrumento MIDI) de forma asincrónica mediante la función [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) .</span><span class="sxs-lookup"><span data-stu-id="438b5-117">Send the second data stream (typically from a MIDI instrument) asynchronously by using the [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) function.</span></span> <span data-ttu-id="438b5-118">El estado de ejecución de un búfer de secuencia no se verá afectado negativamente por las llamadas asincrónicas realizadas por el segundo flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="438b5-118">The running status of a stream buffer will not be adversely affected by the asynchronous calls made by the second data stream.</span></span>

<span data-ttu-id="438b5-119">Cada mensaje corto enviado con **midiOutShortMsg** debe ser un mensaje MIDI completo, con un byte de estado y el número de bytes de datos adecuado.</span><span class="sxs-lookup"><span data-stu-id="438b5-119">Each short message sent with **midiOutShortMsg** must be a complete MIDI message, with a status byte and the appropriate number of data bytes.</span></span> <span data-ttu-id="438b5-120">Si se omite el byte de estado, **midiOutShortMsg** devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="438b5-120">If the status byte is omitted, **midiOutShortMsg** returns an error.</span></span> <span data-ttu-id="438b5-121">(Sin embargo, no hay ningún estado en ejecución con la salida de Stream).</span><span class="sxs-lookup"><span data-stu-id="438b5-121">(However, there is no running status with stream output.)</span></span>

 

 