---
title: Funciones de patrón de control en desuso
description: Funciones de patrón de control en desuso
ms.assetid: 06434b07-7592-4909-8c4e-064382bdbf98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d124482ac7cfb9c14a72644558df0eb174e574f598fda5ef2ffd2fed928a717
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795465"
---
# <a name="deprecated-control-pattern-functions"></a>Funciones de patrón de control en desuso

> [!Note]  
> Las funciones de patrón de control descritas en esta sección están en desuso. Las aplicaciones cliente deben usar las interfaces del Modelo de objetos componentes (COM) descritas en las secciones siguientes:
>
> -   [Automatización de la interfaz de usuario interfaces de elementos para clientes](uiauto-entry-uiautoclientinterfaces.md)
> -   [Interfaz de condición de propiedad para clientes](uiauto-client-propconditioninterfaces.md)
> -   [Interfaces de patrón de control para clientes](uiauto-client-controlpatterninterfaces.md)
> -   [Interfaces de control de eventos para clientes](uiauto-client-eventhandlinginterfaces.md)
> -   [Interfaces de generador de proxy para clientes](uiauto-client-proxyfactoryinterfaces.md)

 

## <a name="in-this-section"></a>En esta sección



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Función</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-dockpattern_setdockposition"><strong>DockPattern_SetDockPosition</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las interfaces COM de Microsoft Automatización de la interfaz de usuario en su lugar.
</blockquote>
<br/> Acopla el elemento Automatización de la interfaz de usuario en el <em>elemento dockPosition solicitado</em> dentro de un contenedor de acoplamiento.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-expandcollapsepattern_collapse"><strong>ExpandCollapsePattern_Collapse</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Oculta todos los nodos descendientes, controles o contenido del Automatización de la interfaz de usuario elemento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-expandcollapsepattern_expand"><strong>ExpandCollapsePattern_Expand</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Expande un control en la pantalla para que muestre más información.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-gridpattern_getitem"><strong>GridPattern_GetItem</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Obtiene el nodo de un elemento de una cuadrícula.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-invokepattern_invoke"><strong>InvokePattern_Invoke</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Envía una solicitud para activar un control e iniciar su acción única e inequívoca.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-itemcontainerpattern_finditembyproperty"><strong>ItemContainerPattern_FindItemByProperty</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Recupera un nodo dentro de un nodo que lo contiene, basándose en un valor de propiedad especificado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_dodefaultaction"><strong>LegacyIAccessiblePattern_DoDefaultAction</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Realiza la acción Microsoft Active Accessibility predeterminada para el elemento .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_getiaccessible"><strong>LegacyIAccessiblePattern_GetIAccessible</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Recupera un <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible"><strong>objeto IAccessible</strong></a> que corresponde al Automatización de la interfaz de usuario elemento .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_select"><strong>LegacyIAccessiblePattern_Select</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Realiza una selección Microsoft Active Accessibility de datos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_setvalue"><strong>LegacyIAccessiblePattern_SetValue</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Establece la Microsoft Active Accessibility valor del nodo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-multipleviewpattern_getviewname"><strong>MultipleViewPattern_GetViewName</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Recupera el nombre de una vista específica del control.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-multipleviewpattern_setcurrentview"><strong>MultipleViewPattern_SetCurrentView</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Establece un control en un diseño diferente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-rangevaluepattern_setvalue"><strong>RangeValuePattern_SetValue</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Establece el valor de un control que tiene un intervalo numérico.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollitempattern_scrollintoview"><strong>ScrollItemPattern_ScrollIntoView</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Desplaza el área de contenido de un objeto contenedor para mostrar el Automatización de la interfaz de usuario dentro de la región visible (ventanilla) del contenedor.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollpattern_scroll"><strong>ScrollPattern_Scroll</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Desplaza la región visible actualmente del área de contenido del <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount"><strong>scrollAmount</strong></a>especificado, horizontal, verticalmente o ambos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollpattern_setscrollpercent"><strong>ScrollPattern_SetScrollPercent</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Desplaza un contenedor a una posición específica horizontal, verticalmente o ambas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_addtoselection"><strong>SelectionItemPattern_AddToSelection</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Agrega un elemento no seleccionado a una selección de un control .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_removefromselection"><strong>SelectionItemPattern_RemoveFromSelection</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Quita un elemento de la selección en un contenedor de selección.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_select"><strong>SelectionItemPattern_Select</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Selecciona un elemento de un contenedor de selección.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-synchronizedinputpattern_cancel"><strong>SynchronizedInputPattern_Cancel</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Hace que Automatización de la interfaz de usuario proveedor deje de escuchar la entrada del mouse o del teclado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-synchronizedinputpattern_startlistening"><strong>SynchronizedInputPattern_StartListening</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Hace que el Automatización de la interfaz de usuario empiece a escuchar la entrada del mouse o del teclado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_get_documentrange"><strong>TextPattern_get_DocumentRange</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Obtiene el intervalo de texto de todo el documento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_get_supportedtextselection"><strong>TextPattern_get_SupportedTextSelection</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Determina si el contenido del contenedor de texto se puede seleccionar y deseleccionado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_getselection"><strong>TextPattern_GetSelection</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Obtiene el intervalo actual de texto seleccionado de un contenedor de texto que admite el patrón de texto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_getvisibleranges"><strong>TextPattern_GetVisibleRanges</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Recupera una matriz de intervalos de texto no contiguos de un contenedor de texto donde cada intervalo comienza con la primera línea parcialmente visible y continúa hasta el final de la última línea parcialmente visible. Por ejemplo, un diseño de varias columnas donde las columnas se desplazan parcialmente fuera del área visible de la ventanilla y el contenido fluye desde la parte inferior de una columna hasta la parte superior de la siguiente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_rangefromchild"><strong>TextPattern_RangeFromChild</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Obtiene el intervalo de texto que abarca un nodo determinado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_rangefrompoint"><strong>TextPattern_RangeFromPoint</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Recupera el intervalo de texto degenerado (vacío) más cercano a las coordenadas de pantalla especificadas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_addtoselection"><strong>TextRange_AddToSelection</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Agrega a la colección existente de texto resaltado en un contenedor de texto que admite varias selecciones <em></em> no unida resaltando el texto complementario correspondiente a los puntos de conexión Start y <em>End</em> del intervalo de texto que realiza la llamada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_clone"><strong>TextRange_Clone</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Copia un intervalo de texto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_compare"><strong>TextRange_Compare</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Compara dos intervalos de texto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_compareendpoints"><strong>TextRange_CompareEndpoints</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Devuelve un valor que indica si dos intervalos de texto tienen puntos de conexión idénticos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_expandtoenclosingunit"><strong>TextRange_ExpandToEnclosingUnit</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Expande el intervalo de texto a una unidad más grande o más pequeña, como Carácter, Palabra, Línea o Página.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_findattribute"><strong>TextRange_FindAttribute</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Busca en una dirección especificada la primera parte de texto que admite un atributo de texto especificado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_findtext"><strong>TextRange_FindText</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Devuelve el primer intervalo de texto en la dirección especificada que contiene el texto que el cliente está buscando.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getattributevalue"><strong>TextRange_GetAttributeValue</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Obtiene el valor de un atributo de texto para un intervalo de texto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getboundingrectangles"><strong>TextRange_GetBoundingRectangles</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Recupera el número mínimo de rectángulos delimitadores que pueden incluir el intervalo, un rectángulo por línea.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getchildren"><strong>TextRange_GetChildren</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Devuelve todos Automatización de la interfaz de usuario elementos incluidos en el intervalo de texto especificado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getenclosingelement"><strong>TextRange_GetEnclosingElement</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Devuelve el nodo del siguiente proveedor más pequeño que cubre el intervalo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_gettext"><strong>TextRange_GetText</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Devuelve el texto de un intervalo de texto, hasta un número especificado de caracteres.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_move"><strong>TextRange_Move</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Mueve el intervalo de texto el número especificado de unidades solicitadas por el cliente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_moveendpointbyrange"><strong>TextRange_MoveEndpointByRange</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Mueve un punto de conexión de un intervalo al punto de conexión de otro intervalo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_moveendpointbyunit"><strong>TextRange_MoveEndpointByUnit</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Mueve un punto de conexión del intervalo el número especificado de unidades.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_removefromselection"><strong>TextRange_RemoveFromSelection</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Quita el texto seleccionado, correspondiente al intervalo de texto de llamada <em>TextPatternRangeEndpoint_Start</em> y <em>puntos</em> de conexión TextPatternRangeEndpoint_End, de una colección existente de texto seleccionado en un contenedor de texto que admite varias selecciones no seleccionadas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_scrollintoview"><strong>TextRange_ScrollIntoView</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Desplaza el texto para que el intervalo especificado sea visible en la ventanilla.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_select"><strong>TextRange_Select</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Selecciona un intervalo de texto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-togglepattern_toggle"><strong>TogglePattern_Toggle</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario com en su lugar.
</blockquote>
<br/> Alterna un control a su siguiente estado admitido.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_move"><strong>TransformPattern_Move</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario COM en su lugar.
</blockquote>
<br/> Mueve un elemento a una ubicación especificada en la pantalla.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_resize"><strong>TransformPattern_Resize</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario COM en su lugar.
</blockquote>
<br/> Cambia el tamaño de un elemento de la pantalla.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_rotate"><strong>TransformPattern_Rotate</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario COM en su lugar.
</blockquote>
<br/> Gira un elemento en la pantalla.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-valuepattern_setvalue"><strong>ValuePattern_SetValue</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario COM en su lugar.
</blockquote>
<br/> Establece el valor de texto de un elemento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-virtualizeditempattern_realize"><strong>VirtualizedItemPattern_Realize</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario COM en su lugar.
</blockquote>
<br/> Hace que el elemento virtual sea totalmente accesible como elemento de automatización de la interfaz de usuario.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_close"><strong>WindowPattern_Close</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario COM en su lugar.
</blockquote>
<br/> Cierra una ventana abierta.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_setwindowvisualstate"><strong>WindowPattern_SetWindowVisualState</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario COM en su lugar.
</blockquote>
<br/> Establece el estado visual de una ventana; por ejemplo, para maximizar una ventana.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_waitforinputidle"><strong>WindowPattern_WaitForInputIdle</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta función es desusada. Las aplicaciones cliente deben usar las Automatización de la interfaz de usuario COM en su lugar.
</blockquote>
<br/> Hace que el código de llamada se bloquee durante el tiempo especificado o hasta que el proceso asociado entre en un estado de inactividad, lo que ocurra primero.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Automatización de la interfaz de usuario clientes](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





