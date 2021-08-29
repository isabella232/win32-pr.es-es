---
description: La estructura TAPI VIDEO STREAM CONFIG CAPS está contenida en la estructura TAPI STREAM CONFIG CAPS cuando el miembro CapsType se establece en el miembro VideoCap de la unión \_ \_ \_ \_ \_ \_ \_ StreamConfigCapsType.
ms.assetid: 8812755a-50e8-4d8e-ab67-7a3a4b2a4a67
title: TAPI_VIDEO_STREAM_CONFIG_CAPS estructura (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d2bc7dc02570b2778f84aaa5f00685e57a54833ddc13c347b62e731e23181c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872905"
---
# <a name="tapi_video_stream_config_caps-structure"></a>Estructura TAPI \_ VIDEO \_ STREAM CONFIG \_ \_ CAPS

\[Esta estructura no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

La **estructura TAPI \_ VIDEO STREAM \_ CONFIG \_ \_ CAPS** está contenida en la estructura [**TAPI STREAM CONFIG \_ \_ \_ CAPS**](tapi-stream-config-caps.md) cuando el **miembro CapsType** se establece en el miembro **VideoCap** de la unión [**StreamConfigCapsType.**](streamconfigcapstype.md)

## <a name="syntax"></a>Sintaxis


```C++
} TAPI_VIDEO_STREAM_CONFIG_CAPS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Descripción**
</dt> <dd>

Una descripción sencilla del tipo de configuración de secuencia de audio para mostrar a los usuarios de la aplicación.

</dd> <dt>

**VideoStandard**
</dt> <dd>

Estándar de vídeo que se usa.

</dd> <dt>

**InputSize**
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

Granularidad del recorte permitido a lo largo del eje X.

</dd> <dt>

**CropGranularityY**
</dt> <dd>

Granularidad del recorte permitido a lo largo del eje Y.

</dd> <dt>

**CropAlignX**
</dt> <dd>

Alineación del recorte del eje X.

</dd> <dt>

**CropAlignY**
</dt> <dd>

Alineación del recorte del eje Y.

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

Granularidad del tamaño de salida a lo largo del eje X.

</dd> <dt>

**OutputGranularityY**
</dt> <dd>

Granularidad del tamaño de salida a lo largo del eje Y.

</dd> <dt>

**StretchTapsX**
</dt> <dd>

Se extiende a lo largo del eje X.

</dd> <dt>

**StretchTapsY**
</dt> <dd>

Se extiende a lo largo del eje Y.

</dd> <dt>

**ShrinkTapsX**
</dt> <dd>

Reducir a lo largo del eje X.

</dd> <dt>

**ShrinkTapsY**
</dt> <dd>

Reducir a lo largo del eje Y.

</dd> <dt>

**MinFrameInterval**
</dt> <dd>

Intervalo mínimo de fotogramas de vídeo.

</dd> <dt>

**MaxFrameInterval**
</dt> <dd>

Intervalo máximo de fotogramas de vídeo.

</dd> <dt>

**MinBitsPerSecond**
</dt> <dd>

Bits mínimos por segundo.

</dd> <dt>

**MaxBitsPerSecond**
</dt> <dd>

Bits máximos por segundo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.1<br/>                                                       |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TAPI \_ STREAM \_ CONFIG \_ CAPS**](tapi-stream-config-caps.md)
</dt> </dl>

 

 




