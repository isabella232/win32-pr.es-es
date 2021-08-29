---
title: Administración de bloques de datos DE MIDI
description: Administración de bloques de datos DE MIDI
ms.assetid: f29fbc08-ef67-489c-aedf-5a2bc65233f7
keywords:
- Interfaz digital instrumentable (MIDI), administración de bloques de datos
- MIDI (Interfaz digital instrumentable), administración de bloques de datos
- Servicios DE MIDI, administración de bloques de datos
- administración de bloques de datos DE MIDI
- Interfaz digital instrumentable (MIDI), procesamiento de mensajes de controlador
- MIDI (Interfaz digital instrumentable), procesamiento de mensajes de controlador
- Servicios DE MIDI, procesamiento de mensajes de controlador
- procesar mensajes del controlador
- Interfaz digital instrumentable (MIDI), bloques de datos
- MIDI (Interfaz digital instrumenta de música), bloques de datos
- Servicios DE MIDI, bloques de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 846c7391fedbcdc4f14934ed73ae9a47de675f435b9b2bd1fb63e97c340d5182
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139154"
---
# <a name="managing-midi-data-blocks"></a>Administración de bloques de datos DE MIDI

Las aplicaciones que usan bloques de datos para pasar mensajes exclusivos del sistema (mediante las funciones [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) y [**midiInAddBuffer)**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) y búferes de flujo (mediante la [**función midiStreamOut)**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) deben proporcionar continuamente bloques de datos al controlador de dispositivo hasta que se complete la reproducción o grabación.

Incluso si se usa un único bloque de datos, una aplicación debe ser capaz de determinar cuándo finaliza un controlador de dispositivo con el bloque de datos para que pueda liberar la memoria asociada con el bloque de datos y la estructura de encabezado. Se pueden usar tres métodos para determinar cuándo finaliza un controlador de dispositivo con un bloque de datos:

-   Especifique una función de devolución de llamada para recibir un mensaje enviado por el controlador cuando termine con un bloque de datos. Para obtener datos de entrada de MIDI con marca de tiempo, debe usar una función de devolución de llamada.
-   Use una devolución de llamada de evento (solo para la salida).
-   Use una devolución de llamada de ventana o subproceso para recibir un mensaje enviado por el controlador cuando termine con un bloque de datos.

Si una aplicación no obtiene un bloque de datos para el controlador de dispositivo cuando es necesario, se puede producir una brecha en la reproducción o una pérdida de información registrada entrante. Como mínimo, una aplicación debe usar un esquema de almacenamiento en búfer doble para mantener al menos un bloque de datos delante del controlador de dispositivo.

## <a name="using-a-callback-function-to-process-driver-messages"></a>Usar una función de devolución de llamada para procesar mensajes de controlador

Puede escribir su propia función de devolución de llamada para procesar los mensajes enviados por el controlador de dispositivo. Para usar una función de devolución de llamada, especifique la marca CALLBACK FUNCTION en el parámetro dwFlags y la dirección de la función de devolución de llamada en el parámetro dwCallback de la \_ función [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) o [**midiOutOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)  

Los mensajes enviados a una función de devolución de llamada son similares a los mensajes enviados a una ventana, salvo que tienen dos parámetros doubleword en lugar de un parámetro entero sin signo y un parámetro doubleword. Para obtener más información sobre estos mensajes, vea [Sending System-Exclusive Messages](sending-system-exclusive-messages.md) and Managing MIDI [Recording](managing-midi-recording.md).

Use una de las técnicas siguientes para pasar datos de instancia de una aplicación a una función de devolución de llamada:

-   Use el *parámetro dwCallbackInstance* de la función que abre el controlador de dispositivo.
-   Use el **miembro dwUser** de la [**estructura MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica un bloque de datos que se envía a un controlador de dispositivo MIDI.

Si necesita más de 32 bits de datos de instancia, pase una dirección de una estructura que contenga la información adicional.

## <a name="using-an-event-callback-to-process-driver-messages"></a>Usar una devolución de llamada de eventos para procesar mensajes del controlador

Para usar una devolución de llamada de eventos, use la función [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) para recuperar el identificador de un evento y especificar CALLBACK EVENT en la llamada a \_ la función [**midiOutOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)

Cualquier elemento que pueda provocar una devolución de llamada de función establece una devolución de llamada de eventos. A diferencia de las funciones de devolución de llamada y las devoluciones de llamada de ventanas o subprocesos, las devoluciones de llamada de eventos no reciben notificaciones específicas de cierre, realización o apertura. Por lo tanto, una aplicación puede tener que comprobar el estado del proceso que está esperando después de que se produzca el evento.

Para obtener más información sobre las devoluciones de llamada de eventos, vea Usar una devolución de llamada [de eventos para administrar la reproducción en búfer.](using-an-callback-to-manage-buffered-playback.md)

## <a name="using-a-window-or-thread-callback-to-process-driver-messages"></a>Usar una devolución de llamada de ventana o subproceso para procesar mensajes de controlador

Para usar una devolución de llamada de ventana, especifique la marca CALLBACK WINDOW en el parámetro dwFlags y un identificador de ventana en la palabra de orden bajo del parámetro dwCallback de la función \_ [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) o [**midiOutOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)   Los mensajes de controlador se enviarán a la función de procedimiento de ventana para la ventana identificada por el identificador en *dwCallback*.

De forma similar, para usar una devolución de llamada de subproceso, especifique la marca CALLBACK THREAD y un identificador de subproceso en la llamada \_ a **midiInOpen** o **midiOutOpen**. En este caso, los mensajes se publicarán en el subproceso especificado en lugar de en una ventana.

Los mensajes enviados a una devolución de llamada de ventana o subproceso son específicos del dispositivo MIDI usado. Para obtener más información sobre estos mensajes, vea [Sending System-Exclusive Messages](sending-system-exclusive-messages.md) and Managing MIDI [Recording](managing-midi-recording.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicios DE MIDI](midi-services.md)
</dt> </dl>

 

 