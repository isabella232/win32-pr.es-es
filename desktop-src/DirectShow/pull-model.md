---
description: Modelo de extracción
ms.assetid: b5246dfe-e6ee-4b91-bfe3-2ec8b8723938
title: Modelo de extracción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd4becd54bffb39acf30b6d29fca45e6a117989
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537161"
---
# <a name="pull-model"></a>Modelo de extracción

En la interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) , el filtro de nivel superior determina qué datos se van a enviar e incorpora los datos al filtro de bajada. En algunos filtros, un modelo de *extracción* es más adecuado. Aquí, el filtro de nivel inferior solicita datos del filtro de nivel superior. Los ejemplos siguen viajando hacia abajo, desde la clavija de salida a la clavija de entrada, pero el filtro de nivel inferior inicia el flujo de datos. Este tipo de conexión utiliza la interfaz [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .

El uso típico del modelo de extracción es la reproducción de archivos. Por ejemplo, en un gráfico de reproducción de AVI, el filtro de [origen de archivo asincrónico](file-source--async--filter.md) realiza operaciones de lectura de archivos genéricas y entrega los datos como un flujo de bytes, sin información de formato. El filtro de [divisor de AVI](avi-splitter-filter.md) Lee los encabezados AVI y analiza el flujo en muestras de audio y vídeo. El divisor de AVI puede determinar qué datos necesita mejor que el filtro de origen de archivo asincrónico y, por lo tanto, usa **IAsyncReader** en lugar de **IMemInputPin**.

Para solicitar datos del PIN de salida, el PIN de entrada llama a uno de los métodos siguientes:

-   [**IAsyncReader:: Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request)
-   [**IAsyncReader::SyncRead**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncread)
-   [**IAsyncReader:: SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned).

El primer método es asincrónico, para admitir varias lecturas superpuestas. Los demás son sincrónicos.

En teoría, cualquier filtro puede admitir **IAsyncReader**, pero en la práctica está diseñado para los filtros de origen que se conectan a los filtros del analizador. El analizador actúa de forma muy similar a un filtro de origen en el modelo de extracción. Cuando se pausa, se crea un subproceso de streaming que extrae datos de la conexión **IAsyncReader** y los envía a nivel inferior. Los pin de salida usan **IMemInputPin** y el resto del gráfico usa el modelo de la instalación estándar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Flujo de datos en el gráfico de filtros](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



