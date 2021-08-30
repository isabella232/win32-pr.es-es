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
ms.openlocfilehash: 53089c9bae4924c03f7069fad9c4cbde5d9c600777627297004f132c6a9cac33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985355"
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
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





