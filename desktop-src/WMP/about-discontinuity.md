---
title: Acerca de la discontinuidad
description: Acerca de la discontinuidad
ms.assetid: 29210758-a1e6-47f2-9428-38f79623fbca
keywords:
- Complementos de Windows Media Player, audio DSP
- complementos, DSP de audio
- Complementos de procesamiento de señal digital, discontinuidad de audio
- Complementos DSP, discontinuidad de audio
- Complementos de DSP de audio, discontinuidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0448220d4616122b3c99670357bbbd78de11c392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418418"
---
# <a name="about-discontinuity"></a>Acerca de la discontinuidad

En cualquier momento, Windows Media Player puede señalar una interrupción en el flujo de entrada mediante una llamada al método **IMediaObject::D iscontinuity** . Esto se produce habitualmente al principio y al final de una secuencia, y también antes de cada operación de búsqueda o cuando se interrumpe el contenido de streaming por cualquier motivo. El complemento DSP de ejemplo que genera el Asistente para complementos de Windows Media Player no necesita tratar con discontinuidad por los siguientes motivos:

-   Los ejemplos de PCM son atómicos, lo que significa que se pueden procesar sin tener en cuenta los demás ejemplos de la secuencia. Algunos formatos de vídeo contienen datos que dependen de fotogramas clave y ejemplos comprimidos.
-   El código de ejemplo se escribe para obligar siempre al cliente a procesar todos los resultados antes de que el complemento acepte más entradas.

La implementación predeterminada de **IMediaObject::D iscontinuity** simplemente devuelve S \_ OK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementar un complemento de DSP de audio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




