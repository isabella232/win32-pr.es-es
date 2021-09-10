---
title: Secuencias DE MIDI
description: Secuencias DE MIDI
ms.assetid: 622472d9-2888-407f-bdaa-4943896c0bac
keywords:
- Interfaz digital de instrumentaciones de música (MIDI),streams
- MIDI (Interfaz digital instrumenta instrumentable), secuencias
- búferes de secuencias, secuencias DE MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4237e1590f3af2e15a3b0b9fedea2fea4c9c40fc
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371042"
---
# <a name="midi-streams"></a>Secuencias DE MIDI

Los eventos DE MIDI se producen en el contexto de una secuencia de datos DE MIDI. Aunque una aplicación puede usar varias secuencias para definir datos de música, el asignador de MIDI no reconoce varias secuencias. La mayoría de las aplicaciones que usan secuencias usan una única secuencia DE MIDI.

Las siguientes funciones funcionan con secuencias.



| Value                                            | Significado                                                                 |
|--------------------------------------------------|-------------------------------------------------------------------------|
| [**midiStreamClose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)       | Cierra una secuencia de MIDI.                                                   |
| [**midiStreamOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen)         | Abre una secuencia de MIDI y recupera un identificador.                             |
| [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)           | Reproduce o pone en cola un flujo (búfer) de datos DE MIDI en un dispositivo de salida DE MIDI. |
| [**midiStreamPause**](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)       | Pausa la reproducción de una secuencia DE MIDI especificada.                             |
| [**midiStreamPosition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) | Recupera la posición actual en una secuencia DE MIDI.                        |
| [**midiStreamProperty**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamproperty) | Establece y recupera las propiedades del flujo.                                   |
| [**midiStreamRestart**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)   | Reinicia la reproducción de una secuencia DE MIDI en pausa.                              |
| [**midiStreamStop**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)         | Desactiva todas las notas de todos los canales MIDI para la secuencia DE MIDI especificada. |



 

 

 