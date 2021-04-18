---
title: Ejemplos de Tracelogging de .NET
description: En este tema se incluye un ejemplo de Tracelogging de código administrado que muestra cómo registrar un evento solo cuando el nivel de detalle de la sesión es detallado y cómo registrar datos de eventos estructurados.
ms.assetid: 156016FE-FDC7-4361-BFD0-5F41254FE14D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8064f2ce139b5fd07bc74b3de6e107abeb958530
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357663"
---
# <a name="net-tracelogging-examples"></a><span data-ttu-id="d0fa9-103">Ejemplos de Tracelogging de .NET</span><span class="sxs-lookup"><span data-stu-id="d0fa9-103">.NET Tracelogging Examples</span></span>

<span data-ttu-id="d0fa9-104">En este tema se incluye un ejemplo de Tracelogging de código administrado que muestra cómo registrar un evento solo cuando el nivel de detalle de la sesión es detallado y cómo registrar datos de eventos estructurados.</span><span class="sxs-lookup"><span data-stu-id="d0fa9-104">This topic contains a managed code Tracelogging example that illustrates how to log an event only when the session verbosity level is verbose, and how to log structured event data.</span></span>


```CSharp
using System;
using System.Text;
using System.Diagnostics.Tracing;

namespace MoreSimpleTraceLoggingExamples
{
    class Program
    {
        private static EventSource log = new EventSource("SimpleTraceLoggingProvider", EventSourceSettings.EtwSelfDescribingEventFormat);

        static void Main(string[] args)
        {
            StringBuilder cmdLine = new StringBuilder();
            foreach (string arg in args)
            {
                cmdLine.AppendFormat("{0} ", arg);
            }

            // Log event verbosity level and opcode
            // This event is only logged when the session verbosity level is verbose.
            log.Write("CmdLine", new EventSourceOptions {Level=EventLevel.Verbose, Opcode=EventOpcode.Info }, 
                                 new { Args = cmdLine.ToString().TrimEnd() });

            try
            {
                int j = 0;
                int i = 1 / j;
            }
            catch (Exception e)
            {
                var error = new Error { ErrorTitle = e.Message, CallStack = e.StackTrace, ErrType = ErrorType.Exception };
                log.Write("Error", new { Error = error, ErrorType = e.ToString() });
            }
        }
    }

    [EventData] // [EventData] makes it possible to pass an instance of the class as an argument to EventSource.Write()
    public class Error
    {
        public string ErrorTitle { get; set; }
        public string CallStack { get; set; }
        public ErrorType ErrType { get; set; }
    }

    public enum ErrorType
    {
        Exception,
        UserError,
        ProgramError
    }
}
```



 

 




