---
title: EN_REQUESTRESIZE de notificación (Richedit.h)
description: Notifica a la ventana primaria de un control de edición enriquecido que el contenido del control es menor o mayor que el tamaño de la ventana del control. Un control de edición enriquecido envía este código de notificación en forma de mensaje WM \_ NOTIFY.
ms.assetid: 708c23b1-7b81-46f1-9595-46230693855d
keywords:
- EN_REQUESTRESIZE código de notificación Windows controles
topic_type:
- apiref
api_name:
- EN_REQUESTRESIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60214d8902297eb7cd77ded481b0604929e7adb1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062031"
---
# <a name="en_requestresize-notification-code"></a>Código de notificación EN \_ REQUESTRESIZE

Notifica a la ventana primaria de un control de edición enriquecido que el contenido del control es menor o mayor que el tamaño de la ventana del control. Un control de edición enriquecido envía este código de notificación en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
EN_REQUESTRESIZE

    pReqResize = (REQRESIZE *) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Estructura [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) que recibe el tamaño solicitado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este código de notificación no devuelve un valor.

## <a name="remarks"></a>Observaciones

Para admitir el comportamiento sin fondo de un control de edición enriquecido, la ventana primaria debe cambiar el tamaño del control cuando recibe este código de notificación.

Para recibir los \_ códigos de notificación EN REQUESTRESIZE, especifique [**ENM \_ REQUESTRESIZE**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el [**mensaje EM \_ SETEVENTMASK.**](em-seteventmask.md)

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

[**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize)
</dt> <dt>

[**WM \_ NOTIFY**](wm-notify.md)
</dt> </dl>

 

 





