---
description: La estructura TAPI STREAM CONFIG CAPS contiene \_ información de configuración de \_ \_ secuencias de audio o vídeo.
ms.assetid: 83b39751-b00f-4762-830b-13cafbcb1cfd
title: TAPI_STREAM_CONFIG_CAPS estructura (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cbbb3b3ec72cc99810311cc510e36c2adc8242e2b3d98b321fd8bc8c6a9ab4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002653"
---
# <a name="tapi_stream_config_caps-structure"></a>Estructura TAPI \_ STREAM \_ CONFIG \_ CAPS

\[Esta estructura no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

La **estructura TAPI \_ STREAM CONFIG \_ \_ CAPS** contiene información de configuración de secuencias de audio o vídeo.

## <a name="syntax"></a>Sintaxis


```C++
} TAPI_STREAM_CONFIG_CAPS, *PTAPI_STREAM_CONFIG_CAPS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**CapsType**
</dt> <dd>

Define si el miembro de unión contiene información de vídeo o audio.

</dd> <dt>

**Videocap**
</dt> <dd>

Estructura [**TAPI \_ VIDEO STREAM \_ CONFIG \_ \_ CAPS**](tapi-video-stream-config-caps.md) que contiene las funcionalidades de secuencia de vídeo.

</dd> <dt>

**AudioCap**
</dt> <dd>

Estructura [**TAPI \_ AUDIO STREAM \_ CONFIG \_ \_ CAPS**](tapi-audio-stream-config-caps.md) que contiene las funcionalidades de secuencia de audio.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.1<br/>                                                       |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITFormatControl::GetStreamCaps**](itformatcontrol-getstreamcaps.md)
</dt> <dt>

[**StreamConfigCapsType**](streamconfigcapstype.md)
</dt> <dt>

[**TAPI \_ VIDEO \_ STREAM \_ CONFIG \_ CAPS**](tapi-video-stream-config-caps.md)
</dt> <dt>

[**TAPI \_ AUDIO \_ STREAM \_ CONFIG \_ CAPS**](tapi-audio-stream-config-caps.md)
</dt> </dl>

 

 




