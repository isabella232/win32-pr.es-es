---
title: TCN_KEYDOWN de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de pestaña que se ha presionado una tecla. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 884e79cd-5732-44cd-8c7a-38bb9349ec7d
keywords:
- TCN_KEYDOWN de notificación Windows controles
topic_type:
- apiref
api_name:
- TCN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a1e963b11faf8f75e50e86e8c120ea0b05f0dc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166170"
---
# <a name="tcn_keydown-notification-code"></a>Código de notificación \_ DE TCN KEYDOWN

Notifica a la ventana primaria de un control de pestaña que se ha presionado una tecla. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TCN_KEYDOWN 

    pnm = (NMTCKEYDOWN*) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTCKEYDOWN.**](/windows/win32/api/commctrl/ns-commctrl-nmtckeydown)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





