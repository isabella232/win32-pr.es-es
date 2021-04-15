---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. FocalLengthInFilm.
ms.assetid: 3ad63a7a-5ced-4e7f-a4a0-e1463f3d3fa3
title: Directiva de metadatos de la foto de System. Photo. FocalLengthInFilm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5df46f3e52c447cb7902fe3cce2da201dae16d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498029"
---
# <a name="systemphotofocallengthinfilm-photo-metadata-policy"></a>Directiva de metadatos de la foto de System. Photo. FocalLengthInFilm

La Directiva de metadatos de fotos para la propiedad [System. Photo. FocalLengthInFilm](../properties/props-system-photo-focallengthinfilm.md) .

### <a name="pkey"></a>PKEY

PKEY \_ FocalLengthInFilm

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ UI4

### <a name="input-type"></a>Tipo de entrada

UShort

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                            | Formato de disco |
|-------|---------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 41989}   | ushort      |
| 2     | /xmp/exif:FocalLengthIn35mmFilm | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                            | Formato de disco |
|-------|---------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 41989}   | ushort      |
| 2     | /xmp/exif:FocalLengthIn35mmFilm | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                            |
|-------|---------------------------------|
| 1     | /app1/IFD/Exif/{ushort = 41989}   |
| 2     | /xmp/exif:focallengthin35mmfilm |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                                | Formato de disco |
|-------|-------------------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 41989}            | ushort      |
| 2     | /ifd/xmp/exif:FocalLengthIn35mmFilm | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                                | Formato de disco |
|-------|-------------------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 41989}            | ushort      |
| 2     | /ifd/xmp/exif:FocalLengthIn35mmFilm | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                                |
|-------|-------------------------------------|
| 1     | /IFD/Exif/{ushort = 41989}            |
| 2     | /ifd/xmp/exif:focallengthin35mmfilm |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Photo. FocalLengthInFilm](../properties/props-system-photo-focallengthinfilm.md)
</dt> </dl>

 

 
