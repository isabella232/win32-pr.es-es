---
description: Evento por usuario generado por un intento de reproducir contenido con una aplicación multimedia conectada a controles parentales.
ms.assetid: 478cc11e-afbd-411a-ab84-b8ca7c3aa503
title: WPCEVENT_MEDIA_PLAYBACK evento (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 036f88b657ea53a0d1a44679cc55c5cd109f9d16cada16f1812d301b472ef93b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951145"
---
# <a name="wpcevent_media_playback-event"></a>Evento DE REPRODUCCIÓN MULTIMEDIA DE WPCEVENT \_ \_

Evento por usuario generado por un intento de reproducir contenido con una aplicación multimedia conectada a controles parentales.


```C++
const EVENT_DESCRIPTOR WPCEVENT_MEDIA_PLAYBACK = {0x6, 0x0, 0x10, 0x4, 0x16, 0x6, 0x8000000000000030};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AppName* 
</dt> <dd>

Nombre de la aplicación multimedia que genera el evento.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Versión de la aplicación multimedia que genera el evento.

</dd> <dt>

*MediaType* 
</dt> <dd>

Valor de la [**enumeración WPC \_ MEDIA \_ TYPE**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_media_type) que indica información sobre el tipo de archivo multimedia al que se accede.

</dd> <dt>

*Ruta de acceso* 
</dt> <dd>

Ruta de acceso al origen del contenido multimedia.

</dd> <dt>

*Título* 
</dt> <dd>

Metadatos del título para el contenido.

</dd> <dt>

*Pml* 
</dt> <dd>

Nivel de administración parental.

</dd> <dt>

*Álbum* 
</dt> <dd>

Metadatos del álbum para el contenido.

</dd> <dt>

*Explícita* 
</dt> <dd>

Valor de la [**enumeración WPC \_ MEDIA \_ EXPLICIT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_media_explicit) que indica información sobre la clasificación explícita del archivo multimedia.

</dd> <dt>

*Motivo* 
</dt> <dd>

Valor de la enumeración [**\_ WPCFLAG ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica información sobre qué eventos están bloqueados para su uso y qué controles están en su lugar.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 




