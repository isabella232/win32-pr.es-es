---
description: Temas de captura avanzada
ms.assetid: 407702b2-5f4f-424d-a3ec-b0473e1b0da3
title: Temas de captura avanzada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4c4e5a077f6f8b17543250efa0f10091f0917e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152518"
---
# <a name="advanced-capture-topics"></a>Temas de captura avanzada

En esta sección se describen algunos aspectos avanzados de la captura de vídeo en DirectShow. La mayoría de los problemas descritos en esta sección se controlan automáticamente mediante la interfaz [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) . Sin embargo, esta información puede ser útil si necesita solucionar problemas de una aplicación de captura de vídeo. También debe leer esta sección si la aplicación genera un gráfico de captura personalizado de algún tipo y observa que ICaptureGraphBuilder2 no se adapta a sus necesidades. Por último, en esta sección se incluye información sobre el uso del filtro de representador de mezcla de vídeo (VMR) en una aplicación de captura de vídeo.

Es posible crear un gráfico de captura de vídeo completamente mediante métodos [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) . También puede combinar las dos interfaces, usando ICaptureGraphBuilder2 para algunas tareas y IGraphBuilder para otras.

Esta sección contiene los siguientes temas:

-   [Control de eventos Repaint en la captura de vídeo](handling-repaint-events-in-video-capture.md)
-   [Trabajar con categorías de PIN](working-with-pin-categories.md)
-   [Usar el filtro Smart Tee](using-the-smart-tee-filter.md)
-   [Usar el mezclador de superposición en la captura de vídeo](using-the-overlay-mixer-in-video-capture.md)
-   [PIN de puerto de vídeo](video-port-pins.md)
-   [Tipo de formato VideoInfo2](videoinfo2-format-type.md)
-   [Crear filtros de Kernel-Mode](creating-kernel-mode-filters.md)
-   [Filtros de controlador de clase WDM](wdm-class-driver-filters.md)
-   [Usar la captura de WDDM en DirectShow](using-wddm-capture-in-directshow.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 



