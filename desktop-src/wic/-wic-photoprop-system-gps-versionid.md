---
description: Directiva de metadatos de fotos para la propiedad System.GPS.VersionID.
ms.assetid: d3c88243-8744-4bb3-ab47-38b5354f6f7e
title: Directiva de metadatos de fotos System.GPS.VersionID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 857ecb6b172dafa2a771d9e81f8b570a89f458c79b7630a2f231ce84dbec4f9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706365"
---
# <a name="systemgpsversionid-photo-metadata-policy"></a>Directiva de metadatos de fotos System.GPS.VersionID

Directiva de metadatos de fotos para [la propiedad System.GPS.VersionID.](../properties/props-system-gps-versionid.md)

### <a name="pkey"></a>Pkey

PKEY \_ GPS \_ VersionID

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

Interfaz de \_ usuario VT VECTOR \| VT \_

### <a name="input-type"></a>Tipo de entrada

Buffer

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policies"></a>Directivas JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=0} |             |
| 2     | /xmp/exif:GPSVersionID   | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=0} |             |
| 2     | /xmp/exif:GPSVersionID   | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                     |
|-------|--------------------------|
| 1     | /app1/ifd/gps/{ushort=0} |
| 2     | /xmp/exif:gpsversionid   |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /ifd/gps/{ushort=0}        |             |
| 2     | /ifd/xmp/exif:GPSVersionID | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /ifd/gps/{ushort=0}        |             |
| 2     | /ifd/xmp/exif:GPSVersionID | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                       |
|-------|----------------------------|
| 1     | /ifd/gps/{ushort=0}        |
| 2     | /ifd/xmp/exif:gpsversionid |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.GPS.VersionID](../properties/props-system-gps-versionid.md)
</dt> </dl>

 

 
