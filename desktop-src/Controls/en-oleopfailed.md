---
title: EN_OLEOPFAILED de notificación (Richedit.h)
description: Notifica a la ventana primaria de un control de edición enriquecido que una acción del usuario en un objeto del Modelo de objetos componentes (COM) ha dado error. Un control de edición enriquecido envía este código de notificación en forma de mensaje WM \_ NOTIFY.
ms.assetid: b674c36f-2454-473e-8e1c-368c0afd8c34
keywords:
- EN_OLEOPFAILED código de notificación Windows controles
topic_type:
- apiref
api_name:
- EN_OLEOPFAILED
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0391bfc61ff9350758ac81ff6f54fb1cff61d0dd1ebbcb2b8ef02ada9fe3fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436685"
---
# <a name="en_oleopfailed-notification-code"></a>Código de notificación DE EN \_ OLEOPFAILED

Notifica a la ventana primaria de un control de edición enriquecido que una acción del usuario en un objeto del Modelo de objetos componentes (COM) ha dado error. Un control de edición enriquecido envía este código de notificación en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
EN_OLEOPFAILED

    penOleOpFailed = (ENOLEOPFAILED *) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Estructura [**ENOLEOPFAILED**](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed) que contiene información sobre el error.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este código de notificación devuelve cero.

## <a name="remarks"></a>Comentarios

La ventana primaria siempre recibirá un mensaje [**WM \_ NOTIFY**](wm-notify.md) para este evento, no requiere una máscara de notificación enviada con [**EM \_ SETEVENTMASK**](em-seteventmask.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**ENOLEOPFAILED**](/windows/desktop/api/Richedit/ns-richedit-enoleopfailed)
</dt> </dl>

 

 





