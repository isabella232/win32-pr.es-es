---
description: Evento por usuario generado por el filtro de contenido web debido al intento de obtener acceso a una dirección URL.
ms.assetid: 636b0ce8-cf08-4536-9b41-79512b02a066
title: Evento WPCEVENT_WEB_URLVISIT (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1075ae930cdaa9ee539dbc17a8c13d5c2a41add
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082606"
---
# <a name="wpcevent_web_urlvisit-event"></a>\_ \_ Evento URLVISIT web WPCEVENT

Evento por usuario generado por el filtro de contenido web debido al intento de obtener acceso a una dirección URL.


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

La aplicación que está generando el evento.

</dd> <dt>

*Versión* 
</dt> <dd>

La cadena de versión de la aplicación.

</dd> <dt>

*Motivo* 
</dt> <dd>

Un valor de la enumeración [**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica información sobre qué eventos están bloqueados y qué controles hay en su lugar.

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

Una cadena delimitada de identificadores de categoría que están bloqueados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                             |
| Encabezado<br/>                   | <dl> <dt>Wpcevent. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Uso de las API de registro para controles parentales](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ args \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




