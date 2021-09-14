---
title: TVM_GETITEMRECT mensaje (Commctrl.h)
description: Recupera el rectángulo delimitador de un elemento de vista de árbol e indica si el elemento está visible. Puede enviar este mensaje explícitamente o mediante la macro TreeView \_ GetItemRect.
ms.assetid: f2d7d7b1-cfe7-4361-bd90-e3e99dbcd99c
keywords:
- TVM_GETITEMRECT controles de Windows mensaje
topic_type:
- apiref
api_name:
- TVM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebdf4d73fb83ddbd8e9e682f11ee1f5ecfbd5153
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165726"
---
# <a name="tvm_getitemrect-message"></a>Mensaje \_ GETITEMRECT de TVM

Recupera el rectángulo delimitador de un elemento de vista de árbol e indica si el elemento está visible. Puede enviar este mensaje explícitamente o mediante la macro [**TreeView \_ GetItemRect.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemrect)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que especifica la parte del elemento para el que se va a recuperar el rectángulo delimitador. Si este parámetro es **TRUE**, el rectángulo delimitador solo incluye el texto del elemento. De lo contrario, incluye toda la línea que ocupa el elemento en el control de vista de árbol.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) que, al enviar el mensaje, contiene el identificador del elemento para el que se va a recuperar el rectángulo. Vea el ejemplo siguiente para obtener más información sobre cómo colocar el identificador de elemento en este parámetro. Después de volver del mensaje, este parámetro contiene el rectángulo delimitador. Las coordenadas son relativas a la esquina superior izquierda del control de vista de árbol.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el elemento está visible y el rectángulo delimitador se recuperó correctamente, el valor devuelto es **TRUE.** De lo contrario, el mensaje **devuelve FALSE** y no recupera el rectángulo delimitador.

## <a name="remarks"></a>Observaciones

Al enviar este mensaje, el *parámetro lParam* contiene el identificador del elemento para el que se recupera el rectángulo. El identificador se coloca en *lParam* como se muestra en el ejemplo siguiente:


```
RECT rc;

*(HTREEITEM*)&rc = hTreeItem;

SendMessage(hwndTreeView, TVM_GETITEMRECT, FALSE, (LPARAM)&rc);
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

