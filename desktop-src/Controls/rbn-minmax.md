---
title: RBN_MINMAX de notificación (Commctrl.h)
description: Enviado por un control rebar antes de maximizar o minimizar una banda. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 75619cb0-ef0b-44fa-83b2-15a5e5e92c60
keywords:
- RBN_MINMAX código de notificación Windows controles
topic_type:
- apiref
api_name:
- RBN_MINMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d18fea875af376b3ec9b311d2aad09597f0ce6ea264963e9e466cc87ce4fe4b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984995"
---
# <a name="rbn_minmax-notification-code"></a>Código de notificación MINMAX de RBN \_

Enviado por un control rebar antes de maximizar o minimizar una banda. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
RBN_MINMAX
```



## <a name="parameters"></a>Parámetros

Este código de notificación no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero para evitar que se haga la operación, cero para permitir que continúe.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





