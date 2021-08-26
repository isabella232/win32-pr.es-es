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
ms.openlocfilehash: 9b15c21b180c2843eda7947946f6dc98d42caab1bad90383d6afe4a4f8002739
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047585"
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

## <a name="remarks"></a>Comentarios

Para admitir el comportamiento sin fondo de un control de edición enriquecido, la ventana primaria debe cambiar el tamaño del control cuando recibe este código de notificación.

Para recibir los \_ códigos de notificación EN REQUESTRESIZE, especifique [**ENM \_ REQUESTRESIZE**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el [**mensaje EM \_ SETEVENTMASK.**](em-seteventmask.md)

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

[**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize)
</dt> <dt>

[**WM \_ NOTIFY**](wm-notify.md)
</dt> </dl>

 

 





