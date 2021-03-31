---
title: Acerca de TraceLogging
description: TraceLogging es el nuevo seguimiento de eventos de Windows 10 para aplicaciones en modo de usuario y controladores de modo kernel.
ms.assetid: 8C6A9E91-98F9-4D6B-A937-A22BA7CEB1E4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c2b1ca72385a51df1e0cd82f3e91c198f15b5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904664"
---
# <a name="about-tracelogging"></a>Acerca de TraceLogging

TraceLogging es el nuevo seguimiento de eventos de Windows 10 para aplicaciones en modo de usuario y controladores de modo kernel. TraceLogging es un formato para el seguimiento de eventos autodescriptivo para Windows (ETW). TraceLogging se basa en el seguimiento de eventos para Windows (ETW) y proporciona una manera simplificada de instrumentar el código.

TraceLogging ofrece la simplicidad del preprocesador de seguimiento de software (WPP) de Windows con la ventaja adicional de poder incluir datos estructurados con eventos, la capacidad de correlacionar eventos y todo sin requerir un archivo XML de manifiesto de instrumentación independiente. Los eventos son autodescriptivos, lo que significa que no es necesario registrar un archivo binario que contenga el manifiesto de instrumentación en el sistema para poder usar las API de la aplicación auxiliar de datos de seguimiento (TDH) para descodificar y Mostrar eventos.

Seguimiento de eventos para Windows (ETW) se incorporó con Windows 2000 y se actualizó en Windows Vista. Tracelogging se basa en las API ETW de Windows Vista. Los proveedores pueden usar la tecnología TraceLogging y seguir trabajando en Windows Vista. Los controladores existentes (con Windows VistaAPIs) se pueden usar para controlar los proveedores de TraceLogging.

TraceLogging también es compatible con las herramientas existentes. Todavía se admiten los proveedores que usan ETW basados en manifiesto. No es necesario convertir proveedores ETW basados en manifiestos en proveedores de TraceLogging a menos que desee aprovechar la simplicidad que proporciona TraceLogging. También se admite el seguimiento de WPP.

TraceLogging se basa en ETW, pero presenta varias mejoras importantes:

-   El seguimiento de un evento es tan sencillo como una llamada API.
-   Los eventos son autodescriptivos y no requieren archivos binarios adicionales que contengan el manifiesto de eventos compilados para interpretar el evento. Todos los metadatos sobre el evento se registran en el evento.
-   Las actividades dentro de un único proceso pueden expresarse fácilmente a través de eventos de inicio y detención.
-   TraceLogging es compatible con la compatibilidad de instrumentación existente. Las nuevas API de ETW continúan siendo compatibles con los proveedores anteriores. Puede invertir en las nuevas API de ETW para escenarios estratégicos y, al mismo tiempo, mantener los puntos de instrumentación antiguos tal como están.
-   TraceLogging ofrece la misma API de seguimiento de eventos para Windows 10, Xbox One y Windows 10 Mobile.
-   Se puede acceder a las API de TraceLogging desde C, C++, .NET y Windows Runtime.

## <a name="api-high-level-overview"></a>Información general de alto nivel de API

Hay tres API de TraceLogging independientes que tienen como destino diferentes audiencias de desarrollador. Cada API se diseñó para satisfacer diferentes conjuntos de requisitos, según corresponda para la audiencia de destino de esa API.

Para desarrolladores de WinRT:

-   [**LoggingChannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) se ha ampliado en Windows 10 para que registre los eventos de seguimiento de eventos para Windows (ETW) autodescriptivos sin necesidad de un manifiesto.
-   [**LoggingActivity**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) se ha ampliado en Windows 10 para proporcionar métodos de inicio y detención de actividad que proporcionan control sobre el formato y el contenido de los eventos de inicio y detención. Además, las actividades se pueden anidar.

Para desarrolladores de C/C++:

-   TraceLoggingProvider. h contiene la API más eficaz, sin embargo, esta API no es adecuada para su uso en escenarios dinámicos (con scripts) como JavaScript. Esta API se puede usar en el modo de usuario y en el código en modo kernel.

Para desarrolladores de código administrado (Microsoft .NET Framework):

-   La clase [EventSource](/dotnet/api/system.diagnostics.tracing.eventsource) incluida con versiones anteriores de la .NET Framework ya admitía la escritura de eventos ETW: genera automáticamente el manifiesto e incrusta el manifiesto en el flujo de eventos. Sin embargo, el desarrollador todavía tenía que realizar un seguimiento del manifiesto para descodificar los eventos (a menos que se trabaje en un escenario donde se admitía el manifiesto incrustado). TraceLogging permite que el manifiesto se elimine por completo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca del seguimiento de eventos](/windows/desktop/ETW/about-event-tracing)
</dt> </dl>

 

 