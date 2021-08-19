---
description: Evento por usuario generado por el filtro de contenido web debido a que se intenta acceder a una dirección URL.
ms.assetid: 636b0ce8-cf08-4536-9b41-79512b02a066
title: WPCEVENT_WEB_URLVISIT evento (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b9524909ee78d14395e2f208fe265b3abc31240d2036788b8b84c4fea05aac9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112705"
---
# <a name="wpcevent_web_urlvisit-event"></a>Evento WPCEVENT \_ WEB \_ URLVISIT

Evento por usuario generado por el filtro de contenido web debido a que se intenta acceder a una dirección URL.


```C++
const EVENT_DESCRIPTOR WPCEVENT_WEB_URLVISIT = {0x3, 0x0, 0x10, 0x4, 0x18, 0x3, 0x8000000000000010};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*URL* 
</dt> <dd>

Dirección URL que está intentando abrirse.

</dd> <dt>

*Aplicación* 
</dt> <dd>

Aplicación que genera el evento.

</dd> <dt>

*Versión* 
</dt> <dd>

Cadena de versión de la aplicación.

</dd> <dt>

*Motivo* 
</dt> <dd>

Valor de la enumeración [**\_ WPCFLAG ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica información sobre qué eventos están bloqueados para su uso y qué controles están en su lugar.

</dd> <dt>

*RatingSystemID* 
</dt> <dd>

GUID que identifica el sistema de clasificación actual.

</dd> <dt>

*CatCount* 
</dt> <dd>

Recuento de entradas bloqueadas en el campo de categoría.

</dd> <dt>

*Categoría* 
</dt> <dd>

Cadena delimitada de identificadores de categoría que están bloqueados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Header<br/>                   | <dl> <dt>Wpcevent.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Uso de las API de registro para los controles parentales](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ ARGS \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




