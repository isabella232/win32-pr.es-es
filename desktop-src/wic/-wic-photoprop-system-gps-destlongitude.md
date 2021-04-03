---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. DestLongitude.
ms.assetid: 885a522d-e1bf-43fb-a996-97e725b6cf0c
title: Directiva de metadatos de la foto System. GPS. DestLongitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e0a4f56e49dfbb3397b96cf7fae35a6065b7aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083172"
---
# <a name="systemgpsdestlongitude-photo-metadata-policy"></a>Directiva de metadatos de la foto System. GPS. DestLongitude

La Directiva de metadatos de la fotografía para la propiedad [System. GPS. DestLongitude](../properties/props-system-gps-destlongitude.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ DestLongitude

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ Vector \| VT \_ R8

### <a name="input-propvariant-type"></a>Tipo de PROPVARIANT de entrada

VT \_ Vector \| VT \_ R8

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Este valor se genera a partir de System. GPS. DestLongitudeNumerator y System. GPS. DestLongitudeDenominator. No se puede escribir directamente. Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /app1/IFD/GPS/{ushort = 22}  |             |
| 2     | /xmp/exif:GPSDestLongitude |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /app1/IFD/GPS/{ushort = 22}  |             |
| 2     | /xmp/exif:GPSDestLongitude |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                       |
|-------|----------------------------|
| 1     | /app1/IFD/GPS/{ushort = 22}  |
| 2     | /xmp/exif:gpsdestlongitude |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                           | Formato de disco |
|-------|--------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 22}           |             |
| 2     | /ifd/xmp/exif:GPSDestLongitude |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                           | Formato de disco |
|-------|--------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 22}           |             |
| 2     | /ifd/xmp/exif:GPSDestLongitude |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                           |
|-------|--------------------------------|
| 1     | /IFD/GPS/{ushort = 22}           |
| 2     | /ifd/xmp/exif:gpsdestlongitude |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. GPS. DestLongitude](../properties/props-system-gps-destlongitude.md)
</dt> </dl>

 

 
