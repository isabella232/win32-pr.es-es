---
title: Mensaje de TVM_GETITEMRECT (commctrl. h)
description: Recupera el rectángulo delimitador de un elemento de vista de árbol e indica si el elemento está visible. Puede enviar este mensaje explícitamente o mediante la \_ macro GetItemRect de TreeView.
ms.assetid: f2d7d7b1-cfe7-4361-bd90-e3e99dbcd99c
keywords:
- TVM_GETITEMRECT controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150184"
---
# <a name="tvm_getitemrect-message"></a>\_Mensaje de GETITEMRECT TVM

Recupera el rectángulo delimitador de un elemento de vista de árbol e indica si el elemento está visible. Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetItemRect de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemrect) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que especifica la parte del elemento para la que se va a recuperar el rectángulo delimitador. Si este parámetro es **true**, el rectángulo delimitador solo incluye el texto del elemento. De lo contrario, incluye la línea completa que el elemento ocupa en el control de vista de árbol.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que, al enviar el mensaje, contiene el identificador del elemento para el que se va a recuperar el rectángulo. Vea el ejemplo siguiente para obtener más información sobre cómo colocar el identificador de elemento en este parámetro. Después de devolver el mensaje, este parámetro contiene el rectángulo delimitador. Las coordenadas son relativas a la esquina superior izquierda del control de vista de árbol.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el elemento está visible y el rectángulo delimitador se recuperó correctamente, el valor devuelto es **true**. De lo contrario, el mensaje devuelve **false** y no recupera el rectángulo delimitador.

## <a name="remarks"></a>Observaciones

Al enviar este mensaje, el parámetro *lParam* contiene el identificador del elemento para el que se recupera el rectángulo. El identificador se coloca en *lParam* tal y como se muestra en el ejemplo siguiente:


```
RECT rc;

*(HTREEITEM*)&rc = hTreeItem;

SendMessage(hwndTreeView, TVM_GETITEMRECT, FALSE, (LPARAM)&rc);
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

