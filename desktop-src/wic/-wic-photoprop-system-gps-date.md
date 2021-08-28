---
description: Directiva de metadatos de fotos para la propiedad System.GPS.Date.
ms.assetid: 75047658-b6f3-454e-961a-89016c244bf6
title: Directiva de metadatos de fotos System.GPS.Date
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c082ec60e230f0ada26902c51b4c369b514d8d7b9996538087919c3279d4022a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118033085"
---
# <a name="systemgpsdate-photo-metadata-policy"></a>Directiva de metadatos de fotos System.GPS.Date

Directiva de metadatos de fotos para [la propiedad System.GPS.Date.](../properties/props-system-gps-date.md)

### <a name="pkey"></a>Pkey

PKEY \_ GPS \_ Date

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="input-type"></a>Tipo de entrada

String.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policies"></a>Directivas JPEG

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=29} | ascii       |
| 2     | /xmp/exif:GPSTimeStamp    | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=29} | ascii       |
| 2     | /xmp/exif:GPSTimeStamp    | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                      |
|-------|---------------------------|
| 1     | /app1/ifd/gps/{ushort=29} |
| 2     | /xmp/exif:GPSTimeStamp    |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /ifd/gps/{ushort=29}       | ascii       |
| 2     | /ifd/xmp/exif:GPSTimeStamp | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /ifd/gps/{ushort=29}       | ascii       |
| 2     | /ifd/xmp/exif:GPSTimeStamp | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                       |
|-------|----------------------------|
| 1     | /ifd/gps/{ushort=29}       |
| 2     | /ifd/xmp/exif:GPSTimeStamp |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.GPS.Date](../properties/props-system-gps-date.md)
</dt> </dl>

 

 
