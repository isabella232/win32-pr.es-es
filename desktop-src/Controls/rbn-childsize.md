---
title: RBN_CHILDSIZE de notificación (Commctrl.h)
description: Enviado por un control rebar cuando se cambia el tamaño de la ventana secundaria de una banda. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: ba64d21a-e568-4894-8007-be644ae4f54a
keywords:
- RBN_CHILDSIZE de notificación Windows controles
topic_type:
- apiref
api_name:
- RBN_CHILDSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d505d13048d96783d53b9b1a821d80712597da4f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167222"
---
# <a name="rbn_childsize-notification-code"></a>Código de notificación CHILDSIZE de RBN \_

Enviado por un control rebar cuando se cambia el tamaño de la ventana secundaria de una banda. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
RBN_CHILDSIZE

    lprbcs = (LPNMREBARCHILDSIZE) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMREBARCHILDSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchildsize) que contiene información sobre el código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para esta notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





