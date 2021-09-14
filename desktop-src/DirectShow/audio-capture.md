---
description: Captura de audio
ms.assetid: 2b7fbdcb-7b59-407e-8e82-e66bd5606507
title: Captura de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e91c9063d96a5e56d078651c338b0ffd80f5aa79
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162214"
---
# <a name="audio-capture"></a>Captura de audio

Una aplicación puede usar DirectShow para capturar datos de audio de micrófonos, reproductores de cinta y otros dispositivos, a través de las entradas de la tarjeta de sonido. Entre los escenarios típicos se incluyen:

-   Grabación de una narración de voz en voz para su posterior reproducción en una secuencia de vídeo.
-   Convertir contenido de audio análogo heredado al formato digital.
-   Captura de voz o música para la transmisión a través de una red.

Los usuarios finales tienen varias opciones para capturar audio desde la tarjeta de sonido al disco duro. La mayoría de las tarjetas proporcionan aplicaciones para mezclar y grabar desde sus entradas de audio. Windows proporciona Sound Recorder, una sencilla aplicación de utilidad para grabar desde un micrófono. El Windows media encoder se puede incorporar a una aplicación DirectShow como un [objeto multimedia DirectX](directx-media-objects.md) (DMO). En esta sección se describe cómo integrar la funcionalidad de captura de audio dentro de su propia aplicación mediante DirectShow.

Esta sección contiene los siguientes temas:

-   [Acerca del filtro de captura de audio](about-the-audio-capture-filter.md)
-   [Selección de un dispositivo de captura](selecting-a-capture-device.md)
-   [Creación de una captura de audio Graph](creating-an-audio-capture-graph.md)
-   [Creación de una captura de audio Graph vista previa](creating-an-audio-capture-graph-with-preview.md)
-   [Establecer propiedades de captura de audio](setting-audio-capture-properties.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de DirectShow](using-directshow.md)
</dt> </dl>

 

 



