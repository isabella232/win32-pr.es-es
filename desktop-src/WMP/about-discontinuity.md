---
title: Acerca de la discontinuidad
description: Acerca de la discontinuidad
ms.assetid: 29210758-a1e6-47f2-9428-38f79623fbca
keywords:
- Reproductor de Windows Media complementos,DSP de audio
- complementos, DSP de audio
- complementos de procesamiento de señal digital, discontinuidad de audio
- Complementos DE DSP, discontinuidad de audio
- complementos DE DSP de audio, discontinuidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40de4c75c2d17699f0c72416873d64177e47d81761b27e5ffd465d89c9ecb9c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903575"
---
# <a name="about-discontinuity"></a>Acerca de la discontinuidad

En cualquier momento, Reproductor de Windows Media una interrupción en el flujo de entrada llamando al método **IMediaObject::D iscontinuity.** Esto se produce rutinariamente al principio y al final de una secuencia, y también antes de cada operación de búsqueda o cuando el contenido de streaming se interrumpe por cualquier motivo. El complemento DSP de ejemplo que genera el asistente Reproductor de Windows Media complemento de Reproductor de Windows Media no necesita tratar las discontinuidades por los siguientes motivos:

-   Las muestras de PCM son atómicas, lo que significa que se pueden procesar sin tener en cuenta las demás muestras de la secuencia. Algunos formatos de vídeo contienen datos que dependen de fotogramas clave y ejemplos comprimidos.
-   El código de ejemplo se escribe para forzar siempre al cliente a procesar toda la salida antes de que el complemento acepte más entradas.

La implementación predeterminada de **IMediaObject::D iscontinuity** simplemente devuelve S \_ OK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de un complemento dsp de audio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




