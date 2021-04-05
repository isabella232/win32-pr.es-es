---
title: Escuchar eventos de la cinta de opciones
description: El marco de la cinta de opciones de Windows usa la infraestructura de seguimiento de eventos para Windows (ETW) para que los desarrolladores puedan saber cómo interactúan los usuarios con la cinta de la aplicación.
ms.assetid: F29A8E41-C902-410E-BD28-653E078320E9
keywords:
- Cinta de Windows, eventos
- Cinta, eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcbfb2c6417c1423cb785b6b80de4396146535c2
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104359467"
---
# <a name="listening-for-ribbon-events"></a>Escuchar eventos de la cinta de opciones

El marco de la cinta de opciones de Windows usa la infraestructura [de seguimiento de eventos para Windows (ETW)](../etw/event-tracing-portal.md) para que los desarrolladores puedan saber cómo interactúan los usuarios con la cinta de la aplicación.

## <a name="introduction"></a>Introducción

El mecanismo de eventos de la cinta de opciones está diseñado de forma que el marco informe los eventos de la interfaz de usuario de la cinta de opciones a la aplicación para que pueda supervisar la actividad del usuario, conocer sus patrones de interacción y evaluar las tendencias de uso. Esta información se puede usar para refinar la experiencia del usuario para futuras iteraciones de la aplicación de la cinta de opciones.

El uso de los eventos de marco de cinta implica lo siguiente:

1.  La aplicación de cinta debe registrar un agente [de escucha de seguimiento de eventos para Windows (ETW)](../etw/event-tracing-portal.md) para recibir notificaciones de eventos de la cinta de opciones desde el marco de cinta.
2.  El marco de cinta activa las devoluciones de llamada de eventos de la interfaz de usuario en tiempo de ejecución, si la aplicación ha registrado un agente [de escucha de seguimiento de eventos para Windows (ETW)](../etw/event-tracing-portal.md) .

## <a name="supported-events"></a>Eventos admitidos

Los eventos expuestos a las aplicaciones de la cinta de opciones se describen en la tabla siguiente. 

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
<td>Tabulación activada</td>
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
<td>Menú de aplicación cerrado</td>
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
<li>CABLE</li>
<li>QUICKACCESSTOOLBAR</li>
<li>APPLICATIONMENU</li>
<li>CONTEXTPOPUP</li>
</ul>
<br/> IDENTIFICADOR de comando primario<br/> Nombre del comando primario<br/> Uno de los siguientes métodos de invocación:
<ul>
<li>HIZO</li>
<li>KEYTIP</li>
<li>TECLADO</li>
<li>ENTRADAS</li>
</ul>
<br/>
<blockquote>
[!Note]<br />
Las galerías de elementos y los cuadros combinados incluyen el índice de elementos seleccionado, pero no incluyen valores de cadena y enteros. Los controles de número no incluyen el valor entero.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Cinta minimizada</td>
<td>Verbo de evento<br/></td>
</tr>
<tr class="odd">
<td>Cinta expandida (clic en el botón expandir o en anclado)</td>
<td>Verbo de evento<br/></td>
</tr>
<tr class="even">
<td>Modo de aplicación cambiado</td>
<td>Verbo de evento<br/> IDENTIFICADOR de modo (valor establecido a través de <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes"><strong>SetModes</strong></a>)<br/>
<blockquote>
[!Note]<br />
La aplicación es responsable de desempaquetar este entero para determinar qué modos se establecieron.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Información sobre herramientas mostrada</td>
<td>Verbo de evento<br/> IDENTIFICADOR de comando primario<br/> Nombre del comando primario<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guías para desarrolladores del marco de cinta de Windows](windowsribbon-guides-entry.md)
</dt> <dt>

[Declarar comandos y controles con el marcado de la cinta de opciones](./windowsribbon-schema.md)
</dt> <dt>

[Instrucciones para la experiencia del usuario en cinta](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Proceso de diseño de la cinta](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

