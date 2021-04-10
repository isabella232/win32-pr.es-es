---
title: Mensaje de LVM_GETITEMTEXT (commctrl. h)
description: Recupera el texto de un elemento o subelemento de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro GetItemText de ListView.
ms.assetid: 5711ed18-a766-4e7f-9e9d-b9203231b369
keywords:
- LVM_GETITEMTEXT controles de mensajes de Windows
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
ms.openlocfilehash: c71eec6b9dab4c649b11da5b24568eea816774ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150893"
---
# <a name="lvm_getitemtext-message"></a>\_Mensaje GETITEMTEXT LVM

Recupera el texto de un elemento o subelemento de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetItemText de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento de vista de lista.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) . Para recuperar el texto del elemento, establezca **iSubItem** en cero. Para recuperar el texto de un subelemento, establezca **iSubItem** en el índice del subelemento. El miembro **miembros pszText** apunta a un búfer que recibe el texto. El miembro **cchTextMax** especifica el número de caracteres del búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si envía este mensaje explícitamente, devuelve el número de caracteres en el miembro **miembros pszText** de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .

## <a name="remarks"></a>Observaciones

También puede enviar este mensaje mediante una llamada a la macro [**\_ GetItemText de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) . Sin embargo, esta macro no devuelve la longitud de la cadena.

**LVM \_ GETITEMTEXT** no se admite en el estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVM \_ GETITEMTEXTW** (Unicode) y **\_ GETITEMTEXTA de LVM** (ANSI)<br/>           |



 

 





