---
title: Asignación y preparación de bloques de datos DE MIDI
description: Asignación y preparación de bloques de datos DE MIDI
ms.assetid: b3a70441-e8f9-4886-bf22-426ebd74d045
keywords:
- Interfaz digital de instrumentación de música (MIDI), asignación de bloques de datos
- MIDI (Interfaz digital de instrumentación de música), asignación de bloques de datos
- Servicios DE MIDI, asignación de bloques de datos
- asignar bloques de datos DE MIDI
- Instrumentar interfaz digital (MIDI), preparar bloques de datos
- MIDI (Interfaz digital instrumentable), preparar bloques de datos
- Servicios DE MIDI, preparar bloques de datos
- preparar bloques de datos DE MIDI
- Interfaz digital instrumentable (MIDI), bloques de datos
- MIDI (Interfaz digital instrumenta de música), bloques de datos
- Servicios DE MIDI, bloques de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48b23a72dfd46035a3d23743faa7228e5fe85aaf
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370838"
---
# <a name="allocating-and-preparing-midi-data-blocks"></a>Asignación y preparación de bloques de datos DE MIDI

Las [**funciones midiOutLongMsg,**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)y [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) requieren que las aplicaciones asignen bloques de datos para pasar a los controladores de dispositivos con fines de reproducción o grabación. Cada una de estas funciones usa una [**estructura MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) para describir su bloque de datos.

Antes de usar una de estas funciones para pasar un bloque de datos a un controlador de dispositivo, debe asignar memoria para el búfer y la estructura de encabezado que describe el bloque de datos.

Windows proporciona las siguientes funciones para preparar y limpiar bloques de datos DE MIDI.



| Value                                                    | Significado                                                |
|----------------------------------------------------------|--------------------------------------------------------|
| [**midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader)       | Prepara un bloque de datos de entrada de MIDI.                      |
| [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader)   | Limpia la preparación de un bloque de datos de entrada DE MIDI.  |
| [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader)     | Prepara un bloque de datos de salida de MIDI.                     |
| [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) | Limpia la preparación de un bloque de datos de salida DE MIDI. |



 

Antes de pasar un bloque de datos MIDI a un controlador de dispositivo, debe preparar el búfer pasandolo a la [**función midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader) o [**midiOutPrepareHeader.**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) Cuando el controlador de dispositivo haya terminado con el búfer y lo devuelva, debe limpiar esta preparación pasando el búfer a la función [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader) o [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) antes de que se pueda liberar cualquier memoria asignada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicios DE MIDI](midi-services.md)
</dt> </dl>

 

 