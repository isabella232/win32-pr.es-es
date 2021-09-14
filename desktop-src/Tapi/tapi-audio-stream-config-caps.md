---
description: La estructura TAPI AUDIO STREAM CONFIG CAPS contiene la estructura TAPI STREAM CONFIG CAPS cuando el miembro CapsType se establece en el miembro AudioCap de la unión \_ \_ \_ \_ \_ \_ \_ StreamConfigCapsType.
ms.assetid: 61575839-4604-4c8b-ae4d-fe796c3c5314
title: TAPI_AUDIO_STREAM_CONFIG_CAPS estructura (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daec587a8e760bedd3ab9c6b3469ef8f70b72383
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071058"
---
# <a name="tapi_audio_stream_config_caps-structure"></a>Estructura TAPI \_ AUDIO \_ STREAM CONFIG \_ \_ CAPS

\[Esta estructura no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

La estructura **TAPI \_ AUDIO STREAM CONFIG \_ \_ \_ CAPS** contiene la estructura [**TAPI STREAM CONFIG \_ \_ \_ CAPS**](tapi-stream-config-caps.md) cuando el **miembro CapsType** se establece en el **miembro AudioCap** de la unión [**StreamConfigCapsType.**](streamconfigcapstype.md)

## <a name="syntax"></a>Sintaxis


```C++
} TAPI_AUDIO_STREAM_CONFIG_CAPS;
```



## <a name="members"></a>Members

<dl> <dt>

**Descripción**
</dt> <dd>

Una descripción detallada del tipo de configuración de secuencia de audio para mostrar a los usuarios de la aplicación.

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

Granularidad del recuento de canales.

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

Granularidad de los bits por valores de ejemplo.

</dd> <dt>

**MinimumSampleFrequency**
</dt> <dd>

Frecuencia de muestreo mínima.

</dd> <dt>

**MaximumSampleFrequency**
</dt> <dd>

Frecuencia de muestreo máxima.

</dd> <dt>

**SampleFrequencyGranularity**
</dt> <dd>

Granularidad de los valores de frecuencia de muestreo.

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

Granularidad de los valores de bytes por segundo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.1<br/>                                                       |
| Encabezado<br/>       | <dl> <dt>Ipmsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TAPI \_ STREAM \_ CONFIG \_ CAPS**](tapi-stream-config-caps.md)
</dt> </dl>

 

 




