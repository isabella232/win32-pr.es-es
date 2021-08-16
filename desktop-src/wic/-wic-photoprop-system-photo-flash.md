---
description: Directiva de metadatos de fotos para la propiedad System.Photo.Flash.
ms.assetid: 24b400a4-f4c7-4b59-a9e3-8a20144cd52e
title: Directiva de metadatos de fotos system.photo.flash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba32a7b4dfcde564f6b0c0c9e175aa56786e1324080264c7c928398fe97e6a34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811735"
---
# <a name="systemphotoflash-photo-metadata-policy"></a>Directiva de metadatos de fotos system.photo.flash

Directiva de metadatos de fotos para [la propiedad System.Photo.Flash.](../properties/props-system-photo-exposuretime.md)

### <a name="pkey"></a>Pkey

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

Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                             | Formato de disco |
|-------|----------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37385}    | ushort      |
| 2     | /xmp/ <xmpstruct> exif:Flash |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                             | Formato de disco |
|-------|----------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37385}    | ushort      |
| 2     | /xmp/ <xmpstruct> exif:Flash |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                             |
|-------|----------------------------------|
| 1     | /app1/ifd/exif/{ushort=37385}    |
| 2     | /xmp/ <xmpstruct> exif:flash |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                                 | Formato de disco |
|-------|--------------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37385}             | ushort      |
| 2     | /ifd/xmp/ <xmpstruct> exif:Flash |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                                 | Formato de disco |
|-------|--------------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37385}             | ushort      |
| 2     | /ifd/xmp/ <xmpstruct> exif:Flash |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                                 |
|-------|--------------------------------------|
| 1     | /ifd/exif/{ushort=37385}             |
| 2     | /ifd/xmp/ <xmpstruct> exif:flash |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.Flash](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
