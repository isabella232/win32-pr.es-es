---
description: Anclar conexiones
ms.assetid: 1406ade4-77d8-49a7-8f36-cc49ff007a26
title: Anclar conexiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cfcd407e785e15f4243f3113a63569f8b4b84de517cdde0f63a88eaef79f85c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432295"
---
# <a name="pin-connections"></a>Anclar conexiones

Los filtros se conectan en sus pines, a través de la [**interfaz IPin.**](/windows/desktop/api/Strmif/nn-strmif-ipin) Los pines de salida se conectan a los pines de entrada. Cada conexión de pin tiene un tipo de medio, descrito por la [**estructura \_ AM MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type)

Una aplicación conecta filtros llamando a métodos en el Administrador de filtros Graph, nunca llamando a métodos en los filtros o anclados ellos mismos. La aplicación puede especificar directamente los filtros que se conectarán mediante una llamada al método [**IFilterGraph::ConnectDirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) o [**IGraphBuilder::Conectar;**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) o puede conectar filtros indirectamente, mediante un método de creación de grafos como [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile).

Para que la conexión se realiza correctamente, ambos filtros deben estar en el gráfico de filtros. La aplicación puede agregar un filtro al gráfico llamando al [**método IFilterGraph::AddFilter.**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) El Administrador Graph filtros también puede agregar filtros al gráfico. Cuando se agrega un filtro, el Administrador de Graph llama al método [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) del filtro para notificarlo.

El esquema general del proceso de conexión es el siguiente:

1.  El Administrador de Graph llama a [**IPin::Conectar**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) en el pin de salida y pasa un puntero al pin de entrada.
2.  Si el pin de salida acepta la conexión, llama a [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) en el pin de entrada.
3.  Si el pin de entrada también acepta la conexión, el intento de conexión se realiza correctamente y los pines están conectados.

Algunos pines se pueden desconectar y volver a conectar mientras el filtro está activo. Este tipo de reconexión se denomina *reconexión* dinámica. Para obtener más información, vea [Dynamic Graph Building](dynamic-graph-building.md). Sin embargo, la mayoría de los filtros no admiten la reconexión dinámica.

Normalmente, los filtros se conectan en orden descendente; es decir, los pines de entrada del filtro se conectan antes que sus pasadores de salida. Un filtro siempre debe admitir este orden de conexión. Algunos filtros también admiten conexiones en el orden opuesto: los pins de salida primero, seguidos de los pines de entrada. Por ejemplo, podría ser posible conectar el pin de salida de un filtro MUX al filtro file-writer antes de conectar los pines de entrada del filtro MUX.

Cuando se llama al método **Conectar** o **ReceiveConnection** de un pin, el pin debe comprobar que puede admitir la conexión. Los detalles dependen del filtro concreto. Entre las tareas más comunes se incluyen las siguientes:

-   Comprobación de que el tipo de medio es aceptable
-   Negociación de un asignador
-   Consulte el otro pin para obtener las interfaces necesarias.

 

 



