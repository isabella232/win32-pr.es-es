---
title: Procesamiento de datos MIDI de dos orígenes MIDI
description: Procesamiento de datos MIDI de dos orígenes MIDI
ms.assetid: d8b605d9-a12a-4830-8f29-ea700aefb41d
keywords:
- Windows multimedia, procesamiento de datos MIDI de dos orígenes
- multimedia, procesamiento de datos MIDI de dos orígenes
- audio multimedia, procesamiento de datos MIDI de dos orígenes
- audio, procesamiento de datos MIDI de dos orígenes
- Interfaz digital de instrumentos musicales (MIDI), procesamiento de datos de dos orígenes
- MIDI (interfaz digital de instrumentos musicales), procesamiento de datos de dos orígenes
- procesamiento de datos MIDI de dos orígenes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513dcd16036f6f833aec6813f75c6c082925f666
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077686"
---
# <a name="processing-midi-data-from-two-midi-sources"></a>Procesamiento de datos MIDI de dos orígenes MIDI

El subsistema MIDI puede enrutar los mensajes MIDI de dos orígenes de datos a un solo dispositivo de salida MIDI para la reproducción simultánea. Por ejemplo, un origen puede ser música de fondo o una línea de graves que se ha grabado previamente y se ha almacenado en un archivo. El segundo origen puede ser datos activos de un instrumento MIDI, como un teclado o guitarra.

Ambos orígenes de datos envían datos MIDI a un único dispositivo MIDI que se identifica con un identificador. Envíe un flujo de datos mediante la función [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout) y uno o más búferes de secuencia. Normalmente, este flujo de datos contiene datos grabados como datos empaquetados en el búfer.

Envíe el segundo flujo de datos (normalmente desde un instrumento MIDI) de forma asincrónica mediante la función [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) . El estado de ejecución de un búfer de secuencia no se verá afectado negativamente por las llamadas asincrónicas realizadas por el segundo flujo de datos.

Cada mensaje corto enviado con **midiOutShortMsg** debe ser un mensaje MIDI completo, con un byte de estado y el número de bytes de datos adecuado. Si se omite el byte de estado, **midiOutShortMsg** devuelve un error. (Sin embargo, no hay ningún estado en ejecución con la salida de Stream).

 

 