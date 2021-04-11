---
title: Información de tiempo
description: Información de tiempo
ms.assetid: ff9d6fb2-1387-49ce-a4de-1b2f67353628
keywords:
- Interfaz digital de instrumentos musicales (MIDI), información de tiempo
- MIDI (interfaz digital de instrumentos musicales), información de tiempo
- búferes de secuencia, información de tiempo
- Estructura MIDIEVENT
- búferes de secuencia, formato SMPTE
- búferes de secuencia, tiempo de nota trimestral
- búferes de secuencia, TICs
- Formato SMPTE
- hora de la nota del cuarto
- ticks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2daf5b1847456e8fb518665521e484118fead79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149198"
---
# <a name="timing-information"></a><span data-ttu-id="554b6-113">Información de tiempo</span><span class="sxs-lookup"><span data-stu-id="554b6-113">Timing Information</span></span>

<span data-ttu-id="554b6-114">La información de tiempo de un evento MIDI se almacena en el miembro **dwDeltaTime** de la estructura [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) .</span><span class="sxs-lookup"><span data-stu-id="554b6-114">Timing information for a MIDI event is stored in the **dwDeltaTime** member of the [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) structure.</span></span> <span data-ttu-id="554b6-115">La hora se indica en pasos, tal como se define en la especificación de *los archivos MIDI estándar 1,0* .</span><span class="sxs-lookup"><span data-stu-id="554b6-115">Time is given in ticks, as defined in the *Standard MIDI Files 1.0* specification.</span></span> <span data-ttu-id="554b6-116">La longitud de un paso se define en el formato de hora y, posiblemente, en el tempo asociado a la secuencia.</span><span class="sxs-lookup"><span data-stu-id="554b6-116">The length of a tick is defined by the time format and possibly the tempo associated with the stream.</span></span> <span data-ttu-id="554b6-117">Para obtener más información sobre las secuencias, consulte [MIDI transmisiones](midi-streams.md).</span><span class="sxs-lookup"><span data-stu-id="554b6-117">For more information about streams, see [MIDI Streams](midi-streams.md).</span></span>

<span data-ttu-id="554b6-118">Un paso se expresa como una nota de microsegundos por trimestre o como TICs del tiempo de SMPTE (sociedad de la imagen de movimiento y de ingenieros de televisión).</span><span class="sxs-lookup"><span data-stu-id="554b6-118">A tick is expressed either as microseconds per quarter note or as ticks of SMPTE (Society of Motion Picture and Television Engineers) time.</span></span> <span data-ttu-id="554b6-119">Las aplicaciones que envían mensajes MIDI individualmente o utilizan mensajes MIDI no procesados usan la información del tiempo y el tiempo de la nota del cuarto para determinar la duración de un TIC.</span><span class="sxs-lookup"><span data-stu-id="554b6-119">Applications that send MIDI messages individually or use unprocessed MIDI messages use quarter note time and tempo information to determine the duration of a tick.</span></span> <span data-ttu-id="554b6-120">Las aplicaciones que preprocesan mensajes MIDI pueden almacenar el tiempo transcurrido como un recuento de las unidades SMPTE que se usan.</span><span class="sxs-lookup"><span data-stu-id="554b6-120">Applications that preprocess MIDI messages can store the elapsed time as a count of the SMPTE units being used.</span></span>

<span data-ttu-id="554b6-121">La hora de la nota del trimestre se indica con un cero en el bit de palabra superior (bit 15) de la palabra de la división de hora.</span><span class="sxs-lookup"><span data-stu-id="554b6-121">Quarter note time is indicated with a zero in the high-word bit (bit 15) of the time-division word.</span></span> <span data-ttu-id="554b6-122">El resto de la palabra contiene la nota TICs por trimestre.</span><span class="sxs-lookup"><span data-stu-id="554b6-122">The remainder of the word contains the ticks per quarter note.</span></span> <span data-ttu-id="554b6-123">Un tempo asociado con una secuencia de datos MIDI se mantiene en unidades (microsegundos por cuarto de nota) coherente con la especificación de *los archivos MIDI estándar 1,0* .</span><span class="sxs-lookup"><span data-stu-id="554b6-123">A tempo associated with a stream of MIDI data is kept in units (microseconds per quarter note) consistent with the *Standard MIDI Files 1.0* specification.</span></span> <span data-ttu-id="554b6-124">Por ejemplo, una nota de trimestre en 4/4 de tiempo que usa un tempo de 500.000 microsegundos por cuarto de nota se reproduce a la tarifa de 120 pulsaciones por minuto.</span><span class="sxs-lookup"><span data-stu-id="554b6-124">For example, a quarter note in 4/4 time that uses a tempo of 500,000 microseconds per quarter note plays at the rate of 120 beats per minute.</span></span>

<span data-ttu-id="554b6-125">Los formatos de división de tiempo SMPTE especifican por completo la duración de un TIC sin necesidad de información sobre el tempo.</span><span class="sxs-lookup"><span data-stu-id="554b6-125">SMPTE time division formats completely specify the length of a tick without the need for tempo information.</span></span> <span data-ttu-id="554b6-126">En el uso de formatos de hora SMPTE, las secuencias MIDI se pueden sincronizar con otros eventos SMPTE, como vídeo o audio seccionado.</span><span class="sxs-lookup"><span data-stu-id="554b6-126">In using SMPTE time formats, MIDI sequences can be synchronized with other SMPTE events, such as video or striped audio.</span></span> <span data-ttu-id="554b6-127">La hora SMPTE se indica con un 1 en el bit de orden superior (bit 15) de la palabra de la división de hora.</span><span class="sxs-lookup"><span data-stu-id="554b6-127">SMPTE time is indicated with a 1 in the high-order bit (bit 15) of the time-division word.</span></span> <span data-ttu-id="554b6-128">El resto del byte más significativo especifica el formato SMPTE en uso como valores negativos.</span><span class="sxs-lookup"><span data-stu-id="554b6-128">The rest of the most-significant byte specifies the SMPTE format in use as negative values.</span></span> <span data-ttu-id="554b6-129">Los formatos SMPTE admitidos y sus valores correspondientes (entre paréntesis) son 24 (-24), 25 (-25), 30 (-30) y 30 Drop (-29).</span><span class="sxs-lookup"><span data-stu-id="554b6-129">The supported SMPTE formats and their corresponding values (in parentheses) are 24 (-24), 25 (-25), 30 (-30), and 30 drop (-29).</span></span> <span data-ttu-id="554b6-130">El byte bajo de la palabra de división de hora especifica el número de TICs por fotograma SMPTE.</span><span class="sxs-lookup"><span data-stu-id="554b6-130">The low byte of the time-division word specifies the number of ticks per SMPTE frame.</span></span>

 

 