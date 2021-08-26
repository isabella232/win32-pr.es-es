---
title: RBN_SPLITTERDRAG de notificación (Commctrl.h)
description: Enviado por un control rebar cuando el usuario arrastra un divisor. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 7827c971-6a92-452f-b961-1abe6ae66d2a
keywords:
- RBN_SPLITTERDRAG código de notificación Windows controles
topic_type:
- apiref
api_name:
- RBN_SPLITTERDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3de913b5815acbdf8b0a98d8131d0a6f071f157fd5bb78040422b6892d7fe09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984945"
---
# <a name="rbn_splitterdrag-notification-code"></a>Código de notificación \_ SPLITTERDRAG de RBN

Enviado por un control rebar cuando el usuario arrastra un divisor. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
RBN_SPLITTERDRAG

    lpnmrbspltr = (LPNMREBARSPLITTER) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMREBARSPLITTER**](/windows/win32/api/commctrl/ns-commctrl-nmrebarsplitter) que contiene información sobre el código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para esta notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





