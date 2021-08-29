---
description: Temas de captura avanzada
ms.assetid: 407702b2-5f4f-424d-a3ec-b0473e1b0da3
title: Temas de captura avanzada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d80ba7615b0ad42bbfe62ae646a4cf7e58897cb678eae836b2b5329eda0e17c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690515"
---
# <a name="advanced-capture-topics"></a>Temas de captura avanzada

En esta sección se describen algunos aspectos avanzados de la captura de vídeo DirectShow. La mayoría de los problemas descritos en esta sección se controlan automáticamente mediante la [**interfaz ICaptureGraphBuilder2.**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) Sin embargo, la información aquí puede ser útil si necesita solucionar problemas de una aplicación de captura de vídeo. También debe leer esta sección si la aplicación compila un gráfico de captura personalizado de algún tipo y descubre que ICaptureGraphBuilder2 no se adapta a sus necesidades. Por último, esta sección contiene información sobre el uso del filtro De representador de mezcla de vídeo (VMR) en una aplicación de captura de vídeo.

Es posible crear un gráfico de captura de vídeo completamente mediante métodos [**IGraphBuilder.**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) También puede combinar las dos interfaces, mediante ICaptureGraphBuilder2 para algunas tareas e IGraphBuilder para otras.

Esta sección contiene los siguientes temas:

-   [Control de eventos de repintado en la captura de vídeo](handling-repaint-events-in-video-capture.md)
-   [Trabajar con categorías de pin](working-with-pin-categories.md)
-   [Uso del filtro de tee inteligente](using-the-smart-tee-filter.md)
-   [Uso de la función overlay Mixer captura de vídeo](using-the-overlay-mixer-in-video-capture.md)
-   [Patillas de puerto de vídeo](video-port-pins.md)
-   [Tipo de formato VideoInfo2](videoinfo2-format-type.md)
-   [Creación de Kernel-Mode filtros](creating-kernel-mode-filters.md)
-   [Filtros de controlador de clase WDM](wdm-class-driver-filters.md)
-   [Uso de la captura wddm en DirectShow](using-wddm-capture-in-directshow.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 



