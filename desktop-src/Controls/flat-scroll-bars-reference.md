---
title: Barra de desplazamiento plana
description: Esta sección contiene información sobre los elementos de programación usados para controlar las barras de desplazamiento sin formato.
ms.assetid: vs|controls|~\controls\flatsb\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e611e8d5755d119a8c24bdbccb9f10408d3d7d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903259"
---
# <a name="flat-scroll-bar"></a>Barra de desplazamiento plana

Esta sección contiene información sobre los elementos de programación usados para controlar las barras de desplazamiento sin formato.

### <a name="overviews"></a>Temas de introducción



| Tema                                    | Contenido                                                                                                                                                                                                                                                                              |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Barras de desplazamiento plana](flat-scroll-bars.md) | Microsoft Internet Explorer 4,0 presentó una nueva tecnología visual denominada barras de desplazamiento plana. Funcionalmente, las barras de desplazamiento sin formato se comportan igual que las barras de desplazamiento estándar. La diferencia es que puede personalizar su apariencia en una extensión mayor que las barras de desplazamiento estándar.<br/> |



 

### <a name="functions"></a>Functions



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tema</th>
<th>Contenido</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_enablescrollbar"><strong>FlatSB_EnableScrollBar</strong></a></td>
<td>Habilita o deshabilita uno o ambos botones de dirección de la barra de desplazamiento plana. Si no se inicializan las barras de desplazamiento sin formato para la ventana, esta función llama a la función <a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>EnableScrollBar</strong></a> estándar. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollinfo"><strong>FlatSB_GetScrollInfo</strong></a></td>
<td>Obtiene la información de una barra de desplazamiento plana. Si no se inicializan las barras de desplazamiento sin formato para la ventana, esta función llama a la función <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a> estándar. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpos"><strong>FlatSB_GetScrollPos</strong></a></td>
<td>Obtiene la posición del control en una barra de desplazamiento plana. Si no se inicializan las barras de desplazamiento sin formato para la ventana, esta función llama a la función <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a> estándar. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a></td>
<td>Obtiene las propiedades de una barra de desplazamiento plana. Esta función también se puede usar para determinar si se ha llamado a <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> para esta ventana. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpropptr"><strong>FlatSB_GetScrollPropPtr</strong></a></td>
<td>Obtiene las propiedades de una barra de desplazamiento plana. Esta función también se puede usar para determinar si se ha llamado a <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> para esta ventana.
<blockquote>
[!Note]<br />
Es idéntico a <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollrange"><strong>FlatSB_GetScrollRange</strong></a></td>
<td>Obtiene el intervalo de desplazamiento de una barra de desplazamiento plana. Si no se inicializan las barras de desplazamiento sin formato para la ventana, esta función llama a la función <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a> estándar. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollinfo"><strong>FlatSB_SetScrollInfo</strong></a></td>
<td>Establece la información de una barra de desplazamiento plana. Si no se inicializan las barras de desplazamiento sin formato para la ventana, esta función llama a la función <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a> estándar. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollpos"><strong>FlatSB_SetScrollPos</strong></a></td>
<td>Establece la posición actual del control Thumb en una barra de desplazamiento plana. Si no se inicializan las barras de desplazamiento sin formato para la ventana, esta función llama a la función <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a> estándar. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop"><strong>FlatSB_SetScrollProp</strong></a></td>
<td>Establece las propiedades de una barra de desplazamiento plana. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollrange"><strong>FlatSB_SetScrollRange</strong></a></td>
<td>Establece el intervalo de desplazamiento de una barra de desplazamiento plana. Si no se inicializan las barras de desplazamiento sin formato para la ventana, esta función llama a la función <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a> estándar. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_showscrollbar"><strong>FlatSB_ShowScrollBar</strong></a></td>
<td>Muestra u oculta una barra de desplazamiento plana. Si no se inicializan las barras de desplazamiento sin formato para la ventana, esta función llama a la función <a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>ShowScrollBar</strong></a> estándar. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a></td>
<td>Inicializa barras de desplazamiento plana para una ventana determinada. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb"><strong>UninitializeFlatSB</strong></a></td>
<td>Desinicializa las barras de desplazamiento plana para una ventana determinada. La ventana especificada se revertirá a las barras de desplazamiento estándar. <br/></td>
</tr>
</tbody>
</table>



 

 

 





