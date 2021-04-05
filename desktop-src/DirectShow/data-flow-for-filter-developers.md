---
description: Flujo de datos para desarrolladores de filtros
ms.assetid: cc7378c8-e268-4caa-98eb-6dc9c3b5bcad
title: Flujo de datos para desarrolladores de filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccb4e4123e8617190a459ff500d1100c0dbbb8ca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104080062"
---
# <a name="data-flow-for-filter-developers"></a>Flujo de datos para desarrolladores de filtros

En esta sección se describe en detalle cómo se mueven los datos a través del gráfico de filtro. Se centra en el transporte de memoria local mediante la interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) o [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) . Está dirigido a los desarrolladores que escriben sus propios filtros personalizados. Para obtener una introducción general al modo en que Microsoft DirectShow controla el flujo de datos, vea [flujo de datos en el gráfico de filtros](data-flow-in-the-filter-graph.md).

Muchos datos se desplazan a través de un gráfico de filtros. Se divide en dos categorías aproximadamente: datos multimedia y datos de control. En general, los datos multimedia viajan hacia abajo y los datos de control están ascendentes. Los datos multimedia incluyen fotogramas de vídeo, muestras de audio, paquetes MPEG, etc. que componen una secuencia, pero también incluyen comandos de vaciado, notificaciones de final de secuencia y otros datos que viajan con la secuencia. Los datos de control no forman parte de la secuencia de medios. Ejemplos de datos de control son las solicitudes de control de calidad y los comandos de búsqueda.

Esta sección contiene los siguientes artículos.

-   [Entrega de ejemplos](delivering-samples.md)
-   [Procesamiento de datos](processing-data.md)
-   [Notificaciones de final de secuencia](end-of-stream-notifications.md)
-   [Nuevos segmentos](new-segments.md)
-   [Vaciar](flushing.md)
-   [Invoca](seeking.md)
-   [Cambios en el formato dinámico](dynamic-format-changes.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de control de calidad](quality-control-management.md)
</dt> <dt>

[Subprocesos y secciones críticas](threads-and-critical-sections.md)
</dt> <dt>

[Escribir filtros de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



