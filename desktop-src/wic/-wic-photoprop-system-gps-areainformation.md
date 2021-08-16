---
description: Directiva de metadatos de fotos para la propiedad System.GPS.AreaInformation.
ms.assetid: d9ecb00b-1f97-4f53-909f-30231104d398
title: Directiva de metadatos de fotos System.GPS.AreaInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4eee2cf4234902049241c833d1077814f5daf88187323c43bc1cb00f6f44aa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205526"
---
# <a name="systemgpsareainformation-photo-metadata-policy"></a>Directiva de metadatos de fotos System.GPS.AreaInformation

Directiva de metadatos de fotos para [la propiedad System.GPS.AreaInformation.](../properties/props-system-gps-areainformation.md)

### <a name="pkey"></a>Pkey

PKEY \_ GPS \_ AreaInformation

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

### <a name="jpeg-policies"></a>Directivas JPEG

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=28}    |             |
| 2     | /xmp/exif:GPSAreaInformation | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=28}    |             |
| 2     | /xmp/exif:GPSAreaInformation | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                         |
|-------|------------------------------|
| 1     | /app1/ifd/gps/{ushort=28}    |
| 2     | /xmp/exif:GPSAreaInformation |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                             | Formato de disco |
|-------|----------------------------------|-------------|
| 1     | /ifd/gps/{ushort=28}             |             |
| 2     | /ifd/xmp/exif:GPSAreaInformation | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                             | Formato de disco |
|-------|----------------------------------|-------------|
| 1     | /ifd/gps/{ushort=28}             |             |
| 2     | /ifd/xmp/exif:GPSAreaInformation | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                             |
|-------|----------------------------------|
| 1     | /ifd/gps/{ushort=28}             |
| 2     | /ifd/xmp/exif:GPSAreaInformation |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.GPS.AreaInformation](../properties/props-system-gps-areainformation.md)
</dt> </dl>

 

 
