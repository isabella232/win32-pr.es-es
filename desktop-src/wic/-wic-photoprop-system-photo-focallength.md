---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. FocalLength.
ms.assetid: a282c31f-00dd-4df5-9b93-300bb9bc8f2d
title: Directiva de metadatos de la foto de System. Photo. FocalLength
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7b36240713782c98d52e4fbf4dae5c0c06082
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716445"
---
# <a name="systemphotofocallength-photo-metadata-policy"></a>Directiva de metadatos de la foto de System. Photo. FocalLength

La Directiva de metadatos de fotos para la propiedad [System. Photo. FocalLength](../properties/props-system-photo-focallength.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ FocalLength

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ R8

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Este valor se genera a partir de System. Photo. FocalLengthNumerator y System. Photo. FocalLengthDenominator. No se puede escribir directamente. Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 37386} |             |
| 2     | /xmp/exif:FocalLength         |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 37386} |             |
| 2     | /xmp/exif:FocalLength         |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                          |
|-------|-------------------------------|
| 1     | /app1/IFD/Exif/{ushort = 37386} |
| 2     | /xmp/exif:focallength         |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 37386}  |             |
| 2     | /ifd/xmp/exif:FocalLength |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 37386}  |             |
| 2     | /ifd/xmp/exif:FocalLength |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                      |
|-------|---------------------------|
| 1     | /IFD/Exif/{ushort = 37386}  |
| 2     | /ifd/xmp/exif:focallength |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Photo. FocalLength](../properties/props-system-photo-focallength.md)
</dt> </dl>

 

 
