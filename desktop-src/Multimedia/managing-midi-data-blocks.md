---
title: Administración de bloques de datos DE MIDI
description: Administración de bloques de datos DE MIDI
ms.assetid: f29fbc08-ef67-489c-aedf-5a2bc65233f7
keywords:
- Interfaz digital de instrumentar música (MIDI), administrar bloques de datos
- MIDI (Interfaz digital de instrumentar música), administrar bloques de datos
- Servicios DE MIDI, administración de bloques de datos
- administración de bloques de datos de MIDI
- Interfaz digital instrumentación de música (MIDI), procesamiento de mensajes de controlador
- MIDI (Interfaz digital de instrumentar música), procesar mensajes de controlador
- Servicios DE MIDI, procesamiento de mensajes del controlador
- procesar mensajes del controlador
- Interfaz digital de instrumentar música (MIDI), bloques de datos
- MIDI (Interfaz digital de instrumentar música), bloques de datos
- Servicios DE MIDI, bloques de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af348d6c53d2944bf22c026674704baa1fe74e07
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173649"
---
# <a name="managing-midi-data-blocks"></a>Administración de bloques de datos DE MIDI

Las aplicaciones que usan bloques de datos para pasar mensajes exclusivos del sistema (mediante las funciones [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) y [**midiInAddBuffer)**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) y búferes de flujo (mediante la [**función midiStreamOut)**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) deben proporcionar continuamente al controlador de dispositivo bloques de datos hasta que se complete la reproducción o la grabación.

Incluso si se usa un único bloque de datos, una aplicación debe ser capaz de determinar cuándo un controlador de dispositivo ha terminado con el bloque de datos para que pueda liberar la memoria asociada con el bloque de datos y la estructura de encabezado. Se pueden usar tres métodos para determinar cuándo finaliza un controlador de dispositivo con un bloque de datos:

-   Especifique una función de devolución de llamada para recibir un mensaje enviado por el controlador cuando termine con un bloque de datos. Para obtener los datos de entrada de MIDI con marca de tiempo, debe usar una función de devolución de llamada.
-   Use una devolución de llamada de evento (solo para la salida).
-   Use una devolución de llamada de subproceso o ventana para recibir un mensaje enviado por el controlador cuando termine con un bloque de datos.

Si una aplicación no obtiene un bloque de datos para el controlador del dispositivo cuando es necesario, puede producirse una brecha en la reproducción o una pérdida de información registrada entrante. Como mínimo, una aplicación debe usar un esquema de almacenamiento en doble búfer para mantener al menos un bloque de datos delante del controlador de dispositivo.

## <a name="using-a-callback-function-to-process-driver-messages"></a>Usar una función de devolución de llamada para procesar mensajes del controlador

Puede escribir su propia función de devolución de llamada para procesar los mensajes enviados por el controlador de dispositivo. Para usar una función de devolución de llamada, especifique la marca CALLBACK FUNCTION en el parámetro dwFlags y la dirección de la función de devolución de llamada en el parámetro dwCallback de la \_ función [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) o [**midiOutOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)  

Los mensajes enviados a una función de devolución de llamada son similares a los mensajes enviados a una ventana, salvo que tienen dos parámetros doubleword en lugar de un parámetro entero sin signo y un parámetro doubleword. Para obtener más información sobre estos mensajes, vea [Envío de System-Exclusive y](sending-system-exclusive-messages.md) Administración de la grabación de [MIDI.](managing-midi-recording.md)

Use una de las técnicas siguientes para pasar datos de instancia de una aplicación a una función de devolución de llamada:

-   Use el *parámetro dwCallbackInstance* de la función que abre el controlador de dispositivo.
-   Use el **miembro dwUser** de la [**estructura MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica un bloque de datos que se envía a un controlador de dispositivo MIDI.

Si necesita más de 32 bits de datos de instancia, pase una dirección de una estructura que contenga la información adicional.

## <a name="using-an-event-callback-to-process-driver-messages"></a>Usar una devolución de llamada de evento para procesar mensajes del controlador

Para usar una devolución de llamada de evento, use la función [CreateEvent](/windows/win32/api/synchapi/nf-synchapi-createeventa) para recuperar el identificador de un evento y especifique CALLBACK EVENT en la llamada a la \_ función [**midiOutOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)

Cualquier elemento que pueda provocar una devolución de llamada de función establece una devolución de llamada de evento. A diferencia de las funciones de devolución de llamada y las devoluciones de llamada de ventanas o subprocesos, las devoluciones de llamada de eventos no reciben notificaciones específicas de cierre, realización o apertura. Por lo tanto, una aplicación puede tener que comprobar el estado del proceso que está esperando después de que se produzca el evento.

Para obtener más información sobre las devoluciones de llamada de eventos, vea Usar una devolución de llamada [de eventos para administrar la reproducción en búfer.](using-an-callback-to-manage-buffered-playback.md)

## <a name="using-a-window-or-thread-callback-to-process-driver-messages"></a>Usar una devolución de llamada de ventana o subproceso para procesar mensajes de controlador

Para usar una devolución de llamada de ventana, especifique la marca CALLBACK WINDOW en el parámetro dwFlags y un identificador de ventana en la palabra de orden bajo del parámetro dwCallback de la función \_ [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) o [**midiOutOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)   Los mensajes del controlador se enviarán a la función de procedimiento de ventana para la ventana identificada por el identificador en *dwCallback*.

Del mismo modo, para usar una devolución de llamada de subproceso, especifique la marca CALLBACK THREAD y un identificador de subproceso en la llamada \_ a **midiInOpen** **o midiOutOpen.** En este caso, los mensajes se publicarán en el subproceso especificado en lugar de en una ventana.

Los mensajes enviados a una devolución de llamada de subproceso o ventana son específicos del dispositivo MIDI usado. Para obtener más información sobre estos mensajes, vea [Envío de System-Exclusive y](sending-system-exclusive-messages.md) Administración de la grabación de [MIDI.](managing-midi-recording.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicios DE MIDI](midi-services.md)
</dt> </dl>

 

 