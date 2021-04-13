---
title: Administración de la grabación de MIDI
description: Administración de la grabación de MIDI
ms.assetid: 48b2d815-72cf-4c96-8d93-247d2426b8f2
keywords:
- Interfaz digital de instrumentos musicales (MIDI), grabación
- MIDI (interfaz digital de instrumentos musicales), grabar
- grabar audio MIDI, administrar
- Grabación MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0edfb81976e1f5333798c9705640e7676281968a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487550"
---
# <a name="managing-midi-recording"></a>Administración de la grabación de MIDI

Después de abrir un dispositivo MIDI, puede empezar a grabar datos MIDI. Windows proporciona las siguientes funciones para la administración de la grabación de MIDI.



| Value                                      | Significado                                                                                           |
|--------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) | Envía un búfer al controlador de dispositivo para que se pueda rellenar con datos MIDI exclusivos del sistema grabados. |
| [**midiInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)         | Detiene la grabación de MIDI y marca todos los búferes pendientes como terminados.                                       |
| [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)         | Inicia la grabación MIDI y restablece la marca de tiempo en cero.                                          |
| [**midiInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)           | Detiene la grabación de MIDI.                                                                             |



 

Para enviar búferes al controlador de dispositivo para grabar mensajes exclusivos del sistema, use [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer). La aplicación recibe una notificación, ya que los búferes se rellenan con datos registrados exclusivos del sistema. Para obtener más información acerca de las técnicas de notificación, consulte [administrar bloques de datos MIDI](managing-midi-data-blocks.md).

La función [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) inicia el proceso de grabación. Al grabar mensajes exclusivos del sistema, envíe al menos un búfer al controlador antes de iniciar la grabación. Para detener la grabación, use [**midiInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop). Antes de cerrar el dispositivo mediante la función [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) , marque los bloques de datos pendientes como si se realizara llamando a [**midiInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset).

Las aplicaciones que requieren datos con marca de tiempo usan una función de devolución de llamada para recibir datos MIDI. Si los requisitos de control de tiempo no son estrictos, puede utilizar una devolución de llamada de ventana o de subproceso. Sin embargo, no puede usar una devolución de llamada de evento para recibir datos MIDI.

Para registrar mensajes exclusivos del sistema con aplicaciones que no utilizan búferes de secuencia, debe proporcionar el controlador de dispositivo con búferes. Estos búferes se especifican mediante una estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Grabación de audio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 