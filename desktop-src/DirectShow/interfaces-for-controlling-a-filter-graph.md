---
description: Interfaces para controlar un gráfico de filtros
ms.assetid: f7de0165-e356-45d5-baed-d127caeebaf6
title: Interfaces para controlar un gráfico de filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e88dc4ba2143bbbf33a58763a5ff9005254236
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806481"
---
# <a name="interfaces-for-controlling-a-filter-graph"></a>Interfaces para controlar un gráfico de filtros

Estas interfaces proporcionan métodos para controlar un gráfico de filtro.



| Interfaz                                  | Descripción                                                                                               |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust)   | Ajuste el reloj del gráfico.                                                                                   |
| [**IAMGraphStreams**](/windows/desktop/api/Strmif/nn-strmif-iamgraphstreams) | Sincronizar secuencias en directo en un gráfico de filtro.                                                               |
| [**IFilterChain**](/windows/desktop/api/Strmif/nn-strmif-ifilterchain)       | Controlan las cadenas de filtros.                                                                                |
| [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)     | Ejecutar, pausar y detener el gráfico de filtro. (También proporciona métodos compatibles con automatización para crear gráficos). |
| [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex)     | Responder a eventos en el gráfico.                                                                           |
| [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)     | Buscar dentro de un archivo.                                                                                       |
| [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand)     | Comandos de cola que se ejecutarán más adelante.                                                                    |
| [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) | Marco: recorra paso a paso un flujo de vídeo.                                                                        |



 

 

 



