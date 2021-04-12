---
description: Componentes de Graph-Building
ms.assetid: d803c56c-6fb1-4937-92e7-9ed2db2afc46
title: Componentes de Graph-Building
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea3ba346356109d8080d887a510cfcb85b6a6c80
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152691"
---
# <a name="graph-building-components"></a>Componentes de Graph-Building

DirectShow proporciona varios componentes que se pueden usar para crear gráficos de filtro. Entre ellas, figuran:

-   [Filtre el administrador de gráficos](filter-graph-manager.md). Este objeto controla el gráfico de filtro. Admite las interfaces [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder), [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)y [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) , entre otros. Todas las aplicaciones de DirectShow usan este objeto en algún momento, aunque en algunos casos otro objeto crea el administrador de gráficos de filtro para la aplicación.
-   [Generador de gráficos de captura](capture-graph-builder.md). Este objeto proporciona métodos adicionales para generar gráficos de filtros. Originalmente se diseñó para crear gráficos que realizan capturas de vídeo (por lo tanto, el nombre), pero resultan útiles para muchos otros tipos de gráficos de filtros personalizados. Admite la interfaz [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) .
-   [Asignador de filtros](filter-mapper.md) y [enumerador de dispositivos del sistema](system-device-enumerator.md). Estos objetos buscan filtros que están registrados en el sistema del usuario o que representan dispositivos de hardware.
-   [Generador de gráficos de DVD](dvd-graph-builder.md). Este objeto crea gráficos de filtro para la reproducción y la navegación de DVD. Admite la interfaz [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) .

### <a name="intelligent-connect"></a>Conexión inteligente

El término "conexión inteligente" abarca un conjunto de algoritmos que el administrador de gráficos de filtro utiliza para compilar todo o parte de un gráfico de filtros. Siempre que el administrador de gráficos de filtro requiere filtros adicionales para completar el gráfico, realiza aproximadamente lo siguiente:

1.  Si hay un filtro actualmente en el gráfico, con al menos un PIN de entrada sin conexión, el administrador de gráficos de filtros intenta usar ese filtro.
2.  De lo contrario, Filter Graph Manager busca en el registro los filtros que pueden aceptar el tipo de medio correcto para la conexión. Cada filtro tiene un valor de registro denominado "mérito", que indica aproximadamente la probabilidad de que el filtro sea útil para completar el gráfico. Filter Graph Manager intenta filtrar en orden de valor de mérito. Para cada tipo de flujo (como audio, vídeo o MIDI), el representador predeterminado tiene un gran mérito. Los descodificadores también tienen un gran mérito. Los filtros de propósito especial tienen un mérito bajo.

Si el administrador de gráficos de filtro se bloquea, se devolverá y probará una combinación diferente de filtros. Puede encontrar los detalles exactos en el tema [conexión inteligente](intelligent-connect.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compilar el gráfico de filtro](building-the-filter-graph.md)
</dt> </dl>

 

 



