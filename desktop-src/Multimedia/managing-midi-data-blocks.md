---
title: Administrar bloques de datos MIDI
description: Administrar bloques de datos MIDI
ms.assetid: f29fbc08-ef67-489c-aedf-5a2bc65233f7
keywords:
- Interfaz digital de instrumentos musicales (MIDI), administrar bloques de datos
- MIDI (interfaz digital de instrumentos musicales), administrar bloques de datos
- Servicios MIDI, administrar bloques de datos
- administrar bloques de datos MIDI
- Interfaz digital de instrumentos musicales (MIDI), procesar mensajes de controlador
- MIDI (interfaz digital de instrumentos musicales), procesar mensajes de controlador
- Servicios MIDI, procesamiento de mensajes de controlador
- procesar mensajes de controlador
- Interfaz digital de instrumentos musicales (MIDI), bloques de datos
- MIDI (interfaz digital de instrumentos musicales), bloques de datos
- Servicios MIDI, bloques de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af348d6c53d2944bf22c026674704baa1fe74e07
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995148"
---
# <a name="managing-midi-data-blocks"></a>Administrar bloques de datos MIDI

Las aplicaciones que usan bloques de datos para pasar mensajes exclusivos del sistema (mediante las funciones [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) y [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) ) y los búferes de secuencia (mediante la función [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) ) deben proporcionar continuamente el controlador de dispositivo con bloqueos de datos hasta que se complete la reproducción o grabación.

Incluso si se usa un solo bloque de datos, una aplicación debe ser capaz de determinar si un controlador de dispositivo ha terminado con el bloque de datos para que pueda liberar la memoria asociada al bloque de datos y la estructura de encabezado. Se pueden usar tres métodos para determinar cuándo un controlador de dispositivo ha terminado con un bloque de datos:

-   Especifique una función de devolución de llamada para recibir un mensaje enviado por el controlador cuando termine con un bloque de datos. Para obtener datos de entrada MIDI con marca de tiempo, debe usar una función de devolución de llamada.
-   Usar una devolución de llamada de evento (solo para salida).
-   Use una devolución de llamada de ventana o de subproceso para recibir un mensaje enviado por el controlador cuando haya terminado con un bloque de datos.

Si una aplicación no obtiene un bloque de datos para el controlador de dispositivo cuando sea necesario, puede producirse un hueco audible en la reproducción o una pérdida de la información grabada entrante. Como mínimo, una aplicación debe usar un esquema de almacenamiento en búfer doble para mantener al menos un bloque de datos antes del controlador de dispositivo.

## <a name="using-a-callback-function-to-process-driver-messages"></a>Usar una función de devolución de llamada para procesar mensajes de controlador

Puede escribir su propia función de devolución de llamada para procesar los mensajes enviados por el controlador de dispositivo. Para usar una función de devolución de llamada, especifique la marca de función de devolución de llamada \_ en el parámetro *dwFlags* y la dirección de la función de devolución de llamada en el parámetro *DwCallback* de la función [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) o [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .

Los mensajes enviados a una función de devolución de llamada son similares a los mensajes enviados a una ventana, salvo que tienen dos parámetros palabra en lugar de un parámetro entero sin signo y un parámetro palabra. Para obtener más información acerca de estos mensajes, consulte [envío de mensajes de System-Exclusive](sending-system-exclusive-messages.md) y administración de la grabación de [MIDI](managing-midi-recording.md).

Use una de las técnicas siguientes para pasar datos de instancia de una aplicación a una función de devolución de llamada:

-   Use el parámetro *dwCallbackInstance* de la función que abre el controlador de dispositivo.
-   Use el miembro **dwUser** de la estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica un bloque de datos que se envía a un controlador de dispositivo MIDI.

Si necesita más de 32 bits de datos de instancia, pase una dirección de una estructura que contenga la información adicional.

## <a name="using-an-event-callback-to-process-driver-messages"></a>Usar una devolución de llamada de evento para procesar mensajes de controlador

Para utilizar una devolución de llamada de evento, utilice la función [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) para recuperar el identificador de un evento y especificar el \_ evento de devolución de llamada en la llamada a la función [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) .

Una devolución de llamada de evento se establece por cualquier cosa que pueda provocar una devolución de llamada de función. A diferencia de las funciones de devolución de llamada y las devoluciones de llamada de ventana o de subproceso, las devoluciones de llamada de eventos no reciben notificaciones de cierre, listo o abierto específicas. Por lo tanto, es posible que una aplicación tenga que comprobar el estado del proceso que espera después de que se produzca el evento.

Para obtener más información sobre las devoluciones de llamada de eventos, vea [usar una devolución de llamada de evento para administrar la reproducción almacenada en búfer](using-an-callback-to-manage-buffered-playback.md).

## <a name="using-a-window-or-thread-callback-to-process-driver-messages"></a>Usar una devolución de llamada de ventana o de subproceso para procesar mensajes de controlador

Para utilizar una devolución de llamada de ventana, especifique la marca de la ventana de devolución de llamada \_ en el parámetro *dwFlags* y un identificador de ventana en la palabra de orden inferior del parámetro *DwCallback* de la función [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) o [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) . Los mensajes de controlador se enviarán a la función de procedimiento de ventana para la ventana identificada por el identificador de *dwCallback*.

Del mismo modo, para usar una devolución de llamada de subproceso, especifique la marca de subproceso \_ de devolución de llamada y un identificador de subproceso en la llamada a **MidiInOpen** o **midiOutOpen**. En este caso, los mensajes se publicarán en el subproceso especificado en lugar de en una ventana.

Los mensajes enviados a una devolución de llamada de ventana o subproceso son específicos del dispositivo MIDI que se usa. Para obtener más información acerca de estos mensajes, consulte [envío de mensajes de System-Exclusive](sending-system-exclusive-messages.md) y administración de la grabación de [MIDI](managing-midi-recording.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicios MIDI](midi-services.md)
</dt> </dl>

 

 