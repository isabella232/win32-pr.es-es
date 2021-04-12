---
title: Inicio rápido administrada de TraceLogging
description: En la siguiente sección se describen los pasos básicos necesarios para agregar TraceLogging a código administrado.
ms.assetid: E144214D-8DCC-4263-8232-9F468C1A3CC0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7108dfc094f3183950dd94e5398263f4bf7cfd5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356997"
---
# <a name="tracelogging-managed-quick-start"></a><span data-ttu-id="87145-103">Inicio rápido administrada de TraceLogging</span><span class="sxs-lookup"><span data-stu-id="87145-103">TraceLogging Managed Quick Start</span></span>

<span data-ttu-id="87145-104">En la siguiente sección se describen los pasos básicos necesarios para agregar TraceLogging a código administrado.</span><span class="sxs-lookup"><span data-stu-id="87145-104">The following section describes the basic steps required to add TraceLogging to managed code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="87145-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="87145-105">Prerequisites</span></span>

-   <span data-ttu-id="87145-106">Windows 10</span><span class="sxs-lookup"><span data-stu-id="87145-106">Windows 10</span></span>

### <a name="simpletraceloggingexamplecs"></a><span data-ttu-id="87145-107">SimpleTraceLoggingExample. CS</span><span class="sxs-lookup"><span data-stu-id="87145-107">SimpleTraceLoggingExample.cs</span></span>

<span data-ttu-id="87145-108">En este ejemplo se muestra cómo registrar eventos Tracelogging sin necesidad de crear manualmente un archivo XML de manifiesto de instrumentación independiente.</span><span class="sxs-lookup"><span data-stu-id="87145-108">This example demonstrates how to log Tracelogging events without the need to manually create a separate instrumentation manifest XML file.</span></span>


```CSharp
using System;
using System.Diagnostics.Tracing;

namespace SimpleTraceLoggingExample
{
    class Program
    {
        private static EventSource log = new EventSource("SimpleTraceLoggingProvider");
        static void Main(string[] args)
        {
            log.Write("Event 1"); // write an event with no fields
            log.Write("Event 2", new { someEventData = DateTime.Now }); // Sending an anonymous type as event data

            ExampleStructuredData EventData = new ExampleStructuredData() { TransactionID = 1234, TransactionDate = DateTime.Now };
            log.Write("Event 3", EventData); // Sending a class decorated with [EventData] as event data
        }
    }

    [EventData] // [EventData] makes it possible to pass an instance of the class as an argument to EventSource.Write()
    public sealed class ExampleStructuredData
    {
        public int TransactionID { get; set; }
        public DateTime TransactionDate { get; set; }
    }
}
```



### <a name="create-the-eventsource"></a><span data-ttu-id="87145-109">Creación de EventSource</span><span class="sxs-lookup"><span data-stu-id="87145-109">Create the EventSource</span></span>

<span data-ttu-id="87145-110">Antes de poder registrar eventos, debe crear una instancia de la clase EventSource.</span><span class="sxs-lookup"><span data-stu-id="87145-110">Before you can log events you must create an instance of the EventSource class.</span></span> <span data-ttu-id="87145-111">El primer parámetro de constructor identifica el nombre de este proveedor.</span><span class="sxs-lookup"><span data-stu-id="87145-111">The first constructor parameter identifies the name of this provider.</span></span> <span data-ttu-id="87145-112">El proveedor se registra automáticamente como se muestra en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="87145-112">The provider is automatically registered for you as illustrated in the example.</span></span>


```CSharp
        private static EventSource log = new EventSource("SimpleTraceLoggingProvider");
```



<span data-ttu-id="87145-113">La instancia es estática porque solo debe haber una instancia de un proveedor específico en la aplicación a la vez.</span><span class="sxs-lookup"><span data-stu-id="87145-113">The instance is static because there should only be one instance of a specific provider in your application at a time.</span></span>

