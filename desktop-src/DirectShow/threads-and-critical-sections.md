---
description: Subprocesos y secciones críticas
ms.assetid: e55acb06-03f4-4191-bffe-3196f41ef2c7
title: Subprocesos y secciones críticas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 576cb28e7e382db92328adf09980a825e71b5a3c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069997"
---
# <a name="threads-and-critical-sections"></a>Subprocesos y secciones críticas

En esta sección se describe el subprocesamiento DirectShow filtros y los pasos que debe seguir para evitar bloqueos o interbloqueos en un filtro personalizado.

Los ejemplos de esta sección usan el pseudocódigo para ilustrar el código que necesitará escribir. Se supone que un filtro personalizado usa clases derivadas de las DirectShow base, como se muestra a continuación:

-   CMyInputPin: se deriva de [**CBaseInputPin**](cbaseinputpin.md).
-   CMyOutputPin: se deriva de [**CBaseOutputPin**](cbaseoutputpin.md).
-   CMyFilter: derivado de [**CBaseFilter.**](cbasefilter.md)
-   CMyInputAllocator: el asignador del pin de entrada, derivado de [**CMemAllocator**](cmemallocator.md). No todos los filtros necesitan un asignador personalizado. Para muchos filtros, la **clase CMemAllocator** es suficiente.

Esta sección contiene los temas siguientes.

-   [Subprocesos de streaming y aplicación](the-streaming-and-application-threads.md)
-   [Pausando](pausing.md)
-   [Recepción y entrega de ejemplos](receiving-and-delivering-samples.md)
-   [Entrega del final de la secuencia](delivering-the-end-of-stream.md)
-   [Vaciar datos](flushing-data.md)
-   [Stopping](stopping.md) (Deteniéndose)
-   [Obtención de búferes](getting-buffers.md)
-   [Subprocesos de streaming y el Administrador de Graph filtros](streaming-threads-and-the-filter-graph-manager.md)
-   [Resumen de subprocesos de filtro](summary-of-filter-threading.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Datos Flow para desarrolladores de filtros](data-flow-for-filter-developers.md)
</dt> <dt>

[Escribir DirectShow filtros](writing-directshow-filters.md)
</dt> </dl>

 

 



