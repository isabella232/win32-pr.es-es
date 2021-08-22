---
description: Directiva de metadatos de fotos para la propiedad System.Photo.Contrast.
ms.assetid: c5e2589d-507c-4b92-9ada-7d64e7c45dd8
title: Directiva de metadatos de fotos System.Photo.Contrast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4a9309ecab96a2244e08ebf05ff8896c792f7366c9db21d41072d2d94aacf47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087101"
---
# <a name="systemphotocontrast-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Photo.Contrast

Directiva de metadatos de fotos para [la propiedad System.Photo.Contrast.](../properties/props-system-photo-contrast.md)

### <a name="pkey"></a>Pkey

PKEY \_ Photo \_ Contrast

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

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=41992} | ushort      |
| 2     | /xmp/exif:Contrast            | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=41992} | ushort      |
| 2     | /xmp/exif:Contrast            | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=41992} |
| 2     | /xmp/exif:contrast            |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort=41992} | ushort      |
| 2     | /ifd/xmp/exif:Contrast   | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort=41992} | ushort      |
| 2     | /ifd/xmp/exif:Contrast   | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                     |
|-------|--------------------------|
| 1     | /ifd/exif/{ushort=41992} |
| 2     | /ifd/xmp/exif:contrast   |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.Contrast](../properties/props-system-photo-contrast.md)
</dt> </dl>

 

 
