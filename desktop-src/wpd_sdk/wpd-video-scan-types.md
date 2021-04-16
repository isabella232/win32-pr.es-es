---
description: El \_ tipo de \_ enumeración de tipos de análisis de vídeo de WPD \_ describe cómo se codifican los campos de un archivo de vídeo.
ms.assetid: ea0dab57-6783-4d02-a43c-414e313f1e80
title: Enumeración WPD_VIDEO_SCAN_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_VIDEO_SCAN_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a636bc95fd3d25de20c2df413576a504c4fa1b96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649534"
---
# <a name="wpd_video_scan_types-enumeration"></a>\_ \_ Enumeración de tipos de análisis de vídeo de WPD \_

El tipo de enumeración de tipos de análisis de vídeo de WPD describe cómo se codifican los campos de un archivo de vídeo. **\_ \_ \_**

## <a name="syntax"></a>Sintaxis


```C++
typedef enum WPD_VIDEO_SCAN_TYPES { 
  WPD_VIDEO_SCAN_TYPE_UNUSED                           = 0,
  WPD_VIDEO_SCAN_TYPE_PROGRESSIVE                      = 1,
  WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST    = 2,
  WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST    = 3,
  WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST         = 4,
  WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST         = 5,
  WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE                  = 6,
  WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE  = 7
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_UNUSED"></span><span id="wpd_video_scan_type_unused"></span>**tipo de examen de vídeo de WPD sin \_ \_ \_ \_ usar**
</dt> <dd>

El tipo de examen no se ha definido para este archivo de vídeo o no es aplicable.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_PROGRESSIVE"></span><span id="wpd_video_scan_type_progressive"></span>**tipo de examen de vídeo de WPD \_ \_ \_ \_ progresiva**
</dt> <dd>

Un archivo de vídeo de análisis progresivo.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_upper_first"></span>**campo de tipo de examen de vídeo de WPD \_ \_ \_ \_ \_ entrelazado \_ superior \_ primero**
</dt> <dd>

Un archivo de vídeo intercalado en el que se dibujan primero los campos alternativos y el campo superior (con la línea 1). Para obtener más información, vea la sección Comentarios.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_lower_first"></span>**campo de tipo de examen de vídeo de WPD \_ \_ \_ \_ \_ entrelazado \_ inferior \_ primero**
</dt> <dd>

Un archivo de vídeo intercalado en el que se dibujan primero los campos alternativos y el campo inferior (con la línea 2). Para obtener más información, vea la sección comentarios que se indican a continuación.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_single_upper_first"></span>**campo de tipo de examen de vídeo de WPD \_ \_ \_ \_ \_ único \_ \_ primero superior**
</dt> <dd>

Un archivo de vídeo intercalado en el que los campos se envían como muestras contiguas y el campo superior (con la línea 1) se dibuja primero. Para obtener más información, vea la sección comentarios que se indican a continuación.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_single_lower_first"></span>**campo de tipo de examen de vídeo de WPD \_ \_ \_ \_ \_ único \_ inferior \_ primero**
</dt> <dd>

Un archivo de vídeo intercalado en el que los campos se envían como muestras contiguas y el campo inferior (con la línea 2) se envía primero.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE"></span><span id="wpd_video_scan_type_mixed_interlace"></span>**tipo de escaneo de vídeo de WPD \_ \_ \_ \_ mezclado \_ entrelazado**
</dt> <dd>

Un archivo de vídeo con una combinación de modos de entrelazado.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE"></span><span id="wpd_video_scan_type_mixed_interlace_and_progressive"></span>**\_ \_ \_ tipo \_ de escaneo de vídeo de WPD mezclado \_ entrelazado \_ y \_ progresivo**
</dt> <dd>

Un archivo de vídeo con una combinación de modos entrelazados y progresivos.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta enumeración se usa en la propiedad [tipo de examen de vídeo de WPD \_ \_ \_ ](properties-and-attributes.md) .

Hay dos tipos de formatos de archivo intercalados que se especifican mediante esta enumeración. **WPD \_ El \_ campo de tipo de examen de vídeo \_ \_ \_ intercalado** se refiere a un formato de archivo en el que se entregan fotogramas, ya que se han analizado los campos alternativos y los datos aparecen línea por línea, como se muestra aquí:

**Fotograma 1**

Campo 1: línea 1

Campo 2: línea 1

Campo 1: línea 2

Campo 2: línea 2

Campo 1: línea 3

Campo 2: línea 3

...

**WPD \_ Campo de tipo de examen de vídeo \_ \_ \_ \_ único** hace referencia a un formato de archivo donde cada campo se almacena en un único bloque de líneas de análisis y los campos se almacenan secuencialmente, como se muestra a continuación:

**Fotograma 1**

Campo 1: línea 1

Campo 1: línea 2

Campo 1: línea 3

...

Seguido de

Campo 2: línea 1

Campo 2: línea 2

Campo 2: línea 3

...

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




