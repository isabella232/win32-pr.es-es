---
title: Flujos MIDI
description: Flujos MIDI
ms.assetid: 622472d9-2888-407f-bdaa-4943896c0bac
keywords:
- Interfaz digital de instrumentos musicales (MIDI), secuencias
- MIDI (interfaz digital de instrumentos musicales), secuencias
- búferes de secuencia, flujos MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4237e1590f3af2e15a3b0b9fedea2fea4c9c40fc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149251"
---
# <a name="midi-streams"></a>Flujos MIDI

Los eventos MIDI se producen en el contexto de un flujo de datos MIDI. Aunque una aplicación puede utilizar varias secuencias para definir datos musicales, el asignador MIDI no reconoce varias secuencias. La mayoría de las aplicaciones que usan secuencias usan una sola secuencia MIDI.

Las siguientes funciones de funcionan con secuencias.



| Value                                            | Significado                                                                 |
|--------------------------------------------------|-------------------------------------------------------------------------|
| [**midiStreamClose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)       | Cierra una secuencia MIDI.                                                   |
| [**midiStreamOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen)         | Abre un flujo MIDI y recupera un identificador.                             |
| [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)           | Reproduce o pone en cola un flujo (búfer) de datos MIDI en un dispositivo de salida MIDI. |
| [**midiStreamPause**](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)       | Pausa la reproducción de una secuencia MIDI especificada.                             |
| [**midiStreamPosition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) | Recupera la posición actual en una secuencia MIDI.                        |
| [**midiStreamProperty**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamproperty) | Establece y recupera las propiedades de la secuencia.                                   |
| [**midiStreamRestart**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)   | Reinicia la reproducción de una secuencia MIDI en pausa.                              |
| [**midiStreamStop**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)         | Desactiva todas las notas en todos los canales MIDI de la secuencia MIDI especificada. |



 

 

 