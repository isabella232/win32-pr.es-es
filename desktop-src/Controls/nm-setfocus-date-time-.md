---
title: NM_SETFOCUS de notificación (fecha y hora) (Commctrl.h)
description: Notifica a la ventana primaria de un control selector de fecha y hora que el control ha recibido el foco de entrada. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 61c62fb2-bc79-404b-9958-7208d1c781fa
keywords:
- NM_SETFOCUS (fecha y hora) de notificación de Windows Controles
topic_type:
- apiref
api_name:
- NM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a10283f2dee05c7babf94ef8bee4c2cf01fe256d24bbea2cd3e54d0afb15f1d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119261535"
---
# <a name="nm_setfocus-date-time-notification-code"></a>Código de notificación DE NM \_ SETFOCUS (fecha y hora)

Notifica a la ventana primaria de un control selector de fecha y hora que el control ha recibido el foco de entrada. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_SETFOCUS 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





