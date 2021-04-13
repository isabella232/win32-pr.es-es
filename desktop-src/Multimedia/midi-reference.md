---
title: Referencia MIDI
description: Referencia MIDI
ms.assetid: 6229a4a7-be42-4e2a-af9d-695c4759a4ef
keywords:
- Windows multimedia, interfaz digital de instrumentos musicales (MIDI)
- multimedia, interfaz digital de instrumentos musicales (MIDI)
- audio multimedia, interfaz digital de instrumentos musicales (MIDI)
- audio, interfaz digital de instrumentos musicales (MIDI)
- Windows multimedia, referencia MIDI
- multimedia, referencia MIDI
- audio multimedia, referencia MIDI
- audio, referencia MIDI
- Interfaz digital de instrumentos musicales (MIDI), referencia
- MIDI (interfaz digital de instrumentos musicales), referencia
- referencia de MIDI, acerca de
- Referencia MIDI, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c21542867faf1e09d68dc4fc81a50d25f56b5c5e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420660"
---
# <a name="midi-reference"></a><span data-ttu-id="d46ab-115">Referencia MIDI</span><span class="sxs-lookup"><span data-stu-id="d46ab-115">MIDI Reference</span></span>

<span data-ttu-id="d46ab-116">En esta sección se describen las funciones, macros, mensajes y estructuras asociadas a la interfaz digital de instrumentos musicales (MIDI).</span><span class="sxs-lookup"><span data-stu-id="d46ab-116">This section describes the functions, macros, messages, and structures associated with the Musical Instrument Digital Interface (MIDI).</span></span> <span data-ttu-id="d46ab-117">Estos elementos se agrupan de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="d46ab-117">These elements are grouped as follows.</span></span>

## <a name="allocating-and-managing-buffers"></a><span data-ttu-id="d46ab-118">Asignación y administración de búferes</span><span class="sxs-lookup"><span data-stu-id="d46ab-118">Allocating and Managing Buffers</span></span>

-   [<span data-ttu-id="d46ab-119">**MIDIHDR**</span><span class="sxs-lookup"><span data-stu-id="d46ab-119">**MIDIHDR**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)
-   [<span data-ttu-id="d46ab-120">**midiInAddBuffer**</span><span class="sxs-lookup"><span data-stu-id="d46ab-120">**midiInAddBuffer**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)
-   [<span data-ttu-id="d46ab-121">**midiInPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="d46ab-121">**midiInPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader)
-   [<span data-ttu-id="d46ab-122">**midiInUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="d46ab-122">**midiInUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader)
-   [<span data-ttu-id="d46ab-123">**midiOutPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="d46ab-123">**midiOutPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader)
-   [<span data-ttu-id="d46ab-124">**midiOutUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="d46ab-124">**midiOutUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader)

## <a name="callback-functions"></a><span data-ttu-id="d46ab-125">Funciones de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="d46ab-125">Callback Functions</span></span>

