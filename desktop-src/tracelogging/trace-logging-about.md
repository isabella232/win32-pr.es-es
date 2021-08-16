---
title: Acerca de TraceLogging
description: TraceLogging es la nueva Windows 10 seguimiento de eventos para aplicaciones en modo de usuario y controladores en modo kernel.
ms.assetid: 8C6A9E91-98F9-4D6B-A937-A22BA7CEB1E4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16cc38210bf4c3ed1ed0b1ebf56ca22a0597b9288fc30ae4c0231d5317465644
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218396"
---
# <a name="about-tracelogging"></a>Acerca de TraceLogging

TraceLogging es la nueva Windows 10 seguimiento de eventos para aplicaciones en modo de usuario y controladores en modo kernel. TraceLogging es un formato para el seguimiento de eventos autodescripto para Windows (ETW). TraceLogging se basa en el seguimiento de eventos Windows (ETW) y proporciona una manera simplificada de instrumentar el código.

TraceLogging ofrece la simplicidad del preprocesador de seguimiento de software (WPP) de Windows con la ventaja adicional de poder incluir datos estructurados con eventos, la capacidad de correlacionar eventos y todo ello sin necesidad de un archivo XML de manifiesto de instrumentación independiente. Los eventos son autodescriptos, lo que significa que no es necesario registrar un archivo binario que contenga el manifiesto de instrumentación en el sistema para usar las API del asistente de datos de seguimiento (TDH) para descodificar y mostrar eventos.

Seguimiento de eventos para Windows (ETW) se introdujo con Windows 2000 y se actualizó en Windows Vista. El registro de seguimiento se basa en Windows API ETW de Vista. Los proveedores pueden usar la tecnología TraceLogging y seguir trabajando en Windows Vista. Los controladores existentes (Windows VistaAPIs) se pueden usar para controlar los proveedores de TraceLogging.

TraceLogging también es compatible con las herramientas existentes. Todavía se admiten los proveedores que usan ETW basado en manifiestos. No es necesario convertir proveedores ETW basados en manifiestos en proveedores de seguimiento a menos que desee aprovechar la simplicidad que proporciona TraceLogging. También se admite el seguimiento de WPP.

TraceLogging se basa en ETW, pero presenta varias mejoras importantes:

-   El seguimiento de un evento es tan sencillo como una llamada API.
-   Los eventos son autodescriptos y no requieren archivos binarios adicionales que contengan el manifiesto de evento compilado para interpretar el evento. Todos los metadatos sobre el evento se registran en el evento.
-   Las actividades dentro de un único proceso se pueden expresar fácilmente a través de eventos de inicio y de detenerse.
-   TraceLogging es compatible con la compatibilidad de instrumentación existente. Las nuevas API de ETW siguen siendo compatibles con los proveedores antiguos. Puede invertir en las nuevas API de ETW para escenarios estratégicos y dejar los puntos de instrumentación antiguos tal como están.
-   TraceLogging ofrece la misma API de seguimiento de eventos para Windows 10, Xbox One y Windows 10 Mobile.
-   Las API de seguimiento son accesibles desde C, C++, .NET y Windows runtime.

## <a name="api-high-level-overview"></a>Introducción a la API de alto nivel

Hay tres API de seguimiento independientes destinadas a diferentes audiencias de desarrolladores. Cada API se diseñó para cumplir distintos conjuntos de requisitos según corresponda para la audiencia de destino de esa API.

Para desarrolladores de WinRT:

-   [**LoggingChannel**](/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel) se ha ampliado en Windows 10 para registrar el seguimiento de eventos autodescripto para eventos de Windows (ETW) sin necesidad de un manifiesto.
-   [**LoggingActivity se**](/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity) ha ampliado en Windows 10 para proporcionar métodos de inicio y de detección de actividad que proporcionan control sobre el formato y el contenido de los eventos Start y Stop. Además, las actividades se pueden anidar.

Para desarrolladores de C/C++:

-   TraceLoggingProvider.h contiene la API más eficaz, pero esta API no es adecuada para su uso en escenarios dinámicos (con script), como Javascript. Esta API se puede usar en el modo de usuario y el código en modo kernel.

Para desarrolladores de código administrado (Microsoft .NET Framework):

-   La [clase EventSource](/dotnet/api/system.diagnostics.tracing.eventsource) que se suministraba con versiones anteriores de .NET Framework ya era compatible con la escritura de eventos ETW: generaba automáticamente el manifiesto e insertaba el manifiesto en el flujo de eventos. Sin embargo, el desarrollador todavía tenía que realizar un seguimiento del manifiesto para descodificar los eventos (a menos que trabajara en un escenario en el que se admite el manifiesto incrustado). TraceLogging permite eliminar completamente el manifiesto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca del seguimiento de eventos](/windows/desktop/ETW/about-event-tracing)
</dt> </dl>

 

 