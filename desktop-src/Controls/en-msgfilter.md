---
title: EN_MSGFILTER de notificación (Richedit.h)
description: Notifica a la ventana primaria de un control de edición enriquecido un evento de teclado o mouse en el control . Un control de edición enriquecido envía este código de notificación en forma de mensaje WM \_ NOTIFY.
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
ms.openlocfilehash: 40ddb3e9b1d5314e2e981b00f0e0ef8e22974242
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062035"
---
# <a name="en_msgfilter-notification-code"></a>Código de notificación DE EN \_ MSGFILTER

Notifica a la ventana primaria de un control de edición enriquecido un evento de teclado o mouse en el control . Un control de edición enriquecido envía este código de notificación en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
EN_MSGFILTER

    pMsgFilter = (MSGFILTER *) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Estructura [**MSGFILTER que**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) contiene información sobre el teclado o el mensaje del mouse. Si la ventana primaria modifica esta estructura y devuelve un valor distinto de cero, se procesa el mensaje modificado en lugar del original.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si el control debe procesar el evento del teclado o del mouse.

Devuelve un valor distinto de cero si el control debe omitir el evento del teclado o del mouse.

## <a name="remarks"></a>Observaciones

Para recibir códigos de notificación EN MSGFILTER para eventos, especifique una o varias de las marcas siguientes en la máscara enviada con el mensaje \_ [**EM \_ SETEVENTMASK.**](em-seteventmask.md)



| Marca                                                                             | Significado                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------|
| [**ENM \_ KEYEVENTS**](rich-edit-control-event-mask-flags.md)       | Para recibir códigos de notificación para eventos de teclado.     |
| [**EVENTOS MOUSE DE ENM \_**](rich-edit-control-event-mask-flags.md)   | Para recibir códigos de notificación para eventos del mouse.        |
| [**ENM \_ SCROLLEVENTS**](rich-edit-control-event-mask-flags.md) | Para recibir códigos de notificación para un evento de rueda del mouse. |



 

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

[**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter)
</dt> <dt>

[**WM \_ NOTIFY**](wm-notify.md)
</dt> </dl>

 

 





