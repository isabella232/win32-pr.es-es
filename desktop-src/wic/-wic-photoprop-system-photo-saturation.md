---
description: Directiva de metadatos de fotos para la propiedad System.Photo.Saturation.
ms.assetid: 1dbb7515-7022-404c-928a-9eb09e43e7a7
title: Directiva de metadatos de fotos System.Photo.Saturation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1be1c5be7a0663d5f57823dcb704b843f56e6076713de3682e4b12d6b533ff48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087018"
---
# <a name="systemphotosaturation-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Photo.Saturation

Directiva de metadatos de fotos para [la propiedad System.Photo.Saturation.](../properties/props-system-photo-saturation.md)

### <a name="pkey"></a>Pkey

Saturación de \_ fotos PKEY \_

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ UI4

### <a name="input-type"></a>Tipo de entrada

UShort

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=41993} | ushort      |
| 2     | /xmp/exif:Saturation          | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=41993} | ushort      |
| 2     | /xmp/exif:Saturation          | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=41993} |
| 2     | /xmp/exif:saturation          |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort=41993} | ushort      |
| 2     | /ifd/xmp/exif:Saturation | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort=41993} | ushort      |
| 2     | /ifd/xmp/exif:Saturation | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                     |
|-------|--------------------------|
| 1     | /ifd/exif/{ushort=41993} |
| 2     | /ifd/xmp/exif:saturation |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.Saturation](../properties/props-system-photo-saturation.md)
</dt> </dl>

 

 
