---
title: Asignación y preparación de bloques de datos MIDI
description: Asignación y preparación de bloques de datos MIDI
ms.assetid: b3a70441-e8f9-4886-bf22-426ebd74d045
keywords:
- Interfaz digital de instrumentos musicales (MIDI), asignar bloques de datos
- MIDI (interfaz digital de instrumentos musicales), asignar bloques de datos
- Servicios MIDI, asignar bloques de datos
- asignación de bloques de datos MIDI
- Interfaz digital de instrumentos musicales (MIDI), preparar bloques de datos
- MIDI (interfaz digital de instrumentos musicales), preparar bloques de datos
- Servicios MIDI, preparar bloques de datos
- preparación de bloques de datos MIDI
- Interfaz digital de instrumentos musicales (MIDI), bloques de datos
- MIDI (interfaz digital de instrumentos musicales), bloques de datos
- Servicios MIDI, bloques de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48b23a72dfd46035a3d23743faa7228e5fe85aaf
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105676375"
---
# <a name="allocating-and-preparing-midi-data-blocks"></a>Asignación y preparación de bloques de datos MIDI

Las funciones [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg), [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)y [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) requieren que las aplicaciones asignen bloques de datos para pasarlos a los controladores de dispositivos con fines de reproducción o grabación. Cada una de estas funciones usa una estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) para describir su bloque de datos.

Antes de usar una de estas funciones para pasar un bloque de datos a un controlador de dispositivo, debe asignar memoria para el búfer y la estructura de encabezado que describe el bloque de datos.

Windows proporciona las siguientes funciones para preparar y limpiar los bloques de datos MIDI.



| Value                                                    | Significado                                                |
|----------------------------------------------------------|--------------------------------------------------------|
| [**midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader)       | Prepara un bloque de datos de entrada MIDI.                      |
| [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader)   | Limpia la preparación de un bloque de datos de entrada MIDI.  |
| [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader)     | Prepara un bloque de datos de salida MIDI.                     |
| [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) | Limpia la preparación de un bloque de datos de salida MIDI. |



 

Antes de pasar un bloque de datos MIDI a un controlador de dispositivo, debe preparar el búfer pasándolo a la función [**midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader) o [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) . Cuando el controlador de dispositivo finaliza con el búfer y lo devuelve, debe limpiar esta preparación pasando el búfer a la función [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader) o [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) antes de que se pueda liberar cualquier memoria asignada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicios MIDI](midi-services.md)
</dt> </dl>

 

 