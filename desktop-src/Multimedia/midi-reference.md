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
# <a name="midi-reference"></a>Referencia MIDI

En esta sección se describen las funciones, macros, mensajes y estructuras asociadas a la interfaz digital de instrumentos musicales (MIDI). Estos elementos se agrupan de la siguiente manera.

## <a name="allocating-and-managing-buffers"></a>Asignación y administración de búferes

-   [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)
-   [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)
-   [**midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader)
-   [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader)
-   [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader)
-   [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader)

## <a name="callback-functions"></a>Funciones de devolución de llamada

-   [**MidiInProc**](/previous-versions//dd798460(v=vs.85))
-   [**MidiOutProc**](/previous-versions//dd798478(v=vs.85))

## <a name="device-capabilities"></a>Capacidades del dispositivo

-   [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps)
-   [**midiInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps)
-   [**midiInGetID**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetid)
-   [**midiInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs)
-   [**MIDIOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps)
-   [**midiOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps)
-   [**midiOutGetID**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetid)
-   [**midiOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs)
-   [**MIDISTRMBUFFVER**](/windows/win32/api/mmeapi/ns-mmeapi-midistrmbuffver)

## <a name="error-processing"></a>Procesamiento de errores

-   [**midiInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext)
-   [**midiOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext)
-   [**ERROR de MIM \_**](mim-error.md)
-   [**LONGERROR de MIM \_**](mim-longerror.md)
-   [**\_error de MIM de mm \_**](mm-mim-error.md)
-   [**MM \_ MIM \_ LONGERROR**](mm-mim-longerror.md)

## <a name="managing-midi-streams"></a>Administración de flujos MIDI

-   [**midiStreamClose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)
-   [**midiStreamOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen)
-   [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)
-   [**midiStreamPause**](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)
-   [**midiStreamPosition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition)
-   [**midiStreamProperty**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamproperty)
-   [**midiStreamRestart**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)
-   [**midiStreamStop**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)

## <a name="opening-and-closing-devices"></a>Apertura y cierre de dispositivos

-   [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)
-   [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)
-   [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose)
-   [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)
-   [**cierre de MIM \_**](mim-close.md)
-   [**MIM \_ abierto**](mim-open.md)
-   [**MM \_ cierre de MIM \_**](mm-mim-close.md)
-   [**MM \_ MIM \_ abierto**](mm-mim-open.md)
-   [**cierre de MM \_ MOM \_**](mm-mom-close.md)
-   [**MM \_ MOM \_ abierto**](mm-mom-open.md)
-   [**cierre de MOM \_**](mom-close.md)
-   [**abierto de MOM \_**](mom-open.md)

## <a name="output-devices"></a>Dispositivos de salida

-   [KEYARRAY](keyarray.md)
-   [**midiOutCacheDrumPatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachedrumpatches)
-   [**midiOutCachePatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachepatches)
-   [**midiOutGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetvolume)
-   [**midiOutSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutsetvolume)
-   [PATCHARRAY](patcharray.md)

## <a name="playing-a-message-or-messages"></a>Reproducir mensajes o mensajes

-   [**MEVT \_ EVENTPARM**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm)
-   [**MEVT \_ EVENTTYPE**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype)
-   [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent)
-   [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)
-   [**midiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)
-   [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg)
-   [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)
-   [**midiStreamPause**](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)
-   [**midiStreamRestart**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)
-   [**midiStreamStop**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)
-   [**MM \_ MOM \_ listo**](mm-mom-done.md)
-   [**MM \_ MOM \_ POSITIONCB**](mm-mom-positioncb.md)
-   [**MOM \_ Done**](mom-done.md)
-   [**MOM \_ POSITIONCB**](mom-positioncb.md)

## <a name="recording"></a>Grabando

-   [**midiConnect**](/windows/win32/api/mmeapi/nf-mmeapi-midiconnect)
-   [**midiDisconnect**](/windows/win32/api/mmeapi/nf-mmeapi-mididisconnect)
-   [**midiInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)
-   [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)
-   [**midiInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)
-   [**MIDIPROPTEMPO**](/windows/win32/api/mmeapi/ns-mmeapi-midiproptempo)
-   [**MIDIPROPTIMEDIV**](/windows/win32/api/mmeapi/ns-mmeapi-midiproptimediv)
-   [**datos de MIM \_**](mim-data.md)
-   [**LONGDATA de MIM \_**](mim-longdata.md)
-   [**MOREDATA de MIM \_**](mim-moredata.md)
-   [**\_datos de MIM mm \_**](mm-mim-data.md)
-   [**MM \_ MIM \_ MOREDATA**](mm-mim-moredata.md)
-   [**MM \_ MIM \_ LONGDATA**](mm-mim-longdata.md)

## <a name="sending-messages-to-devices"></a>Envío de mensajes a dispositivos

-   [**midiInMessage**](/windows/win32/api/mmeapi/nf-mmeapi-midiinmessage)
-   [**midiOutMessage**](/windows/win32/api/mmeapi/nf-mmeapi-midioutmessage)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaz digital de instrumentos digitales (MIDI)](musical-instrument-digital-interface--midi.md)
</dt> </dl>

 

 