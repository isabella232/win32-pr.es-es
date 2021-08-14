---
title: Escuchar eventos de la cinta de opciones
description: El marco Windows cinta de opciones de Windows usa la infraestructura de seguimiento de eventos para Windows (ETW) para permitir que los desarrolladores aprendan cómo interactúan los usuarios con la cinta de opciones de su aplicación.
ms.assetid: F29A8E41-C902-410E-BD28-653E078320E9
keywords:
- Windows Cinta de opciones, eventos
- Cinta de opciones, eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9519553a40cd613085949d4650c2689e817f387e47e9ab4380b629464e90d2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118202975"
---
# <a name="listening-for-ribbon-events"></a>Escuchar eventos de la cinta de opciones

El marco Windows Ribbon usa la infraestructura de seguimiento de eventos para [Windows (ETW)](../etw/event-tracing-portal.md) para permitir que los desarrolladores aprendan cómo interactúan los usuarios con la cinta de opciones de su aplicación.

## <a name="introduction"></a>Introducción

El mecanismo de eventos del marco de la cinta de opciones está diseñado de forma que el marco informa de eventos de la interfaz de usuario de la cinta de opciones a la aplicación para que pueda supervisar la actividad del usuario, conocer sus patrones de interacción y evaluar las tendencias de uso. Esta información se puede usar para refinar la experiencia del usuario para futuras iteraciones de la aplicación de cinta de opciones.

El uso de los eventos del marco de la cinta implica lo siguiente:

1.  La aplicación de cinta de opciones debe registrar un agente de escucha de Seguimiento de eventos [Windows (ETW)](../etw/event-tracing-portal.md) para recibir notificaciones de eventos de la cinta de opciones desde el marco de la cinta de opciones.
2.  El marco de la cinta de opciones activa devoluciones de llamada de eventos de la interfaz de usuario de la cinta en tiempo de ejecución, si la aplicación ha registrado un agente de escucha de seguimiento de eventos Windows [(ETW).](../etw/event-tracing-portal.md)

## <a name="supported-events"></a>Eventos admitidos

Los eventos expuestos a las aplicaciones de cinta de opciones se describen en la tabla siguiente. 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Evento</th>
<th>Informe de eventos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Pestaña activada</td>
<td>Identificador de comando<br/> Nombre de comando<br/> Verbo de evento<br/></td>
</tr>
<tr class="even">
<td>Pestaña contextual activada</td>
<td>Identificador de comando<br/> Nombre de comando<br/> Verbo de evento<br/></td>
</tr>
<tr class="odd">
<td>Menú de la aplicación abierto</td>
<td>Verbo de evento<br/></td>
</tr>
<tr class="even">
<td>Menú de la aplicación cerrado</td>
<td>Verbo de evento<br/></td>
</tr>
<tr class="odd">
<td>Menú (normal o galería) abierto</td>
<td>Identificador de comando<br/> Nombre de comando<br/> Verbo de evento<br/>
<blockquote>
[!Note]<br />
Los eventos de menú QAT no se exponen.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Menú (normal o galería) cerrado</td>
<td>Identificador de comando<br/> Nombre de comando<br/> Verbo de evento<br/>
<blockquote>
[!Note]<br />
Los eventos de menú QAT no se exponen.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Get-Help</td>
<td>Identificador de comando<br/> Nombre de comando<br/> Verbo de evento<br/> Una de las siguientes ubicaciones de eventos:
<ul>
<li>Cinta</li>
<li>QUICKACCESSTOOLBAR</li>
<li>APPLICATIONMENU</li>
<li>CONTEXTPOPUP</li>
</ul>
<br/> Identificador de comando primario<br/> Nombre del comando primario<br/> Uno de los métodos de invocación siguientes:
<ul>
<li>Haga clic</li>
<li>KEYTIP</li>
<li>Teclado</li>
<li>Tocar</li>
</ul>
<br/>
<blockquote>
[!Note]<br />
Las galerías de elementos y los cuadros combinados incluyen el índice de elemento seleccionado, pero no incluyen valores de cadena ni enteros. Los spinners no incluyen el valor entero.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Cinta minimizada</td>
<td>Verbo de evento<br/></td>
</tr>
<tr class="odd">
<td>Cinta expandida (botón Expandir clic o pulsar anclado)</td>
<td>Verbo de evento<br/></td>
</tr>
<tr class="even">
<td>Modo de aplicación cambiado</td>
<td>Verbo de evento<br/> Id. de modo (valor establecido a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes"><strong>través de SetModes)</strong></a><br/>
<blockquote>
[!Note]<br />
La aplicación es responsable de desempaquetar este entero para determinar qué modos se han establecido.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Información sobre herramientas mostrada</td>
<td>Verbo de evento<br/> Identificador de comando primario<br/> Nombre del comando primario<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Guías para desarrolladores de Ribbon Framework](windowsribbon-guides-entry.md)
</dt> <dt>

[Declarar comandos y controles con marcado de cinta](./windowsribbon-schema.md)
</dt> <dt>

[Directrices de la experiencia del usuario de la cinta de opciones](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Proceso de diseño de la cinta de opciones](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

