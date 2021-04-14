---
description: Captura de audio
ms.assetid: 2b7fbdcb-7b59-407e-8e82-e66bd5606507
title: Captura de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e91c9063d96a5e56d078651c338b0ffd80f5aa79
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104360002"
---
# <a name="audio-capture"></a>Captura de audio

Una aplicación puede usar DirectShow para capturar datos de audio de micrófonos, reproductores de cinta y otros dispositivos a través de las entradas de la tarjeta de sonido. Entre los escenarios típicos se incluyen:

-   Grabar una narración de VoiceOver para grabaciones posteriores en una secuencia de vídeo.
-   Conversión de contenido de audio analógico heredado a formato digital.
-   Capturar voz o música para su transmisión a través de una red.

Los usuarios finales tienen varias opciones para capturar audio de la tarjeta de sonido en el disco duro. La mayoría de las tarjetas proporcionan aplicaciones para mezclar y grabar desde sus entradas de audio. Windows proporciona grabadora de sonidos, una sencilla aplicación de utilidad para grabar desde un micrófono. El codificador de Windows Media se puede incorporar en una aplicación de DirectShow como un [objeto multimedia de DirectX](directx-media-objects.md) (DMO). En esta sección se describe cómo integrar la funcionalidad de captura de audio dentro de su propia aplicación mediante DirectShow.

Esta sección contiene los siguientes temas:

-   [Acerca del filtro de captura de audio](about-the-audio-capture-filter.md)
-   [Selección de un dispositivo de captura](selecting-a-capture-device.md)
-   [Creación de un gráfico de captura de audio](creating-an-audio-capture-graph.md)
-   [Creación de un gráfico de captura de audio con vista previa](creating-an-audio-capture-graph-with-preview.md)
-   [Establecer propiedades de captura de audio](setting-audio-capture-properties.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar DirectShow](using-directshow.md)
</dt> </dl>

 

 



