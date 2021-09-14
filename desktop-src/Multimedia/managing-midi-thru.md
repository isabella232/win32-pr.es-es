---
title: Administración de la a través de MIDI
description: Administración de la a través de MIDI
ms.assetid: ba03a2a1-d998-498d-ad53-027ba2b6e276
keywords:
- Interfaz digital de instrumentar música (MIDI), controlador
- MIDI (Interfaz digital de instrumentar música), a través del controlador
- grabación de audio MIDI, controlador de through
- Controlador DE PASO A TRAVÉS DE MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24214dd3f6cd13ca034b2555398f6055e4ce2da1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173646"
---
# <a name="managing-midi-thru"></a>Administración de la a través de MIDI

Puede conectar un dispositivo de entrada MIDI directamente a un dispositivo de salida DE LÍNEA para que cuando el dispositivo de entrada reciba un mensaje [**MIM \_ DATA,**](mim-data.md) el sistema envíe un mensaje con los mismos datos de eventos DE MIDI al controlador del dispositivo de salida. Para conectar un dispositivo de salida DE LÍNEA a un dispositivo de entrada de MIDI, use la [**función midiConnect.**](/windows/win32/api/mmeapi/nf-mmeapi-midiconnect)

Para lograr el mejor rendimiento posible con varias salidas, una aplicación puede optar por proporcionar una forma especial de controlador de salida DE MIDI, denominado *controlador a través de*. Aunque el sistema permite que solo un dispositivo de salida DE MIDI esté conectado a un dispositivo de entrada DE MIDI, se pueden conectar varios dispositivos de salida DE MIDI a un controlador through. Una aplicación de este tipo en un sistema de este tipo podría conectar el dispositivo de entrada MIDI a este dispositivo a través de y conectar el dispositivo a través de MIDI a tantos dispositivos de salida DE MIDI como sea necesario. Para obtener más información sobre los controladores, consulte la Windows device-driver.

## <a name="using-messages-to-manage-midi-recording"></a>Uso de mensajes para administrar la grabación DE MIDI

Los mensajes siguientes se pueden enviar a un procedimiento de devolución de llamada de ventana o subproceso para administrar la grabación DE MIDI.



| Value                                          | Significado                                                                                                                                |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**MM \_ MIM \_ CLOSE**](mm-mim-close.md)         | Se envía cuando se cierra un dispositivo de entrada MIDI mediante la [**función midiInClose.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)                                      |
| [**MM \_ MIM \_ DATA**](mm-mim-data.md)           | Se envía cuando se recibe un mensaje COMPLETO de MIDI. (Este mensaje se usa para todos los mensajes DE MIDI excepto los mensajes exclusivos del sistema).          |
| [**MM \_ MIM \_ ERROR**](mm-mim-error.md)         | Se envía cuando se recibe un mensaje MIDI no válido. (Este mensaje se usa para todos los mensajes DE MIDI excepto los mensajes exclusivos del sistema).          |
| [**MM \_ MIM \_ LONGDATA**](mm-mim-longdata.md)   | Se envía cuando se recibe un mensaje completo exclusivo del sistema MIDI o cuando se ha rellenado un búfer con datos exclusivos del sistema.     |
| [**MM \_ MIM \_ LONGERROR**](mm-mim-longerror.md) | Se envía cuando se recibe un mensaje exclusivo del sistema MIDI no válido.                                                                        |
| [**MM \_ MIM \_ MOREDATA**](mm-mim-moredata.md)   | Se envía cuando una aplicación no está [**procesando los MIM \_ DATA**](mim-data.md) lo suficientemente rápido como para mantenerse al día con el controlador de dispositivo de entrada. |
| [**MM \_ MIM \_ OPEN**](mm-mim-open.md)           | Se envía cuando se abre un dispositivo de entrada MIDI mediante la [**función midiInOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)                                        |



 

Un *parámetro wParam* y un *parámetro lParam* están asociados a cada uno de estos mensajes. El *parámetro wParam* siempre especifica el identificador de un dispositivo MIDI abierto. El *parámetro lParam* no se usa para los mensajes [**MM MIM \_ \_ CLOSE**](mm-mim-close.md) [**y MM MIM \_ \_ OPEN.**](mm-mim-open.md)

Para el [**mensaje MM \_ MIM \_ LONGDATA,**](mm-mim-longdata.md) *lpMidiHdr* especifica una dirección de una estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica el búfer para los mensajes exclusivos del sistema. Es posible que el búfer no se llene por completo, ya que el tamaño de los mensajes exclusivos del sistema normalmente no se conoce antes de grabarse y porque se deben asignar búferes cuyo tamaño total puede contener el mensaje esperado más grande. Para determinar la cantidad de datos válidos presentes en el búfer, use el **miembro dwBytesRecorded** de la **estructura MIDIHDR.**

## <a name="using-a-callback-function-to-manage-midi-recording"></a>Usar una función de devolución de llamada para administrar la grabación DE MIDI

Puede definir su propia función de devolución de llamada para administrar la grabación de los dispositivos de entrada DE LÍNEA. La función de devolución de llamada se documenta [**como MidiInProc**](/previous-versions//dd798460(v=vs.85)).

Los mensajes siguientes se pueden enviar al parámetro *wMsg* de la función de devolución de **llamada MidiInProc.**



| Value                                   | Significado                                                                                                                                |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**\_MIM CERCA**](mim-close.md)         | Se envía cuando el dispositivo se cierra mediante la [**función midiInClose.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)                                               |
| [**\_MIM DATOS**](mim-data.md)           | Se envía cuando se recibe un mensaje MIDI completo (este mensaje se usa para todos los mensajes DE MIDI excepto los mensajes exclusivos del sistema).           |
| [**\_MIM ERROR**](mim-error.md)         | Se envía cuando se recibe un mensaje MIDI no válido (este mensaje se usa para todos los mensajes DE MIDI excepto los mensajes exclusivos del sistema).           |
| [**\_MIM LONGDATA**](mim-longdata.md)   | Se envía cuando se recibe un mensaje completo exclusivo del sistema MIDI o cuando se ha rellenado un búfer con datos exclusivos del sistema.     |
| [**\_MIM LONGERROR**](mim-longerror.md) | Se envía cuando se recibe un mensaje exclusivo del sistema MIDI no válido.                                                                        |
| [**\_MIM MOREDATA**](mim-moredata.md)   | Se envía cuando una aplicación no está [**procesando los MIM \_ DATA**](mim-data.md) lo suficientemente rápido como para mantenerse al día con el controlador de dispositivo de entrada. |
| [**\_MIM ABIERTO**](mim-open.md)           | Se envía cuando se abre el dispositivo de entrada MIDI mediante la [**función midiInOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)                                      |



 

Estos mensajes son similares a los enviados a las funciones de procedimiento de ventana, pero los parámetros son diferentes. Un identificador del dispositivo MIDI abierto se pasa como parámetro a la función de devolución de llamada, junto con la palabra doble de los datos de instancia que se pasaron **mediante el uso de midiInOpen**.

Para el [**MIM \_ LONGDATA,**](mim-longdata.md) *lpMidiHdr* especifica una dirección de una estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica el búfer para los mensajes exclusivos del sistema. Es posible que el búfer no esté completamente rellenado. Para determinar la cantidad de datos válidos presentes en el búfer, use el **miembro dwBytesRecorded** de la **estructura MIDIHDR.**

Una vez que el controlador del dispositivo haya finalizado con un bloque de datos, puede limpiar y liberar el bloque de datos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Grabación de audio DE AUDIO DE AUDIO](recording-midi-audio.md)
</dt> </dl>

 

 