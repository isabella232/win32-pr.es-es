---
description: La estructura WIA RAW HEADER define una imagen en el formato de datos RAW de un dispositivo y permite a las aplicaciones usar el formato RAW en \_ las transferencias de Windows Image Acquisition \_ (WIA).
ms.assetid: c7b50816-d596-4c62-a00e-cd8d6e303e42
title: WIA_RAW_HEADER estructura (Wiadef.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574405"
---
# <a name="wia_raw_header-structure"></a>Estructura DE \_ ENCABEZADO SIN FORMATO DE WIA \_

La **estructura WIA \_ RAW \_ HEADER** define una imagen en el formato de datos RAW de un dispositivo y permite a las aplicaciones usar el formato RAW en las transferencias Windows adquisición de imágenes (WIA).

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



## <a name="members"></a>Members

<dl> <dt>

**Tag**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Nombre del formato. Debe ser el literal 'WRAW' (cuatro caracteres ASCII de un solo byte).

</dd> <dt>

**Versión**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Versión del formato RAW. Use siempre 0x00010000.

</dd> <dt>

**HeaderSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Bytes válidos totales en el encabezado.

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

Número de bytes de una línea de una imagen sin comprimir. Use 0 cuando los datos se comprimen para indicar que se desconoce el número de bytes por línea.

</dd> <dt>

**BitsPerPixel**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Número total de bits por píxel para todos los canales del píxel.

</dd> <dt>

**ChannelsPerPixel**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Número de canales de color en un píxel.

</dd> <dt>

**DataType**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

EL TIPO DE DATOS IPA DE WIA \_ \_ de la imagen. Puesto que WIA IPA FORMAT se establece en \_ \_ WiaImgFmt RAW, se trata de una lista de valores permitidos de los que \_ elige la aplicación.

</dd> <dt>

**BitsPerChannel \[ 8\]**
</dt> <dd>

Tipo: **BYTE**

</dd> <dd>

Número de bits de un canal, hasta un máximo de 8.

</dd> <dt>

**Compresión**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Valor COMPRESSION \_ de WIA IPA \_ que especifica el tipo de compresión usado, si lo hay.

</dd> <dt>

**PhotometricInterp**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Valor PHOTOMETRIC INTERP de WIA \_ IPA \_ que especifica la \_ interpretación fotométrica de la imagen.

</dd> <dt>

**LineOrder**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Valor que representa el orden de línea de la imagen. Siempre es WIA \_ LINE ORDER TOP TO BOTTOM o \_ \_ \_ \_ WIA LINE ORDER BOTTOM TO \_ \_ \_ \_ \_ TOP.

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

Tamaño, en bytes, de la tabla de paleta. (Es 0, si no hay ninguna paleta).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Dado que no se trata de un formato de archivo, use una cadena vacía para la propiedad WIA \_ IPA \_ FILE \_ EXTENSION.

La paleta y los datos pueden estar en cualquier orden.

**RawDataSize** no incluye el encabezado ni la paleta. Use este campo para comprobar que la transferencia de la imagen se ha realizado correctamente.

**PaletteSize** es bytes, no el número de entradas de la paleta.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Wiadef.h</dt> </dl> |



 

 




