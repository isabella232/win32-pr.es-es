---
description: Graph-Building componentes
ms.assetid: d803c56c-6fb1-4937-92e7-9ed2db2afc46
title: Graph-Building componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea3ba346356109d8080d887a510cfcb85b6a6c80
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251115"
---
# <a name="graph-building-components"></a>Graph-Building componentes

DirectShow proporciona varios componentes que se pueden usar para crear gráficos de filtro. que incluyen la siguiente información:

-   [Filtrar Graph Manager](filter-graph-manager.md). Este objeto controla el gráfico de filtro. Admite las interfaces [**IGraphBuilder,**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)e [**IMediaEventEx,**](/windows/desktop/api/Control/nn-control-imediaeventex) entre otras. Todas DirectShow aplicaciones usan este objeto en algún momento, aunque en algunos casos otro objeto crea el Administrador de filtros Graph para la aplicación.
-   [Capture Graph Builder](capture-graph-builder.md). Este objeto proporciona métodos adicionales para crear gráficos de filtro. Originalmente se diseñó para crear gráficos que realizan la captura de vídeo (de ahí el nombre), pero es útil para muchos otros tipos de gráficos de filtros personalizados. Admite la [**interfaz ICaptureGraphBuilder2.**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)
-   [Filtrar asignador y](filter-mapper.md) [enumerador de dispositivos del sistema](system-device-enumerator.md). Estos objetos localizan filtros que están registrados en el sistema del usuario o que representan dispositivos de hardware.
-   [DVD Graph Builder](dvd-graph-builder.md). Este objeto crea gráficos de filtro para la reproducción y navegación de DVD. Admite la [**interfaz IDvdGraphBuilder.**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder)

### <a name="intelligent-connect"></a>Inteligencia Conectar

El término "Conectar inteligente" abarca un conjunto de algoritmos que el Administrador de filtros Graph usa para compilar todo o parte de un gráfico de filtros. Cada vez que Graph Administrador de filtros requiere filtros adicionales para completar el gráfico, hace aproximadamente lo siguiente:

1.  Si hay un filtro actualmente en el gráfico, con al menos un pin de entrada no asociado, el Administrador de filtros Graph intenta usar ese filtro.
2.  De lo contrario, el Administrador de Graph busca en el Registro filtros que puedan aceptar el tipo de medio correcto para la conexión. Cada filtro tiene un valor del Registro denominado "Valor", que indica aproximadamente la probabilidad de que el filtro sea útil para completar el gráfico. El Administrador de Graph prueba los filtros en orden de valor de puntuación. Para cada tipo de secuencia (por ejemplo, audio, vídeo o MIDI), el representador predeterminado tiene un gran grado. Los descodificadores también tienen un gran grado. Los filtros de uso especial tienen poco peso.

Si el Administrador Graph filtros se queda bloqueado, se volverá a intentar y probará una combinación diferente de filtros. Puede encontrar los detalles exactos en el tema [Intelligent Conectar](intelligent-connect.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compilar el filtro Graph](building-the-filter-graph.md)
</dt> </dl>

 

 



