---
description: Directiva de metadatos de fotos para la propiedad System.GPS.Status.
ms.assetid: 74ea0384-3b1f-4d5e-8713-7b3936813a3a
title: Directiva de metadatos de fotos System.GPS.Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a99237b9fe14d9adbc97dd5de95158a8aa714caaa4a0a8440d9f3798a2155d20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710520"
---
# <a name="systemgpsstatus-photo-metadata-policy"></a>Directiva de metadatos de fotos System.GPS.Status

Directiva de metadatos de fotos para [la propiedad System.GPS.Status.](../properties/props-system-gps-status.md)

### <a name="pkey"></a>Pkey

Estado de GPS de PKEY \_ \_

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT de entrada

Se \_ prefiere VT LPWSTR, pero también \_ se acepta VT LPSTR.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se concilian los valores de esquemas diferentes.

### <a name="jpeg-policies"></a>Directivas JPEG

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Path                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=9} | ascii       |
| 2     | /xmp/exif:GPSStatus      | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Path                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=9} | ascii       |
| 2     | /xmp/exif:GPSStatus      | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                     |
|-------|--------------------------|
| 1     | /app1/ifd/gps/{ushort=9} |
| 2     | /xmp/exif:gpsstatus      |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Path                    | Formato de disco |
|-------|-------------------------|-------------|
| 1     | /ifd/gps/{ushort=9}     | ascii       |
| 2     | /ifd/xmp/exif:GPSStatus | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Path                    | Formato de disco |
|-------|-------------------------|-------------|
| 1     | /ifd/gps/{ushort=9}     | ascii       |
| 2     | /ifd/xmp/exif:GPSStatus | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                    |
|-------|-------------------------|
| 1     | /ifd/gps/{ushort=9}     |
| 2     | /ifd/xmp/exif:gpsstatus |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.GPS.Status](../properties/props-system-gps-status.md)
</dt> </dl>

 

 
