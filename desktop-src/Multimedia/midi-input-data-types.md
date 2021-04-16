---
title: Tipos de datos de entrada MIDI
description: Tipos de datos de entrada MIDI
ms.assetid: c67f149e-60b8-4f9e-8e3c-a88cd579d29f
keywords:
- Interfaz digital de instrumentos musicales (MIDI), tipos de datos de entrada
- MIDI (interfaz digital de instrumentos musicales), tipos de datos de entrada
- grabar audio MIDI, tipos de datos de entrada
- Tipos de datos de entrada MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8f0738827cce4cfd8cb4a237dcd2031c2fe71a7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105676373"
---
# <a name="midi-input-data-types"></a>Tipos de datos de entrada MIDI

Windows define los siguientes tipos de datos para las funciones de entrada MIDI.



| Value                            | Significado                                                                                                                                                                                     |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HMIDIIN**                      | Identificador de un dispositivo de entrada MIDI.                                                                                                                                                              |
| [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)       | Encabezado para un búfer de secuencia o un bloque de datos exclusivos del sistema MIDI. En el caso de las aplicaciones de entrada, esta estructura solo registra los datos exclusivos del sistema (no se admite la transmisión por secuencias para la entrada MIDI). |
| [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) | Estructura usada para consultar las capacidades de un dispositivo de entrada MIDI.                                                                                                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Grabación de audio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 