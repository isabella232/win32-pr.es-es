---
description: El tipo de enumeración WPD VIDEO SCAN TYPES describe cómo se codifican los campos de \_ \_ un archivo de \_ vídeo.
ms.assetid: ea0dab57-6783-4d02-a43c-414e313f1e80
title: WPD_VIDEO_SCAN_TYPES enumeración (PortableDevice.h)
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
ms.openlocfilehash: 5f2c6f8a5707780bae6c8a135e3ca940fb4a77408c3df835b321b5b190644fcc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703725"
---
# <a name="wpd_video_scan_types-enumeration"></a>Enumeración \_ WPD VIDEO \_ SCAN \_ TYPES

El **tipo de \_ enumeración WPD VIDEO \_ SCAN \_ TYPES** describe cómo se codifican los campos de un archivo de vídeo.

## <a name="syntax"></a>Syntax


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

<span id="WPD_VIDEO_SCAN_TYPE_UNUSED"></span><span id="wpd_video_scan_type_unused"></span>**TIPO DE \_ EXAMEN DE \_ VÍDEO WPD SIN \_ \_ USAR**
</dt> <dd>

El tipo de examen no se ha definido para este archivo de vídeo o no es aplicable.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_PROGRESSIVE"></span><span id="wpd_video_scan_type_progressive"></span>**TIPO DE \_ EXAMEN DE \_ VÍDEO WPD \_ \_ PROGRESIVA**
</dt> <dd>

Un archivo de vídeo de examen progresiva.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_upper_first"></span>**CAMPO DE \_ TIPO DE EXAMEN DE VÍDEO \_ \_ WPD \_ \_ INTERCALADO EN PRIMER \_ \_ LUGAR**
</dt> <dd>

Un archivo de vídeo intercalado donde los campos alternativos y el campo superior (con la línea 1) se dibujan primero. Para obtener más información, vea la sección Comentarios.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_lower_first"></span>**CAMPO DE \_ TIPO DE EXAMEN DE VÍDEO \_ \_ WPD \_ \_ INTERCALADO EN PRIMER \_ \_ LUGAR**
</dt> <dd>

Un archivo de vídeo intercalado donde los campos alternativos y el campo inferior (con la línea 2) se dibujan primero. Para obtener más información, vea Comentarios, a continuación de esta sección.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_single_upper_first"></span>**CAMPO WPD \_ VIDEO SCAN TYPE SINGLE UPPER \_ \_ \_ \_ \_ \_ FIRST**
</dt> <dd>

Un archivo de vídeo intercalado donde los campos se envían como ejemplos contiguos y el campo superior (con la línea 1) se dibuja primero. Para obtener más información, vea Comentarios, a continuación de esta sección.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_single_lower_first"></span>**CAMPO WPD \_ VIDEO SCAN TYPE SINGLE LOWER \_ \_ \_ \_ \_ \_ FIRST**
</dt> <dd>

Un archivo de vídeo intercalado donde los campos se envían como ejemplos contiguos y el campo inferior (con la línea 2) se envía primero.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE"></span><span id="wpd_video_scan_type_mixed_interlace"></span>**INTERLACE MIXTO DE TIPO DE EXAMEN \_ \_ DE VÍDEO \_ \_ \_ WPD**
</dt> <dd>

Un archivo de vídeo con una combinación de modos de entrelazado.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE"></span><span id="wpd_video_scan_type_mixed_interlace_and_progressive"></span>**INTERLACE MIXTO Y PROGRESIVA DE TIPO DE EXAMEN DE VÍDEO \_ \_ \_ \_ \_ \_ WPD \_**
</dt> <dd>

Un archivo de vídeo con una combinación de modos entrelazados y progresivas.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta enumeración la usa la [propiedad WPD \_ VIDEO SCAN \_ \_ TYPE.](properties-and-attributes.md)

Hay dos tipos de formatos de archivo intercalados especificados por esta enumeración. **WPD \_ VIDEO \_ SCAN TYPE FIELD \_ \_ \_ INTERLEAVED** hace referencia a un formato de archivo en el que los fotogramas se entregan cuando se analizan campos alternativos y los datos van línea a línea, como se muestra aquí:

**Fotograma 1**

Campo 1: Línea 1

Campo 2: Línea 1

Campo 1: Línea 2

Campo 2: Línea 2

Campo 1: Línea 3

Campo 2: Línea 3

...

**WPD \_ VIDEO \_ SCAN TYPE FIELD \_ \_ \_ SINGLE** hace referencia a un formato de archivo en el que cada campo se almacena en un único bloque de líneas de examen y los campos se almacenan secuencialmente, como se muestra aquí:

**Fotograma 1**

Campo 1: Línea 1

Campo 1: Línea 2

Campo 1: Línea 3

...

Seguido de

Campo 2: Línea 1

Campo 2: Línea 2

Campo 2: Línea 3

...

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




