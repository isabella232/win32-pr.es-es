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
# <a name="event-tracing-reference"></a><span data-ttu-id="c5df9-103">Referencia de seguimiento de eventos</span><span class="sxs-lookup"><span data-stu-id="c5df9-103">Event Tracing Reference</span></span>

<span data-ttu-id="c5df9-104">Los siguientes elementos de programación se usan para escribir aplicaciones que incorporan seguimiento de eventos:</span><span class="sxs-lookup"><span data-stu-id="c5df9-104">You use the following programming elements to write applications that incorporate event tracing:</span></span>

-   [<span data-ttu-id="c5df9-105">Enumeraciones de seguimiento de eventos</span><span class="sxs-lookup"><span data-stu-id="c5df9-105">Event Tracing Enumerations</span></span>](/windows/desktop/api/_etw/#enumerations)
-   [<span data-ttu-id="c5df9-106">Funciones de seguimiento de eventos</span><span class="sxs-lookup"><span data-stu-id="c5df9-106">Event Tracing Functions</span></span>](/windows/desktop/api/_etw/#functions)
-   [<span data-ttu-id="c5df9-107">Interfaces de seguimiento de eventos</span><span class="sxs-lookup"><span data-stu-id="c5df9-107">Event Tracing Interfaces</span></span>](/windows/desktop/api/_etw/#interfaces)
-   [<span data-ttu-id="c5df9-108">Estructuras de seguimiento de eventos</span><span class="sxs-lookup"><span data-stu-id="c5df9-108">Event Tracing Structures</span></span>](/windows/desktop/api/_etw/#structures)
-   [<span data-ttu-id="c5df9-109">Constantes de seguimiento de eventos</span><span class="sxs-lookup"><span data-stu-id="c5df9-109">Event Tracing Constants</span></span>](event-tracing-constants.md)

<span data-ttu-id="c5df9-110">Para obtener más información sobre los ejemplos que usan estos elementos de programación, vea [ejemplos de seguimiento de eventos](event-tracing-samples.md).</span><span class="sxs-lookup"><span data-stu-id="c5df9-110">For details on samples that use these programming elements, see [Event Tracing Samples](event-tracing-samples.md).</span></span>

<span data-ttu-id="c5df9-111">Esta sección también contiene información sobre:</span><span class="sxs-lookup"><span data-stu-id="c5df9-111">This section also contains information on:</span></span>

-   <span data-ttu-id="c5df9-112">[Herramientas](event-tracing-tools.md) que proporciona ETW</span><span class="sxs-lookup"><span data-stu-id="c5df9-112">[Tools](event-tracing-tools.md) that ETW provides</span></span>
-   <span data-ttu-id="c5df9-113">[Definiciones de clases MOF](event-tracing-mof-classes.md) para eventos de kernel</span><span class="sxs-lookup"><span data-stu-id="c5df9-113">[MOF class definitions](event-tracing-mof-classes.md) for kernel events</span></span>
-   <span data-ttu-id="c5df9-114">[Calificadores de clase MOF](event-tracing-mof-qualifiers.md) usados al definir las clases de eventos</span><span class="sxs-lookup"><span data-stu-id="c5df9-114">[MOF class qualifiers](event-tracing-mof-qualifiers.md) used when defining your event classes</span></span>

## <a name="process-etw-traces-in-net-code"></a><span data-ttu-id="c5df9-115">Procesar seguimientos de ETW en código .NET</span><span class="sxs-lookup"><span data-stu-id="c5df9-115">Process ETW traces in .NET code</span></span>

<span data-ttu-id="c5df9-116">También puede usar la [API TraceProcessing de .net](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) para analizar seguimientos de ETW para las aplicaciones y otros componentes de software.</span><span class="sxs-lookup"><span data-stu-id="c5df9-116">You can also use the [.NET TraceProcessing API](https://www.nuget.org/packages/Microsoft.Windows.EventTracing.Processing.All) to analyze ETW traces for your applications and other software components.</span></span> <span data-ttu-id="c5df9-117">Esta API se usa internamente en Microsoft para analizar los datos de ETW generados por Windows Engineering System y también se usa para potenciar varias tablas en el [analizador de rendimiento de Windows](/windows-hardware/test/wpt/windows-performance-analyzer).</span><span class="sxs-lookup"><span data-stu-id="c5df9-117">This API is used internally at Microsoft to analyze ETW data produced the Windows engineering system, and it is also used to power several tables in [Windows Performance Analyzer](/windows-hardware/test/wpt/windows-performance-analyzer).</span></span> <span data-ttu-id="c5df9-118">Esta API está disponible como un paquete NuGet.</span><span class="sxs-lookup"><span data-stu-id="c5df9-118">This API is available as a NuGet package.</span></span>

<span data-ttu-id="c5df9-119">Para obtener más información, consulte [este artículo](/windows/apps/trace-processing/overview).</span><span class="sxs-lookup"><span data-stu-id="c5df9-119">For more information, see [this article](/windows/apps/trace-processing/overview).</span></span>
