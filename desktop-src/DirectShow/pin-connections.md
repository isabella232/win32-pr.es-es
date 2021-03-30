---
description: Anclar conexiones
ms.assetid: 1406ade4-77d8-49a7-8f36-cc49ff007a26
title: Anclar conexiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b509abddf4a915b65dfd322f76b4afb132a7f835
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422841"
---
# <a name="pin-connections"></a>Anclar conexiones

Los filtros se conectan a sus pin a través de la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) . Los pin de salida se conectan a los pin de entrada. Cada conexión de pin tiene un tipo de medio, descrito por la estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

Una aplicación conecta filtros mediante la llamada a métodos en el administrador de gráficos de filtro, nunca llamando a métodos en los filtros o PIN. La aplicación puede especificar directamente los filtros que se van a conectar, llamando al método [**IFilterGraph:: ConnectDirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) o [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) ; o bien, puede conectar los filtros indirectamente mediante un método de creación de gráficos como [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile).

Para que la conexión se realice correctamente, ambos filtros deben estar en el gráfico de filtro. La aplicación puede Agregar un filtro al gráfico llamando al método [**IFilterGraph:: addFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) . El administrador de gráficos de filtro también puede Agregar filtros al gráfico. Cuando se agrega un filtro, el administrador de gráficos de filtros llama al método [**IBaseFilter:: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) del filtro para notificar al filtro.

El esquema general del proceso de conexión es el siguiente:

1.  El administrador de gráficos de filtro llama a [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) en el terminal de salida, pasando un puntero al pin de entrada.
2.  Si el PIN de salida acepta la conexión, llama a [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) en el PIN de entrada.
3.  Si el PIN de entrada también acepta la conexión, el intento de conexión se realiza correctamente y los pin están conectados.

Algunos PIN se pueden desconectar y volver a conectar mientras el filtro está activo. Este tipo de reconexión se denomina reconexión *dinámica* . Para obtener más información, vea [creación de gráficos dinámicos](dynamic-graph-building.md). Sin embargo, la mayoría de los filtros no admiten la reconexión dinámica.

Normalmente, los filtros se conectan en orden descendente; es decir, los pines de entrada del filtro están conectados antes de sus clavijas de salida. Un filtro siempre debe admitir este orden de conexión. Algunos filtros también admiten conexiones en el orden opuesto: los pin de salida primero, seguidos de los pin de entrada. Por ejemplo, podría ser posible conectar un PIN de salida del filtro MUX al filtro de escritura de archivos antes de conectar los pin de entrada del filtro MUX.

Cuando se llama al método **Connect** o **ReceiveConnection** de un PIN, el PIN debe comprobar que puede admitir la conexión. Los detalles dependen del filtro determinado. Entre las tareas más comunes se incluyen las siguientes:

-   Comprobar que el tipo de medio es aceptable
-   Negociar un asignador
-   Consulte el otro PIN para obtener las interfaces necesarias.

 

 



