---
description: Directiva de metadatos de fotos para la propiedad System.GPS.MeasureMode.
ms.assetid: 911a0d81-bd12-4155-b45a-ae1a18f2dd07
title: Directiva de metadatos de fotos System.GPS.MeasureMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a9449ca9a7d1ee5ef213c37562392be2842a09f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267364"
---
# <a name="systemgpsmeasuremode-photo-metadata-policy"></a>Directiva de metadatos de fotos System.GPS.MeasureMode

Directiva de metadatos de fotos para [la propiedad System.GPS.MeasureMode.](../properties/props-system-gps-measuremode.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ MeasureMode

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT de entrada

Se \_ prefiere VT LPWSTR, pero también \_ se acepta VT LPSTR.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policies"></a>Directivas JPEG

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Path                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=10} | ascii       |
| 2     | /xmp/exif:GPSMeasureMode  | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Path                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=10} | ascii       |
| 2     | /xmp/exif:GPSMeasureMode  | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                      |
|-------|---------------------------|
| 1     | /app1/ifd/gps/{ushort=10} |
| 2     | /xmp/exif:gpsmeasuremode  |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Path                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /ifd/gps/{ushort=10}         | ascii       |
| 2     | /ifd/xmp/exif:GPSMeasureMode | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Path                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /ifd/gps/{ushort=10}         | ascii       |
| 2     | /ifd/xmp/exif:GPSMeasureMode | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                         |
|-------|------------------------------|
| 1     | /ifd/gps/{ushort=10}         |
| 2     | /ifd/xmp/exif:gpsmeasuremode |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.GPS.MeasureMode](../properties/props-system-gps-measuremode.md)
</dt> </dl>

 

 
