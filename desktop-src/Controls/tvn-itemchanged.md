---
title: TVN_ITEMCHANGED de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de vista de árbol que los atributos de elemento han cambiado. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: b09164bc-54da-457a-9fb7-3beab3dae3e4
keywords:
- TVN_ITEMCHANGED código de notificación Windows controles
topic_type:
- apiref
api_name:
- TVN_ITEMCHANGED
- TVN_ITEMCHANGEDA
- TVN_ITEMCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d140346d66a87bd394bc5aa36555b8accedef56891e722a4b28272e22f804ed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018653"
---
# <a name="tvn_itemchanged-notification-code"></a>Código de notificación ITEMCHANGED de TVN \_

Notifica a la ventana primaria de un control de vista de árbol que los atributos de elemento han cambiado. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_ITEMCHANGED
        
    pnm = (NMTVITEMCHANGE *) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) que describe el elemento que ha cambiado. El **miembro uChanged** se establece en TVIF \_ STATE.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **FALSE** para aceptar el cambio o **TRUE** para evitar el cambio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TVN \_ ITEMCHANGEDW** (Unicode) y **TVN \_ ITEMCHANGEDA** (ANSI)<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[TVN \_ ITEMCHANGING](tvn-itemchanging.md)
</dt> </dl>

 

 





