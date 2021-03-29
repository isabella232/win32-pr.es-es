---
title: Mensaje de LVM_SETITEMTEXT (commctrl. h)
description: Cambia el texto de un elemento o subelemento de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro SetItemText de ListView.
ms.assetid: 1a9c7e4d-78e0-44c7-bf4f-d0fc7a0049f3
keywords:
- LVM_SETITEMTEXT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETITEMTEXT
- LVM_SETITEMTEXTA
- LVM_SETITEMTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d326e48047325fc9aff2c6607da6d7d377965adf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905290"
---
# <a name="lvm_setitemtext-message"></a>\_Mensaje SETITEMTEXT LVM

Cambia el texto de un elemento o subelemento de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetItemText de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero del elemento de vista de lista.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) . El miembro **iSubItem** es el índice del subelemento, o puede ser cero para establecer la etiqueta del elemento. El miembro **miembros pszText** es la dirección de una cadena terminada en null que contiene el nuevo texto. también puede ser **null**. El miembro **miembros pszText** también puede ser LPSTR \_ TEXTCALLBACK para indicar un elemento de devolución de llamada para el que la ventana primaria almacena el texto. En este caso, el control de vista de lista envía el elemento primario a un código de notificación [**LVN \_ GETDISPINFO**](lvn-getdispinfo.md) cuando necesita el texto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si envía este mensaje explícitamente, devuelve **true** si es correcto o **false** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVM \_ SETITEMTEXTW** (Unicode) y **\_ SETITEMTEXTA de LVM** (ANSI)<br/>           |



 

 





