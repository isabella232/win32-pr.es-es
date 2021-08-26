---
title: RBN_DELETEDBAND de notificación (Commctrl.h)
description: Enviado por un control rebar después de que se haya eliminado una banda. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: ef4aca07-de08-47de-b236-321e84e6e81c
keywords:
- RBN_DELETEDBAND código de notificación Windows controles
topic_type:
- apiref
api_name:
- RBN_DELETEDBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0e60d1a8ad062d77800ccc9e2790718f5d8c8dcac2fb87a37f62b8f1131e5cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985245"
---
# <a name="rbn_deletedband-notification-code"></a>Código de notificación DELETEDBAND de RBN \_

Enviado por un control rebar después de que se haya eliminado una banda. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
RBN_DELETEDBAND

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) que contiene información sobre el código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para esta notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





