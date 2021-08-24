---
title: TVM_GETNEXTITEM mensaje (Commctrl.h)
description: Recupera el elemento de vista de árbol que lleva la relación especificada a un elemento especificado. Puede enviar este mensaje explícitamente mediante la macro TreeView \_ GetNextItem.
ms.assetid: 505c713c-7728-4119-bc0e-482fe7e73193
keywords:
- TVM_GETNEXTITEM controles de Windows mensaje
topic_type:
- apiref
api_name:
- TVM_GETNEXTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84dbbd39ca347bcf1084ddfaa46c997cc5c4e5dd4d52250136a230dd834ac836
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698685"
---
# <a name="tvm_getnextitem-message"></a>Mensaje \_ GETNEXTITEM de TVM

Recupera el elemento de vista de árbol que lleva la relación especificada a un elemento especificado. Puede enviar este mensaje explícitamente mediante la macro [**TreeView \_ GetNextItem.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextitem)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Marca que especifica el elemento que se recuperará. Este parámetro puede ser uno de los siguientes valores:



| Valor                                                                                                                                                                              | Significado                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVGN_CARET"></span><span id="tvgn_caret"></span><dl> <dt>**TVGN \_ CARET**</dt> </dl>                               | Recupera el elemento seleccionado actualmente. Puede usar la macro [**TreeView \_ GetSelection**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getselection) para enviar este mensaje.<br/>                                                                                                                                                                          |
| <span id="TVGN_CHILD"></span><span id="tvgn_child"></span><dl> <dt>**TVGN \_ CHILD**</dt> </dl>                               | Recupera el primer elemento secundario del elemento especificado por el *parámetro hitem.* Puede usar la macro [**TreeView \_ GetChild**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getchild) para enviar este mensaje.<br/>                                                                                                                                          |
| <span id="TVGN_DROPHILITE"></span><span id="tvgn_drophilite"></span><dl> <dt>**TVGN \_ DROPHILITE**</dt> </dl>                | Recupera el elemento que es el destino de una operación de arrastrar y colocar. Puede usar la macro [**TreeView \_ GetDropHilight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getdrophilight) para enviar este mensaje.<br/>                                                                                                                                         |
| <span id="TVGN_FIRSTVISIBLE"></span><span id="tvgn_firstvisible"></span><dl> <dt>**TVGN \_ FIRSTVISIBLE**</dt> </dl>          | Recupera el primer elemento que está visible en la ventana de vista de árbol. Puede usar la macro [**TreeView \_ GetFirstVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getfirstvisible) para enviar este mensaje.<br/>                                                                                                                                         |
| <span id="TVGN_LASTVISIBLE"></span><span id="tvgn_lastvisible"></span><dl> <dt>**TVGN \_ LASTVISIBLE**</dt> </dl>             | [Versión 4.71.](common-control-versions.md) Recupera el último elemento expandido del árbol. Esto no recupera el último elemento visible en la ventana de vista de árbol. Puede usar la macro [**TreeView \_ GetLastVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getlastvisible) para enviar este mensaje.<br/>                                            |
| <span id="TVGN_NEXT"></span><span id="tvgn_next"></span><dl> <dt>**TVGN \_ SIGUIENTE**</dt> </dl>                                  | Recupera el siguiente elemento relacionado. Puede usar la macro [**TreeView \_ GetNextSibling**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextsibling) para enviar este mensaje.<br/>                                                                                                                                                                            |
| <span id="TVGN_NEXTSELECTED"></span><span id="tvgn_nextselected"></span><dl> <dt>**TVGN \_ NEXTSELECTED**</dt> </dl>          | **Windows Vista y versiones posteriores.** Recupera el siguiente elemento seleccionado. Puede usar la macro [**TreeView \_ GetNextSelected**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextselected) para enviar este mensaje.<br/>                                                                                                                                            |
| <span id="TVGN_NEXTVISIBLE"></span><span id="tvgn_nextvisible"></span><dl> <dt>**TVGN \_ NEXTVISIBLE**</dt> </dl>             | Recupera el siguiente elemento visible que sigue al elemento especificado. El elemento especificado debe estar visible. Use el [**mensaje \_ GETITEMRECT de TVM**](tvm-getitemrect.md) para determinar si un elemento está visible. Puede usar la macro [**TreeView \_ GetNextVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextvisible) para enviar este mensaje.<br/>   |
| <span id="TVGN_PARENT"></span><span id="tvgn_parent"></span><dl> <dt>**TVGN \_ PRIMARIO**</dt> </dl>                            | Recupera el elemento primario del elemento especificado. Puede usar la macro [**TreeView \_ GetParent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getparent) para enviar este mensaje.<br/>                                                                                                                                                                           |
| <span id="TVGN_PREVIOUS"></span><span id="tvgn_previous"></span><dl> <dt>**TVGN \_ ANTERIOR**</dt> </dl>                      | Recupera el elemento relacionado anterior. Puede usar la macro [**TreeView \_ GetPrevSibling**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevsibling) para enviar este mensaje.<br/>                                                                                                                                                                        |
| <span id="TVGN_PREVIOUSVISIBLE"></span><span id="tvgn_previousvisible"></span><dl> <dt>**TVGN \_ PREVIOUSVISIBLE**</dt> </dl> | Recupera el primer elemento visible que precede al elemento especificado. El elemento especificado debe estar visible. Use el [**mensaje \_ GETITEMRECT de TVM**](tvm-getitemrect.md) para determinar si un elemento está visible. Puede usar la macro [**TreeView \_ GetPrevVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevvisible) para enviar este mensaje.<br/> |
| <span id="TVGN_ROOT"></span><span id="tvgn_root"></span><dl> <dt>**RAÍZ DE \_ TVGN**</dt> </dl>                                  | Recupera el elemento superior o el primer elemento del control de vista de árbol. Puede usar la macro [**TreeView \_ GetRoot**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getroot) para enviar este mensaje. <br/>                                                                                                                                                       |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de un elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador al elemento si se realiza correctamente. En la mayoría de los casos, el mensaje devuelve **un valor NULL** para indicar un error. Para obtener información detallada, consulte la sección Comentarios.

## <a name="remarks"></a>Comentarios

Este mensaje devolverá **NULL si** el elemento que se recupera es el nodo raíz del árbol. Por ejemplo, si usa este mensaje con la marca TVGN PARENT en un elemento secundario de primer nivel del nodo raíz de la vista de árbol, el mensaje devolverá \_ **NULL.**

También puede usar una de estas macros relacionadas:



|                                                               |
|---------------------------------------------------------------|
| [**TreeView \_ GetChild**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getchild)               |
| [**TreeView \_ GetDropHilight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getdrophilight)   |
| [**TreeView \_ GetFirstVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getfirstvisible) |
| [**TreeView \_ GetLastVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getlastvisible)   |
| [**TreeView \_ GetNextSibling**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextsibling)   |
| [**TreeView \_ GetNextVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextvisible)   |
| [**TreeView \_ GetParent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getparent)             |
| [**TreeView \_ GetPrevSibling**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevsibling)   |
| [**TreeView \_ GetPrevVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevvisible)   |
| [**TreeView \_ GetRoot**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getroot)                 |
| [**TreeView \_ GetSelection**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getselection)       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





