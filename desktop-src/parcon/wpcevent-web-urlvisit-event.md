---
description: Evento por usuario generado por el filtro de contenido web debido a que se intenta acceder a una dirección URL.
ms.assetid: 636b0ce8-cf08-4536-9b41-79512b02a066
title: WPCEVENT_WEB_URLVISIT evento (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1075ae930cdaa9ee539dbc17a8c13d5c2a41add
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268383"
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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Encabezado<br/>                   | <dl> <dt>Wpcevent.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Uso de las API de registro para los controles parentales](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ ARGS \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




