---
title: TVM_DELETEITEM mensaje (Commctrl.h)
description: Quita un elemento y todos sus elementos secundarios de un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro TreeView \_ DeleteItem.
ms.assetid: 225420a5-6ded-4786-a080-2817aa5f66c9
keywords:
- TVM_DELETEITEM controles de Windows mensaje
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
ms.openlocfilehash: 7ef0165ffaf1f0f04b32cda43e21c97fed012ad6d61b32f8919612f8924f7c66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018693"
---
# <a name="tvm_deleteitem-message"></a>Mensaje \_ DELETEITEM de TVM

Quita un elemento y todos sus elementos secundarios de un control de vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**TreeView \_ DeleteItem.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteitem)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

**Identificador HTREEITEM** para el elemento que se eliminará. Si *lParam se* establece en TVI ROOT o \_ en **NULL,** se eliminan todos los elementos. También puede usar la macro [**\_ DeleteAllItems de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems) para eliminar todos los elementos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="remarks"></a>Comentarios

No es seguro eliminar elementos en respuesta a una notificación como [TVN \_ SELCHANGING.](tvn-selchanging.md)

Una vez eliminado un elemento, su identificador no es válido y no se puede usar.

La ventana primaria recibe un [código de notificación \_ DELETEITEM de TVN](tvn-deleteitem.md) cuando se quita cada elemento.

Si se está editando la etiqueta de elemento, se cancela la operación de edición y la ventana primaria recibe el código de [notificación \_ ENDLABELEDIT de TVN.](tvn-endlabeledit.md)

Si elimina todos los elementos de un control de vista de árbol que tiene el estilo [**\_ TVS NOSCROLL,**](tree-view-control-window-styles.md) es posible que los elementos agregados posteriormente no se muestren correctamente. Para obtener más información, [**vea TreeView \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





