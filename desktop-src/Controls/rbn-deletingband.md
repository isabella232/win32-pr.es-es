---
title: RBN_DELETINGBAND de notificación (Commctrl.h)
description: Enviado por un control rebar cuando una banda está a punto de eliminarse. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 92840cb1-375e-4c37-bde4-7ba02a1ff4f1
keywords:
- RBN_DELETINGBAND código de notificación Windows controles
topic_type:
- apiref
api_name:
- RBN_DELETINGBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf810fd8800d7774a0dbf9a65cdf08c2d53d92ba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167218"
---
# <a name="rbn_deletingband-notification-code"></a>Código de notificación \_ DE RBN DELETINGBAND

Enviado por un control rebar cuando una banda está a punto de eliminarse. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
RBN_DELETINGBAND

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
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





