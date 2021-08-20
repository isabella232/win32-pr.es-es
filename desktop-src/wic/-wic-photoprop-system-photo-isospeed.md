---
description: Directiva de metadatos de fotos para la propiedad System.Photo.ISOSpeed.
ms.assetid: 22b5552c-41b1-4090-a827-b920dcbba5e9
title: Directiva de metadatos de fotos System.Photo.ISOSpeed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c01cb8c3e8e4c80c63985b49e8eda49ebe16d47982dde4cd051f555b8c93d68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964813"
---
# <a name="systemphotoisospeed-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Photo.ISOSpeed

Directiva de metadatos de fotos para [la propiedad System.Photo.ISOSpeed.](../properties/props-system-photo-focallengthinfilm.md)

### <a name="pkey"></a>Pkey

PKEY \_ Photo \_ ISOSpeed

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ UI2

### <a name="input-type"></a>Tipo de entrada

UShort

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                                    | Formato de disco |
|-------|-----------------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=34855}           | ushort      |
| 2     | /xmp/ <xmpseq> exif:ISOSpeedRatings | unicode     |
| 3     | /xmp/exif:ISOSpeed                      | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                                    | Formato de disco |
|-------|-----------------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=34855}           | ushort      |
| 2     | /xmp/ <xmpseq> exif:ISOSpeedRatings | unicode     |
| 3     | /xmp/exif:ISOSpeed                      | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                                    |
|-------|-----------------------------------------|
| 1     | /app1/ifd/exif/{ushort=34855}           |
| 2     | /xmp/ <xmpseq> exif:isospeedratings |
| 3     | /xmp/exif:isospeed                      |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                                        | Formato de disco |
|-------|---------------------------------------------|-------------|
| 1     | /ifd/exif/{ushort=34855}                    | ushort      |
| 2     | /ifd/xmp/ <xmpseq> exif:ISOSpeedRatings | unicode     |
| 3     | /ifd/xmp/exif:ISOSpeed                      | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                                        | Formato de disco |
|-------|---------------------------------------------|-------------|
| 1     | /ifd/exif/{ushort=34855}                    | ushort      |
| 2     | /ifd/xmp/ <xmpseq> exif:ISOSpeedRatings | unicode     |
| 3     | /ifd/xmp/exif:ISOSpeed                      | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                                        |
|-------|---------------------------------------------|
| 1     | /ifd/exif/{ushort=34855}                    |
| 2     | /ifd/xmp/ <xmpseq> exif:isospeedratings |
| 3     | /ifd/xmp/exif:isospeed                      |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.ISOSpeed](../properties/props-system-photo-focallengthinfilm.md)
</dt> </dl>

 

 
