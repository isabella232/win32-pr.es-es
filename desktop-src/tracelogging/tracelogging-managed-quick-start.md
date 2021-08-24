---
title: Seguimiento de registros administrados Inicio rápido
description: En la sección siguiente se describen los pasos básicos necesarios para agregar TraceLogging al código administrado.
ms.assetid: E144214D-8DCC-4263-8232-9F468C1A3CC0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: be29e4a1bd6721b8f53dbe2394be3552ca4845143cf948f130ef55e11881b518
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589245"
---
# <a name="tracelogging-managed-quick-start"></a>Seguimiento de registros administrados Inicio rápido

En la sección siguiente se describen los pasos básicos necesarios para agregar TraceLogging al código administrado.

## <a name="prerequisites"></a>Prerrequisitos

-   Windows 10

### <a name="simpletraceloggingexamplecs"></a>SimpleTraceLoggingExample.cs

En este ejemplo se muestra cómo registrar eventos de seguimiento sin necesidad de crear manualmente un archivo XML de manifiesto de instrumentación independiente.


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



### <a name="create-the-eventsource"></a>Creación de EventSource

Para poder registrar eventos, debe crear una instancia de la clase EventSource. El primer parámetro de constructor identifica el nombre de este proveedor. El proveedor se registra automáticamente, como se muestra en el ejemplo.


```CSharp
        private static EventSource log = new EventSource("SimpleTraceLoggingProvider");
```



La instancia es estática porque solo debe haber una instancia de un proveedor específico en la aplicación a la vez.

### <a name="log-tracelogging-events"></a>Registrar eventos de registro de seguimiento

Una vez creado el proveedor, el código siguiente del ejemplo anterior registra un evento simple.


```CSharp
            log.Write("Event 1"); // write an event with no fields
```



### <a name="log-structured-event-payload-data"></a>Registrar datos de carga de eventos estructurados

Puede definir datos de carga estructurados que se registran con el evento . Proporcione datos de carga estructurados como un tipo anónimo o como una instancia de una clase que se ha anotado con el atributo como se muestra `[EventData]` en el ejemplo siguiente.


```CSharp
            log.Write("Event 2", new { someEventData = DateTime.Now }); // Sending an anonymous type as event data

            ExampleStructuredData EventData = new ExampleStructuredData() { TransactionID = 1234, TransactionDate = DateTime.Now };
            log.Write("Event 3", EventData); // Sending a class decorated with [EventData] as event data
```



Debe agregar el atributo a `[EventData]` las clases de carga de eventos que defina como se muestra a continuación.


```CSharp
    [EventData] // [EventData] makes it possible to pass an instance of the class as an argument to EventSource.Write()
    public sealed class ExampleStructuredData
    {
        public int TransactionID { get; set; }
        public DateTime TransactionDate { get; set; }
    }
```



El atributo reemplaza la necesidad de crear manualmente un archivo de manifiesto para describir los datos del evento. Ahora todo lo que tiene que hacer es pasar una instancia de la clase al método EventSource.Write() para registrar el evento y los datos de carga correspondientes.

## <a name="summary-and-next-steps"></a>Resumen y pasos siguientes

Vea [Registrar y mostrar eventos de](tracelogging-record-and-display-tracelogging-events.md) seguimiento para obtener información sobre cómo capturar y ver los datos de TraceLogging mediante las versiones internas más recientes de Windows Performance Tools (WPT).

Consulte [Ejemplos de registro de seguimiento de .NET](tracelogging-net-examples.md) para obtener más ejemplos administrados de TraceLogging.

 

 




