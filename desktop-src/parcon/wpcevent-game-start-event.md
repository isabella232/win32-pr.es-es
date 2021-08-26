---
description: Evento por usuario generado por el sistema al intentar iniciar un juego. El sistema de Games Explorer proporciona varios valores de campo y los metadatos correspondientes del archivo de definición de juego (GDF) proporcionados por los juegos compatibles.
ms.assetid: c870f9fb-3be1-4039-9a33-dddff17a4faa
title: WPCEVENT_GAME_START evento (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41367a47a9bace8dd615ab4b6eea0a875099aab465c285389478c4bee0a39392
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951505"
---
# <a name="wpcevent_game_start-event"></a>Evento GAME \_ START de WPCEVENT \_

Evento por usuario generado por el sistema al intentar iniciar un juego. El sistema de Games Explorer proporciona varios valores de campo y los metadatos correspondientes del archivo de definición de juego (GDF) proporcionados por los juegos compatibles.


```C++
const EVENT_DESCRIPTOR WPCEVENT_GAME_START = {0x2, 0x0, 0x10, 0x4, 0x16, 0x2, 0x8000000000000030};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AppID* 
</dt> <dd>

GUID del juego que intentó iniciarse.

</dd> <dt>

*InstanceID* 
</dt> <dd>

GUID que se usa para distinguir entre varias instalaciones.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Cadena de versión del juego.

</dd> <dt>

*Ruta de acceso* 
</dt> <dd>

Ruta de acceso al directorio principal de la instalación del juego.

</dd> <dt>

*Rating* 
</dt> <dd>

Cadena que identifica el nivel de clasificación de un juego dentro del sistema de clasificación.

</dd> <dt>

*RatingSystem* 
</dt> <dd>

GUID que identifica el sistema de clasificación actual al que se aplica el nivel de clasificación.

</dd> <dt>

*Motivo* 
</dt> <dd>

Valor de la enumeración [**\_ WPCFLAG ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica información sobre qué eventos están bloqueados para su uso y qué controles están en su lugar.

</dd> <dt>

*DescCount* 
</dt> <dd>

Recuento de descriptores que están presentes en el campo descriptor.

</dd> <dt>

*Descriptor* 
</dt> <dd>

Cadena delimitada que contiene descriptores bloqueados para el juego.

</dd> <dt>

*Pid* 
</dt> <dd>

El identificador de proceso del juego, que se usa para correlacionar con un cierre de corrección de compatibilidad (shim) del proceso.

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

 

 




