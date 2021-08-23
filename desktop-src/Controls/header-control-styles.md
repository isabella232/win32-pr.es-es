---
title: Estilos de control de encabezado (CommCtrl.h)
description: Los controles de encabezado tienen una serie de estilos, descritos en esta sección, que determinan la apariencia y el comportamiento del control. Los estilos iniciales se establecen al crear el control de encabezado.
ms.assetid: e47dc6c3-a1af-456c-9235-29ce63f1e13b
topic_type:
- apiref
api_name:
- HDS_BUTTONS
- HDS_DRAGDROP
- HDS_FILTERBAR
- HDS_FLAT
- HDS_FULLDRAG
- HDS_HIDDEN
- HDS_HORZ
- HDS_HOTTRACK
- HDS_CHECKBOXES
- HDS_NOSIZING
- HDS_OVERFLOW
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe76446196c565796388a5bcd402e9fb3a071e1b14626d7ead949ab9eb0e3b61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435107"
---
# <a name="header-control-styles"></a>Estilos de control de encabezado

Los controles de encabezado tienen una serie de estilos, descritos en esta sección, que determinan la apariencia y el comportamiento del control. Los estilos iniciales se establecen al crear el control de encabezado.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_BUTTONS"></span><span id="hds_buttons"></span><dl> <dt><strong>HDS_BUTTONS</strong></dt> </dl></td>
<td style="text-align: left;">Cada elemento del control tiene un aspecto y se comporta como un botón de inserción. Este estilo es útil si una aplicación lleva a cabo una tarea cuando el usuario hace clic en un elemento del control de encabezado. Por ejemplo, una aplicación podría ordenar la información de las columnas de forma diferente en función del elemento en el que haga clic el usuario. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_DRAGDROP"></span><span id="hds_dragdrop"></span><dl> <dt><strong>HDS_DRAGDROP</strong></dt> </dl></td>
<td style="text-align: left;">Permite la reordenación de arrastrar y colocar de elementos de encabezado. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_FILTERBAR"></span><span id="hds_filterbar"></span><dl> <dt><strong>HDS_FILTERBAR</strong></dt> </dl></td>
<td style="text-align: left;">Incluya una barra de filtro como parte del control de encabezado estándar. Esta barra permite a los usuarios aplicar cómodamente un filtro a la pantalla. Las llamadas <a href="hdm-layout.md"><strong>a HDM_LAYOUT</strong></a> darán como resultado un nuevo tamaño para el control y harán que la vista de lista se actualice. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_FLAT"></span><span id="hds_flat"></span><dl> <dt><strong>HDS_FLAT</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versión 6.0 y posteriores.</a> Hace que el control de encabezado se desentrase sin formato cuando el sistema operativo se ejecuta en modo clásico. <br/>
<blockquote>
[!Note]<br />
Comctl32.dll versión 6 no es redistribuible, pero se incluye en Windows. Para usar Comctl32.dll versión 6, es especificarlo en un manifiesto. Para obtener más información sobre los manifiestos, vea <a href="cookbook-overview.md">Habilitar estilos visuales.</a>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_FULLDRAG"></span><span id="hds_fulldrag"></span><dl> <dt><strong>HDS_FULLDRAG</strong></dt> </dl></td>
<td style="text-align: left;">Hace que el control de encabezado muestre el contenido de la columna incluso mientras el usuario cambia el tamaño de una columna. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_HIDDEN"></span><span id="hds_hidden"></span><dl> <dt><strong>HDS_HIDDEN</strong></dt> </dl></td>
<td style="text-align: left;">Indica un control de encabezado que está pensado para ocultarse. Este estilo no oculta el control. En su lugar, al enviar el <a href="hdm-layout.md"><strong>mensaje HDM_LAYOUT</strong></a> a un control de encabezado con el estilo HDS_HIDDEN, el control devuelve cero en el miembro <strong>cy</strong> de la <a href="/windows/win32/api/winuser/ns-winuser-windowpos"><strong>estructura WINDOWPOS.</strong></a> A continuación, ocultaría el control estableciendo su alto en cero. Esto puede ser útil cuando se desea usar el control como contenedor de información en lugar de un control visual. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_HORZ"></span><span id="hds_horz"></span><dl> <dt><strong>HDS_HORZ</strong></dt> </dl></td>
<td style="text-align: left;">Crea un control de encabezado con una orientación horizontal. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_HOTTRACK"></span><span id="hds_hottrack"></span><dl> <dt><strong>HDS_HOTTRACK</strong></dt> </dl></td>
<td style="text-align: left;">Habilita el seguimiento en caliente. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_CHECKBOXES"></span><span id="hds_checkboxes"></span><dl> <dt><strong>HDS_CHECKBOXES</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versión 6.00 y posteriores.</a> Permite la colocación de casillas en los elementos de encabezado. Para obtener más información, vea el <strong>miembro fmt</strong> de <a href="/windows/win32/api/commctrl/ns-commctrl-hditema"><strong>HDITEM.</strong></a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_NOSIZING"></span><span id="hds_nosizing"></span><dl> <dt><strong>HDS_NOSIZING</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versión 6.00 y posteriores.</a> El usuario no puede arrastrar el divisor en el control de encabezado.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_OVERFLOW"></span><span id="hds_overflow"></span><dl> <dt><strong>HDS_OVERFLOW</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versión 6.00 y posteriores.</a> Se muestra un botón cuando no se pueden mostrar todos los elementos dentro del rectángulo del control de encabezado. Cuando se hace clic en él, este botón envía una <a href="hdn-overflowclick.md">HDN_OVERFLOWCLICK</a> notificación.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Observaciones

Para recuperar y cambiar los estilos después de crear el control, use las funciones [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) [**y SetWindowLong.**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



