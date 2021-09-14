---
title: LVM_SETITEMTEXT mensaje (Commctrl.h)
description: Cambia el texto de un elemento de vista de lista o un subelemento. Puede enviar este mensaje explícitamente o mediante la macro \_ ListView SetItemText.
ms.assetid: 1a9c7e4d-78e0-44c7-bf4f-d0fc7a0049f3
keywords:
- LVM_SETITEMTEXT controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362678"
---
# <a name="lvm_setitemtext-message"></a>Mensaje \_ SETITEMTEXT de LVM

Cambia el texto de un elemento de vista de lista o un subelemento. Puede enviar este mensaje explícitamente o mediante la macro [**\_ ListView SetItemText.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero del elemento de vista de lista.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura LVITEM.**](/windows/win32/api/commctrl/ns-commctrl-lvitema) El **miembro iSubItem** es el índice del subelemento o puede ser cero para establecer la etiqueta del elemento. El **miembro pszText** es la dirección de una cadena terminada en NULL que contiene el nuevo texto; también puede ser **NULL.** El **miembro pszText** también puede ser LPSTR TEXTCALLBACK para indicar un elemento de devolución de llamada para el que la \_ ventana primaria almacena el texto. En este caso, el control list-view envía al elemento primario un código de [**notificación \_ LVN GETDISPINFO**](lvn-getdispinfo.md) cuando necesita el texto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si envía este mensaje explícitamente, devuelve **TRUE** si se realiza correctamente o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVM \_ SETITEMTEXTW** (Unicode) y **LVM \_ SETITEMTEXTA** (ANSI)<br/>           |



 

 





