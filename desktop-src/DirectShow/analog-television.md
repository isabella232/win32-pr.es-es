---
description: Televisión análoga
ms.assetid: 9f2c18ec-3684-42a8-a3df-5f8827b27642
title: Televisión análoga
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 886c2b3f93ca70fb4a533f131611431c4a15df51169f70ed49f321c0ccfc8c2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824768"
---
# <a name="analog-television"></a>Televisión análoga

La televisión análoga difiere de otros escenarios de captura de vídeo de varias maneras:

-   La tarjeta de afinador se afina a una señal análoga, que luego se digitaliza.
-   El audio se lleva en la señal análoga. La forma en que el audio llega a la tarjeta de sonido varía en función del hardware.
-   La señal puede contener datos adicionales en el intervalo de espacio en blanco vertical (VBI), como subtítulos (CC), teletexto estándar mundial (WST) y servicios de datos extendidos (XDS).

En el diagrama siguiente se muestra un gráfico de filtros típico para la vista previa de televisión.

![gráfico de televisión análoga](images/vidcap06.png)

-   El [filtro tv Tuner controla](tv-tuner-filter.md) el ajuste.
-   El [filtro tv Audio](tv-audio-filter.md) controla la decodificación de audio.
-   Si la tarjeta de afinador tiene más de una entrada física, el filtro [de](analog-video-crossbar-filter.md) barra cruzada de vídeo análogo permite a la aplicación seleccionar qué entrada se descodifica y representa.
-   El [filtro captura de vídeo wdm](wdm-video-capture-filter.md) entrega la secuencia de vídeo digitalizado.

Capture Graph Builder inserta automáticamente los filtros que se requieren en la parte superior del filtro de captura.

Esta sección contiene los siguientes temas:

-   [Ajuste de televisión análoga](analog-television-tuning.md)
-   [Audio de televisión análoga](analog-television-audio.md)
-   [Subtítulos y teletexto](closed-captions-and-teletext.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 



