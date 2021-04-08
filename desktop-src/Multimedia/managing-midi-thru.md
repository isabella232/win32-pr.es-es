---
title: Administración de MIDI a través de
description: Administración de MIDI a través de
ms.assetid: ba03a2a1-d998-498d-ad53-027ba2b6e276
keywords:
- Interfaz digital de instrumentos musicales (MIDI), a través del controlador
- MIDI (interfaz digital de instrumentos musicales), a través del controlador
- grabación de audio MIDI, a través de un controlador
- Controlador de MIDI a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24214dd3f6cd13ca034b2555398f6055e4ce2da1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995147"
---
# <a name="managing-midi-thru"></a>Administración de MIDI a través de

Puede conectar un dispositivo de entrada MIDI directamente a un dispositivo de salida MIDI para que cuando el dispositivo de entrada reciba un mensaje de [**\_ datos de MIM**](mim-data.md) , el sistema envíe un mensaje con los mismos datos de eventos MIDI al controlador de dispositivo de salida. Para conectar un dispositivo de salida MIDI a un dispositivo de entrada MIDI, utilice la función [**midiConnect**](/windows/win32/api/mmeapi/nf-mmeapi-midiconnect) .

Para lograr el mejor rendimiento posible con varias salidas, una aplicación puede elegir proporcionar una forma especial de controlador de salida MIDI, denominada *controlador a través* de. Aunque el sistema solo permite que un dispositivo de salida MIDI se conecte a un dispositivo de entrada MIDI, se pueden conectar varios dispositivos de salida MIDI a un controlador a través de. Una aplicación de este tipo de sistema podría conectar el dispositivo de entrada MIDI a este dispositivo a través del dispositivo y conectar el dispositivo MIDI a tantos dispositivos de salida MIDI como sea necesario. Para obtener más información acerca de los controladores, consulte la documentación del controlador de dispositivos Windows.

## <a name="using-messages-to-manage-midi-recording"></a>Uso de mensajes para administrar grabaciones MIDI

Los siguientes mensajes se pueden enviar a un procedimiento de devolución de llamada de ventana o de subproceso para administrar la grabación de MIDI.



| Value                                          | Significado                                                                                                                                |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**MM \_ cierre de MIM \_**](mm-mim-close.md)         | Se envía cuando se cierra un dispositivo de entrada MIDI mediante la función [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) .                                      |
| [**\_datos de MIM mm \_**](mm-mim-data.md)           | Se envía cuando se recibe un mensaje MIDI completo. (Este mensaje se utiliza para todos los mensajes MIDI excepto los mensajes exclusivos del sistema).          |
| [**\_error de MIM de mm \_**](mm-mim-error.md)         | Se envía cuando se recibe un mensaje MIDI no válido. (Este mensaje se utiliza para todos los mensajes MIDI excepto los mensajes exclusivos del sistema).          |
| [**MM \_ MIM \_ LONGDATA**](mm-mim-longdata.md)   | Se envía cuando se recibe un mensaje exclusivo del sistema de MIDI completo o cuando un búfer se ha rellenado con datos exclusivos del sistema.     |
| [**MM \_ MIM \_ LONGERROR**](mm-mim-longerror.md) | Se envía cuando se recibe un mensaje no exclusivo del sistema MIDI no válido.                                                                        |
| [**MM \_ MIM \_ MOREDATA**](mm-mim-moredata.md)   | Se envía cuando una aplicación no procesa los mensajes de [**\_ datos de MIM**](mim-data.md) lo suficientemente rápido para mantenerse al día con el controlador de dispositivo de entrada. |
| [**MM \_ MIM \_ abierto**](mm-mim-open.md)           | Se envía cuando se abre un dispositivo de entrada MIDI mediante la función [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .                                        |



 

Un parámetro *wParam* y un parámetro *lParam* están asociados a cada uno de estos mensajes. El parámetro *wParam* siempre especifica el identificador de un dispositivo MIDI abierto. El parámetro *lParam* no se utiliza para los mensajes [**\_ \_ abiertos**](mm-mim-open.md) de MIM y mm de MIM de [**mm \_ \_**](mm-mim-close.md) .

En el caso del mensaje de [**\_ \_ LONGDATA**](mm-mim-longdata.md) de las mm de MIM, *lpMidiHdr* especifica una dirección de una estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica el búfer para los mensajes exclusivos del sistema. El búfer no se puede rellenar por completo, porque el tamaño de los mensajes exclusivos del sistema no suele conocerse antes de registrarse y porque se deben asignar los búferes cuyo tamaño total pueda contener el mensaje más grande esperado. Para determinar la cantidad de datos válidos presentes en el búfer, use el miembro **dwBytesRecorded** de la estructura **MIDIHDR** .

## <a name="using-a-callback-function-to-manage-midi-recording"></a>Usar una función de devolución de llamada para administrar la grabación MIDI

Puede definir su propia función de devolución de llamada para administrar la grabación de dispositivos de entrada MIDI. La función de devolución de llamada se documenta como [**MidiInProc**](/previous-versions//dd798460(v=vs.85)).

Los siguientes mensajes se pueden enviar al parámetro *wMsg* de la función de devolución de llamada **MidiInProc** .



| Value                                   | Significado                                                                                                                                |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**cierre de MIM \_**](mim-close.md)         | Se envía cuando el dispositivo se cierra con la función [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) .                                               |
| [**datos de MIM \_**](mim-data.md)           | Se envía cuando se recibe un mensaje MIDI completo (este mensaje se utiliza para todos los mensajes MIDI excepto los mensajes exclusivos del sistema).           |
| [**ERROR de MIM \_**](mim-error.md)         | Se envía cuando se recibe un mensaje MIDI no válido (este mensaje se utiliza para todos los mensajes MIDI excepto los mensajes exclusivos del sistema).           |
| [**LONGDATA de MIM \_**](mim-longdata.md)   | Se envía cuando se recibe un mensaje exclusivo del sistema de MIDI completo o cuando un búfer se ha rellenado con datos exclusivos del sistema.     |
| [**LONGERROR de MIM \_**](mim-longerror.md) | Se envía cuando se recibe un mensaje no exclusivo del sistema MIDI no válido.                                                                        |
| [**MOREDATA de MIM \_**](mim-moredata.md)   | Se envía cuando una aplicación no procesa los mensajes de [**\_ datos de MIM**](mim-data.md) lo suficientemente rápido para mantenerse al día con el controlador de dispositivo de entrada. |
| [**MIM \_ abierto**](mim-open.md)           | Se envía cuando el dispositivo de entrada MIDI se abre mediante la función [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .                                      |



 

Estos mensajes son similares a los enviados a las funciones de procedimiento de ventana, pero los parámetros son diferentes. Un identificador del dispositivo MIDI abierto se pasa como un parámetro a la función de devolución de llamada, junto con la palabra de datos de instancia que se pasó mediante **midiInOpen**.

Para el mensaje de [**\_ LONGDATA de MIM**](mim-longdata.md) , *lpMidiHdr* especifica una dirección de una estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica el búfer para los mensajes exclusivos del sistema. Es posible que el búfer no se llene completamente. Para determinar la cantidad de datos válidos presentes en el búfer, use el miembro **dwBytesRecorded** de la estructura **MIDIHDR** .

Una vez que el controlador de dispositivo finaliza con un bloque de datos, puede limpiar y liberar el bloque de datos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Grabación de audio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 