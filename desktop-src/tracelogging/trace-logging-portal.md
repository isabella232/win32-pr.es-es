---
title: TraceLogging
description: .
ms.assetid: c516424a-9eba-4b56-80de-8c713fd3461a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975c2f70cc645cc04d6b1461e32bb3b899097d1c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "103796384"
---
# <a name="tracelogging"></a>TraceLogging

## <a name="purpose"></a>Propósito

TraceLogging es el nuevo marco de seguimiento de eventos de Windows 10 para aplicaciones en modo de usuario y controladores de modo kernel. TraceLogging se basa en el seguimiento de eventos para Windows (ETW) y proporciona una manera simplificada de instrumentar el código.

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
<td>TraceLogging es el nuevo seguimiento de eventos de Windows 10 para aplicaciones en modo de usuario y controladores de modo kernel. TraceLogging es un formato para el seguimiento de eventos autodescriptivo para Windows (ETW). TraceLogging se basa en el seguimiento de eventos para Windows (ETW) y proporciona una manera simplificada de instrumentar el código.<br/></td>
</tr>
<tr class="even">
<td><a href="tracelogging-using-tracelogging.md">Usar TraceLogging</a><br/></td>
<td>En los temas siguientes se proporciona una guía de inicio rápido de TraceLogging para código nativo y administrado, con ejemplos.<br/></td>
</tr>
<tr class="odd">
<td><a href="trace-logging-reference.md">Referencia de TraceLogging</a><br/></td>
<td>En los temas siguientes se proporciona información sobre la API de TraceLogging nativa.<br/> TraceLogging se basa en el seguimiento de eventos para Windows (ETW) y proporciona una manera simplificada de instrumentar el código. TraceLogging permite incluir datos estructurados con eventos, correlacionar eventos y no requiere un archivo XML de manifiesto de instrumentación independiente.<br/> <span class="underline">Para desarrolladores de WinRT</span><br/>
<ul>
<li><a href="/uwp/api/Windows.Foundation.Diagnostics.LoggingChannel"><strong>LoggingChannel</strong></a> se ha ampliado en Windows 10 para que registre los eventos de seguimiento de eventos para Windows (ETW) autodescriptivos sin necesidad de un manifiesto.</li>
<li><a href="/windows/win32/api/traceloggingactivity/nl-traceloggingactivity-traceloggingactivity"><strong>LoggingActivity</strong></a> se ha ampliado en Windows 10 para proporcionar métodos de inicio y detención de actividad que proporcionan control sobre el formato y el contenido de los eventos de inicio y detención. Además, las actividades se pueden anidar.</li>
</ul>
<span class="underline">Para desarrolladores de código administrado (Microsoft .NET Framework)</span><br/>
<ul>
<li>La clase <a href="/dotnet/api/system.diagnostics.tracing.eventsource">EventSource</a> incluida con versiones anteriores de la .NET Framework ya admite la escritura de eventos ETW sin necesidad de un manifiesto. Sin embargo, los desarrolladores debían usar EventSource como clase base y agregar atributos y métodos a la clase derivada que se han convertido en un manifiesto ETW automáticamente. Ahora, los desarrolladores no tienen que derivar de EventSource y, en su lugar, pueden usar EventSource directamente para registrar eventos autodescriptivos que no requieren un manifiesto.</li>
</ul>
<span class="underline">Para desarrolladores de C/C++</span><br/>
<ul>
<li>TraceLoggingProvider. h es la API recomendada para desarrolladores de C/C++ en modo de usuario o kernel. Esta API no es muy adecuada para su uso en escenarios dinámicos (con scripts) como JavaScript. En los vínculos siguientes se describe la API de C/C++.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="developer-audience"></a>Audiencia de desarrolladores

TraceLogging está diseñado para que lo usen los desarrolladores de aplicaciones en modo de usuario y los desarrolladores de controladores en modo kernel que deseen agregar seguimiento a su código.

