---
title: Estilos extendidos de la barra de herramientas (CommCtrl.h)
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
ms.openlocfilehash: 71e242426269d4049b913a41910d325c360886f3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166010"
---
# <a name="toolbar-extended-styles"></a>Estilos extendidos de la barra de herramientas

En esta sección se enumeran los estilos extendidos admitidos por los controles de barra de herramientas.




| Constante | Descripción | 
|----------|-------------|
| <span id="TBSTYLE_EX_DRAWDDARROWS"></span><span id="tbstyle_ex_drawddarrows"></span><dl><dt><strong>TBSTYLE_EX_DRAWDDARROWS</strong></dt></dl> | <a href="common-control-versions.md">Versión 4.71.</a> Este estilo permite que los botones tengan una flecha desplegable independiente. Los botones que <a href="toolbar-control-and-button-styles.md"><strong>tienen BTNS_DROPDOWN</strong></a> estilo se dibujarán con una flecha desplegable en una sección independiente, a la derecha del botón. Si se hace clic en la flecha, solo se descomprime la parte de la flecha del botón y el control de barra de herramientas envía un código de notificación TBN_DROPDOWN para solicitar <a href="tbn-dropdown.md">a</a> la aplicación que muestre el menú desplegable. Si se hace clic en la parte principal del botón, el control de barra de herramientas envía WM_COMMAND mensaje con el identificador del botón. Normalmente, la aplicación responde iniciando el primer comando en el menú.<br /> Hay muchas situaciones en las que puede que desee tener solo algunos de los botones desplegables en una barra de herramientas con flechas separadas. Para ello, establezca el TBSTYLE_EX_DRAWDDARROWS estilo extendido. Dé a los botones que no tendrán flechas separadas <a href="toolbar-control-and-button-styles.md"><strong>el BTNS_WHOLEDROPDOWN</strong></a> estilo. Los botones con este estilo tendrán una flecha que se muestra junto a la imagen. Sin embargo, la flecha no será independiente y, cuando se haga clic en cualquier parte del botón, el control de barra de herramientas enviará un <a href="tbn-dropdown.md">TBN_DROPDOWN</a> de notificación. Para evitar problemas de repintado, este estilo debe establecerse antes de que el control de la barra de herramientas se vuelva visible.<br /> | 
| <span id="TBSTYLE_EX_HIDECLIPPEDBUTTONS"></span><span id="tbstyle_ex_hideclippedbuttons"></span><dl><dt><strong>TBSTYLE_EX_HIDECLIPPEDBUTTONS</strong></dt></dl> | <a href="common-control-versions.md">Versión 5.81.</a> Este estilo oculta los botones recortados parcialmente. El uso más común de este estilo es para las barras de herramientas que forman parte de un control rebar. Si una banda adyacente cubre parte de un botón, no se mostrará el botón. Sin embargo, si la <a href="/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa"><strong></strong></a> banda de rebar tiene el RBBS_USECHEVRON, el botón se mostrará en el menú desplegable del botón de contenido adicional. <br /> | 
| <span id="TBSTYLE_EX_DOUBLEBUFFER"></span><span id="tbstyle_ex_doublebuffer"></span><dl><dt><strong>TBSTYLE_EX_DOUBLEBUFFER</strong></dt></dl> | <a href="common-control-versions.md">Versión 6.</a> Este estilo requiere que la barra de herramientas se almacena en búfer doble. El almacenamiento en búfer doble es un mecanismo que detecta cuándo ha cambiado la barra de herramientas. <br /><blockquote>[!Note]<br />Comctl32.dll versión 6 no es redistribuible, pero se incluye en Windows o posterior. Para usar Comctl32.dll versión 6, es especificarlo en un manifiesto. Para obtener más información sobre los manifiestos, vea <a href="cookbook-overview.md">Habilitar estilos visuales.</a></blockquote><br /> | 
| <span id="TBSTYLE_EX_MIXEDBUTTONS"></span><span id="tbstyle_ex_mixedbuttons"></span><dl><dt><strong>TBSTYLE_EX_MIXEDBUTTONS</strong></dt></dl> | <a href="common-control-versions.md">Versión 5.81.</a> Este estilo permite establecer texto para todos los botones, pero solo se muestra para esos botones con el <a href="toolbar-control-and-button-styles.md"><strong>BTNS_SHOWTEXT</strong></a> de botón. También <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_LIST</strong></a> el estilo de la tabla. Normalmente, cuando un botón no muestra texto, <a href="tbn-getinfotip.md"></a> la aplicación debe controlar TBN_GETINFOTIP o <a href="ttn-getdispinfo.md">TTN_GETDISPINFO</a> mostrar una información sobre herramientas. Con el TBSTYLE_EX_MIXEDBUTTONS extendido, el texto que se establece pero no se muestra en un botón se usará automáticamente como texto de información sobre herramientas del botón. La aplicación solo necesita controlar TBN_GETINFOTIP o TTN_GETDISPINFO si necesita más flexibilidad para especificar el texto de la información sobre herramientas. <br /> | 
| <span id="TBSTYLE_EX_MULTICOLUMN"></span><span id="tbstyle_ex_multicolumn"></span><dl><dt><strong>TBSTYLE_EX_MULTICOLUMN</strong></dt></dl> | <a href="common-control-versions.md">Versión 5.82.</a> <strong>Diseñado para uso interno; no se recomienda para su uso en aplicaciones.</strong> Este estilo proporciona a la barra de herramientas una orientación vertical y organiza los botones de la barra de herramientas en columnas. Los botones fluyen verticalmente hasta que un botón ha superado el alto delimitador de la barra de herramientas (consulte <a href="tb-setboundingsize.md"><strong>TB_SETBOUNDINGSIZE</strong></a>) y, a continuación, se crea una nueva columna. La barra de herramientas fluye los botones de esta manera hasta que se coloquen todos los botones. Para usar este estilo, también TBSTYLE_EX_VERTICAL el estilo de la aplicación. <br /><blockquote>[!Note]<br />Es posible que este estilo no se pueda usar en versiones futuras de Comctl32.dll. Además, este estilo no se define en commctrl.h. Agregue la siguiente definición a los archivos de origen de la aplicación para usar este estilo: <code>#define TBSTYLE_EX_MULTICOLUMN 0x00000002</code></blockquote><br /> | 
| <span id="TBSTYLE_EX_VERTICAL"></span><span id="tbstyle_ex_vertical"></span><dl><dt><strong>TBSTYLE_EX_VERTICAL</strong></dt></dl> | <a href="common-control-versions.md">Versión 5.82.</a> <strong>Diseñado para uso interno; no se recomienda para su uso en aplicaciones.</strong> Este estilo proporciona a la barra de herramientas una orientación vertical. Los botones de la barra de herramientas fluyen de arriba abajo en lugar de horizontalmente. <br /><blockquote>[!Note]<br />Es posible que este estilo no se pueda usar en versiones futuras de Comctl32.dll. Además, este estilo no se define en commctrl.h. Agregue la siguiente definición a los archivos de origen de la aplicación para usar este estilo: <code>#define TBSTYLE_EX_VERTICAL 0x00000004</code></blockquote><br /> | 




## <a name="remarks"></a>Observaciones

Para establecer un estilo extendido, envíe al control de barra de herramientas [**un mensaje \_ TB SETEXTENDEDSTYLE.**](tb-setextendedstyle.md) Para determinar qué estilos extendidos están establecidos actualmente, envíe un [**mensaje \_ GETEXTENDEDSTYLE de**](tb-getextendedstyle.md) TB.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





