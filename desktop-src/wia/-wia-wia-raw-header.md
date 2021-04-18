---
description: La \_ estructura de \_ encabezado sin formato de WIA define una imagen en el formato de datos sin procesar de un dispositivo y permite a las aplicaciones usar el formato RAW en las transferencias de adquisición de imágenes de Windows (WIA).
ms.assetid: c7b50816-d596-4c62-a00e-cd8d6e303e42
title: WIA_RAW_HEADER estructura (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_RAW_HEADER
api_type:
- HeaderDef
api_location:
- Wiadef.h
ms.openlocfilehash: 8da33f0b257168712f1b16fb7f940df5db862d3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715174"
---
# <a name="wia_raw_header-structure"></a>\_Estructura de encabezado sin formato de WIA \_

La estructura de **\_ \_ encabezado sin formato de WIA** define una imagen en el formato de datos sin procesar de un dispositivo y permite a las aplicaciones usar el formato RAW en las transferencias de adquisición de imágenes de Windows (WIA).

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _WIA_RAW_HEADER {
  DWORD Tag;
  DWORD Version;
  DWORD HeaderSize;
  DWORD XRes;
  DWORD YRes;
  DWORD XExtent;
  DWORD YExtent;
  DWORD BytesPerLine;
  DWORD BitsPerPixel;
  DWORD ChannelsPerPixel;
  DWORD DataType;
  BYTE  BitsPerChannel[8];
  DWORD Compression;
  DWORD PhotometricInterp;
  DWORD LineOrder;
  DWORD RawDataOffset;
  DWORD RawDataSize;
  DWORD PaletteOffset;
  DWORD PaletteSize;
} WIA_RAW_HEADER;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Tag**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Nombre del formato. Debe ser el literal ' WRAW ' (cuatro caracteres ASCII de un solo byte).

</dd> <dt>

**Versión**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Versión del formato sin formato. Use siempre 0x00010000.

</dd> <dt>

**HeaderSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Bytes totales válidos en el encabezado.

</dd> <dt>

**XRes**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Resolución horizontal en puntos por pulgada.

</dd> <dt>

**YRes**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Resolución vertical en puntos por pulgada.

</dd> <dt>

**XExtent**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Ancho de la imagen en píxeles.

</dd> <dt>

**YExtent**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Alto de la imagen en píxeles.

</dd> <dt>

**BytesPerLine**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

El número de bytes en una línea de una imagen sin comprimir. Use 0 cuando se compriman los datos para indicar que se desconoce el número de bytes por línea.

</dd> <dt>

**BitsPerPixel**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Número total de bits por píxel para todos los canales de píxeles.

</dd> <dt>

**ChannelsPerPixel**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Número de canales de color de un píxel.

</dd> <dt>

**DataType**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

\_ \_ Tipo de la imagen del IPA de WIA. Puesto que \_ \_ el formato de IPA de WIA se establece en WiaImgFmt \_ raw, se trata de una lista de valores permitidos entre los que la aplicación elige.

</dd> <dt>

**BitsPerChannel \[ 8\]**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Número de bits de un canal, hasta un máximo de 8.

</dd> <dt>

**Compresión**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Un \_ \_ valor de compresión de IPA de WIA que especifica el tipo de compresión utilizado, si existe.

</dd> <dt>

**PhotometricInterp**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Un \_ \_ valor INTERP de fotométrico del IPA \_ de WIA que especifica la interpretación fotométrica de la imagen.

</dd> <dt>

**LineOrder**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Valor que representa el orden de la línea de la imagen. Siempre es el orden de las \_ líneas \_ de WIA \_ de arriba abajo o el \_ \_ \_ orden de las líneas de la parte \_ \_ inferior \_ \_ .

</dd> <dt>

**RawDataOffset**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Posición de los datos de imagen sin procesar en bytes, empezando por la posición donde finaliza el encabezado o la posición donde finaliza la paleta.

</dd> <dt>

**RawDataSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tamaño, en bytes, de los datos de imagen sin procesar.

</dd> <dt>

**PaletteOffset**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Posición de la paleta en bytes, empezando por la posición donde finaliza el encabezado o la posición donde finalizan los datos. (Este valor es 0, si no hay ninguna paleta).

</dd> <dt>

**PaletteSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tamaño, en bytes, de la tabla Palette. (Es 0 si no hay ninguna paleta).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Dado que este no es un formato de archivo, use una cadena vacía para la propiedad de extensión de archivo del IPA de WIA \_ \_ \_ .

La paleta y los datos pueden aparecer en cualquier orden.

**RawDataSize** no incluye el encabezado o la paleta. Utilice este campo para comprobar que la transferencia de la imagen se ha realizado correctamente.

**PaletteSize** es bytes, no el número de entradas de la paleta.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




