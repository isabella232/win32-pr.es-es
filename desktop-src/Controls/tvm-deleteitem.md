---
title: Mensaje de TVM_DELETEITEM (commctrl. h)
description: Quita un elemento y todos sus elementos secundarios de un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro DeleteItem de TreeView.
ms.assetid: 225420a5-6ded-4786-a080-2817aa5f66c9
keywords:
- TVM_DELETEITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8783fd5acdf7319699cdc67cbb3ea075e4dbbc28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490846"
---
# <a name="tvm_deleteitem-message"></a>Mensaje de TVM \_ DELETEITEM

Quita un elemento y todos sus elementos secundarios de un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**\_ DeleteItem de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteitem) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de **HTREEITEM** del elemento que se va a eliminar. Si *lParam* se establece en TVI \_ root o en **null**, se eliminan todos los elementos. También puede usar la macro [**\_ DeleteAllItems de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems) para eliminar todos los elementos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

No es seguro eliminar elementos en respuesta a una notificación como [TVN \_ SELCHANGING](tvn-selchanging.md).

Una vez que se elimina un elemento, su identificador no es válido y no se puede usar.

La ventana primaria recibe un código de notificación [TVN \_ DELETEITEM](tvn-deleteitem.md) cuando se quita cada elemento.

Si se está editando la etiqueta del elemento, la operación de edición se cancela y la ventana primaria recibe el código de notificación [TVN \_ ENDLABELEDIT](tvn-endlabeledit.md) .

Si elimina todos los elementos de un control de vista de árbol que tenga el estilo de [**\_ desplazamientos de los televisores**](tree-view-control-window-styles.md) , es posible que los elementos agregados posteriormente no se muestren correctamente. Para obtener más información, vea [**TreeView \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





