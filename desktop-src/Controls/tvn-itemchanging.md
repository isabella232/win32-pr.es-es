---
title: TVN_ITEMCHANGING de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de vista de árbol que los atributos de elemento están a punto de cambiar. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: c997871c-8eca-46c0-999d-2f6d7e3e6c96
keywords:
- TVN_ITEMCHANGING código de notificación Windows controles
topic_type:
- apiref
api_name:
- TVN_ITEMCHANGING
- TVN_ITEMCHANGINGA
- TVN_ITEMCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85416e22562720455da3e3c03c95b3cee25b5f0f7420a31250b244f47dab0caa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957874"
---
# <a name="tvn_itemchanging-notification-code"></a>Código de notificación \_ DE TVN ITEMCHANGING

Notifica a la ventana primaria de un control de vista de árbol que los atributos de elemento están a punto de cambiar. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_ITEMCHANGING
        
    pnm = (NMTVITEMCHANGE *) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) que describe el elemento que está cambiando. El **miembro uChanged** se establece en TVIF \_ STATE.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **FALSE** para aceptar el cambio o **TRUE** para evitar el cambio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TVN \_ ITEMCHANGINGW** (Unicode) y **TVN \_ ITEMCHANGINGA** (ANSI)<br/>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ELEMENTO \_ DE TVNCHANGED](tvn-itemchanged.md)
</dt> </dl>

 

 





