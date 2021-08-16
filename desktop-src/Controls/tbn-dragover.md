---
title: TBN_DRAGOVER de notificación (Commctrl.h)
description: Determina si se debe enviar un mensaje MARKBUTTON de \_ TB para un botón que se está arrastrando. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 2bb5c52e-0c90-4662-8ffd-045ecc7ed7e5
keywords:
- TBN_DRAGOVER código de notificación Windows controles
topic_type:
- apiref
api_name:
- TBN_DRAGOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 718a51f14f096edbd8df72b0c5fc33ca65ec0c303a095f108981482c9fb3cda5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829349"
---
# <a name="tbn_dragover-notification-code"></a>Código de notificación DRAGOVER de TBN \_

Determina si se debe [**enviar un \_ mensaje MARKBUTTON**](tb-markbutton.md) de TB para un botón que se está arrastrando. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_DRAGOVER

    lpnmtb = (NMTBHOTITEM*) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) que especifica qué elemento se está arrastrando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**FALSE** si la barra de herramientas debe enviar un mensaje \_ MARKBUTTON de TB; de lo **contrario, TRUE.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





