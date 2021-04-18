---
description: Evento por usuario generado por un intento de reproducir contenido con una aplicación multimedia conectada a controles parentales.
ms.assetid: 478cc11e-afbd-411a-ab84-b8ca7c3aa503
title: Evento WPCEVENT_MEDIA_PLAYBACK (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfdf4e884cc0e87f579d245676f78232a5ae0177
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105717385"
---
# <a name="wpcevent_media_playback-event"></a>\_Evento de \_ reproducción multimedia WPCEVENT

Evento por usuario generado por un intento de reproducir contenido con una aplicación multimedia conectada a controles parentales.


```C++
const EVENT_DESCRIPTOR WPCEVENT_MEDIA_PLAYBACK = {0x6, 0x0, 0x10, 0x4, 0x16, 0x6, 0x8000000000000030};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AppName* 
</dt> <dd>

El nombre de la aplicación multimedia que está generando el evento.

</dd> <dt>

*Versiónaplicación* 
</dt> <dd>

Versión de la aplicación multimedia que está generando el evento.

</dd> <dt>

*MediaType* 
</dt> <dd>

Un valor de la enumeración de [**\_ \_ tipo de medio WPC**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_media_type) que indica información sobre el tipo de archivo multimedia al que se tiene acceso.

</dd> <dt>

*Ruta de acceso* 
</dt> <dd>

Ruta de acceso al origen del contenido multimedia.

</dd> <dt>

*Título* 
</dt> <dd>

Los metadatos de título para el contenido.

</dd> <dt>

*PML* 
</dt> <dd>

El nivel de administración parental.

</dd> <dt>

*Álbum* 
</dt> <dd>

Los metadatos del álbum para el contenido.

</dd> <dt>

*Explícita* 
</dt> <dd>

Un valor de la enumeración de [**WPC \_ media \_ Explicit**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_media_explicit) que indica información sobre la clasificación explícita del archivo multimedia.

</dd> <dt>

*Motivo* 
</dt> <dd>

Un valor de la enumeración [**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica información sobre qué eventos están bloqueados y qué controles hay en su lugar.

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

 

 




