---
description: Modelo de extracción
ms.assetid: b5246dfe-e6ee-4b91-bfe3-2ec8b8723938
title: Modelo de extracción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9832f719e21d85fd09fbf92303e404290d7d99efd6953ace398f77167d0263a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747895"
---
# <a name="pull-model"></a>Modelo de extracción

En la [**interfaz IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) el filtro ascendente determina qué datos enviar e inserta los datos en el filtro de bajada. Para algunos filtros, un *modelo de extracción* es más adecuado. En este caso, el filtro de nivel inferior solicita datos del filtro ascendente. Los ejemplos siguen fluyendo hacia abajo, desde el pin de salida al pin de entrada, pero el filtro de bajada inicia el flujo de datos. Este tipo de conexión usa la [**interfaz IAsyncReader.**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader)

El uso típico del modelo de extracción es en la reproducción de archivos. Por ejemplo, en un gráfico de reproducción de AVI, el filtro [Async File Source](file-source--async--filter.md) realiza operaciones genéricas de lectura de archivos y entrega los datos como una secuencia de bytes, sin información de formato. El [filtro divisor AVI](avi-splitter-filter.md) lee los encabezados AVI y analiza la secuencia en muestras de vídeo y audio. El divisor AVI puede determinar qué datos necesita mejor que el filtro Async File Source y, por tanto, usa **IAsyncReader** en lugar de **IMemInputPin**.

Para solicitar datos del pin de salida, el pin de entrada llama a uno de los métodos siguientes:

-   [**IAsyncReader::Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request)
-   [**IAsyncReader::SyncRead**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncread)
-   [**IAsyncReader::SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned).

El primer método es asincrónico, para admitir varias lecturas superpuestas. Los demás son sincrónicos.

En teoría, cualquier filtro puede admitir **IAsyncReader,** pero en la práctica está diseñado para filtros de origen que se conectan a filtros de analizador. El analizador actúa de forma muy parecido a un filtro de origen en el modelo de inserción. Cuando se pone en pausa, crea un subproceso de streaming que extrae datos de la conexión **IAsyncReader** y los inserta de bajada. Los pines de salida **usan IMemInputPin** y el resto del gráfico usa el modelo de inserción estándar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Datos Flow en el filtro Graph](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



