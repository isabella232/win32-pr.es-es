---
description: Directiva de metadatos de fotos para la propiedad System.GPS.AreaInformation.
ms.assetid: d9ecb00b-1f97-4f53-909f-30231104d398
title: Directiva de metadatos de fotos System.GPS.AreaInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e14837da9ffa8b688caf1a544e222043988cf3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572273"
---
# <a name="systemgpsareainformation-photo-metadata-policy"></a>Directiva de metadatos de fotos System.GPS.AreaInformation

Directiva de metadatos de fotos para [la propiedad System.GPS.AreaInformation.](../properties/props-system-gps-areainformation.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ AreaInformation

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ LPWSTR

### <a name="input-type"></a>Tipo de entrada

Cadena

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policies"></a>Directivas JPEG

### <a name="read-paths"></a>Leer rutas de acceso



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

### <a name="read-paths"></a>Leer rutas de acceso



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



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.GPS.AreaInformation](../properties/props-system-gps-areainformation.md)
</dt> </dl>

 

 
