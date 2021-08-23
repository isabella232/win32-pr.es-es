---
description: Directiva de metadatos de fotos para la propiedad System.Photo.RelatedSoundFile.
ms.assetid: 3b212d90-7ae2-4b7c-b77a-2017490aca40
title: Directiva de metadatos de fotos System.Photo.RelatedSoundFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aae80ad39b8d3dab271aacf4815836e8b386c150ec80be63a83a4ab5937635e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549435"
---
# <a name="systemphotorelatedsoundfile-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Photo.RelatedSoundFile

Directiva de metadatos de fotos para [la propiedad System.Photo.RelatedSoundFile.](../properties/props-system-photo-relatedsoundfile.md)

### <a name="pkey"></a>Pkey

PKEY \_ Photo \_ RelatedSoundFile

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ LPWSTR

### <a name="input-type"></a>Tipo de entrada

String.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=40964} | ascii       |
| 2     | /xmp/exif:RelatedSoundFile    | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=40964} | ascii       |
| 2     | /xmp/exif:RelatedSoundFile    | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=40964} |
| 2     | /xmp/exif:RelatedSoundFile    |



 

### <a name="tiff-policy"></a>Directiva TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                           | Formato de disco |
|-------|--------------------------------|-------------|
| 1     | /ifd/exif/{ushort=40964}       | ascii       |
| 2     | /ifd/xmp/exif:RelatedSoundFile | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                           | Formato de disco |
|-------|--------------------------------|-------------|
| 1     | /ifd/exif/{ushort=40964}       | ascii       |
| 2     | /ifd/xmp/exif:RelatedSoundFile | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                           |
|-------|--------------------------------|
| 1     | /ifd/exif/{ushort=40964}       |
| 2     | /ifd/xmp/exif:RelatedSoundFile |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.RelatedSoundFile](../properties/props-system-photo-relatedsoundfile.md)
</dt> </dl>

 

 
