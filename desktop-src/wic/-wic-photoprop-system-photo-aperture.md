---
description: La Directiva de metadatos de la fotografía para la propiedad System. Photo. abertura.
ms.assetid: 3048eb9d-4ed4-4b5b-960e-9d0fd6704041
title: Directiva de metadatos de fotografía de System. Photo. abertura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc02826b0602d0052f129640901ac3564a0eadb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688386"
---
# <a name="systemphotoaperture-photo-metadata-policy"></a>Directiva de metadatos de fotografía de System. Photo. abertura

La Directiva de metadatos de la fotografía para la propiedad [System. Photo. abertura](../properties/props-system-photo-aperture.md) .

### <a name="pkey"></a>PKEY

\_Abertura de fotografía de PKEY \_

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ R8

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Este valor se genera a partir de System. Photo. ApertureNumerator y System. Photo. ApertureDenominator. No se puede escribir directamente. Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 37378} |             |
| 2     | /xmp/exif:ApertureValue       |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 37378} |             |
| 2     | /xmp/exif:ApertureValue       |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                          |
|-------|-------------------------------|
| 1     | /app1/IFD/Exif/{ushort = 37378} |
| 2     | /xmp/exif:aperturevalue       |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                        | Formato de disco |
|-------|-----------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 37378}    |             |
| 2     | /ifd/xmp/exif:ApertureValue |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                        | Formato de disco |
|-------|-----------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 37378}    |             |
| 2     | /ifd/xmp/exif:ApertureValue |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                        |
|-------|-----------------------------|
| 1     | /IFD/Exif/{ushort = 37378}    |
| 2     | /ifd/xmp/exif:aperturevalue |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Photo. abertura](../properties/props-system-photo-aperture.md)
</dt> </dl>

 

 
