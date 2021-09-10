---
title: Tipos de datos de entrada DE MIDI
description: Tipos de datos de entrada DE MIDI
ms.assetid: c67f149e-60b8-4f9e-8e3c-a88cd579d29f
keywords:
- Interfaz digital instrumentable (MIDI), tipos de datos de entrada
- MIDI (Interfaz digital de instrumentado), tipos de datos de entrada
- grabación de audio MIDI, tipos de datos de entrada
- Tipos de datos de entrada de MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8f0738827cce4cfd8cb4a237dcd2031c2fe71a7
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370909"
---
# <a name="midi-input-data-types"></a>Tipos de datos de entrada DE MIDI

Windows define los siguientes tipos de datos para las funciones de entrada de MIDI.



| Value                            | Significado                                                                                                                                                                                     |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HMIDIIN**                      | Identificador de un dispositivo de entrada DE LÍNEA.                                                                                                                                                              |
| [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)       | Encabezado para un búfer de flujo o un bloque de datos exclusivos del sistema DE LÍNEA. En el caso de las aplicaciones de entrada, esta estructura registra solo datos exclusivos del sistema (el streaming no se admite para la entrada MIDI). |
| [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) | Estructura que se usa para consultar las funcionalidades de un dispositivo de entrada DE LÍNEA.                                                                                                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Grabación de audio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 