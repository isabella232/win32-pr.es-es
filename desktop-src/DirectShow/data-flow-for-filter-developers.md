---
description: Datos Flow para desarrolladores de filtros
ms.assetid: cc7378c8-e268-4caa-98eb-6dc9c3b5bcad
title: Datos Flow para desarrolladores de filtros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77ced9507856d7a6b8aea2acaea86c20b393b8d937ab4427bf522596a29ba690
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749375"
---
# <a name="data-flow-for-filter-developers"></a>Datos Flow para desarrolladores de filtros

En esta sección se describe en detalle cómo se mueven los datos a través del gráfico de filtros. Se centra en el transporte de memoria local mediante la [**interfaz IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**o IAsyncReader.**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) Está destinado a desarrolladores que escriben sus propios filtros personalizados. Para obtener una introducción general sobre cómo Microsoft DirectShow controla el flujo de datos, vea [Data Flow en el](data-flow-in-the-filter-graph.md)cuadro Graph .

Muchos datos se mueven a través de un gráfico de filtros. Se divide aproximadamente en dos categorías: datos multimedia y datos de control. En general, los datos multimedia viajan de bajada y los datos de control se desplazan en sentido ascendente. Los datos multimedia incluyen fotogramas de vídeo, ejemplos de audio, paquetes MPEG, etc., que son una secuencia, pero también incluyen comandos de vaciado, notificaciones de fin de secuencia y otros datos que viajan con la secuencia. Los datos de control no forman parte del flujo multimedia. Algunos ejemplos de datos de control son las solicitudes de control de calidad y los comandos de búsqueda.

Esta sección contiene los artículos siguientes.

-   [Entrega de ejemplos](delivering-samples.md)
-   [Procesamiento de datos](processing-data.md)
-   [Notificaciones de fin de flujo](end-of-stream-notifications.md)
-   [Nuevos segmentos](new-segments.md)
-   [Lavado](flushing.md)
-   [Buscando](seeking.md)
-   [Cambios de formato dinámico](dynamic-format-changes.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de control de calidad](quality-control-management.md)
</dt> <dt>

[Subprocesos y secciones críticas](threads-and-critical-sections.md)
</dt> <dt>

[Escribir DirectShow filtros](writing-directshow-filters.md)
</dt> </dl>

 

 



