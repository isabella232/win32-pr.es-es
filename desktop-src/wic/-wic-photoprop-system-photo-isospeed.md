---
description: Directiva de metadatos de fotos para la propiedad System.Photo.ISOSpeed.
ms.assetid: 22b5552c-41b1-4090-a827-b920dcbba5e9
title: Directiva de metadatos de fotos System.Photo.ISOSpeed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6612bffdeaafb69ea1b1122a1d75c00214d366e9
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881632"
---
# <a name="systemphotoisospeed-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Photo.ISOSpeed

Directiva de metadatos de fotos para [la propiedad System.Photo.ISOSpeed.](../properties/props-system-photo-focallengthinfilm.md)

### <a name="pkey"></a>PKEY

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

Se concilian los valores de esquemas diferentes.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido de | Ruta de acceso                                    | Formato de disco |
|-------|-----------------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=34855}           | ushort      |
| 2     | /xmp/ &lt; xmpseq &gt; exif:ISOSpeedRatings | unicode     |
| 3     | /xmp/exif:ISOSpeed                      | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido de | Ruta de acceso                                    | Formato de disco |
|-------|-----------------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=34855}           | ushort      |
| 2     | /xmp/ &lt; xmpseq &gt; exif:ISOSpeedRatings | unicode     |
| 3     | /xmp/exif:ISOSpeed                      | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido de | Ruta de acceso                                    |
|-------|-----------------------------------------|
| 1     | /app1/ifd/exif/{ushort=34855}           |
| 2     | /xmp/ &lt; xmpseq &gt; exif:isospeedratings |
| 3     | /xmp/exif:isospeed                      |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido de | Ruta de acceso                                        | Formato de disco |
|-------|---------------------------------------------|-------------|
| 1     | /ifd/exif/{ushort=34855}                    | ushort      |
| 2     | /ifd/xmp/ &lt; xmpseq &gt; exif:ISOSpeedRatings | unicode     |
| 3     | /ifd/xmp/exif:ISOSpeed                      | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido de | Ruta de acceso                                        | Formato de disco |
|-------|---------------------------------------------|-------------|
| 1     | /ifd/exif/{ushort=34855}                    | ushort      |
| 2     | /ifd/xmp/ &lt; xmpseq &gt; exif:ISOSpeedRatings | unicode     |
| 3     | /ifd/xmp/exif:ISOSpeed                      | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido de | Ruta de acceso                                        |
|-------|---------------------------------------------|
| 1     | /ifd/exif/{ushort=34855}                    |
| 2     | /ifd/xmp/ &lt; xmpseq &gt; exif:isospeedratings |
| 3     | /ifd/xmp/exif:isospeed                      |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.ISOSpeed](../properties/props-system-photo-focallengthinfilm.md)
</dt> </dl>

 

 
