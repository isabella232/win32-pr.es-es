---
title: RBN_BEGINDRAG de notificación (Commctrl.h)
description: Enviado por un control rebar cuando el usuario comienza a arrastrar una banda. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: e1565b31-7694-43cc-87ee-c9294a0612cd
keywords:
- RBN_BEGINDRAG código de notificación Windows controles
topic_type:
- apiref
api_name:
- RBN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c797e026484b32e68408cf720a1d4681d066c5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167241"
---
# <a name="rbn_begindrag-notification-code"></a>Código de notificación \_ BEGINDRAG de RBN

Enviado por un control rebar cuando el usuario comienza a arrastrar una banda. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
RBN_BEGINDRAG

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) que contiene información sobre el código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero para permitir que la barra de rebar continúe con la operación de arrastre o distinto de cero para anular la operación de arrastre.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





