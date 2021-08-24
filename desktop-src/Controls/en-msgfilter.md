---
title: EN_MSGFILTER de notificación (Richedit.h)
description: Notifica a la ventana primaria de un control de edición enriquecido un evento de teclado o mouse en el control. Un control de edición enriquecido envía este código de notificación en forma de mensaje WM \_ NOTIFY.
ms.assetid: 96cf0047-baae-46cd-82e8-ab6f3f353260
keywords:
- EN_MSGFILTER código de notificación Windows controles
topic_type:
- apiref
api_name:
- EN_MSGFILTER
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87d2cbe47af3d74deb4795946d58871b4729118db0e839027e78e05976ebf855
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436715"
---
# <a name="en_msgfilter-notification-code"></a>Código de notificación EN \_ MSGFILTER

Notifica a la ventana primaria de un control de edición enriquecido un evento de teclado o mouse en el control. Un control de edición enriquecido envía este código de notificación en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
EN_MSGFILTER

    pMsgFilter = (MSGFILTER *) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Estructura [**MSGFILTER que**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) contiene información sobre el mensaje del teclado o del mouse. Si la ventana primaria modifica esta estructura y devuelve un valor distinto de cero, se procesa el mensaje modificado en lugar del original.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si el control debe procesar el evento de teclado o mouse.

Devuelve un valor distinto de cero si el control debe omitir el evento de teclado o mouse.

## <a name="remarks"></a>Observaciones

Para recibir códigos de notificación EN MSGFILTER para eventos, especifique una o varias de las marcas siguientes en la máscara enviada con el mensaje \_ [**EM \_ SETEVENTMASK.**](em-seteventmask.md)



| Marca                                                                             | Significado                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------|
| [**ENM \_ KEYEVENTS**](rich-edit-control-event-mask-flags.md)       | Para recibir códigos de notificación para eventos de teclado.     |
| [**ENM \_ MOUSEEVENTS**](rich-edit-control-event-mask-flags.md)   | Para recibir códigos de notificación para eventos del mouse.        |
| [**EVENTOS DE DESPLAZAMIENTO DE ENM \_**](rich-edit-control-event-mask-flags.md) | Para recibir códigos de notificación para un evento de rueda del mouse. |



 

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

[**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter)
</dt> <dt>

[**WM \_ NOTIFY**](wm-notify.md)
</dt> </dl>

 

 





