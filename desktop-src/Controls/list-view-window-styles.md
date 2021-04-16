---
title: List-View estilos de ventana (CommCtrl. h)
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
ms.openlocfilehash: cae95bdb8dc1263b485f0bd2c50a8124dd57fc3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649716"
---
# <a name="list-view-window-styles"></a>List-View estilos de ventana

Los siguientes estilos de ventana son específicos de los controles de vista de lista.



| Constante                                                                                                                                                                        | Descripción                                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVS_ALIGNLEFT"></span><span id="lvs_alignleft"></span><dl> <dt>**LVS \_ ALIGNLEFT**</dt> </dl>                   | Los elementos se alinean a la izquierda en el icono y en la vista de iconos pequeños. <br/>                                                                                                                                                                                                                                                                                             |
| <span id="LVS_ALIGNMASK"></span><span id="lvs_alignmask"></span><dl> <dt>**LVS \_ ALIGNMASK**</dt> </dl>                   | Alineación actual del control. <br/>                                                                                                                                                                                                                                                                                                                |
| <span id="LVS_ALIGNTOP"></span><span id="lvs_aligntop"></span><dl> <dt>**LVS \_ ALIGNTOP**</dt> </dl>                      | Los elementos se alinean con la parte superior del control de vista de lista en el icono y en la vista de iconos pequeños. <br/>                                                                                                                                                                                                                                                            |
| <span id="LVS_AUTOARRANGE"></span><span id="lvs_autoarrange"></span><dl> <dt>**autoorganización LVS \_**</dt> </dl>             | Los iconos se mantienen organizados automáticamente en el icono y en la vista de iconos pequeños. <br/>                                                                                                                                                                                                                                                                              |
| <span id="LVS_EDITLABELS"></span><span id="lvs_editlabels"></span><dl> <dt>**LVS \_ EDITLABELS**</dt> </dl>                | El texto del elemento puede editarse en su lugar. La ventana primaria debe procesar el código de notificación [ \_ ENDLABELEDIT de LVN](lvn-endlabeledit.md) . <br/>                                                                                                                                                                                                               |
| <span id="LVS_ICON"></span><span id="lvs_icon"></span><dl> <dt>**icono de LVS \_**</dt> </dl>                                  | Este estilo especifica la vista de iconos. <br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="LVS_LIST"></span><span id="lvs_list"></span><dl> <dt>**lista de LVS \_**</dt> </dl>                                  | Este estilo especifica la vista de lista. <br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="LVS_NOCOLUMNHEADER"></span><span id="lvs_nocolumnheader"></span><dl> <dt>**LVS \_ NOCOLUMNHEADER**</dt> </dl>    | Los encabezados de columna no se muestran en la vista de informe. De forma predeterminada, las columnas tienen encabezados en la vista de informe. <br/>                                                                                                                                                                                                                                               |
| <span id="LVS_NOLABELWRAP"></span><span id="lvs_nolabelwrap"></span><dl> <dt>**LVS \_ NOLABELWRAP**</dt> </dl>             | El texto del elemento se muestra en una sola línea en la vista de iconos. De forma predeterminada, el texto del elemento puede ajustarse en la vista de iconos. <br/>                                                                                                                                                                                                                                              |
| <span id="LVS_NOSCROLL"></span><span id="lvs_noscroll"></span><dl> <dt>**LVS \_ NOscroll**</dt> </dl>                      | El desplazamiento está deshabilitado. Todos los elementos deben estar dentro del área cliente. Este estilo no es compatible con los estilos de **\_ Informe** **\_ lista de LVS** o LVS. Vea el artículo de Knowledge Base Q137520 para más información. <br/>                                                                                                                                      |
| <span id="LVS_NOSORTHEADER"></span><span id="lvs_nosortheader"></span><dl> <dt>**LVS \_ NOSORTHEADER**</dt> </dl>          | Los encabezados de columna no funcionan como los botones. Este estilo se puede usar si al hacer clic en un encabezado de columna en la vista de informe no se lleva a cabo una acción, como la ordenación. <br/>                                                                                                                                                                                       |
| <span id="LVS_OWNERDATA"></span><span id="lvs_ownerdata"></span><dl> <dt>**LVS \_ OWNERDATA**</dt> </dl>                   | [Versión 4,70](common-control-versions.md). Este estilo especifica un control de vista de lista virtual. Para obtener más información sobre este estilo de control de lista, vea [acerca de los controles List-View](list-view-controls-overview.md). <br/>                                                                                                                             |
| <span id="LVS_OWNERDRAWFIXED"></span><span id="lvs_ownerdrawfixed"></span><dl> <dt>**LVS \_ OWNERDRAWFIXED**</dt> </dl>    | La ventana propietaria puede pintar elementos en la vista de informe. El control de vista de lista envía un mensaje de [**WM \_ DRAWITEM**](wm-drawitem.md) para pintar cada elemento; no envía mensajes independientes para cada subelemento. El miembro **iItemData** de la estructura [**drawitemstruct (**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) contiene los datos del elemento para el elemento de vista de lista especificado. <br/> |
| <span id="LVS_REPORT"></span><span id="lvs_report"></span><dl> <dt>**\_Informe LVS**</dt> </dl>                            | Este estilo especifica la vista de informe. Cuando se usa el \_ estilo de informe LVS con un control de vista de lista, la primera columna siempre está alineada a la izquierda. No se puede usar \_ el derecho LVCFMT para cambiar esta alineación. Vea [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) para obtener más información sobre la alineación de las columnas. <br/>                                                                      |
| <span id="LVS_SHAREIMAGELISTS"></span><span id="lvs_shareimagelists"></span><dl> <dt>**LVS \_ SHAREIMAGELISTS**</dt> </dl> | La lista de imágenes no se eliminará cuando se destruya el control. Este estilo permite el uso de las mismas listas de imágenes con varios controles de vista de lista. <br/>                                                                                                                                                                                          |
| <span id="LVS_SHOWSELALWAYS"></span><span id="lvs_showselalways"></span><dl> <dt>**LVS \_ SHOWSELALWAYS**</dt> </dl>       | La selección, si la hay, se muestra siempre, incluso si el control no tiene el foco. <br/>                                                                                                                                                                                                                                                            |
| <span id="LVS_SINGLESEL"></span><span id="lvs_singlesel"></span><dl> <dt>**LVS \_ SINGLESEL**</dt> </dl>                   | Solo se puede seleccionar un elemento cada vez. De forma predeterminada, se pueden seleccionar varios elementos. <br/>                                                                                                                                                                                                                                                            |
| <span id="LVS_SMALLICON"></span><span id="lvs_smallicon"></span><dl> <dt>**LVS \_ SmallIcon**</dt> </dl>                   | Este estilo especifica la vista de iconos pequeños. <br/>                                                                                                                                                                                                                                                                                                           |
| <span id="LVS_SORTASCENDING"></span><span id="lvs_sortascending"></span><dl> <dt>**LVS \_ SORTASCENDING**</dt> </dl>       | Los índices de elementos se ordenan en función del texto del elemento en orden ascendente. <br/>                                                                                                                                                                                                                                                                                  |
| <span id="LVS_SORTDESCENDING"></span><span id="lvs_sortdescending"></span><dl> <dt>**LVS \_ SORTDESCENDING**</dt> </dl>    | Los índices de elementos se ordenan en función del texto del elemento en orden descendente. <br/>                                                                                                                                                                                                                                                                                 |
| <span id="LVS_TYPEMASK"></span><span id="lvs_typemask"></span><dl> <dt>**LVS \_ TYPEMASK**</dt> </dl>                      | Determina el estilo de ventana actual del control. <br/>                                                                                                                                                                                                                                                                                                  |
| <span id="LVS_TYPESTYLEMASK"></span><span id="lvs_typestylemask"></span><dl> <dt>**LVS \_ TYPESTYLEMASK**</dt> </dl>       | Determina los estilos de ventana que controlan la alineación y el comportamiento de los encabezados y los elementos. <br/>                                                                                                                                                                                                                                                    |



## <a name="remarks"></a>Observaciones

En el caso de los estilos **LVS \_ SORTASCENDING** y **LVS \_ SORTDESCENDING** , los índices de elementos se ordenan en función del texto del elemento en orden ascendente o descendente, respectivamente. Dado que las vistas de **\_ Informe** **\_ lista de LVS** y LVS muestran los elementos en el mismo orden que sus índices, los resultados de la ordenación son inmediatamente visibles para el usuario. El **\_ icono de LVS** y las vistas de **LVS \_ SmallIcon** no usan índices de elementos para determinar la posición de los iconos. Con esas vistas, los resultados de la ordenación no son visibles para el usuario.

Puede usar la **LVS \_ TYPEMASK** Mask para aislar los estilos de ventana que corresponden a la vista actual: **\_ icono LVS**, **\_ lista LVS**, **\_ Informe LVS** y **LVS \_ SmallIcon**.

Puede usar la **LVS \_ ALIGNMASK** Mask para aislar los estilos de ventana que especifican la alineación de los elementos: **LVS \_ ALIGNLEFT** y **LVS \_ ALIGNTOP**.

Puede usar la **LVS \_ TYPESTYLEMASK** Mask para aislar los estilos de ventana que controlan la alineación de los elementos (**LVS \_ ALIGNLEFT** y **LVS \_ ALIGNTOP**) y los que controlan el comportamiento y la apariencia del encabezado (**LVS \_ NOCOLUMNHEADER** y **LVS \_ NOSORTHEADER**).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estilos y vistas de la vista de lista](list-view-controls-overview.md)
</dt> </dl>

 

 





