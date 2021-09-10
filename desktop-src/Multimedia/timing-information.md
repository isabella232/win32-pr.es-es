---
title: Información de tiempo
description: Información de tiempo
ms.assetid: ff9d6fb2-1387-49ce-a4de-1b2f67353628
keywords:
- Interfaz digital de instrumentar música (MIDI), información de control de tiempo
- MIDI (Interfaz digital de instrumentar música), información de control de tiempo
- búferes de flujo, información de control de tiempo
- Estructura MIDIEVENT
- búferes de flujo, formato SMPTE
- búferes de flujo, hora de la nota del trimestre
- búferes de flujo, pasos
- Formato SMPTE
- hora de la nota del trimestre
- ticks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2daf5b1847456e8fb518665521e484118fead79
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371053"
---
# <a name="timing-information"></a>Información de tiempo

La información de control de tiempo de un evento MIDI se almacena en el **miembro dwDeltaTime** de la [**estructura MIDIEVENT.**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) El tiempo se da en pasos, tal como se define en la *especificación Standard MIDI Files 1.0.* La longitud de un paso se define por el formato de hora y, posiblemente, el tempo asociado a la secuencia. Para obtener más información sobre las secuencias, vea [LA SECUENCIAS](midi-streams.md).

Un tic se expresa como microsegundos por nota de trimestre o como tics de tiempo de SMPTE (Society of Motion Picture and Tv Engineers). Las aplicaciones que envían mensajes MIDI individualmente o usan mensajes MIDI no procesados usan información de tiempo de nota trimestral y tempo para determinar la duración de un paso. Las aplicaciones que preprocesen mensajes MIDI pueden almacenar el tiempo transcurrido como un recuento de las unidades de SMPTE que se usan.

El tiempo de la nota del trimestre se indica con un cero en el bit de palabra alta (bit 15) de la palabra de división de tiempo. El resto de la palabra contiene los tics por nota de trimestre. Un tempo asociado a una secuencia de datos DE MIDI se mantiene en unidades (microsegundos por nota de trimestre) coherentes con la especificación Standard *MIDI Files 1.0.* Por ejemplo, un cuarto de nota en tiempo de 4/4 que usa un tempo de 500 000 microsegundos por trimestre se reproduce a una velocidad de 120 latidos por minuto.

Los formatos de división de tiempo de SMPTE especifican completamente la longitud de un tic sin necesidad de información de tempo. Al usar formatos de hora SMPTE, las secuencias DE MIDI se pueden sincronizar con otros eventos SMPTE, como vídeo o audio seccionado. La hora de SMPTE se indica con un 1 en el bit de orden superior (bit 15) de la palabra de división de tiempo. El resto del byte más significativo especifica el formato SMPTE en uso como valores negativos. Los formatos SMPTE admitidos y sus valores correspondientes (entre paréntesis) son 24 (-24), 25 (-25), 30 (-30) y 30 drop (-29). El byte bajo de la palabra de división de tiempo especifica el número de pasos por fotograma de SMPTE.

 

 