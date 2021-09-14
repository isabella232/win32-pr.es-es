---
title: Administración de la grabación de MIDI
description: Administración de la grabación de MIDI
ms.assetid: 48b2d815-72cf-4c96-8d93-247d2426b8f2
keywords:
- Interfaz digital instrumentable (MIDI), grabación
- MIDI (Interfaz digital instrumenta de música), grabación
- grabación de audio MIDI, administración
- Grabación DE MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0edfb81976e1f5333798c9705640e7676281968a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127375198"
---
# <a name="managing-midi-recording"></a>Administración de la grabación de MIDI

Después de abrir un dispositivo MIDI, puede empezar a grabar datos DE MIDI. Windows proporciona las siguientes funciones para administrar la grabación DE MIDI.



| Value                                      | Significado                                                                                           |
|--------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer) | Envía un búfer al controlador del dispositivo para que se pueda rellenar con datos DE MIDI exclusivos del sistema registrados. |
| [**midiInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)         | Detiene la grabación de MIDI y marca todos los búferes pendientes como se ha hecho.                                       |
| [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)         | Inicia la grabación de MIDI y restablece la marca de tiempo a cero.                                          |
| [**midiInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)           | Detiene la grabación de MIDI.                                                                             |



 

Para enviar búferes al controlador de dispositivo para grabar mensajes exclusivos del sistema, use [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer). La aplicación se notifica a medida que los búferes se rellenan con datos registrados exclusivos del sistema. Para obtener más información sobre las técnicas de notificación, vea [Managing MIDI Data Blocks](managing-midi-data-blocks.md).

La [**función midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) comienza el proceso de grabación. Al grabar mensajes exclusivos del sistema, envíe al menos un búfer al controlador antes de iniciar la grabación. Para detener la grabación, use [**midiInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop). Antes de cerrar el dispositivo mediante la [**función midiInClose,**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose) marque los bloques de datos pendientes como se hace mediante una [**llamada a midiInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset).

Las aplicaciones que requieren datos con marca de tiempo usan una función de devolución de llamada para recibir datos de MIDI. Si los requisitos de tiempo no son estrictos, puede usar una devolución de llamada de ventana o subproceso. Sin embargo, no puede usar una devolución de llamada de eventos para recibir datos DE MIDI.

Para registrar mensajes exclusivos del sistema con aplicaciones que no usan búferes de flujo, debe proporcionar búferes al controlador de dispositivo. Estos búferes se especifican mediante una [**estructura MIDIHDR.**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Grabación de audio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 