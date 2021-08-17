---
title: List-View de ventana (CommCtrl.h)
description: Los siguientes estilos de ventana son específicos de los controles de vista de lista.
ms.assetid: 8b57239b-112e-4fb6-b394-15501bd3f5b3
topic_type:
- apiref
api_name:
- LVS_ALIGNLEFT
- LVS_ALIGNMASK
- LVS_ALIGNTOP
- LVS_AUTOARRANGE
- LVS_EDITLABELS
- LVS_ICON
- LVS_LIST
- LVS_NOCOLUMNHEADER
- LVS_NOLABELWRAP
- LVS_NOSCROLL
- LVS_NOSORTHEADER
- LVS_OWNERDATA
- LVS_OWNERDRAWFIXED
- LVS_REPORT
- LVS_SHAREIMAGELISTS
- LVS_SHOWSELALWAYS
- LVS_SINGLESEL
- LVS_SMALLICON
- LVS_SORTASCENDING
- LVS_SORTDESCENDING
- LVS_TYPEMASK
- LVS_TYPESTYLEMASK
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3e326f4508d08f1052747e64ea5eba184f45f7e73a1cb55539255a27fd8c8c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412030"
---
# <a name="list-view-window-styles"></a>List-View de ventana

Los siguientes estilos de ventana son específicos de los controles de vista de lista.



| Constante                                                                                                                                                                        | Descripción                                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVS_ALIGNLEFT"></span><span id="lvs_alignleft"></span><dl> <dt>**LVS \_ ALIGNLEFT**</dt> </dl>                   | Los elementos se alinean a la izquierda en el icono y en la vista de iconos pequeños. <br/>                                                                                                                                                                                                                                                                                             |
| <span id="LVS_ALIGNMASK"></span><span id="lvs_alignmask"></span><dl> <dt>**LVS \_ ALIGNMASK**</dt> </dl>                   | Alineación actual del control. <br/>                                                                                                                                                                                                                                                                                                                |
| <span id="LVS_ALIGNTOP"></span><span id="lvs_aligntop"></span><dl> <dt>**LVS \_ ALIGNTOP**</dt> </dl>                      | Los elementos se alinean con la parte superior del control de vista de lista en la vista de icono y icono pequeño. <br/>                                                                                                                                                                                                                                                            |
| <span id="LVS_AUTOARRANGE"></span><span id="lvs_autoarrange"></span><dl> <dt>**LVS \_ AUTOARRANGE**</dt> </dl>             | Los iconos se mantienen organizados automáticamente en el icono y la vista de iconos pequeños. <br/>                                                                                                                                                                                                                                                                              |
| <span id="LVS_EDITLABELS"></span><span id="lvs_editlabels"></span><dl> <dt>**LVS \_ EDITLABELS**</dt> </dl>                | El texto del elemento se puede editar en su lugar. La ventana primaria debe procesar el [código de notificación \_ ENDLABELEDIT de LVN.](lvn-endlabeledit.md) <br/>                                                                                                                                                                                                               |
| <span id="LVS_ICON"></span><span id="lvs_icon"></span><dl> <dt>**ICONO \_ LVS**</dt> </dl>                                  | Este estilo especifica la vista de iconos. <br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="LVS_LIST"></span><span id="lvs_list"></span><dl> <dt>**LVS \_ LIST**</dt> </dl>                                  | Este estilo especifica la vista de lista. <br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="LVS_NOCOLUMNHEADER"></span><span id="lvs_nocolumnheader"></span><dl> <dt>**LVS \_ NOCOLUMNHEADER**</dt> </dl>    | Los encabezados de columna no se muestran en la vista de informe. De forma predeterminada, las columnas tienen encabezados en la vista de informe. <br/>                                                                                                                                                                                                                                               |
| <span id="LVS_NOLABELWRAP"></span><span id="lvs_nolabelwrap"></span><dl> <dt>**LVS \_ NOLABELWRAP**</dt> </dl>             | El texto del elemento se muestra en una sola línea en la vista de iconos. De forma predeterminada, el texto del elemento puede ajustarse en la vista de iconos. <br/>                                                                                                                                                                                                                                              |
| <span id="LVS_NOSCROLL"></span><span id="lvs_noscroll"></span><dl> <dt>**LVS \_ NOSCROLL**</dt> </dl>                      | El desplazamiento está deshabilitado. Todos los elementos deben estar dentro del área de cliente. Este estilo no es compatible con los estilos **LVS \_ LIST** o **LVS \_ REPORT.** Consulte Knowledge Base artículo Q137520 para más información. <br/>                                                                                                                                      |
| <span id="LVS_NOSORTHEADER"></span><span id="lvs_nosortheader"></span><dl> <dt>**LVS \_ NOSORTHEADER**</dt> </dl>          | Los encabezados de columna no funcionan como botones. Este estilo se puede usar si al hacer clic en un encabezado de columna en la vista de informe no se lleva a cabo una acción, como la ordenación. <br/>                                                                                                                                                                                       |
| <span id="LVS_OWNERDATA"></span><span id="lvs_ownerdata"></span><dl> <dt>**LVS \_ OWNERDATA**</dt> </dl>                   | [Versión 4.70.](common-control-versions.md) Este estilo especifica un control de vista de lista virtual. Para obtener más información sobre este estilo de control de lista, vea [About List-View Controls](list-view-controls-overview.md). <br/>                                                                                                                             |
| <span id="LVS_OWNERDRAWFIXED"></span><span id="lvs_ownerdrawfixed"></span><dl> <dt>**LVS \_ OWNERDRAWFIXED**</dt> </dl>    | La ventana del propietario puede pintar elementos en la vista de informe. El control list-view envía un [**mensaje \_ DRAWITEM de WM**](wm-drawitem.md) para pintar cada elemento; no envía mensajes independientes para cada subelemento. El **miembro iItemData** de la [**estructura DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) contiene los datos del elemento para el elemento de vista de lista especificado. <br/> |
| <span id="LVS_REPORT"></span><span id="lvs_report"></span><dl> <dt>**INFORME \_ LVS**</dt> </dl>                            | Este estilo especifica la vista de informe. Cuando se usa el estilo \_ LVS REPORT con un control list-view, la primera columna siempre se alinea a la izquierda. No puede usar LVCFMT \_ RIGHT para cambiar esta alineación. Consulte [**LVCOLUMN para**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) obtener más información sobre la alineación de columnas. <br/>                                                                      |
| <span id="LVS_SHAREIMAGELISTS"></span><span id="lvs_shareimagelists"></span><dl> <dt>**LVS \_ SHAREIMAGELISTS**</dt> </dl> | La lista de imágenes no se eliminará cuando se destruya el control. Este estilo permite el uso de las mismas listas de imágenes con varios controles de vista de lista. <br/>                                                                                                                                                                                          |
| <span id="LVS_SHOWSELALWAYS"></span><span id="lvs_showselalways"></span><dl> <dt>**LVS \_ SHOWSELALWAYS**</dt> </dl>       | Siempre se muestra la selección, si existe, aunque el control no tenga el foco. <br/>                                                                                                                                                                                                                                                            |
| <span id="LVS_SINGLESEL"></span><span id="lvs_singlesel"></span><dl> <dt>**LVS \_ SINGLESEL**</dt> </dl>                   | Solo se puede seleccionar un elemento a la vez. De forma predeterminada, se pueden seleccionar varios elementos. <br/>                                                                                                                                                                                                                                                            |
| <span id="LVS_SMALLICON"></span><span id="lvs_smallicon"></span><dl> <dt>**LVS \_ SMALLICON**</dt> </dl>                   | Este estilo especifica una vista de icono pequeña. <br/>                                                                                                                                                                                                                                                                                                           |
| <span id="LVS_SORTASCENDING"></span><span id="lvs_sortascending"></span><dl> <dt>**LVS \_ SORTASCENDING**</dt> </dl>       | Los índices de elementos se ordenan en función del texto del elemento en orden ascendente. <br/>                                                                                                                                                                                                                                                                                  |
| <span id="LVS_SORTDESCENDING"></span><span id="lvs_sortdescending"></span><dl> <dt>**LVS \_ SORTDESCENDING**</dt> </dl>    | Los índices de elementos se ordenan en función del texto del elemento en orden descendente. <br/>                                                                                                                                                                                                                                                                                 |
| <span id="LVS_TYPEMASK"></span><span id="lvs_typemask"></span><dl> <dt>**MÁSCARA DE \_ TIPOS LVS**</dt> </dl>                      | Determina el estilo de ventana actual del control. <br/>                                                                                                                                                                                                                                                                                                  |
| <span id="LVS_TYPESTYLEMASK"></span><span id="lvs_typestylemask"></span><dl> <dt>**LVS \_ TYPESTYLEMASK**</dt> </dl>       | Determina los estilos de ventana que controlan la alineación de elementos y la apariencia y el comportamiento del encabezado. <br/>                                                                                                                                                                                                                                                    |



