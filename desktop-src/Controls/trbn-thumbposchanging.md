---
title: TRBN_THUMBPOSCHANGING de notificación (Commctrl.h)
description: Notifica que la posición del control en una barra de seguimiento está cambiando. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 0876e026-bc07-409d-b174-b97ed704fc11
keywords:
- TRBN_THUMBPOSCHANGING código de notificación Windows controles
topic_type:
- apiref
api_name:
- TRBN_THUMBPOSCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48f05f67eb20c78f764957e73d2293d32e88f25a73d44d6b58f9a1c310b8d9d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751045"
---
# <a name="trbn_thumbposchanging-notification-code"></a>Código de notificación \_ THUMBPOSCHANGING de TRBN

Notifica que la posición del control en una barra de seguimiento está cambiando. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TRBN_THUMBPOSCHANGING

    lpNMTrbThumbPosChanging = (NMTRBTHUMBPOSCHANGING*) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTRBTHUMBPOSCHANGING.**](/windows/win32/api/commctrl/ns-commctrl-nmtrbthumbposchanging) El autor de la llamada es responsable de asignar esta estructura y establecer sus miembros, incluidos los miembros de la estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** para evitar que el control de posición se mueva a la posición especificada.

## <a name="remarks"></a>Comentarios

Envíe esta notificación a los clientes que no escuchan mensajes [**\_ WM HSCROLL**](wm-hscroll.md) [**o WM \_ VSCROLL.**](wm-vscroll.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





