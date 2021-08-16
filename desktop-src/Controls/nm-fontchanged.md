---
title: NM_FONTCHANGED de notificación (Commctrl.h)
description: Enviado por un control de vista de lista cuando el control ha cambiado una fuente. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: ffa019b0-34be-4bb3-b9dd-c267545fec84
keywords:
- NM_FONTCHANGED código de notificación Windows controles
topic_type:
- apiref
api_name:
- NM_FONTCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5369b7719a02e28562f4e71aecffdd3680aa602b6154eac9cc8685bdbe2b2b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411154"
---
# <a name="nm_fontchanged-notification-code"></a>Código \_ de notificación FONTCHANGED de NM

Enviado por un control de vista de lista cuando el control ha cambiado una fuente. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_FONTCHANGED
        
    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El control omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