## <a name="remarks"></a>Comentarios

Para los **estilos LVS \_ SORTASCENDING** y **LVS \_ SORTDESCENDING,** los índices de elementos se ordenan en función del texto del elemento en orden ascendente o descendente, respectivamente. Dado que **las vistas LVS \_ LIST** y **LVS \_ REPORT** muestran elementos en el mismo orden que sus índices, los resultados de la ordenación son inmediatamente visibles para el usuario. Las **vistas LVS \_ ICON y** **LVS \_ SMALLICON** no usan índices de elementos para determinar la posición de los iconos. Con esas vistas, los resultados de la ordenación no son visibles para el usuario.

Puede usar la máscara **LVS \_ TYPEMASK** para aislar los estilos de ventana correspondientes a la vista actual: **LVS \_ ICON**, **LVS \_ LIST,** **LVS \_ REPORT** y **LVS \_ SMALLICON.**

Puede usar la máscara **\_ LVS ALIGNMASK** para aislar los estilos de ventana que especifican la alineación de elementos: **LVS \_ ALIGNLEFT** y **LVS \_ ALIGNTOP.**

Puede usar la máscara **LVS \_ TYPESTYLEMASK** para aislar los estilos de ventana que controlan la alineación de elementos **(LVS \_ ALIGNLEFT** y **LVS \_ ALIGNTOP)** y los que controlan la apariencia y el comportamiento del encabezado **(LVS \_ NOCOLUMNHEADER** y **LVS \_ NOSORTHEADER).**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estilos y vistas de vista de lista](list-view-controls-overview.md)
</dt> </dl>

 

 





