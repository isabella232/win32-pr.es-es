---
title: Información de tiempo
description: Información de tiempo
ms.assetid: ff9d6fb2-1387-49ce-a4de-1b2f67353628
keywords:
- Interfaz digital de instrumentos musicales (MIDI), información de tiempo
- MIDI (interfaz digital de instrumentos musicales), información de tiempo
- búferes de secuencia, información de tiempo
- Estructura MIDIEVENT
- búferes de secuencia, formato SMPTE
- búferes de secuencia, tiempo de nota trimestral
- búferes de secuencia, TICs
- Formato SMPTE
- hora de la nota del cuarto
- ticks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2daf5b1847456e8fb518665521e484118fead79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149198"
---
# <a name="timing-information"></a>Información de tiempo

La información de tiempo de un evento MIDI se almacena en el miembro **dwDeltaTime** de la estructura [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) . La hora se indica en pasos, tal como se define en la especificación de *los archivos MIDI estándar 1,0* . La longitud de un paso se define en el formato de hora y, posiblemente, en el tempo asociado a la secuencia. Para obtener más información sobre las secuencias, consulte [MIDI transmisiones](midi-streams.md).

Un paso se expresa como una nota de microsegundos por trimestre o como TICs del tiempo de SMPTE (sociedad de la imagen de movimiento y de ingenieros de televisión). Las aplicaciones que envían mensajes MIDI individualmente o utilizan mensajes MIDI no procesados usan la información del tiempo y el tiempo de la nota del cuarto para determinar la duración de un TIC. Las aplicaciones que preprocesan mensajes MIDI pueden almacenar el tiempo transcurrido como un recuento de las unidades SMPTE que se usan.

La hora de la nota del trimestre se indica con un cero en el bit de palabra superior (bit 15) de la palabra de la división de hora. El resto de la palabra contiene la nota TICs por trimestre. Un tempo asociado con una secuencia de datos MIDI se mantiene en unidades (microsegundos por cuarto de nota) coherente con la especificación de *los archivos MIDI estándar 1,0* . Por ejemplo, una nota de trimestre en 4/4 de tiempo que usa un tempo de 500.000 microsegundos por cuarto de nota se reproduce a la tarifa de 120 pulsaciones por minuto.

Los formatos de división de tiempo SMPTE especifican por completo la duración de un TIC sin necesidad de información sobre el tempo. En el uso de formatos de hora SMPTE, las secuencias MIDI se pueden sincronizar con otros eventos SMPTE, como vídeo o audio seccionado. La hora SMPTE se indica con un 1 en el bit de orden superior (bit 15) de la palabra de la división de hora. El resto del byte más significativo especifica el formato SMPTE en uso como valores negativos. Los formatos SMPTE admitidos y sus valores correspondientes (entre paréntesis) son 24 (-24), 25 (-25), 30 (-30) y 30 Drop (-29). El byte bajo de la palabra de división de hora especifica el número de TICs por fotograma SMPTE.

 

 