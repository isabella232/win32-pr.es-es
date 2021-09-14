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
ms.openlocfilehash: ca49cd4fd77425f202c5d8ee06cb0b3d7712e610
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061935"
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

## <a name="remarks"></a>Observaciones

Un control de encabezado envía este código de notificación después de que el usuario suelte el botón izquierdo del mouse.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **HDN \_ ITEMCLICKW** (Unicode) y **HDN \_ ITEMCLICKA** (ANSI)<br/>               |



 

 





