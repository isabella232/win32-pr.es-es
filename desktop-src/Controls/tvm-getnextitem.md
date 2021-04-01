---
title: Mensaje de TVM_GETNEXTITEM (commctrl. h)
description: Recupera el elemento de vista de árbol que lleva la relación especificada a un elemento especificado. Puede enviar este mensaje explícitamente mediante la \_ macro GetNextItem de TreeView.
ms.assetid: 505c713c-7728-4119-bc0e-482fe7e73193
keywords:
- TVM_GETNEXTITEM controles de mensajes de Windows
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
ms.openlocfilehash: 3099af5e9abcd3e9c144cfc615a12dd2acb0332b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150059"
---
# <a name="tvm_getnextitem-message"></a>\_Mensaje de GETNEXTITEM TVM

Recupera el elemento de vista de árbol que lleva la relación especificada a un elemento especificado. Puede enviar este mensaje explícitamente mediante la macro [**\_ GetNextItem de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextitem) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Marca que especifica el elemento que se va a recuperar. Este parámetro puede ser uno de los siguientes valores:



| Value                                                                                                                                                                              | Significado                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVGN_CARET"></span><span id="tvgn_caret"></span><dl> <dt>**\_símbolo de intercalación de TVGN**</dt> </dl>                               | Recupera el elemento actualmente seleccionado. Puede usar la macro [**\_ getSelection de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getselection) para enviar este mensaje.<br/>                                                                                                                                                                          |
| <span id="TVGN_CHILD"></span><span id="tvgn_child"></span><dl> <dt>**\_secundario TVGN**</dt> </dl>                               | Recupera el primer elemento secundario del elemento especificado por el parámetro *hitem* . Puede usar la macro [**\_ GetChild de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getchild) para enviar este mensaje.<br/>                                                                                                                                          |
| <span id="TVGN_DROPHILITE"></span><span id="tvgn_drophilite"></span><dl> <dt>**TVGN \_ DROPHILITE**</dt> </dl>                | Recupera el elemento que es el destino de una operación de arrastrar y colocar. Puede usar la macro [**\_ GetDropHilight de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getdrophilight) para enviar este mensaje.<br/>                                                                                                                                         |
| <span id="TVGN_FIRSTVISIBLE"></span><span id="tvgn_firstvisible"></span><dl> <dt>**TVGN \_ FIRSTVISIBLE**</dt> </dl>          | Recupera el primer elemento que está visible en la ventana de vista de árbol. Puede usar la macro [**\_ GetFirstVisible de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getfirstvisible) para enviar este mensaje.<br/>                                                                                                                                         |
| <span id="TVGN_LASTVISIBLE"></span><span id="tvgn_lastvisible"></span><dl> <dt>**TVGN \_ LASTVISIBLE**</dt> </dl>             | [Versión 4,71](common-control-versions.md). Recupera el último elemento expandido en el árbol. Esto no recupera el último elemento visible en la ventana de vista de árbol. Puede usar la macro [**\_ GetLastVisible de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getlastvisible) para enviar este mensaje.<br/>                                            |
| <span id="TVGN_NEXT"></span><span id="tvgn_next"></span><dl> <dt>**TVGN \_ siguiente**</dt> </dl>                                  | Recupera el siguiente elemento relacionado. Puede usar la macro [**\_ GetNextSibling de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextsibling) para enviar este mensaje.<br/>                                                                                                                                                                            |
| <span id="TVGN_NEXTSELECTED"></span><span id="tvgn_nextselected"></span><dl> <dt>**TVGN \_ NEXTSELECTED**</dt> </dl>          | **Windows Vista y versiones posteriores.** Recupera el siguiente elemento seleccionado. Puede usar la macro [**\_ GetNextSelected de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextselected) para enviar este mensaje.<br/>                                                                                                                                            |
| <span id="TVGN_NEXTVISIBLE"></span><span id="tvgn_nextvisible"></span><dl> <dt>**TVGN \_ NEXTVISIBLE**</dt> </dl>             | Recupera el siguiente elemento visible que sigue al elemento especificado. El elemento especificado debe estar visible. Use el mensaje [**TVM \_ GETITEMRECT**](tvm-getitemrect.md) para determinar si un elemento está visible. Puede usar la macro [**\_ GetNextVisible de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextvisible) para enviar este mensaje.<br/>   |
| <span id="TVGN_PARENT"></span><span id="tvgn_parent"></span><dl> <dt>**\_primario TVGN**</dt> </dl>                            | Recupera el elemento primario del elemento especificado. Puede usar la macro de [**TreeView \_ GetParent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getparent) para enviar este mensaje.<br/>                                                                                                                                                                           |
| <span id="TVGN_PREVIOUS"></span><span id="tvgn_previous"></span><dl> <dt>**TVGN \_ anterior**</dt> </dl>                      | Recupera el elemento relacionado anterior. Puede usar la macro [**\_ GetPrevSibling de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevsibling) para enviar este mensaje.<br/>                                                                                                                                                                        |
| <span id="TVGN_PREVIOUSVISIBLE"></span><span id="tvgn_previousvisible"></span><dl> <dt>**TVGN \_ PREVIOUSVISIBLE**</dt> </dl> | Recupera el primer elemento visible que precede al elemento especificado. El elemento especificado debe estar visible. Use el mensaje [**TVM \_ GETITEMRECT**](tvm-getitemrect.md) para determinar si un elemento está visible. Puede usar la macro [**\_ GetPrevVisible de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevvisible) para enviar este mensaje.<br/> |
| <span id="TVGN_ROOT"></span><span id="tvgn_root"></span><dl> <dt>**\_raíz TVGN**</dt> </dl>                                  | Recupera el elemento superior o el primer elemento del control de vista de árbol. Puede usar la macro [**\_ GetRoot de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getroot) para enviar este mensaje. <br/>                                                                                                                                                       |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de un elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador del elemento si se realiza correctamente. En la mayoría de los casos, el mensaje devuelve un valor **null** para indicar un error. Para obtener información detallada, consulte la sección Comentarios.

## <a name="remarks"></a>Observaciones

Este mensaje devolverá **null** si el elemento que se va a recuperar es el nodo raíz del árbol. Por ejemplo, si usa este mensaje con la \_ marca primaria TVGN en un elemento secundario de primer nivel del nodo raíz de la vista de árbol, el mensaje devolverá **null**.

También puede usar una de estas macros relacionadas:



|                                                               |
|---------------------------------------------------------------|
| [**GetChild de TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getchild)               |
| [**GetDropHilight de TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getdrophilight)   |
| [**GetFirstVisible de TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getfirstvisible) |
| [**GetLastVisible de TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getlastvisible)   |
| [**GetNextSibling de TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextsibling)   |
| [**GetNextVisible de TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextvisible)   |
| [**TreeView \_ GetParent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getparent)             |
| [**GetPrevSibling de TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevsibling)   |
| [**GetPrevVisible de TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevvisible)   |
| [**GetRoot de TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getroot)                 |
| [**GetSelection de TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getselection)       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





