---
description: Evento por usuario generado por el sistema al intentar iniciar un juego. Los distintos valores de campo se proporcionan mediante el sistema explorador de juegos y los metadatos correspondientes del archivo de definición de juego (GDF) proporcionados por los juegos admitidos.
ms.assetid: c870f9fb-3be1-4039-9a33-dddff17a4faa
title: Evento WPCEVENT_GAME_START (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5cc47144910f624005031573e28f5078db10ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082607"
---
# <a name="wpcevent_game_start-event"></a>Evento de inicio de \_ juego de WPCEVENT \_

Evento por usuario generado por el sistema al intentar iniciar un juego. Los distintos valores de campo se proporcionan mediante el sistema explorador de juegos y los metadatos correspondientes del archivo de definición de juego (GDF) proporcionados por los juegos admitidos.


```C++
const EVENT_DESCRIPTOR WPCEVENT_GAME_START = {0x2, 0x0, 0x10, 0x4, 0x16, 0x2, 0x8000000000000030};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AppID* 
</dt> <dd>

El GUID del juego que intentó iniciar.

</dd> <dt>

*InstanceID* 
</dt> <dd>

GUID que se usa para distinguir entre varias instalaciones.

</dd> <dt>

*Versiónaplicación* 
</dt> <dd>

La cadena de versión del juego.

</dd> <dt>

*Ruta de acceso* 
</dt> <dd>

La ruta de acceso al directorio principal de la instalación del juego.

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

Un valor de la enumeración [**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica información sobre qué eventos están bloqueados y qué controles hay en su lugar.

</dd> <dt>

*DescCount* 
</dt> <dd>

Recuento de descriptores que se encuentran en el campo descriptor.

</dd> <dt>

*Descriptor* 
</dt> <dd>

Una cadena delimitada que contiene descriptores que están bloqueados para el juego.

</dd> <dt>

*ID* 
</dt> <dd>

El identificador de proceso del juego, que se usa para correlacionar con un cierre de correcciones de compatibilidad (shim) del proceso.

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

 

 




