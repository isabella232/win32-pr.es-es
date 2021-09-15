---
description: Directiva de metadatos de fotos para la propiedad System.Photo.RelatedSoundFile.
ms.assetid: 3b212d90-7ae2-4b7c-b77a-2017490aca40
title: Directiva de metadatos de fotos System.Photo.RelatedSoundFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07a29adb71f572868f21b1b8427e71b09616b24c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247532"
---
# <a name="systemphotorelatedsoundfile-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Photo.RelatedSoundFile

Directiva de metadatos de fotos para la [propiedad System.Photo.RelatedSoundFile.](../properties/props-system-photo-relatedsoundfile.md)

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ RelatedSoundFile

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ LPWSTR

### <a name="input-type"></a>Tipo de entrada

Cadena

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Path                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=40964} | ascii       |
| 2     | /xmp/exif:Related SoundFile    | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Path                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=40964} | ascii       |
| 2     | /xmp/exif:Related SoundFile    | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=40964} |
| 2     | /xmp/exif:Related SoundFile    |



 

### <a name="tiff-policy"></a>Directiva TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Path                           | Formato de disco |
|-------|--------------------------------|-------------|
| 1     | /ifd/exif/{ushort=40964}       | ascii       |
| 2     | /ifd/xmp/exif:Related SoundFile | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Path                           | Formato de disco |
|-------|--------------------------------|-------------|
| 1     | /ifd/exif/{ushort=40964}       | ascii       |
| 2     | /ifd/xmp/exif:Related SoundFile | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                           |
|-------|--------------------------------|
| 1     | /ifd/exif/{ushort=40964}       |
| 2     | /ifd/xmp/exif:Related SoundFile |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.Related SoundFile](../properties/props-system-photo-relatedsoundfile.md)
</dt> </dl>

 

 
