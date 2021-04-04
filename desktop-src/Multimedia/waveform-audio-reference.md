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
# <a name="waveform-audio-reference"></a>Referencia de audio de forma de onda

En esta sección se enumeran las funciones, las estructuras y los mensajes asociados con el audio de onda, que se documentan en [referencia de multimedia](multimedia-reference.md). Estos elementos se agrupan de la siguiente manera.

## <a name="auxiliary-devices"></a>Dispositivos auxiliares

-   [**AUXCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps)
-   [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)
-   [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)
-   [**auxGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetvolume)
-   [**auxOutMessage**](/windows/win32/api/mmeapi/nf-mmeapi-auxoutmessage)
-   [**auxSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-auxsetvolume)

## <a name="easy-playback"></a>Reproducción sencilla

-   [**Reproducción**](/previous-versions//dd743680(v=vs.85))
-   [**sndPlaySound**](/previous-versions//dd798676(v=vs.85))

## <a name="errors"></a>Errors

-   [**waveInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-waveingeterrortext)
-   [**waveOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgeterrortext)

## <a name="opening-and-closing"></a>Abrir y cerrar

-   [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat)
-   [**MM \_ - \_ cerrar Wim**](mm-wim-close.md)
-   [**MM \_ Wim \_ abierto**](mm-wim-open.md)
-   [**cierre de MM \_ WOM \_**](mm-wom-close.md)
-   [**MM \_ WOM \_ abierto**](mm-wom-open.md)
-   [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat)
-   [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex)
-   [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose)
-   [**waveInProc**](/previous-versions//dd743849(v=vs.85))
-   [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen)
-   [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose)
-   [**waveOutProc**](/previous-versions//dd743869(v=vs.85))
-   [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen)
-   [**\_cerrar Wim**](wim-close.md)
-   [**WIM \_ abierto**](wim-open.md)
-   [**WOM \_ cerrar**](wom-close.md)
-   [**WOM \_ abrir**](wom-open.md)

## <a name="pitch"></a>Inclinación

-   [**waveOutGetPitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetpitch)
-   [**waveOutSetPitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetpitch)

## <a name="playback-rate"></a>Velocidad de reproducción

-   [**waveOutGetPlaybackRate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetplaybackrate)
-   [**waveOutSetPlaybackRate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetplaybackrate)

## <a name="playback-progress"></a>Progreso de la reproducción

-   [**MM \_ WOM \_ listo**](mm-wom-done.md)
-   [**waveOutBreakLoop**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop)
-   [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause)
-   [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)
-   [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart)
-   [**WOM \_ completado**](wom-done.md)

## <a name="playing"></a>Reproduciendo

-   [**MM \_ WOM \_ listo**](mm-wom-done.md)
-   [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)
-   [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)
-   [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader)
-   [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite)
-   [**WOM \_ completado**](wom-done.md)

## <a name="querying-a-device"></a>Consultar un dispositivo

-   [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)
-   [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)
-   [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)
-   [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)
-   [**waveOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps)
-   [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs)

## <a name="recording"></a>Grabando

-   [**\_datos Wim \_ mm**](mm-wim-data.md)
-   [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer)
-   [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader)
-   [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)
-   [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)
-   [**waveInStop**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstop)
-   [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader)
-   [**\_datos Wim**](wim-data.md)

## <a name="retrieving-device-identifiers"></a>Recuperando identificadores de dispositivo

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

[Audio de onda](waveform-audio.md)
</dt> </dl>

 

 