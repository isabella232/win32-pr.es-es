---
title: Referencia de audio de forma de onda
description: En esta sección se enumeran las funciones, las estructuras y los mensajes asociados con el audio de onda, que se documentan en referencia de multimedia. Estos elementos se agrupan de la siguiente manera.
ms.assetid: 723953f7-b38e-4f24-8d54-9849e013011d
keywords:
- Multimedia de Windows, referencia de audio de onda
- multimedia, referencia de audio de onda
- audio multimedia, referencia de onda
- audio, referencia de onda
- Multimedia de Windows, audio de onda
- multimedia, audio de onda
- audio multimedia, de onda
- audio, de onda
- audio de la onda, referencia
- referencia de audio de onda, acerca de
- referencia de wavefore audio, acerca de
- referencia de audio de la onda, dispositivos auxiliares
- referencia de wavefore audio, dispositivos auxiliares
- referencia de audio de onda, reproducción
- referencia de wavefore audio, reproducción
- referencia de audio de onda, errores
- referencia de wavefore audio, errores
- referencia de audio de onda, abrir
- referencia de wavefore audio, abrir
- referencia de audio de onda, cerrar
- referencia de wavefore audio, cerrar
- referencia de audio de onda, paso
- referencia de wavefore audio, brea
- referencia de audio de onda, volumen
- referencia de wavefore audio, volumen
- referencia de audio de onda, mensajes
- referencia de wavefore audio, mensajes
- referencia de audio de forma de onda, posición actual
- referencia de wavefore audio, posición actual
- referencia de audio de onda, grabación
- referencia de wavefore audio, grabación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c74b37984b2d3fab5dad1ea0df4f1f62dfa1855e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077662"
---
# <a name="waveform-audio-reference"></a><span data-ttu-id="858ad-135">Referencia de audio de forma de onda</span><span class="sxs-lookup"><span data-stu-id="858ad-135">Waveform Audio Reference</span></span>

<span data-ttu-id="858ad-136">En esta sección se enumeran las funciones, las estructuras y los mensajes asociados con el audio de onda, que se documentan en [referencia de multimedia](multimedia-reference.md).</span><span class="sxs-lookup"><span data-stu-id="858ad-136">This section lists the functions, structures, and messages associated with waveform audio, which are documented under [Multimedia Reference](multimedia-reference.md).</span></span> <span data-ttu-id="858ad-137">Estos elementos se agrupan de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="858ad-137">These elements are grouped as follows.</span></span>

## <a name="auxiliary-devices"></a><span data-ttu-id="858ad-138">Dispositivos auxiliares</span><span class="sxs-lookup"><span data-stu-id="858ad-138">Auxiliary Devices</span></span>

-   [<span data-ttu-id="858ad-139">**AUXCAPS**</span><span class="sxs-lookup"><span data-stu-id="858ad-139">**AUXCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps)
-   [<span data-ttu-id="858ad-140">**auxGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="858ad-140">**auxGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)
-   [<span data-ttu-id="858ad-141">**auxGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="858ad-141">**auxGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)
-   [<span data-ttu-id="858ad-142">**auxGetVolume**</span><span class="sxs-lookup"><span data-stu-id="858ad-142">**auxGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxgetvolume)
-   [<span data-ttu-id="858ad-143">**auxOutMessage**</span><span class="sxs-lookup"><span data-stu-id="858ad-143">**auxOutMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxoutmessage)
-   [<span data-ttu-id="858ad-144">**auxSetVolume**</span><span class="sxs-lookup"><span data-stu-id="858ad-144">**auxSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxsetvolume)

## <a name="easy-playback"></a><span data-ttu-id="858ad-145">Reproducción sencilla</span><span class="sxs-lookup"><span data-stu-id="858ad-145">Easy Playback</span></span>

