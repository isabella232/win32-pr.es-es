---
description: La estructura de los límites de la configuración de la \_ secuencia de audio TAPI \_ \_ \_ está contenida en la estructura de la configuración de la secuencia de TAPI \_ \_ \_ Cap cuando el miembro CapsType se establece en el miembro AudioCap de la Unión StreamConfigCapsType.
ms.assetid: 61575839-4604-4c8b-ae4d-fe796c3c5314
title: TAPI_AUDIO_STREAM_CONFIG_CAPS estructura (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daec587a8e760bedd3ab9c6b3469ef8f70b72383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679487"
---
# <a name="tapi_audio_stream_config_caps-structure"></a>Estructura de los límites de configuración de la \_ secuencia de audio TAPI \_ \_ \_

\[ Esta estructura no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

La estructura de los límites de la configuración de la **\_ secuencia de audio \_ \_ \_ TAPI** está contenida en la estructura de la configuración de la [**secuencia de TAPI \_ \_ \_ Cap**](tapi-stream-config-caps.md) cuando el miembro **CapsType** se establece en el miembro **AudioCap** de la Unión [**StreamConfigCapsType**](streamconfigcapstype.md) .

## <a name="syntax"></a>Sintaxis


```C++
} TAPI_AUDIO_STREAM_CONFIG_CAPS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Descripción**
</dt> <dd>

Descripción detallada del tipo de configuración de la secuencia de audio que se va a mostrar a los usuarios de la aplicación.

</dd> <dt>

**MinimumChannels**
</dt> <dd>

Número mínimo de canales asociados a la secuencia.

</dd> <dt>

**MaximumChannels**
</dt> <dd>

Número máximo de canales asociados a la secuencia.

</dd> <dt>

**ChannelsGranularity**
</dt> <dd>

La granularidad del número de canales.

</dd> <dt>

**MinimumBitsPerSample**
</dt> <dd>

Número mínimo de bits por muestra.

</dd> <dt>

**MaximumBitsPerSample**
</dt> <dd>

Número máximo de bits por muestra.

</dd> <dt>

**BitsPerSampleGranularity**
</dt> <dd>

La granularidad de los bits por los valores de ejemplo.

</dd> <dt>

**MinimumSampleFrequency**
</dt> <dd>

La frecuencia de muestreo mínima.

</dd> <dt>

**MaximumSampleFrequency**
</dt> <dd>

La frecuencia de muestreo máxima.

</dd> <dt>

**SampleFrequencyGranularity**
</dt> <dd>

La granularidad de los valores de frecuencia de muestreo.

</dd> <dt>

**MinimumAvgBytesPerSec**
</dt> <dd>

Promedio mínimo de bytes por segundo.

</dd> <dt>

**MaximumAvgBytesPerSec**
</dt> <dd>

Promedio máximo de bytes por segundo.

</dd> <dt>

**AvgBytesPerSecGranularity**
</dt> <dd>

La granularidad de los valores de bytes por segundo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,1<br/>                                                       |
| Encabezado<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Cap de \_ configuración de secuencia TAPI \_**](tapi-stream-config-caps.md)
</dt> </dl>

 

 




