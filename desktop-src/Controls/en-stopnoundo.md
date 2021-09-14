---
title: EN_STOPNOUNDO de notificación (Richedit.h)
description: Notifica a la ventana primaria de un control de edición enriquecido que se ha producido una acción para la que el control no puede asignar suficiente memoria para mantener el estado de deshacer. Un control de edición enriquecido envía este código de notificación en forma de mensaje WM \_ NOTIFY.
ms.assetid: 5608f6dd-83dc-4712-b485-dd9bc17dea24
keywords:
- EN_STOPNOUNDO de notificación Windows controles
topic_type:
- apiref
api_name:
- EN_STOPNOUNDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab71e6e1a78c468e6349fc1f42d03e9b68fb043
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062016"
---
# <a name="en_stopnoundo-notification-code"></a>Código de notificación DE EN \_ STOPNOUNDO

Notifica a la ventana primaria de un control de edición enriquecido que se ha producido una acción para la que el control no puede asignar suficiente memoria para mantener el estado de deshacer. Un control de edición enriquecido envía este código de notificación en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
EN_STOPNOUNDO

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Estructura [**NMHDR.**](/windows/desktop/api/richedit/ns-richedit-nmhdr)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero para continuar con la **operación de deshacer.**

Devuelve un valor distinto de cero para detener la **operación de deshacer.**

## <a name="remarks"></a>Observaciones

La ventana primaria siempre recibirá un mensaje [**WM \_ NOTIFY**](wm-notify.md) para este evento, no requiere una máscara de notificación enviada con [**EM \_ SETEVENTMASK**](em-seteventmask.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> <dt>

[**WM \_ NOTIFY**](wm-notify.md)
</dt> </dl>

 

 





