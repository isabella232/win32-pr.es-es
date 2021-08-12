---
title: LVM_SETITEMTEXT mensaje (Commctrl.h)
description: Cambia el texto de un elemento de vista de lista o un subelemento. Puede enviar este mensaje explícitamente o mediante la macro \_ ListView SetItemText.
ms.assetid: 1a9c7e4d-78e0-44c7-bf4f-d0fc7a0049f3
keywords:
- LVM_SETITEMTEXT mensaje Controles de Windows
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
ms.openlocfilehash: 14eb5ddcff18a84f93febb22ef6661d8871df9b5578cc79f071b6e51b557c87b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670878"
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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows \[ Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVM \_ SETITEMTEXTW** (Unicode) y **LVM \_ SETITEMTEXTA** (ANSI)<br/>           |



 

 





