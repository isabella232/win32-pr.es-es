---
title: TVN_BEGINRDRAG de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de vista de árbol el inicio de una operación de arrastrar y colocar que implica el botón derecho del mouse. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 4a61d8b5-ceb9-46a3-95ef-27e843e8c986
keywords:
- TVN_BEGINRDRAG código de notificación Windows controles
topic_type:
- apiref
api_name:
- TVN_BEGINRDRAG
- TVN_BEGINRDRAGA
- TVN_BEGINRDRAGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f7ce3fb92f39097c51cf54d707fac4341bc2a4c098b5abb0b36abcbd47f5744
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669179"
---
# <a name="tvn_beginrdrag-notification-code"></a>Código de notificación \_ DE TVN BEGINRDRAG

Notifica a la ventana primaria de un control de vista de árbol el inicio de una operación de arrastrar y colocar que implica el botón derecho del mouse. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_BEGINRDRAG 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTREEVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) El **miembro itemNew** es una [**estructura TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contiene información válida en los miembros **hItem**, **state** y **lParam** sobre el elemento que se va a arrastrar. El **miembro ptDrag** especifica las coordenadas de pantalla actuales del mouse.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TVN \_ BEGINRDRAGW** (Unicode) y **TVN \_ BEGINRDRAGA** (ANSI)<br/>             |



 

 





