---
description: Temas de captura avanzada
ms.assetid: 407702b2-5f4f-424d-a3ec-b0473e1b0da3
title: Temas de captura avanzada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4c4e5a077f6f8b17543250efa0f10091f0917e8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162389"
---
# <a name="advanced-capture-topics"></a>Temas de captura avanzada

En esta sección se describen algunos aspectos avanzados de la captura de vídeo DirectShow. La mayoría de los problemas descritos en esta sección se controlan automáticamente mediante la [**interfaz ICaptureGraphBuilder2.**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) Sin embargo, la información aquí puede ser útil si necesita solucionar problemas de una aplicación de captura de vídeo. También debe leer esta sección si la aplicación compila un gráfico de captura personalizado de algún tipo y descubre que ICaptureGraphBuilder2 no se adapta a sus necesidades. Por último, esta sección contiene información sobre el uso del filtro Representador de mezcla de vídeo (VMR) en una aplicación de captura de vídeo.

Es posible crear un gráfico de captura de vídeo completamente mediante métodos [**IGraphBuilder.**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) También puede combinar las dos interfaces, mediante ICaptureGraphBuilder2 para algunas tareas e IGraphBuilder para otras.

Esta sección contiene los siguientes temas:

-   [Control de eventos de repintado en la captura de vídeo](handling-repaint-events-in-video-capture.md)
-   [Trabajar con categorías de pin](working-with-pin-categories.md)
-   [Uso del filtro smart tee](using-the-smart-tee-filter.md)
-   [Uso de la función overlay Mixer captura de vídeo](using-the-overlay-mixer-in-video-capture.md)
-   [Anclar puertos de vídeo](video-port-pins.md)
-   [Tipo de formato VideoInfo2](videoinfo2-format-type.md)
-   [Creación de Kernel-Mode filtros](creating-kernel-mode-filters.md)
-   [Filtros de controlador de clase WDM](wdm-class-driver-filters.md)
-   [Uso de la captura de WDDM en DirectShow](using-wddm-capture-in-directshow.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 



