---
description: Enumera los elementos utilizados con el seguimiento de eventos.
ms.assetid: 8cb5907e-9006-45d1-9d48-13a43a631664
title: Referencia de seguimiento de eventos
ms.topic: article
ms.date: 01/30/2020
ms.openlocfilehash: 7e0ee4576b9b9d64a5766c6ab096ea34abc2b176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985947"
---
# <a name="event-tracing-reference"></a>Referencia de seguimiento de eventos

Los siguientes elementos de programación se usan para escribir aplicaciones que incorporan seguimiento de eventos:

-   [Enumeraciones de seguimiento de eventos](/windows/desktop/api/_etw/#enumerations)
-   [Funciones de seguimiento de eventos](/windows/desktop/api/_etw/#functions)
-   [Interfaces de seguimiento de eventos](/windows/desktop/api/_etw/#interfaces)
-   [Estructuras de seguimiento de eventos](/windows/desktop/api/_etw/#structures)
-   [Constantes de seguimiento de eventos](event-tracing-constants.md)

Para obtener más información sobre los ejemplos que usan estos elementos de programación, vea [ejemplos de seguimiento de eventos](event-tracing-samples.md).

Esta sección también contiene información sobre:

-   [Herramientas](event-tracing-tools.md) que proporciona ETW
-   [Definiciones de clases MOF](event-tracing-mof-classes.md) para eventos de kernel
-   [Calificadores de clase MOF](event-tracing-mof-qualifiers.md) usados al definir las clases de eventos

## <a name="process-etw-traces-in-net-code"></a>Procesar seguimientos de ETW en código .NET

También puede usar la [API TraceProcessing de .net](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) para analizar seguimientos de ETW para las aplicaciones y otros componentes de software. Esta API se usa internamente en Microsoft para analizar los datos de ETW generados por Windows Engineering System y también se usa para potenciar varias tablas en el [analizador de rendimiento de Windows](/windows-hardware/test/wpt/windows-performance-analyzer). Esta API está disponible como un paquete NuGet.

Para obtener más información, consulte [este artículo](/windows/apps/trace-processing/overview).
