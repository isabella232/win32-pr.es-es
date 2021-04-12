---
description: Televisión analógica
ms.assetid: 9f2c18ec-3684-42a8-a3df-5f8827b27642
title: Televisión analógica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33af8ba94831afed59d783598dbf6bc0eaee0ec6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152246"
---
# <a name="analog-television"></a>Televisión analógica

La televisión analógica es diferente de otros escenarios de captura de vídeo de varias maneras:

-   La tarjeta de sintonizador se ajusta a una señal analógica, que luego se digitaliza.
-   El audio se lleva a cabo en la señal analógica. La forma en que el audio alcanza la tarjeta de sonido varía en función del hardware.
-   La señal puede contener datos adicionales en el intervalo de espacio en blanco (VBI) vertical, como subtítulos (CC), teletexto estándar universal (elemento WST) y Extended Data Services (XDS).

En el diagrama siguiente se muestra un gráfico de filtro típico para la vista previa de televisión.

![gráfico de televisión analógica](images/vidcap06.png)

-   El filtro de [sintonizador de TV](tv-tuner-filter.md) controla la optimización.
-   El filtro de [audio de TV](tv-audio-filter.md) controla la descodificación de audio.
-   Si la tarjeta de sintonizador tiene más de una entrada física, el filtro de [Cruz de vídeo analógico](analog-video-crossbar-filter.md) permite a la aplicación seleccionar qué entrada se descodifica y se representa.
-   El filtro de [captura de vídeo WDM](wdm-video-capture-filter.md) entrega el flujo de vídeo digitalizado.

El generador de gráficos de captura inserta automáticamente los filtros que se requieren al ascendente desde el filtro de captura.

Esta sección contiene los siguientes temas:

-   [Optimización de televisión analógica](analog-television-tuning.md)
-   [Audio analógico de televisión](analog-television-audio.md)
-   [Subtítulos y teletexto](closed-captions-and-teletext.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 



