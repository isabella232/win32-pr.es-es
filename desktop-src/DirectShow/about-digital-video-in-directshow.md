---
description: Acerca de vídeo digital en DirectShow
ms.assetid: 0570bf7c-c38d-4ada-9593-27b9be117893
title: Acerca de vídeo digital en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f4ae0253754583bb89132289db87f0aad673d6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104569409"
---
# <a name="about-digital-video-in-directshow"></a>Acerca de vídeo digital en DirectShow

El vídeo digital (DV) se puede capturar desde una cámara DV, almacenarse en un archivo en el equipo del usuario o almacenarse en cinta con una grabadora de cintas de vídeo (VTR). Por lo tanto, las operaciones que puede realizar una aplicación en una secuencia DV incluyen:

-   Capturar vídeo en directo desde una cámara DV.
-   Transmita datos DV desde cinta VTR al equipo.
-   Transmita datos de DV del equipo al VTR.
-   Leer datos de DV desde un archivo.
-   Escribir datos de DV en un archivo.
-   Representar el audio y el vídeo en un flujo DV.

DirectShow proporciona los siguientes filtros DV:

-   [Controlador MSDV](msdv-driver.md). El controlador MSDV controla un dispositivo DV, como una videocámara. El dispositivo puede tener una subunidad de cámara y una subunidad de VTR; MSDV controla ambas subunidads. El controlador MSDV aparece en las aplicaciones como un filtro DirectShow.
-   Filtro de [divisor DV](dv-splitter-filter.md) . Los fotogramas DV contienen audio y vídeo en el mismo fotograma. El filtro de divisor DV extrae los datos de audio y los envía como uno o dos flujos de audio. Genera los datos originales como una secuencia de vídeo DV independiente.
-   Filtro de [descodificador de vídeo DV](dv-video-decoder-filter.md) . Descodifica vídeo DV en vídeo sin comprimir.
-   Filtro de [codificador de vídeo DV](dv-video-encoder-filter.md) . Codifica vídeo sin comprimir en vídeo codificado en DV.
-   [DV multiplexor](dv-muxer-filter.md). Combina una secuencia de vídeo DV con uno o dos flujos de audio para crear una única secuencia DV intercalada.

El divisor de DV y el descodificador de vídeo DV funcionan juntos. El divisor toma el flujo intercalado y genera secuencias de vídeo de audio y DV independientes. El descodificador convierte el vídeo DV en vídeo sin comprimir. En la imagen siguiente se ilustra este proceso.

![divisor DV y descodificador DV](images/dv-filters1.png)

El codificador de vídeo DV y el multiplexor DV invierten el proceso: el codificador convierte el vídeo sin comprimir en vídeo DV y el MUX combina audio y vídeo DV para crear una única secuencia intercalada, tal como se muestra en el diagrama siguiente.

![codificador DV y DV multiplexor](images/dv-filters2.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



