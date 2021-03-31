---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. EXIFVersion.
ms.assetid: 0f9c5ea8-918f-4101-8492-3f408145a73e
title: Directiva de metadatos de la foto de System. Photo. EXIFVersion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eb823db41cb54a06fba235df5be4bb4acd55ea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278634"
---
# <a name="systemphotoexifversion-photo-metadata-policy"></a>Directiva de metadatos de la foto de System. Photo. EXIFVersion

La Directiva de metadatos de fotos para la propiedad [System. Photo. EXIFVersion](../properties/props-system-photo-exifversion.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ EXIFVersion

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ LPWStr

### <a name="input-type"></a>Tipo de entrada

String.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                          | Formato de disco   |
|-------|-------------------------------|---------------|
| 1     | /app1/IFD/Exif/{ushort = 36864} | \_versión EXIF |
| 2     | /xmp/exif:ExifVersion         | unicode       |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                          | Formato de disco   |
|-------|-------------------------------|---------------|
| 1     | /app1/IFD/Exif/{ushort = 36864} | \_versión EXIF |
| 2     | /xmp/exif:ExifVersion         | unicode       |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                          |
|-------|-------------------------------|
| 1     | /app1/IFD/Exif/{ushort = 36864} |
| 2     | /xmp/exif:ExifVersion         |



 

### <a name="tiff-policy"></a>Directiva TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                      | Formato de disco   |
|-------|---------------------------|---------------|
| 1     | /IFD/Exif/{ushort = 36864}  | \_versión EXIF |
| 2     | /ifd/xmp/exif:ExifVersion | unicode       |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                      | Formato de disco   |
|-------|---------------------------|---------------|
| 1     | /IFD/Exif/{ushort = 36864}  | \_versión EXIF |
| 2     | /ifd/xmp/exif:ExifVersion | unicode       |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                      |
|-------|---------------------------|
| 1     | /IFD/Exif/{ushort = 36864}  |
| 2     | /ifd/xmp/exif:ExifVersion |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Photo. EXIFVersion](../properties/props-system-photo-exifversion.md)
</dt> </dl>

 

 
