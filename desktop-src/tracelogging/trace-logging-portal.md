---
title: TraceLogging
description: TraceLogging
ms.assetid: c516424a-9eba-4b56-80de-8c713fd3461a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7bd83c608d2ac98fdccce760c851496af80c217
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116723"
---
# <a name="tracelogging"></a>TraceLogging

## <a name="purpose"></a>Propósito

TraceLogging es la nueva plataforma Windows 10 seguimiento de eventos para aplicaciones en modo de usuario y controladores en modo kernel. TraceLogging se basa en Seguimiento de eventos para Windows (ETW) y proporciona una manera simplificada de instrumentar el código.

## <a name="in-this-section"></a>En esta sección



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tema</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="trace-logging-about.md">Acerca de TraceLogging</a><br/></td>
<td>TraceLogging es la nueva Windows 10 seguimiento de eventos para aplicaciones en modo de usuario y controladores en modo kernel. TraceLogging es un formato para la descripción Seguimiento de eventos para Windows (ETW). TraceLogging se basa en Seguimiento de eventos para Windows (ETW) y proporciona una manera simplificada de instrumentar el código.<br/></td>
</tr>
<tr class="even">
<td><a href="tracelogging-using-tracelogging.md">Uso de TraceLogging</a><br/></td>
<td>En los temas siguientes se proporciona un inicio rápido de TraceLogging para código nativo y administrado, con ejemplos.<br/></td>
</tr>
<tr class="odd">
<td><a href="trace-logging-reference.md">Referencia de registro de seguimiento</a><br/></td>
<td>En los temas siguientes se proporciona información sobre tracelogging API nativa.<br/> TraceLogging se basa en Seguimiento de eventos para Windows (ETW) y proporciona una manera simplificada de instrumentar el código. TraceLogging permite incluir datos estructurados con eventos, correlacionar eventos y no requiere un archivo XML de manifiesto de instrumentación independiente.<br/> <span class="underline">Para desarrolladores de WinRT</span><br/>
<ul>
<li><a href="/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel"><strong>LoggingChannel</strong></a> se ha ampliado en Windows 10 para registrar eventos de Seguimiento de eventos para Windows autodescriptos (ETW) sin necesidad de un manifiesto.</li>
<li><a href="/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity"><strong>LoggingActivity se</strong></a> ha ampliado en Windows 10 para proporcionar métodos de inicio y de detección de actividad que proporcionan control sobre el formato y el contenido de los eventos Start y Stop. Además, las actividades se pueden anidar.</li>
</ul>
<span class="underline">Para desarrolladores de código administrado (Microsoft .NET Framework)</span><br/>
<ul>
<li>La <a href="/dotnet/api/system.diagnostics.tracing.eventsource">clase EventSource</a> que se suministraba con versiones anteriores del .NET Framework ya admite la escritura de eventos ETW sin necesidad de un manifiesto. Sin embargo, los desarrolladores tenían que usar EventSource como una clase base y agregar atributos y métodos a la clase derivada que se convertían en un manifiesto ETW automáticamente. Ahora, los desarrolladores no tienen que derivar de EventSource y, en su lugar, pueden usar EventSource directamente para registrar eventos autodescriptos que no requieren un manifiesto.</li>
</ul>
<span class="underline">Para desarrolladores de C/C++</span><br/>
<ul>
<li>TraceLoggingProvider.h es la API recomendada para desarrolladores de C/C++ en modo de usuario o kernel. Esta API no es adecuada para su uso en escenarios dinámicos (con script), como Javascript. Los vínculos siguientes describen la API de C/C++.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="developer-audience"></a>Audiencia de desarrolladores

TraceLogging está diseñado para su uso por parte de desarrolladores de aplicaciones en modo de usuario y desarrolladores de controladores en modo kernel que desean agregar seguimiento a su código.

