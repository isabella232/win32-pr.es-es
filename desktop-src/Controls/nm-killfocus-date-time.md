---
title: NM_KILLFOCUS de notificación (fecha y hora) (Commctrl.h)
description: Notifica a la ventana primaria de un control selector de fecha y hora que el control ha perdido el foco de entrada. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 33d6b88b-9608-4227-a822-1dc7a77d3a3f
keywords:
- NM_KILLFOCUS (fecha y hora) del código de notificación Windows controles
topic_type:
- apiref
api_name:
- NM_KILLFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a0147fd5d79998024df8c12d9be4a9a71ee3c1751a3f31d21d090ea2c7e9a92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018843"
---
# <a name="nm_killfocus-date-time-notification-code"></a>Código \_ de notificación DE NM KILLFOCUS (fecha y hora)

Notifica a la ventana primaria de un control selector de fecha y hora que el control ha perdido el foco de entrada. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_KILLFOCUS

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Dirección de una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





