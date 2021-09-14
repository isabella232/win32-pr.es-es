---
title: EN_SELCHANGE de notificación (Richedit.h)
description: Notifica a la ventana primaria de un control de edición enriquecido que la selección actual ha cambiado. Un control de edición enriquecido envía este código de notificación en forma de mensaje WM \_ NOTIFY.
ms.assetid: 53d47b53-a73c-4652-889c-2374f8e99382
keywords:
- EN_SELCHANGE código de notificación Windows controles
topic_type:
- apiref
api_name:
- EN_SELCHANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79dfcf951f88fa1e10f4723bd9843421f0e20ae5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062019"
---
# <a name="en_selchange-notification-code"></a>Código \_ de notificación DE EN SELCHANGE

Notifica a la ventana primaria de un control de edición enriquecido que la selección actual ha cambiado. Un control de edición enriquecido envía este código de notificación en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
EN_SELCHANGE

    pSelChange = (SELCHANGE *) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Estructura [**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange) que recibe información sobre la selección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este código de notificación no devuelve un valor.

## <a name="remarks"></a>Observaciones

Para recibir códigos de \_ notificación EN SELCHANGE, especifique [**ENM \_ SELCHANGE**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el [**mensaje EM \_ SETEVENTMASK.**](em-seteventmask.md)

Este código de notificación se envía cuando cambia la posición del cursor de inserción y no se selecciona ningún texto (la selección está vacía). La posición del cursor de referencia puede cambiar cuando el usuario hace clic en el mouse, los tipos o presiona una tecla de flecha.

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

[**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange)
</dt> <dt>

[**WM \_ NOTIFY**](wm-notify.md)
</dt> </dl>

 

 





