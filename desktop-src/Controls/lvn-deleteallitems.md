---
title: LVN_DELETEALLITEMS de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de vista de lista que todos los elementos del control están a punto de eliminarse. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: e4a219cf-4af9-4d02-8810-f576ba658177
keywords:
- LVN_DELETEALLITEMS código de notificación Windows controles
topic_type:
- apiref
api_name:
- LVN_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06f76ec4deaf67c1448fab5054c05ea8ede79c0972061c8be8e4f36b2e40ef54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019133"
---
# <a name="lvn_deleteallitems-notification-code"></a>Código de \_ notificación LVN DELETEALLITEMS

Notifica a la ventana primaria de un control de vista de lista que todos los elementos del control están a punto de eliminarse. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_DELETEALLITEMS

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMLISTVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) El **miembro iItem** es -1 y los demás miembros son cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para suprimir los códigos [de notificación \_ LVN DELETEITEM](lvn-deleteitem.md) subsiguientes, devuelva **TRUE**.

Para recibir los códigos [de notificación \_ LVN DELETEITEM](lvn-deleteitem.md) posteriores, devuelva **FALSE**.

## <a name="remarks"></a>Comentarios

Un control de vista de lista envía el código de notificación [**LVM \_ DELETEALLITEMS**](lvm-deleteallitems.md) cuando se destruye o cuando recibe el mensaje **\_ LVM DELETEALLITEMS.** Si **LVM \_ DELETEALLITEMS** no devuelve **TRUE,** el control también enviará un código de [notificación \_ LVN DELETEITEM](lvn-deleteitem.md) a medida que se elimine cada elemento.

Si el controlador de [**mensajes LVM \_ DELETEALLITEMS**](lvm-deleteallitems.md) está en un procedimiento de cuadro de diálogo, devuelva **TRUE** desde el procedimiento del cuadro de diálogo y use la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con DWL MSGRESULT para establecer el valor devuelto del \_ mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

