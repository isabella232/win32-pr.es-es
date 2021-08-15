---
description: Directiva de metadatos de fotos para la propiedad System.Image.ColorSpace.
ms.assetid: 10770f16-8db2-4719-bce3-452f578002ec
title: Directiva de metadatos de fotos System.Image.ColorSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c7d7c9134a8bd93a12ba6cfb6bd8605e228cb6b745ad4401a94f91a2ba9ff9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710425"
---
# <a name="systemimagecolorspace-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Image.ColorSpace

Directiva de metadatos de fotos para [la propiedad System.Image.ColorSpace.](../properties/props-system-image-colorspace.md)

### <a name="pkey"></a>Pkey

PKEY \_ Image \_ ColorSpace

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ UI2

### <a name="input-type"></a>Tipo de entrada

UShort

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se concilian los valores de esquemas diferentes.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Path                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=40961} | ushort      |
| 2     | /xmp/exif:ColorSpace          | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Path                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=40961} | ushort      |
| 2     | /xmp/exif:ColorSpace          | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=40961} |
| 2     | /xmp/exif:colorspace          |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Path                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort=40961} | ushort      |
| 2     | /ifd/xmp/exif:ColorSpace | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Path                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort=40961} | ushort      |
| 2     | /ifd/xmp/exif:ColorSpace | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                     |
|-------|--------------------------|
| 1     | /ifd/exif/{ushort=40961} |
| 2     | /ifd/xmp/exif:colorspace |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Image.ColorSpace](../properties/props-system-image-colorspace.md)
</dt> </dl>

 

 
