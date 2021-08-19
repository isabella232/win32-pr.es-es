---
title: LVM_GETITEMTEXT mensaje (Commctrl.h)
description: Recupera el texto de un elemento de vista de lista o un subelemento. Puede enviar este mensaje explícitamente o mediante la macro ListView \_ GetItemText.
ms.assetid: 5711ed18-a766-4e7f-9e9d-b9203231b369
keywords:
- LVM_GETITEMTEXT controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETITEMTEXT
- LVM_GETITEMTEXTA
- LVM_GETITEMTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32d5292f9814b3ef62667d44582eab44a2f18ac6c274682d180dd26f1b7cdd9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062585"
---
# <a name="lvm_getitemtext-message"></a>Mensaje \_ GETITEMTEXT de LVM

Recupera el texto de un elemento de vista de lista o un subelemento. Puede enviar este mensaje explícitamente o mediante la macro [**ListView \_ GetItemText.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento list-view.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura LVITEM.**](/windows/win32/api/commctrl/ns-commctrl-lvitema) Para recuperar el texto del elemento, establezca **iSubItem** en cero. Para recuperar el texto de un subelemento, establezca **iSubItem** en el índice del subelemento. El **miembro pszText** apunta a un búfer que recibe el texto. El **miembro cchTextMax** especifica el número de caracteres del búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si envía este mensaje explícitamente, devuelve el número de caracteres del **miembro pszText** de la [**estructura LVITEM.**](/windows/win32/api/commctrl/ns-commctrl-lvitema)

## <a name="remarks"></a>Comentarios

También puede enviar este mensaje llamando a la macro [**ListView \_ GetItemText.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) Sin embargo, esta macro no devuelve la longitud de la cadena.

**LVM \_ GETITEMTEXT no** se admite en el [**estilo \_ OWNERDATA de LVS.**](list-view-window-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVM \_ GETITEMTEXTW** (Unicode) y **LVM \_ GETITEMTEXTA** (ANSI)<br/>           |



 

 