-   <span data-ttu-id="858ad-146">[**Reproducción**](/previous-versions//dd743680(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="858ad-146">[**PlaySound**](/previous-versions//dd743680(v=vs.85))</span></span>
-   <span data-ttu-id="858ad-147">[**sndPlaySound**](/previous-versions//dd798676(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="858ad-147">[**sndPlaySound**](/previous-versions//dd798676(v=vs.85))</span></span>

## <a name="errors"></a><span data-ttu-id="858ad-148">Errors</span><span class="sxs-lookup"><span data-stu-id="858ad-148">Errors</span></span>

-   [<span data-ttu-id="858ad-149">**waveInGetErrorText**</span><span class="sxs-lookup"><span data-stu-id="858ad-149">**waveInGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingeterrortext)
-   [<span data-ttu-id="858ad-150">**waveOutGetErrorText**</span><span class="sxs-lookup"><span data-stu-id="858ad-150">**waveOutGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgeterrortext)

## <a name="opening-and-closing"></a><span data-ttu-id="858ad-151">Abrir y cerrar</span><span class="sxs-lookup"><span data-stu-id="858ad-151">Opening and Closing</span></span>

-   [<span data-ttu-id="858ad-152">**PCMWAVEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="858ad-152">**PCMWAVEFORMAT**</span></span>](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat)
-   [<span data-ttu-id="858ad-153">**MM \_ - \_ cerrar Wim**</span><span class="sxs-lookup"><span data-stu-id="858ad-153">**MM\_WIM\_CLOSE**</span></span>](mm-wim-close.md)
-   [<span data-ttu-id="858ad-154">**MM \_ Wim \_ abierto**</span><span class="sxs-lookup"><span data-stu-id="858ad-154">**MM\_WIM\_OPEN**</span></span>](mm-wim-open.md)
-   [<span data-ttu-id="858ad-155">**cierre de MM \_ WOM \_**</span><span class="sxs-lookup"><span data-stu-id="858ad-155">**MM\_WOM\_CLOSE**</span></span>](mm-wom-close.md)
-   [<span data-ttu-id="858ad-156">**MM \_ WOM \_ abierto**</span><span class="sxs-lookup"><span data-stu-id="858ad-156">**MM\_WOM\_OPEN**</span></span>](mm-wom-open.md)
-   [<span data-ttu-id="858ad-157">**WAVEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="858ad-157">**WAVEFORMAT**</span></span>](/windows/win32/api/mmreg/ns-mmreg-waveformat)
-   [<span data-ttu-id="858ad-158">**WAVEFORMATEX**</span><span class="sxs-lookup"><span data-stu-id="858ad-158">**WAVEFORMATEX**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex)
-   [<span data-ttu-id="858ad-159">**waveInClose**</span><span class="sxs-lookup"><span data-stu-id="858ad-159">**waveInClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose)
-   <span data-ttu-id="858ad-160">[**waveInProc**](/previous-versions//dd743849(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="858ad-160">[**waveInProc**](/previous-versions//dd743849(v=vs.85))</span></span>
-   [<span data-ttu-id="858ad-161">**waveInOpen**</span><span class="sxs-lookup"><span data-stu-id="858ad-161">**waveInOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen)
-   [<span data-ttu-id="858ad-162">**waveOutClose**</span><span class="sxs-lookup"><span data-stu-id="858ad-162">**waveOutClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose)
-   <span data-ttu-id="858ad-163">[**waveOutProc**](/previous-versions//dd743869(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="858ad-163">[**waveOutProc**](/previous-versions//dd743869(v=vs.85))</span></span>
-   [<span data-ttu-id="858ad-164">**waveOutOpen**</span><span class="sxs-lookup"><span data-stu-id="858ad-164">**waveOutOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen)
-   [<span data-ttu-id="858ad-165">**\_cerrar Wim**</span><span class="sxs-lookup"><span data-stu-id="858ad-165">**WIM\_CLOSE**</span></span>](wim-close.md)
-   [<span data-ttu-id="858ad-166">**WIM \_ abierto**</span><span class="sxs-lookup"><span data-stu-id="858ad-166">**WIM\_OPEN**</span></span>](wim-open.md)
-   [<span data-ttu-id="858ad-167">**WOM \_ cerrar**</span><span class="sxs-lookup"><span data-stu-id="858ad-167">**WOM\_CLOSE**</span></span>](wom-close.md)
-   [<span data-ttu-id="858ad-168">**WOM \_ abrir**</span><span class="sxs-lookup"><span data-stu-id="858ad-168">**WOM\_OPEN**</span></span>](wom-open.md)

## <a name="pitch"></a><span data-ttu-id="858ad-169">Inclinación</span><span class="sxs-lookup"><span data-stu-id="858ad-169">Pitch</span></span>

-   [<span data-ttu-id="858ad-170">**waveOutGetPitch**</span><span class="sxs-lookup"><span data-stu-id="858ad-170">**waveOutGetPitch**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetpitch)
-   [<span data-ttu-id="858ad-171">**waveOutSetPitch**</span><span class="sxs-lookup"><span data-stu-id="858ad-171">**waveOutSetPitch**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetpitch)

## <a name="playback-rate"></a><span data-ttu-id="858ad-172">Velocidad de reproducción</span><span class="sxs-lookup"><span data-stu-id="858ad-172">Playback Rate</span></span>

-   [<span data-ttu-id="858ad-173">**waveOutGetPlaybackRate**</span><span class="sxs-lookup"><span data-stu-id="858ad-173">**waveOutGetPlaybackRate**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetplaybackrate)
-   [<span data-ttu-id="858ad-174">**waveOutSetPlaybackRate**</span><span class="sxs-lookup"><span data-stu-id="858ad-174">**waveOutSetPlaybackRate**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetplaybackrate)

## <a name="playback-progress"></a><span data-ttu-id="858ad-175">Progreso de la reproducción</span><span class="sxs-lookup"><span data-stu-id="858ad-175">Playback Progress</span></span>

-   [<span data-ttu-id="858ad-176">**MM \_ WOM \_ listo**</span><span class="sxs-lookup"><span data-stu-id="858ad-176">**MM\_WOM\_DONE**</span></span>](mm-wom-done.md)
-   [<span data-ttu-id="858ad-177">**waveOutBreakLoop**</span><span class="sxs-lookup"><span data-stu-id="858ad-177">**waveOutBreakLoop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop)
-   [<span data-ttu-id="858ad-178">**waveOutPause**</span><span class="sxs-lookup"><span data-stu-id="858ad-178">**waveOutPause**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause)
-   [<span data-ttu-id="858ad-179">**waveOutReset**</span><span class="sxs-lookup"><span data-stu-id="858ad-179">**waveOutReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)
-   [<span data-ttu-id="858ad-180">**waveOutRestart**</span><span class="sxs-lookup"><span data-stu-id="858ad-180">**waveOutRestart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart)
-   [<span data-ttu-id="858ad-181">**WOM \_ completado**</span><span class="sxs-lookup"><span data-stu-id="858ad-181">**WOM\_DONE**</span></span>](wom-done.md)

## <a name="playing"></a><span data-ttu-id="858ad-182">Reproduciendo</span><span class="sxs-lookup"><span data-stu-id="858ad-182">Playing</span></span>

-   [<span data-ttu-id="858ad-183">**MM \_ WOM \_ listo**</span><span class="sxs-lookup"><span data-stu-id="858ad-183">**MM\_WOM\_DONE**</span></span>](mm-wom-done.md)
-   [<span data-ttu-id="858ad-184">**WAVEHDR**</span><span class="sxs-lookup"><span data-stu-id="858ad-184">**WAVEHDR**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)
-   [<span data-ttu-id="858ad-185">**waveOutPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="858ad-185">**waveOutPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)
-   [<span data-ttu-id="858ad-186">**waveOutUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="858ad-186">**waveOutUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader)
-   [<span data-ttu-id="858ad-187">**waveOutWrite**</span><span class="sxs-lookup"><span data-stu-id="858ad-187">**waveOutWrite**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite)
-   [<span data-ttu-id="858ad-188">**WOM \_ completado**</span><span class="sxs-lookup"><span data-stu-id="858ad-188">**WOM\_DONE**</span></span>](wom-done.md)

## <a name="querying-a-device"></a><span data-ttu-id="858ad-189">Consultar un dispositivo</span><span class="sxs-lookup"><span data-stu-id="858ad-189">Querying a Device</span></span>

-   [<span data-ttu-id="858ad-190">**WAVEINCAPS**</span><span class="sxs-lookup"><span data-stu-id="858ad-190">**WAVEINCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)
-   [<span data-ttu-id="858ad-191">**waveInGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="858ad-191">**waveInGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)
-   [<span data-ttu-id="858ad-192">**waveInGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="858ad-192">**waveInGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)
-   [<span data-ttu-id="858ad-193">**WAVEOUTCAPS**</span><span class="sxs-lookup"><span data-stu-id="858ad-193">**WAVEOUTCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)
-   [<span data-ttu-id="858ad-194">**waveOutGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="858ad-194">**waveOutGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps)
-   [<span data-ttu-id="858ad-195">**waveOutGetNumDevs**</span><span class="sxs-lookup"><span data-stu-id="858ad-195">**waveOutGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs)

## <a name="recording"></a><span data-ttu-id="858ad-196">Grabando</span><span class="sxs-lookup"><span data-stu-id="858ad-196">Recording</span></span>

-   [<span data-ttu-id="858ad-197">**\_datos Wim \_ mm**</span><span class="sxs-lookup"><span data-stu-id="858ad-197">**MM\_WIM\_DATA**</span></span>](mm-wim-data.md)
-   [<span data-ttu-id="858ad-198">**waveInAddBuffer**</span><span class="sxs-lookup"><span data-stu-id="858ad-198">**waveInAddBuffer**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer)
-   [<span data-ttu-id="858ad-199">**waveInPrepareHeader**</span><span class="sxs-lookup"><span data-stu-id="858ad-199">**waveInPrepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader)
-   [<span data-ttu-id="858ad-200">**waveInReset**</span><span class="sxs-lookup"><span data-stu-id="858ad-200">**waveInReset**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)
-   [<span data-ttu-id="858ad-201">**waveInStart**</span><span class="sxs-lookup"><span data-stu-id="858ad-201">**waveInStart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)
-   [<span data-ttu-id="858ad-202">**waveInStop**</span><span class="sxs-lookup"><span data-stu-id="858ad-202">**waveInStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinstop)
-   [<span data-ttu-id="858ad-203">**waveInUnprepareHeader**</span><span class="sxs-lookup"><span data-stu-id="858ad-203">**waveInUnprepareHeader**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader)
-   [<span data-ttu-id="858ad-204">**\_datos Wim**</span><span class="sxs-lookup"><span data-stu-id="858ad-204">**WIM\_DATA**</span></span>](wim-data.md)

## <a name="retrieving-device-identifiers"></a><span data-ttu-id="858ad-205">Recuperando identificadores de dispositivo</span><span class="sxs-lookup"><span data-stu-id="858ad-205">Retrieving Device Identifiers</span></span>

-   [<span data-ttu-id="858ad-206">**waveInGetID**</span><span class="sxs-lookup"><span data-stu-id="858ad-206">**waveInGetID**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingetid)
-   [<span data-ttu-id="858ad-207">**waveOutGetID**</span><span class="sxs-lookup"><span data-stu-id="858ad-207">**waveOutGetID**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetid)

## <a name="retrieving-the-current-position"></a><span data-ttu-id="858ad-208">Recuperar la posición actual</span><span class="sxs-lookup"><span data-stu-id="858ad-208">Retrieving the Current Position</span></span>

-   [<span data-ttu-id="858ad-209">**waveInGetPosition**</span><span class="sxs-lookup"><span data-stu-id="858ad-209">**waveInGetPosition**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingetposition)
-   [<span data-ttu-id="858ad-210">**waveOutGetPosition**</span><span class="sxs-lookup"><span data-stu-id="858ad-210">**waveOutGetPosition**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition)

## <a name="sending-custom-messages"></a><span data-ttu-id="858ad-211">Envío de mensajes personalizados</span><span class="sxs-lookup"><span data-stu-id="858ad-211">Sending Custom Messages</span></span>

-   [<span data-ttu-id="858ad-212">**waveInMessage**</span><span class="sxs-lookup"><span data-stu-id="858ad-212">**waveInMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveinmessage)
-   [<span data-ttu-id="858ad-213">**waveOutMessage**</span><span class="sxs-lookup"><span data-stu-id="858ad-213">**waveOutMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutmessage)

## <a name="volume"></a><span data-ttu-id="858ad-214">Volumen</span><span class="sxs-lookup"><span data-stu-id="858ad-214">Volume</span></span>

-   [<span data-ttu-id="858ad-215">**waveOutGetVolume**</span><span class="sxs-lookup"><span data-stu-id="858ad-215">**waveOutGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetvolume)
-   [<span data-ttu-id="858ad-216">**waveOutSetVolume**</span><span class="sxs-lookup"><span data-stu-id="858ad-216">**waveOutSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetvolume)

## <a name="related-topics"></a><span data-ttu-id="858ad-217">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="858ad-217">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="858ad-218">Audio de onda</span><span class="sxs-lookup"><span data-stu-id="858ad-218">Waveform Audio</span></span>](waveform-audio.md)
</dt> </dl>

 

 