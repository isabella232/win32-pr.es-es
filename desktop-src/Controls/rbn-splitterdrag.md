---
title: RBN_SPLITTERDRAG de notificación (Commctrl.h)
description: Enviado por un control rebar cuando el usuario arrastra un divisor. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 7827c971-6a92-452f-b961-1abe6ae66d2a
keywords:
- RBN_SPLITTERDRAG de notificación de Windows controles
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
ms.openlocfilehash: fe0b2d3fc00433be9cd3011f2f2b24d515b8cbd0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167201"
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
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





