---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. ProcessingMethod.
ms.assetid: 840021a8-ec1d-4916-93b2-7cc1803e2d8c
title: Directiva de metadatos de la foto System. GPS. ProcessingMethod
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02bf1484eb8e8a53c65a9cd43c54b076e418d4eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678481"
---
# <a name="systemgpsprocessingmethod-photo-metadata-policy"></a>Directiva de metadatos de la foto System. GPS. ProcessingMethod

La Directiva de metadatos de la fotografía para la propiedad [System. GPS. ProcessingMethod](../properties/props-system-gps-processingmethod.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ ProcessingMethod

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ LPWStr

### <a name="input-propvariant-type"></a>Tipo de PROPVARIANT de entrada

\_Se prefiere VT LPWStr, pero \_ también se acepta VT LPSTR.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policies"></a>Directivas JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/GPS/{ushort = 27}     |             |
| 2     | /xmp/exif:GPSProcessingMethod | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/GPS/{ushort = 27}     |             |
| 2     | /xmp/exif:GPSProcessingMethod | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                          |
|-------|-------------------------------|
| 1     | /app1/IFD/GPS/{ushort = 27}     |
| 2     | /xmp/exif:gpsprocessingmethod |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                              | Formato de disco |
|-------|-----------------------------------|-------------|
| 1     | /ifd/xmp/exif:GPSProcessingMethod | unicode     |
| 2     | /IFD/GPS/{ushort = 27}              |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                              | Formato de disco |
|-------|-----------------------------------|-------------|
| 1     | /ifd/xmp/exif:GPSProcessingMethod | unicode     |
| 2     | /IFD/GPS/{ushort = 27}              |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                              |
|-------|-----------------------------------|
| 1     | /ifd/xmp/exif:gpsprocessingmethod |
| 2     | /IFD/GPS/{ushort = 27}              |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. GPS. ProcessingMethod](../properties/props-system-gps-processingmethod.md)
</dt> </dl>

 

 
