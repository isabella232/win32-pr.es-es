---
title: Procesamiento de datos DE MIDI de dos orígenes DE MIDI
description: Procesamiento de datos DE MIDI de dos orígenes DE MIDI
ms.assetid: d8b605d9-a12a-4830-8f29-ea700aefb41d
keywords:
- Windows multimedia, procesamiento de datos DE MIDI de dos orígenes
- multimedia, procesamiento de datos MIDI de dos orígenes
- audio multimedia, procesamiento de datos MIDI de dos orígenes
- audio, procesamiento de datos MIDI de dos orígenes
- Interfaz digital de instrumentar música (MIDI), procesar datos de dos orígenes
- MIDI (Interfaz digital instrumenta de música), procesamiento de datos de dos orígenes
- procesar datos DE MIDI de dos orígenes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9a5eb31c4c6b4b965321b7458d058a3547426b95236d6e0b52d6eb0f55b3e74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805795"
---
# <a name="processing-midi-data-from-two-midi-sources"></a>Procesamiento de datos DE MIDI de dos orígenes DE MIDI

El subsistema MIDI puede enrutar mensajes MIDI desde dos orígenes de datos a un único dispositivo de salida DE MIDI para la reproducción simultánea. Por ejemplo, un origen puede ser música de fondo o una línea de sonido que se ha grabado previamente y almacenado en un archivo. El segundo origen puede ser datos en directo de un instrumento MIDI, como un teclado o un teclado.

Ambos orígenes de datos envían datos DE MIDI a un único dispositivo MIDI que se identifica con un identificador. Envíe un flujo de datos mediante la [**función midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) y uno o varios búferes de flujo. Este flujo de datos normalmente contiene datos pregrabados que se empaquetan en el búfer.

Envíe el segundo flujo de datos (normalmente desde un instrumento MIDI) de forma asincrónica mediante la [**función midiOutShortMsg.**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) El estado de ejecución de un búfer de flujo no se verá afectado negativamente por las llamadas asincrónicas realizadas por el segundo flujo de datos.

Cada mensaje corto enviado **con midiOutShortMsg** debe ser un mensaje MIDI completo, con un byte de estado y el número adecuado de bytes de datos. Si se omite el byte de estado, **midiOutShortMsg** devuelve un error. (Sin embargo, no hay ningún estado de ejecución con salida de flujo).

 

 