---
title: Estilos extendidos de barra de herramientas (CommCtrl. h)
description: En esta sección se enumeran los estilos extendidos admitidos por los controles de barra de herramientas.
ms.assetid: da31dbbf-8d0a-4711-a1af-382c62e653cd
topic_type:
- apiref
api_name:
- TBSTYLE_EX_DRAWDDARROWS
- TBSTYLE_EX_HIDECLIPPEDBUTTONS
- TBSTYLE_EX_DOUBLEBUFFER
- TBSTYLE_EX_MIXEDBUTTONS
- TBSTYLE_EX_MULTICOLUMN
- TBSTYLE_EX_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056e48753485364017f04f7b84e609b19473bf5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649686"
---
# <a name="toolbar-extended-styles"></a>Estilos extendidos de barra de herramientas

En esta sección se enumeran los estilos extendidos admitidos por los controles de barra de herramientas.



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
<td style="text-align: left;"><span id="TBSTYLE_EX_DRAWDDARROWS"></span><span id="tbstyle_ex_drawddarrows"></span><dl> <dt><strong>TBSTYLE_EX_DRAWDDARROWS</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versión 4,71</a>. Este estilo permite que los botones tengan una flecha de lista desplegable independiente. Los botones que tienen el estilo de <a href="toolbar-control-and-button-styles.md"><strong>BTNS_DROPDOWN</strong></a> se dibujarán con una flecha de lista desplegable en una sección independiente, a la derecha del botón. Si se hace clic en la flecha, solo se detendrá la parte de la flecha del botón y el control de barra de herramientas enviará un <a href="tbn-dropdown.md">TBN_DROPDOWN</a> código de notificación para solicitar a la aplicación que muestre el menú desplegable. Si se hace clic en la parte principal del botón, el control de barra de herramientas envía un mensaje de WM_COMMAND con el identificador del botón. Normalmente, la aplicación responde iniciando el primer comando en el menú.<br/> Hay muchas situaciones en las que quizás desee tener solo algunos de los botones de lista desplegable en una barra de herramientas con flechas separadas. Para ello, establezca el estilo extendido TBSTYLE_EX_DRAWDDARROWS. Asigne a los botones que no tendrán flechas separadas el estilo de <a href="toolbar-control-and-button-styles.md"><strong>BTNS_WHOLEDROPDOWN</strong></a> . Los botones con este estilo tendrán una flecha junto a la imagen. Sin embargo, la flecha no será independiente y cuando se haga clic en cualquier parte del botón, el control de barra de herramientas enviará un código de notificación <a href="tbn-dropdown.md">TBN_DROPDOWN</a> . Para evitar problemas de repintado, este estilo debe establecerse antes de que el control de barra de herramientas se vuelva visible.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_HIDECLIPPEDBUTTONS"></span><span id="tbstyle_ex_hideclippedbuttons"></span><dl> <dt><strong>TBSTYLE_EX_HIDECLIPPEDBUTTONS</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versión 5,81</a>. Este estilo oculta los botones recortados parcialmente. El uso más común de este estilo es para las barras de herramientas que forman parte de un control rebar. Si una banda adyacente cubre parte de un botón, el botón no se mostrará. Sin embargo, si la banda rebar tiene el estilo de <a href="/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa"><strong>RBBS_USECHEVRON</strong></a> , el botón se mostrará en el menú desplegable del botón de contenido adicional. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TBSTYLE_EX_DOUBLEBUFFER"></span><span id="tbstyle_ex_doublebuffer"></span><dl> <dt><strong>TBSTYLE_EX_DOUBLEBUFFER</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versión 6</a>. Este estilo requiere que la barra de herramientas tenga doble búfer. El doble búfer es un mecanismo que detecta cuándo ha cambiado la barra de herramientas. <br/>
<blockquote>
[!Note]<br />
Comctl32.dll versión 6 no es redistribuible, pero se incluye en Windows o posterior. Para usar Comctl32.dll versión 6, especifíquelo en un manifiesto. Para obtener más información sobre los manifiestos, vea <a href="cookbook-overview.md">habilitar estilos visuales</a>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_MIXEDBUTTONS"></span><span id="tbstyle_ex_mixedbuttons"></span><dl> <dt><strong>TBSTYLE_EX_MIXEDBUTTONS</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versión 5,81</a>. Este estilo permite establecer el texto de todos los botones, pero solo se muestra para esos botones con el estilo de botón de <a href="toolbar-control-and-button-styles.md"><strong>BTNS_SHOWTEXT</strong></a> . También se debe establecer el estilo <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_LIST</strong></a> . Normalmente, cuando un botón no muestra texto, la aplicación debe controlar <a href="tbn-getinfotip.md">TBN_GETINFOTIP</a> o <a href="ttn-getdispinfo.md">TTN_GETDISPINFO</a> para mostrar una información sobre herramientas. Con el TBSTYLE_EX_MIXEDBUTTONS estilo extendido, el texto que se establece pero no se muestra en un botón se usará automáticamente como texto de la información sobre herramientas del botón. La aplicación solo necesita controlar TBN_GETINFOTIP o TTN_GETDISPINFO si necesita más flexibilidad para especificar el texto de la información sobre herramientas. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TBSTYLE_EX_MULTICOLUMN"></span><span id="tbstyle_ex_multicolumn"></span><dl> <dt><strong>TBSTYLE_EX_MULTICOLUMN</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versión 5,82</a>. <strong>Diseñado para uso interno; no se recomienda para su uso en aplicaciones de.</strong> Este estilo proporciona a la barra de herramientas una orientación vertical y organiza los botones de la barra de herramientas en columnas. Los botones fluyen verticalmente hasta que un botón supera el alto de límite de la barra de herramientas (vea <a href="tb-setboundingsize.md"><strong>TB_SETBOUNDINGSIZE</strong></a>) y, a continuación, se crea una nueva columna. La barra de herramientas fluye los botones de esta manera hasta que se coloquen todos los botones. Para usar este estilo, también se debe establecer el estilo TBSTYLE_EX_VERTICAL. <br/>
<blockquote>
[!Note]<br />
Es posible que este estilo no se admita en versiones futuras de Comctl32.dll. Además, este estilo no se define en commctrl. h. Agregue la siguiente definición a los archivos de origen de la aplicación para usar este estilo: <code>#define TBSTYLE_EX_MULTICOLUMN 0x00000002</code>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TBSTYLE_EX_VERTICAL"></span><span id="tbstyle_ex_vertical"></span><dl> <dt><strong>TBSTYLE_EX_VERTICAL</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versión 5,82</a>. <strong>Diseñado para uso interno; no se recomienda para su uso en aplicaciones de.</strong> Este estilo proporciona a la barra de herramientas una orientación vertical. Los botones de la barra de herramientas fluyen de arriba abajo en lugar de horizontalmente. <br/>
<blockquote>
[!Note]<br />
Es posible que este estilo no se admita en versiones futuras de Comctl32.dll. Además, este estilo no se define en commctrl. h. Agregue la siguiente definición a los archivos de origen de la aplicación para usar este estilo: <code>#define TBSTYLE_EX_VERTICAL 0x00000004</code>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Observaciones

Para establecer un estilo extendido, envíe el control de barra de herramientas a un mensaje [**TB \_ SETEXTENDEDSTYLE**](tb-setextendedstyle.md) . Para determinar qué estilos extendidos están establecidos actualmente, envíe un mensaje de [**TB \_ GETEXTENDEDSTYLE**](tb-getextendedstyle.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