-   <span data-ttu-id="d46ab-126">[**MidiInProc**](/previous-versions//dd798460(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d46ab-126">[**MidiInProc**](/previous-versions//dd798460(v=vs.85))</span></span>
-   <span data-ttu-id="d46ab-127">[**MidiOutProc**](/previous-versions//dd798478(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d46ab-127">[**MidiOutProc**](/previous-versions//dd798478(v=vs.85))</span></span>

## <a name="device-capabilities"></a><span data-ttu-id="d46ab-128">Capacidades del dispositivo</span><span class="sxs-lookup"><span data-stu-id="d46ab-128">Device Capabilities</span></span>

-   [<span data-ttu-id="d46ab-129">**MIDIINCAPS**</span><span class="sxs-lookup"><span data-stu-id="d46ab-129">**MIDIINCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps)
-   [<span data-ttu-id="d46ab-130">**midiInGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="d46ab-130">**midiInGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps)
-   [<span data-ttu-id="d46ab-131">**midiInGetID**</span><span class="sxs-lookup"><span data-stu-id="d46ab-131">**midiInGetID**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetid)
-   [<span data-ttu-id="d46ab-132">**midiInGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="d46ab-132">**midiInGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs)
-   [<span data-ttu-id="d46ab-133">**MIDIOUTCAPS**</span><span class="sxs-lookup"><span data-stu-id="d46ab-133">**MIDIOUTCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps)
-   [<span data-ttu-id="d46ab-134">**midiOutGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="d46ab-134">**midiOutGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps)
-   [<span data-ttu-id="d46ab-135">**midiOutGetID**</span><span class="sxs-lookup"><span data-stu-id="d46ab-135">**midiOutGetID**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetid)
-   [<span data-ttu-id="d46ab-136">**midiOutGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="d46ab-136">**midiOutGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs)
-   [<span data-ttu-id="d46ab-137">**MIDISTRMBUFFVER**</span><span class="sxs-lookup"><span data-stu-id="d46ab-137">**MIDISTRMBUFFVER**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midistrmbuffver)

## <a name="error-processing"></a><span data-ttu-id="d46ab-138">Procesamiento de errores</span><span class="sxs-lookup"><span data-stu-id="d46ab-138">Error Processing</span></span>

-   [<span data-ttu-id="d46ab-139">**midiInGetErrorText**</span><span class="sxs-lookup"><span data-stu-id="d46ab-139">**midiInGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext)
-   [<span data-ttu-id="d46ab-140">**midiOutGetErrorText**</span><span class="sxs-lookup"><span data-stu-id="d46ab-140">**midiOutGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext)
-   [<span data-ttu-id="d46ab-141">**ERROR de MIM \_**</span><span class="sxs-lookup"><span data-stu-id="d46ab-141">**MIM\_ERROR**</span></span>](mim-error.md)
-   [<span data-ttu-id="d46ab-142">**LONGERROR de MIM \_**</span><span class="sxs-lookup"><span data-stu-id="d46ab-142">**MIM\_LONGERROR**</span></span>](mim-longerror.md)
-   [<span data-ttu-id="d46ab-143">**\_error de MIM de mm \_**</span><span class="sxs-lookup"><span data-stu-id="d46ab-143">**MM\_MIM\_ERROR**</span></span>](mm-mim-error.md)
-   [<span data-ttu-id="d46ab-144">**MM \_ MIM \_ LONGERROR**</span><span class="sxs-lookup"><span data-stu-id="d46ab-144">**MM\_MIM\_LONGERROR**</span></span>](mm-mim-longerror.md)

## <a name="managing-midi-streams"></a><span data-ttu-id="d46ab-145">Administración de flujos MIDI</span><span class="sxs-lookup"><span data-stu-id="d46ab-145">Managing MIDI Streams</span></span>

-   [<span data-ttu-id="d46ab-146">**midiStreamClose**</span><span class="sxs-lookup"><span data-stu-id="d46ab-146">**midiStreamClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)
-   [<span data-ttu-id="d46ab-147">**midiStreamOpen**</span><span class="sxs-lookup"><span data-stu-id="d46ab-147">**midiStreamOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen)
-   [<span data-ttu-id="d46ab-148">**midiStreamOut**</span><span class="sxs-lookup"><span data-stu-id="d46ab-148">**midiStreamOut**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)
-   [<span data-ttu-id="d46ab-149">**midiStreamPause**</span><span class="sxs-lookup"><span data-stu-id="d46ab-149">**midiStreamPause**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)
-   [<span data-ttu-id="d46ab-150">**midiStreamPosition**</span><span class="sxs-lookup"><span data-stu-id="d46ab-150">**midiStreamPosition**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition)
-   [<span data-ttu-id="d46ab-151">**midiStreamProperty**</span><span class="sxs-lookup"><span data-stu-id="d46ab-151">**midiStreamProperty**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamproperty)
-   [<span data-ttu-id="d46ab-152">**midiStreamRestart**</span><span class="sxs-lookup"><span data-stu-id="d46ab-152">**midiStreamRestart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)
-   [<span data-ttu-id="d46ab-153">**midiStreamStop**</span><span class="sxs-lookup"><span data-stu-id="d46ab-153">**midiStreamStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)

## <a name="opening-and-closing-devices"></a><span data-ttu-id="d46ab-154">Apertura y cierre de dispositivos</span><span class="sxs-lookup"><span data-stu-id="d46ab-154">Opening and Closing Devices</span></span>

-   [<span data-ttu-id="d46ab-155">**midiInClose**</span><span class="sxs-lookup"><span data-stu-id="d46ab-155">**midiInClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)
-   [<span data-ttu-id="d46ab-156">**midiInOpen**</span><span class="sxs-lookup"><span data-stu-id="d46ab-156">**midiInOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)
-   [<span data-ttu-id="d46ab-157">**midiOutClose**</span><span class="sxs-lookup"><span data-stu-id="d46ab-157">**midiOutClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose)
-   [<span data-ttu-id="d46ab-158">**midiOutOpen**</span><span class="sxs-lookup"><span data-stu-id="d46ab-158">**midiOutOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)
-   [<span data-ttu-id="d46ab-159">**cierre de MIM \_**</span><span class="sxs-lookup"><span data-stu-id="d46ab-159">**MIM\_CLOSE**</span></span>](mim-close.md)
-   [<span data-ttu-id="d46ab-160">**MIM \_ abierto**</span><span class="sxs-lookup"><span data-stu-id="d46ab-160">**MIM\_OPEN**</span></span>](mim-open.md)
-   [<span data-ttu-id="d46ab-161">**MM \_ cierre de MIM \_**</span><span class="sxs-lookup"><span data-stu-id="d46ab-161">**MM\_MIM\_CLOSE**</span></span>](mm-mim-close.md)
-   [<span data-ttu-id="d46ab-162">**MM \_ MIM \_ abierto**</span><span class="sxs-lookup"><span data-stu-id="d46ab-162">**MM\_MIM\_OPEN**</span></span>](mm-mim-open.md)
-   [<span data-ttu-id="d46ab-163">**cierre de MM \_ MOM \_**</span><span class="sxs-lookup"><span data-stu-id="d46ab-163">**MM\_MOM\_CLOSE**</span></span>](mm-mom-close.md)
-   [<span data-ttu-id="d46ab-164">**MM \_ MOM \_ abierto**</span><span class="sxs-lookup"><span data-stu-id="d46ab-164">**MM\_MOM\_OPEN**</span></span>](mm-mom-open.md)
-   [<span data-ttu-id="d46ab-165">**cierre de MOM \_**</span><span class="sxs-lookup"><span data-stu-id="d46ab-165">**MOM\_CLOSE**</span></span>](mom-close.md)
-   [<span data-ttu-id="d46ab-166">**abierto de MOM \_**</span><span class="sxs-lookup"><span data-stu-id="d46ab-166">**MOM\_OPEN**</span></span>](mom-open.md)

## <a name="output-devices"></a><span data-ttu-id="d46ab-167">Dispositivos de salida</span><span class="sxs-lookup"><span data-stu-id="d46ab-167">Output Devices</span></span>

-   [<span data-ttu-id="d46ab-168">KEYARRAY</span><span class="sxs-lookup"><span data-stu-id="d46ab-168">KEYARRAY</span></span>](keyarray.md)
-   [<span data-ttu-id="d46ab-169">**midiOutCacheDrumPatches**</span><span class="sxs-lookup"><span data-stu-id="d46ab-169">**midiOutCacheDrumPatches**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachedrumpatches)
-   [<span data-ttu-id="d46ab-170">**midiOutCachePatches**</span><span class="sxs-lookup"><span data-stu-id="d46ab-170">**midiOutCachePatches**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachepatches)
-   [<span data-ttu-id="d46ab-171">**midiOutGetVolume**</span><span class="sxs-lookup"><span data-stu-id="d46ab-171">**midiOutGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetvolume)
-   [<span data-ttu-id="d46ab-172">**midiOutSetVolume**</span><span class="sxs-lookup"><span data-stu-id="d46ab-172">**midiOutSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutsetvolume)
-   [<span data-ttu-id="d46ab-173">PATCHARRAY</span><span class="sxs-lookup"><span data-stu-id="d46ab-173">PATCHARRAY</span></span>](patcharray.md)

## <a name="playing-a-message-or-messages"></a><span data-ttu-id="d46ab-174">Reproducir mensajes o mensajes</span><span class="sxs-lookup"><span data-stu-id="d46ab-174">Playing a Message or Messages</span></span>

-   [<span data-ttu-id="d46ab-175">**MEVT \_ EVENTPARM**</span><span class="sxs-lookup"><span data-stu-id="d46ab-175">**MEVT\_EVENTPARM**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm)
-   [<span data-ttu-id="d46ab-176">**MEVT \_ EVENTTYPE**</span><span class="sxs-lookup"><span data-stu-id="d46ab-176">**MEVT\_EVENTTYPE**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype)
-   [<span data-ttu-id="d46ab-177">**MIDIEVENT**</span><span class="sxs-lookup"><span data-stu-id="d46ab-177">**MIDIEVENT**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midievent)
-   [<span data-ttu-id="d46ab-178">**midiOutLongMsg**</span><span class="sxs-lookup"><span data-stu-id="d46ab-178">**midiOutLongMsg**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)
-   [<span data-ttu-id="d46ab-179">**midiOutReset**</span><span class="sxs-lookup"><span data-stu-id="d46ab-179">**midiOutReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)
-   [<span data-ttu-id="d46ab-180">**midiOutShortMsg**</span><span class="sxs-lookup"><span data-stu-id="d46ab-180">**midiOutShortMsg**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg)
-   [<span data-ttu-id="d46ab-181">**midiStreamOut**</span><span class="sxs-lookup"><span data-stu-id="d46ab-181">**midiStreamOut**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)
-   [<span data-ttu-id="d46ab-182">**midiStreamPause**</span><span class="sxs-lookup"><span data-stu-id="d46ab-182">**midiStreamPause**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)
-   [<span data-ttu-id="d46ab-183">**midiStreamRestart**</span><span class="sxs-lookup"><span data-stu-id="d46ab-183">**midiStreamRestart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)
-   [<span data-ttu-id="d46ab-184">**midiStreamStop**</span><span class="sxs-lookup"><span data-stu-id="d46ab-184">**midiStreamStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)
-   [<span data-ttu-id="d46ab-185">**MM \_ MOM \_ listo**</span><span class="sxs-lookup"><span data-stu-id="d46ab-185">**MM\_MOM\_DONE**</span></span>](mm-mom-done.md)
-   [<span data-ttu-id="d46ab-186">**MM \_ MOM \_ POSITIONCB**</span><span class="sxs-lookup"><span data-stu-id="d46ab-186">**MM\_MOM\_POSITIONCB**</span></span>](mm-mom-positioncb.md)
-   [<span data-ttu-id="d46ab-187">**MOM \_ Done**</span><span class="sxs-lookup"><span data-stu-id="d46ab-187">**MOM\_DONE**</span></span>](mom-done.md)
-   [<span data-ttu-id="d46ab-188">**MOM \_ POSITIONCB**</span><span class="sxs-lookup"><span data-stu-id="d46ab-188">**MOM\_POSITIONCB**</span></span>](mom-positioncb.md)

## <a name="recording"></a><span data-ttu-id="d46ab-189">Grabando</span><span class="sxs-lookup"><span data-stu-id="d46ab-189">Recording</span></span>

-   [<span data-ttu-id="d46ab-190">**midiConnect**</span><span class="sxs-lookup"><span data-stu-id="d46ab-190">**midiConnect**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiconnect)
-   [<span data-ttu-id="d46ab-191">**midiDisconnect**</span><span class="sxs-lookup"><span data-stu-id="d46ab-191">**midiDisconnect**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mididisconnect)
-   [<span data-ttu-id="d46ab-192">**midiInReset**</span><span class="sxs-lookup"><span data-stu-id="d46ab-192">**midiInReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)
-   [<span data-ttu-id="d46ab-193">**midiInStart**</span><span class="sxs-lookup"><span data-stu-id="d46ab-193">**midiInStart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)
-   [<span data-ttu-id="d46ab-194">**midiInStop**</span><span class="sxs-lookup"><span data-stu-id="d46ab-194">**midiInStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)
-   [<span data-ttu-id="d46ab-195">**MIDIPROPTEMPO**</span><span class="sxs-lookup"><span data-stu-id="d46ab-195">**MIDIPROPTEMPO**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midiproptempo)
-   [<span data-ttu-id="d46ab-196">**MIDIPROPTIMEDIV**</span><span class="sxs-lookup"><span data-stu-id="d46ab-196">**MIDIPROPTIMEDIV**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-midiproptimediv)
-   [<span data-ttu-id="d46ab-197">**datos de MIM \_**</span><span class="sxs-lookup"><span data-stu-id="d46ab-197">**MIM\_DATA**</span></span>](mim-data.md)
-   [<span data-ttu-id="d46ab-198">**LONGDATA de MIM \_**</span><span class="sxs-lookup"><span data-stu-id="d46ab-198">**MIM\_LONGDATA**</span></span>](mim-longdata.md)
-   [<span data-ttu-id="d46ab-199">**MOREDATA de MIM \_**</span><span class="sxs-lookup"><span data-stu-id="d46ab-199">**MIM\_MOREDATA**</span></span>](mim-moredata.md)
-   [<span data-ttu-id="d46ab-200">**\_datos de MIM mm \_**</span><span class="sxs-lookup"><span data-stu-id="d46ab-200">**MM\_MIM\_DATA**</span></span>](mm-mim-data.md)
-   [<span data-ttu-id="d46ab-201">**MM \_ MIM \_ MOREDATA**</span><span class="sxs-lookup"><span data-stu-id="d46ab-201">**MM\_MIM\_MOREDATA**</span></span>](mm-mim-moredata.md)
-   [<span data-ttu-id="d46ab-202">**MM \_ MIM \_ LONGDATA**</span><span class="sxs-lookup"><span data-stu-id="d46ab-202">**MM\_MIM\_LONGDATA**</span></span>](mm-mim-longdata.md)

## <a name="sending-messages-to-devices"></a><span data-ttu-id="d46ab-203">Envío de mensajes a dispositivos</span><span class="sxs-lookup"><span data-stu-id="d46ab-203">Sending Messages to Devices</span></span>

-   [<span data-ttu-id="d46ab-204">**midiInMessage**</span><span class="sxs-lookup"><span data-stu-id="d46ab-204">**midiInMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midiinmessage)
-   [<span data-ttu-id="d46ab-205">**midiOutMessage**</span><span class="sxs-lookup"><span data-stu-id="d46ab-205">**midiOutMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutmessage)

## <a name="related-topics"></a><span data-ttu-id="d46ab-206">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d46ab-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d46ab-207">Interfaz digital de instrumentos digitales (MIDI)</span><span class="sxs-lookup"><span data-stu-id="d46ab-207">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> </dl>

 

 