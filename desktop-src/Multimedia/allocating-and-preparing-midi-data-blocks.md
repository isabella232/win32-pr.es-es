---
title: Asignación y preparación de bloques de datos DE MIDI
description: Asignación y preparación de bloques de datos DE MIDI
ms.assetid: b3a70441-e8f9-4886-bf22-426ebd74d045
keywords:
- Interfaz digital de instrumentación musical (MIDI), asignación de bloques de datos
- MIDI (Interfaz digital de instrumentación musical), asignación de bloques de datos
- Servicios DE MIDI, asignación de bloques de datos
- asignar bloques de datos DE MIDI
- Interfaz digital de instrumentar música (MIDI), preparar bloques de datos
- MIDI (Interfaz digital de instrumentar música), preparar bloques de datos
- Servicios DE MIDI, preparar bloques de datos
- preparar bloques de datos DE MIDI
- Interfaz digital de instrumentar música (MIDI), bloques de datos
- MIDI (Interfaz digital de instrumentar música), bloques de datos
- Servicios DE MIDI, bloques de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 137556c1344e6f2e8db8557d45a70c5981fa7bab99e7452cc1f756b4a8ee159b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808495"
---
# <a name="allocating-and-preparing-midi-data-blocks"></a>Asignación y preparación de bloques de datos DE MIDI

Las [**funciones midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg), [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)y [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) requieren que las aplicaciones asignen bloques de datos para pasar a los controladores de dispositivo con fines de reproducción o grabación. Cada una de estas funciones usa una [**estructura MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) para describir su bloque de datos.

Antes de usar una de estas funciones para pasar un bloque de datos a un controlador de dispositivo, debe asignar memoria para el búfer y la estructura de encabezado que describe el bloque de datos.

Windows proporciona las siguientes funciones para preparar y limpiar bloques de datos DE MIDI.



| Valor                                                    | Significado                                                |
|----------------------------------------------------------|--------------------------------------------------------|
| [**midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader)       | Prepara un bloque de datos de entrada de MIDI.                      |
| [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader)   | Limpia la preparación de un bloque de datos de entrada DE MIDI.  |
| [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader)     | Prepara un bloque de datos de salida DE MIDI.                     |
| [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) | Limpia la preparación de un bloque de datos de salida DE MIDI. |



 

Antes de pasar un bloque de datos MIDI a un controlador de dispositivo, debe preparar el búfer pasando a la [**función midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader) o [**midiOutPrepareHeader.**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader) Cuando el controlador del dispositivo haya terminado con el búfer y lo devuelva, debe limpiar esta preparación pasando el búfer a la función [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader) o [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader) antes de liberar cualquier memoria asignada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicios DE MIDI](midi-services.md)
</dt> </dl>

 

 