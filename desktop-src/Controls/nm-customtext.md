---
title: NM_CUSTOMTEXT de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control las operaciones de texto personalizadas. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: b4bde648-3479-4fac-ad32-b34c7272c1fc
keywords:
- NM_CUSTOMTEXT código de notificación Windows controles
topic_type:
- apiref
api_name:
- NM_CUSTOMTEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 512ccb6cd94ce680b9832c342696941d98c0e6543c319caeb89eb409de1fe73c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018883"
---
# <a name="nm_customtext-notification-code"></a>Código de notificación DE NM \_ CUSTOMTEXT

Notifica a la ventana primaria de un control las operaciones de texto personalizadas. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_CUSTOMTEXT

    lpnmct = (NMCUSTOMTEXT) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMCUSTOMTEXT**](/windows/win32/api/commctrl/ns-commctrl-nmcustomtext) que contiene información adicional sobre esta notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El control omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





