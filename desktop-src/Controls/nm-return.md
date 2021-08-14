---
title: NM_RETURN de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control que el control tiene el foco de entrada y que el usuario ha presionado la tecla ENTRAR. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 2c4839bc-6b23-469b-978f-cdf5f7bc0549
keywords:
- NM_RETURN código de notificación Windows controles
topic_type:
- apiref
api_name:
- NM_RETURN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5bc3104f87c6b0adf8c9ce486b62dc42ecd5e4a0fff6c407ce93bec9a3c8f90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118410535"
---
# <a name="nm_return-notification-code"></a>Código de \_ notificación NM RETURN

Notifica a la ventana primaria de un control que el control tiene el foco de entrada y que el usuario ha presionado la tecla ENTRAR. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_RETURN 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El control omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





