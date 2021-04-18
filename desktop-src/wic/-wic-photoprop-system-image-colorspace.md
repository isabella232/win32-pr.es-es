---
description: La Directiva de metadatos de la fotografía para la propiedad System. Image. ColorSpace.
ms.assetid: 10770f16-8db2-4719-bce3-452f578002ec
title: Directiva de metadatos de la foto de System. Image. ColorSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6ef2003d05fa19b958b28950f71ec2d5f73027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706405"
---
# <a name="systemimagecolorspace-photo-metadata-policy"></a>Directiva de metadatos de la foto de System. Image. ColorSpace

La Directiva de metadatos de la fotografía para la propiedad [System. Image. ColorSpace](../properties/props-system-image-colorspace.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Image \_ ColorSpace

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ UI2

### <a name="input-type"></a>Tipo de entrada

UShort

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 40961} | ushort      |
| 2     | /xmp/exif:ColorSpace          | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 40961} | ushort      |
| 2     | /xmp/exif:ColorSpace          | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                          |
|-------|-------------------------------|
| 1     | /app1/IFD/Exif/{ushort = 40961} |
| 2     | /xmp/exif:colorspace          |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 40961} | ushort      |
| 2     | /ifd/xmp/exif:ColorSpace | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 40961} | ushort      |
| 2     | /ifd/xmp/exif:ColorSpace | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                     |
|-------|--------------------------|
| 1     | /IFD/Exif/{ushort = 40961} |
| 2     | /ifd/xmp/exif:colorspace |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Image. ColorSpace](../properties/props-system-image-colorspace.md)
</dt> </dl>

 

 