### <a name="log-tracelogging-events"></a><span data-ttu-id="87145-114">Registrar eventos de Tracelogging</span><span class="sxs-lookup"><span data-stu-id="87145-114">Log Tracelogging events</span></span>

<span data-ttu-id="87145-115">Una vez creado el proveedor, el siguiente código del ejemplo anterior registra un evento simple.</span><span class="sxs-lookup"><span data-stu-id="87145-115">After the provider is created, the following code from the example above logs a simple event.</span></span>


```CSharp
            log.Write("Event 1"); // write an event with no fields
```



### <a name="log-structured-event-payload-data"></a><span data-ttu-id="87145-116">Registrar datos de carga de eventos estructurados</span><span class="sxs-lookup"><span data-stu-id="87145-116">Log structured event payload data</span></span>

<span data-ttu-id="87145-117">Puede definir los datos de carga estructurada que se registran con el evento.</span><span class="sxs-lookup"><span data-stu-id="87145-117">You can define structured payload data that is logged with the event.</span></span> <span data-ttu-id="87145-118">Proporcione datos de carga estructurada como un tipo anónimo o como una instancia de una clase que se haya anotado con el `[EventData]` atributo, tal como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="87145-118">Provide structured payload data either as an anonymous type or as an instance of a class that has been annotated with the `[EventData]` attribute as shown in the following example.</span></span>


```CSharp
            log.Write("Event 2", new { someEventData = DateTime.Now }); // Sending an anonymous type as event data

            ExampleStructuredData EventData = new ExampleStructuredData() { TransactionID = 1234, TransactionDate = DateTime.Now };
            log.Write("Event 3", EventData); // Sending a class decorated with [EventData] as event data
```



<span data-ttu-id="87145-119">Debe agregar el `[EventData]` atributo a las clases de carga de evento que defina como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="87145-119">You must add the `[EventData]` attribute to event payload classes that you define as shown below.</span></span>


```CSharp
    [EventData] // [EventData] makes it possible to pass an instance of the class as an argument to EventSource.Write()
    public sealed class ExampleStructuredData
    {
        public int TransactionID { get; set; }
        public DateTime TransactionDate { get; set; }
    }
```



<span data-ttu-id="87145-120">El atributo reemplaza la necesidad de crear manualmente un archivo de manifiesto para describir los datos de evento.</span><span class="sxs-lookup"><span data-stu-id="87145-120">The attribute replaces the need to manually create a manifest file to describe the event data.</span></span> <span data-ttu-id="87145-121">Ahora todo lo que tiene que hacer es pasar una instancia de la clase al método EventSource. Write () para registrar el evento y los datos de carga correspondientes.</span><span class="sxs-lookup"><span data-stu-id="87145-121">Now all you have to do is pass an instance of the class to the EventSource.Write() method to log the event and corresponding payload data.</span></span>

## <a name="summary-and-next-steps"></a><span data-ttu-id="87145-122">Resumen y pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="87145-122">Summary and next steps</span></span>

<span data-ttu-id="87145-123">Consulte [registro y visualización de eventos TraceLogging](tracelogging-record-and-display-tracelogging-events.md) para obtener información sobre cómo capturar y ver datos de TraceLogging con las versiones internas más recientes de las herramientas de rendimiento de Windows (WPT).</span><span class="sxs-lookup"><span data-stu-id="87145-123">See [Record and Display TraceLogging Events](tracelogging-record-and-display-tracelogging-events.md) for information about how to capture and view TraceLogging data using the latest internal versions of the Windows Performance Tools (WPT).</span></span>

<span data-ttu-id="87145-124">Consulte [ejemplos de Tracelogging de .net](tracelogging-net-examples.md) para obtener más ejemplos de Tracelogging administrados.</span><span class="sxs-lookup"><span data-stu-id="87145-124">See [.NET Tracelogging Examples](tracelogging-net-examples.md) for more managed TraceLogging examples.</span></span>

 

 




