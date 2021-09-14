---
description: Acerca de Digital Video en DirectShow
ms.assetid: 0570bf7c-c38d-4ada-9593-27b9be117893
title: Acerca de Digital Video en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f4ae0253754583bb89132289db87f0aad673d6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162490"
---
# <a name="about-digital-video-in-directshow"></a>Acerca de Digital Video en DirectShow

El vídeo digital (DV) se puede capturar desde una cámara DV, almacenarse en un archivo en el equipo del usuario o almacenarse en cinta mediante una grabadora de cinta de vídeo (VTR). Por lo tanto, las operaciones que una aplicación puede realizar en una secuencia DV incluyen:

-   Captura de vídeo en directo desde una cámara DV.
-   Transmita datos DV de la cinta VTR al equipo.
-   Transmitir datos DV desde el equipo a VTR.
-   Lee datos DV de un archivo.
-   Escribir datos DV en un archivo.
-   Represente el audio y el vídeo en una secuencia DV.

DirectShow proporciona los siguientes filtros DV:

-   [Controlador MSDV](msdv-driver.md). El controlador MSDV controla un dispositivo DV, como una cámara de vídeo. El dispositivo puede tener una subunidad de cámara y una subunidad VTR. MSDV controla ambas subunidades. El controlador MSDV aparece en las aplicaciones como un DirectShow filtro.
-   [Filtro de divisor DV.](dv-splitter-filter.md) Los marcos DV contienen audio y vídeo en el mismo fotograma. El filtro divisor DV extrae los datos de audio y los genera como una o dos secuencias de audio. Genera los datos originales como una secuencia de vídeo DV independiente.
-   [Filtro descodificador de vídeo DV.](dv-video-decoder-filter.md) Descodifica vídeo DV en vídeo sin comprimir.
-   [Filtro DV Video Encoder.](dv-video-encoder-filter.md) Codifica vídeo sin comprimir en vídeo codificado en DV.
-   [DV Muxer](dv-muxer-filter.md). Combina una secuencia de vídeo DV con una o dos secuencias de audio para crear una única secuencia DV intercalada.

El divisor DV y el descodificador de vídeo DV funcionan juntos. El divisor toma la secuencia intercalada y genera secuencias de audio y vídeo DV independientes. El descodificador convierte el vídeo DV en vídeo sin comprimir. En la imagen siguiente se muestra este proceso.

![divisor dv y descodificador dv](images/dv-filters1.png)

Dv Video Encoder y DV Muxer invierten el proceso: el codificador convierte vídeo sin comprimir en vídeo DV y el mux combina audio y vídeo DV para crear una única secuencia intercalada, como se muestra en el diagrama siguiente.

![codificador dv y dv muxer](images/dv-filters2.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



