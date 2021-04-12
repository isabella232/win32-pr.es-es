---
description: Subprocesos y secciones críticas
ms.assetid: e55acb06-03f4-4191-bffe-3196f41ef2c7
title: Subprocesos y secciones críticas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 576cb28e7e382db92328adf09980a825e71b5a3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361666"
---
# <a name="threads-and-critical-sections"></a>Subprocesos y secciones críticas

En esta sección se describen los subprocesos de los filtros de DirectShow y los pasos que debe seguir para evitar bloqueos o interbloqueos en un filtro personalizado.

En los ejemplos de esta sección se usa pseudocódigo para ilustrar el código que se debe escribir. Suponen que un filtro personalizado usa clases derivadas de las clases base de DirectShow, como se indica a continuación:

-   CMyInputPin: se deriva de [**CBaseInputPin**](cbaseinputpin.md).
-   CMyOutputPin: se deriva de [**CBaseOutputPin**](cbaseoutputpin.md).
-   CMyFilter: se deriva de [**CBaseFilter**](cbasefilter.md).
-   CMyInputAllocator: asignador del PIN de entrada, derivado de [**CMemAllocator**](cmemallocator.md). No todos los filtros necesitan un asignador personalizado. Para muchos filtros, la clase **CMemAllocator** es suficiente.

Esta sección contiene los temas siguientes.

-   [Los subprocesos streaming y Application](the-streaming-and-application-threads.md)
-   [Pausando](pausing.md)
-   [Recibir y entregar ejemplos](receiving-and-delivering-samples.md)
-   [Entrega del final de la secuencia](delivering-the-end-of-stream.md)
-   [Vaciar datos](flushing-data.md)
-   [Stopping](stopping.md) (Deteniéndose)
-   [Obtener búferes](getting-buffers.md)
-   [Streaming de subprocesos y Filter Graph Manager](streaming-threads-and-the-filter-graph-manager.md)
-   [Resumen de subprocesos de filtro](summary-of-filter-threading.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Flujo de datos para desarrolladores de filtros](data-flow-for-filter-developers.md)
</dt> <dt>

[Escribir filtros de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



