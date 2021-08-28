---
title: HDN_ITEMCLICK de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de encabezado que el usuario hizo clic en el control. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 25ed0070-5891-4f36-9ae0-fc04e064401f
keywords:
- HDN_ITEMCLICK código de notificación Windows controles
topic_type:
- apiref
api_name:
- HDN_ITEMCLICK
- HDN_ITEMCLICKA
- HDN_ITEMCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe6bf01ed46d0294f654c21dc854933f0be04695f7edeee7a6849e23b01b027f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118006192"
---
# <a name="hdn_itemclick-notification-code"></a>Código de notificación ITEMCLICK de HDN \_

Notifica a la ventana primaria de un control de encabezado que el usuario hizo clic en el control. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
HDN_ITEMCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que identifica el control de encabezado y especifica el índice del elemento de encabezado en el que se hizo clic y el botón del mouse utilizado para hacer clic en el elemento. El **miembro pItem** se establece en **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Un control de encabezado envía este código de notificación después de que el usuario suelte el botón izquierdo del mouse.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **HDN \_ ITEMCLICKW** (Unicode) y **HDN \_ ITEMCLICKA** (ANSI)<br/>               |



 

 





