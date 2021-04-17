---
description: La estructura de los Cap de configuración de la \_ secuencia TAPI \_ \_ contiene información de configuración de flujo de audio o vídeo.
ms.assetid: 83b39751-b00f-4762-830b-13cafbcb1cfd
title: TAPI_STREAM_CONFIG_CAPS estructura (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379ca481d3bebaf8ceb11bfc2dbdab6642ca20b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680360"
---
# <a name="tapi_stream_config_caps-structure"></a>Estructura de los límites de configuración de la \_ secuencia TAPI \_ \_

\[ Esta estructura no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

La estructura de los **\_ \_ \_ Cap** de configuración de la secuencia TAPI contiene información de configuración de flujo de audio o vídeo.

## <a name="syntax"></a>Sintaxis


```C++
} TAPI_STREAM_CONFIG_CAPS, *PTAPI_STREAM_CONFIG_CAPS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**CapsType**
</dt> <dd>

Define si el miembro de Unión contiene información de vídeo o de audio.

</dd> <dt>

**VideoCap**
</dt> <dd>

Una estructura de [**vídeo de configuración de \_ secuencia de vídeo \_ \_ \_ TAPI**](tapi-video-stream-config-caps.md) que contiene las capacidades de flujo de vídeo.

</dd> <dt>

**AudioCap**
</dt> <dd>

Una estructura de [**\_ configuración de flujo de audio \_ \_ \_ TAPI**](tapi-audio-stream-config-caps.md) que contiene las capacidades de secuencia de audio.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,1<br/>                                                       |
| Encabezado<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITFormatControl::GetStreamCaps**](itformatcontrol-getstreamcaps.md)
</dt> <dt>

[**StreamConfigCapsType**](streamconfigcapstype.md)
</dt> <dt>

[**\_Cap de \_ configuración de secuencia de vídeo TAPI \_ \_**](tapi-video-stream-config-caps.md)
</dt> <dt>

[**\_Cap de \_ configuración de secuencia de audio TAPI \_ \_**](tapi-audio-stream-config-caps.md)
</dt> </dl>

 

 




