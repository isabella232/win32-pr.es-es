---
description: Enumera los elementos utilizados con el seguimiento de eventos.
ms.assetid: 8cb5907e-9006-45d1-9d48-13a43a631664
title: Referencia de seguimiento de eventos
ms.topic: article
ms.date: 01/30/2020
ms.openlocfilehash: 20aaf59de3419b4015f03b38db69839b6f258ccd561b1e918694396e875ae5a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083285"
---
# <a name="event-tracing-reference"></a>Referencia de seguimiento de eventos

Use los siguientes elementos de programación para escribir aplicaciones que incorporen el seguimiento de eventos:

-   [Enumeraciones de seguimiento de eventos](/windows/desktop/api/_etw/#enumerations)
-   [Funciones de seguimiento de eventos](/windows/desktop/api/_etw/#functions)
-   [Interfaces de seguimiento de eventos](/windows/desktop/api/_etw/#interfaces)
-   [Estructuras de seguimiento de eventos](/windows/desktop/api/_etw/#structures)
-   [Constantes de seguimiento de eventos](event-tracing-constants.md)

Para obtener más información sobre los ejemplos que usan estos elementos de programación, vea [Ejemplos de seguimiento de eventos](event-tracing-samples.md).

Esta sección también contiene información sobre:

-   [Herramientas](event-tracing-tools.md) que proporciona ETW
-   [Definiciones de clase MOF para](event-tracing-mof-classes.md) eventos de kernel
-   [Calificadores de clase MOF usados](event-tracing-mof-qualifiers.md) al definir las clases de eventos

## <a name="process-etw-traces-in-net-code"></a>Procesar seguimientos ETW en código .NET

También puede usar la [API TraceProcessing de .NET](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) para analizar los seguimientos ETW de las aplicaciones y otros componentes de software. Esta API se usa internamente en Microsoft para analizar los datos ETW generados por el sistema de ingeniería Windows y también se usa para crear varias tablas [en Windows Analizador de rendimiento](/windows-hardware/test/wpt/windows-performance-analyzer). Esta API está disponible como un paquete NuGet aplicación.

Para obtener más información, consulta [este artículo](/windows/apps/trace-processing/overview).
