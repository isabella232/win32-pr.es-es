---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. altitud.
ms.assetid: 63d59aa3-52a6-4b6f-b6ec-a1c4abcee83f
title: Directiva de metadatos de la foto System. GPS. altitud
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003d39d135c625a01035c023b5d7dc8d890b3b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716896"
---
# <a name="systemgpsaltitude-photo-metadata-policy"></a>Directiva de metadatos de la foto System. GPS. altitud

La Directiva de metadatos de la fotografía para la propiedad [System. GPS. altitud](../properties/props-system-gps-altitude.md) .

### <a name="pkey"></a>PKEY

\_Altitud de GPS de PKEY \_

### <a name="description"></a>Descripción

La altitud se indica como un valor absoluto al que se hace referencia en metros.

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ R8

### <a name="input-propvariant-type"></a>Tipo de PROPVARIANT de entrada

VT \_ R8

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Este valor se puede escribir escribiendo en System. GPS. altitud. Numerator y System. GPS. altitud. denominador. No se puede escribir directamente. Las rutas de acceso de escritura de las tablas siguientes indican dónde se puede guardar el valor cuando se genera, no cuando se escribe directamente. Cuando se lee el valor, se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /app1/IFD/GPS/{ushort = 6} |             |
| 2     | /xmp/exif:GPSAltitude    |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /app1/IFD/GPS/{ushort = 6} |             |
| 2     | /xmp/exif:GPSAltitude    |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                     |
|-------|--------------------------|
| 1     | /app1/IFD/GPS/{ushort = 6} |
| 2     | /xmp/exif:gpsaltitude    |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 6}       |             |
| 2     | /ifd/xmp/exif:GPSAltitude |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 6}       |             |
| 2     | /ifd/xmp/exif:GPSAltitude |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                      |     |
|-------|---------------------------|-----|
| 1     | /IFD/GPS/{ushort = 6}       |     |
| 2     | /ifd/xmp/exif:gpsaltitude |     |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. GPS. altitud](../properties/props-system-gps-altitude.md)
</dt> </dl>

 

 
