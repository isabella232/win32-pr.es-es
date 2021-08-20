---
title: SBN_SIMPLEMODECHANGE de notificación (Commctrl.h)
description: Enviado por un control de barra de estado cuando cambia el modo simple debido a un mensaje \_ SIMPLE de SB. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: b2df8feb-5028-4488-a99b-4ceff5b48a92
keywords:
- SBN_SIMPLEMODECHANGE código de notificación Windows controles
topic_type:
- apiref
api_name:
- SBN_SIMPLEMODECHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 813158c851e628a60a081a4a3eef90abb2eceac1a64fd81c33a75375229681da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408861"
---
# <a name="sbn_simplemodechange-notification-code"></a>Código de notificación \_ SIMPLEMODECHANGE de SBN

Enviado por un control de barra de estado cuando cambia el modo simple debido a un [**mensaje \_ SIMPLE de SB.**](sb-simple.md) Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
SBN_SIMPLEMODECHANGE

    lpnmh = (NMHDR*) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información sobre el código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La barra de estado omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





