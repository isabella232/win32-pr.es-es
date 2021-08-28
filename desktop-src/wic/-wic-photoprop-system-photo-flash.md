---
description: Directiva de metadatos de fotos para la propiedad System.Photo.Flash.
ms.assetid: 24b400a4-f4c7-4b59-a9e3-8a20144cd52e
title: Directiva de metadatos de fotos system.photo.flash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7798e88c40193cac5c577f1960eee96fc2d868
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880077"
---
# <a name="systemphotoflash-photo-metadata-policy"></a>Directiva de metadatos de fotos system.photo.flash

Directiva de metadatos de fotos para [la propiedad System.Photo.Flash.](../properties/props-system-photo-exposuretime.md)

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ Flash

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ UI1 (si el esquema de origen era XMP) o VT \_ UI2 (si el esquema de origen era EXIF)

\\lang1036

### <a name="input-type"></a>Tipo de entrada

VT \_ UI1, VTUI2, VT \_ UI4

\\lang1033

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se concilian los valores de esquemas diferentes.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido de | Ruta de acceso                             | Formato de disco |
|-------|----------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37385}    | ushort      |
| 2     | /xmp/ &lt; xmpstruct &gt; exif:Flash |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido de | Ruta de acceso                             | Formato de disco |
|-------|----------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37385}    | ushort      |
| 2     | /xmp/ &lt; xmpstruct &gt; exif:Flash |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido de | Ruta de acceso                             |
|-------|----------------------------------|
| 1     | /app1/ifd/exif/{ushort=37385}    |
| 2     | /xmp/ &lt; xmpstruct &gt; exif:flash |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido de | Ruta de acceso                                 | Formato de disco |
|-------|--------------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37385}             | ushort      |
| 2     | /ifd/xmp/ &lt; xmpstruct &gt; exif:Flash |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido de | Ruta de acceso                                 | Formato de disco |
|-------|--------------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37385}             | ushort      |
| 2     | /ifd/xmp/ &lt; xmpstruct &gt; exif:Flash |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido de | Ruta de acceso                                 |
|-------|--------------------------------------|
| 1     | /ifd/exif/{ushort=37385}             |
| 2     | /ifd/xmp/ &lt; xmpstruct &gt; exif:flash |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.Flash](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
