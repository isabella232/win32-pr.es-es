---
title: Referencia de audio de forma de onda
description: En esta sección se enumeran las funciones, estructuras y mensajes asociados al audio de forma de onda, que se documentan en Referencia multimedia. Estos elementos se agrupan como se muestra a continuación.
ms.assetid: 723953f7-b38e-4f24-8d54-9849e013011d
keywords:
- Windows multimedia, referencia de audio de forma de onda
- multimedia, referencia de audio de forma de onda
- audio multimedia, referencia de forma de onda
- audio, referencia de forma de onda
- Windows multimedia, audio de forma de onda
- multimedia, audio de forma de onda
- audio multimedia, forma de onda
- audio, forma de onda
- audio de forma de onda, referencia
- referencia de audio de forma de onda, acerca de
- referencia de audio wavefore, acerca de
- referencia de audio de forma de onda, dispositivos auxiliares
- referencia de audio wavefore, dispositivos auxiliares
- referencia de audio de forma de onda, reproducción
- referencia de audio wavefore, reproducción
- referencia de audio de forma de onda, errores
- referencia de audio wavefore, errores
- referencia de audio de forma de onda, apertura
- referencia de audio wavefore, apertura
- referencia de audio de forma de onda, cierre
- referencia de audio wavefore, cierre
- referencia de audio de forma de onda, pitch
- referencia de audio wavefore, pitch
- referencia de audio de forma de onda, volumen
- referencia de audio wavefore, volumen
- referencia de audio de forma de onda, mensajes
- referencia de audio wavefore, mensajes
- referencia de audio de forma de onda, posición actual
- referencia de audio wavefore, posición actual
- referencia de audio de forma de onda, grabación
- referencia de audio wavefore, grabación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c74b37984b2d3fab5dad1ea0df4f1f62dfa1855e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071702"
---
# <a name="waveform-audio-reference"></a>Referencia de audio de forma de onda

En esta sección se enumeran las funciones, estructuras y mensajes asociados al audio de forma de onda, que se documentan en [Referencia multimedia.](multimedia-reference.md) Estos elementos se agrupan como se muestra a continuación.

## <a name="auxiliary-devices"></a>Dispositivos auxiliares

-   [**AUXCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps)
-   [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)
-   [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)
-   [**auxGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetvolume)
-   [**auxOutMessage**](/windows/win32/api/mmeapi/nf-mmeapi-auxoutmessage)
-   [**auxSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-auxsetvolume)

## <a name="easy-playback"></a>Reproducción sencilla

-   [**PlaySound**](/previous-versions//dd743680(v=vs.85))
-   [**sndPlaySound**](/previous-versions//dd798676(v=vs.85))

## <a name="errors"></a>Errors

-   [**waveInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-waveingeterrortext)
-   [**waveOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgeterrortext)

## <a name="opening-and-closing"></a>Apertura y cierre

-   [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat)
-   [**MM \_ WIM \_ CLOSE**](mm-wim-close.md)
-   [**MM \_ WIM \_ OPEN**](mm-wim-open.md)
-   [**MM \_ WOM \_ CLOSE**](mm-wom-close.md)
-   [**MM \_ WOM \_ OPEN**](mm-wom-open.md)
-   [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat)
-   [**FORMA DE ONDAATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex)
-   [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose)
-   [**waveInProc**](/previous-versions//dd743849(v=vs.85))
-   [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen)
-   [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose)
-   [**waveOutProc**](/previous-versions//dd743869(v=vs.85))
-   [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen)
-   [**WIM \_ CLOSE**](wim-close.md)
-   [**WIM \_ OPEN**](wim-open.md)
-   [**WOM \_ CLOSE**](wom-close.md)
-   [**WOM \_ OPEN**](wom-open.md)

## <a name="pitch"></a>Inclinación

-   [**waveOutGetPitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetpitch)
-   [**waveOutSetPjunto**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetpitch)

## <a name="playback-rate"></a>Velocidad de reproducción

-   [**waveOutGetPlaybackRate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetplaybackrate)
-   [**waveOutSetPlaybackRate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetplaybackrate)

## <a name="playback-progress"></a>Progreso de reproducción

-   [**MM \_ WOM \_ DONE**](mm-wom-done.md)
-   [**waveOutBreakLoop**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop)
-   [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause)
-   [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)
-   [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart)
-   [**WOM \_ DONE**](wom-done.md)

## <a name="playing"></a>Reproduciendo

-   [**MM \_ WOM \_ DONE**](mm-wom-done.md)
-   [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)
-   [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)
-   [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader)
-   [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite)
-   [**WOM \_ DONE**](wom-done.md)

## <a name="querying-a-device"></a>Consulta de un dispositivo

-   [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)
-   [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)
-   [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)
-   [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)
-   [**waveOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps)
-   [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs)

## <a name="recording"></a>Grabación

-   [**MM \_ WIM \_ DATA**](mm-wim-data.md)
-   [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer)
-   [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader)
-   [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)
-   [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)
-   [**waveInStop**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstop)
-   [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader)
-   [**DATOS \_ DE WIM**](wim-data.md)

## <a name="retrieving-device-identifiers"></a>Recuperar identificadores de dispositivo

-   [**waveInGetID**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetid)
-   [**waveOutGetID**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetid)

## <a name="retrieving-the-current-position"></a>Recuperar la posición actual

-   [**waveInGetPosition**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetposition)
-   [**waveOutGetPosition**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition)

## <a name="sending-custom-messages"></a>Envío de mensajes personalizados

-   [**waveInMessage**](/windows/win32/api/mmeapi/nf-mmeapi-waveinmessage)
-   [**waveOutMessage**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutmessage)

## <a name="volume"></a>Volumen

-   [**waveOutGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetvolume)
-   [**waveOutSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetvolume)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Audio de forma de onda](waveform-audio.md)
</dt> </dl>

 

 