---
description: La estructura de los límites de la configuración de la \_ secuencia de vídeo TAPI \_ \_ \_ está contenida en la estructura de la configuración de la secuencia de TAPI \_ \_ \_ Cap cuando el miembro CapsType se establece en el miembro VideoCap de la Unión StreamConfigCapsType.
ms.assetid: 8812755a-50e8-4d8e-ab67-7a3a4b2a4a67
title: TAPI_VIDEO_STREAM_CONFIG_CAPS estructura (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 525a35cb7c7332aa4e80fe8d5e2436e75e2d5c08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680931"
---
# <a name="tapi_video_stream_config_caps-structure"></a>Estructura de los límites de la configuración de la \_ secuencia de vídeo TAPI \_ \_ \_

\[ Esta estructura no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

La estructura de los límites de la configuración de la **\_ secuencia de vídeo \_ \_ \_ TAPI** está contenida en la estructura de la configuración de la [**secuencia de TAPI \_ \_ \_ Cap**](tapi-stream-config-caps.md) cuando el miembro **CapsType** se establece en el miembro **VideoCap** de la Unión [**StreamConfigCapsType**](streamconfigcapstype.md) .

## <a name="syntax"></a>Sintaxis


```C++
} TAPI_VIDEO_STREAM_CONFIG_CAPS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Descripción**
</dt> <dd>

Descripción detallada del tipo de configuración de la secuencia de audio que se va a mostrar a los usuarios de la aplicación.

</dd> <dt>

**Videoestándar**
</dt> <dd>

Estándar de vídeo que se está usando.

</dd> <dt>

**Inlocate**
</dt> <dd>

Tamaño de entrada del marco.

</dd> <dt>

**MinCroppingSize**
</dt> <dd>

Tamaño mínimo de recorte.

</dd> <dt>

**MaxCroppingSize**
</dt> <dd>

Tamaño máximo de recorte.

</dd> <dt>

**CropGranularityX**
</dt> <dd>

Granularidad del recorte que se permite a lo largo del eje x.

</dd> <dt>

**CropGranularityY**
</dt> <dd>

Granularidad del recorte que se permite a lo largo del eje y.

</dd> <dt>

**CropAlignX**
</dt> <dd>

Alineación del recorte del eje x.

</dd> <dt>

**CropAlignY**
</dt> <dd>

Alineación del recorte del eje y.

</dd> <dt>

**MinOutputSize**
</dt> <dd>

Tamaño mínimo resultante de la ventana de vídeo.

</dd> <dt>

**MaxOutputSize**
</dt> <dd>

Tamaño máximo resultante de la ventana de vídeo.

</dd> <dt>

**OutputGranularityX**
</dt> <dd>

Granularidad del tamaño de salida a lo largo del eje x.

</dd> <dt>

**OutputGranularityY**
</dt> <dd>

Granularidad del tamaño de salida a lo largo del eje y.

</dd> <dt>

**StretchTapsX**
</dt> <dd>

Estire a lo largo del eje x.

</dd> <dt>

**StretchTapsY**
</dt> <dd>

Ajustar a lo largo del eje y.

</dd> <dt>

**ShrinkTapsX**
</dt> <dd>

Reducir a lo largo del eje x.

</dd> <dt>

**ShrinkTapsY**
</dt> <dd>

Reducir a lo largo del eje y.

</dd> <dt>

**MinFrameInterval**
</dt> <dd>

Intervalo mínimo de trama de vídeo.

</dd> <dt>

**MaxFrameInterval**
</dt> <dd>

Intervalo máximo de trama de vídeo.

</dd> <dt>

**MinBitsPerSecond**
</dt> <dd>

Mínimo de bits por segundo.

</dd> <dt>

**MaxBitsPerSecond**
</dt> <dd>

Número máximo de bits por segundo.

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

 

 




