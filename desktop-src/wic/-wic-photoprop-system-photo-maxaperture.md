---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. MaxAperture.
ms.assetid: 9d12d265-0b0a-44d9-bbf6-ca7d748382ee
title: Directiva de metadatos de la foto de System. Photo. MaxAperture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f3dab4d5ebf89033de03dfce887a7cea10fa11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678095"
---
# <a name="systemphotomaxaperture-photo-metadata-policy"></a>Directiva de metadatos de la foto de System. Photo. MaxAperture

La Directiva de metadatos de fotos para la propiedad [System. Photo. MaxAperture](../properties/props-system-photo-maxaperture.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ MaxAperture

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ R8

### <a name="input-type"></a>Tipo de entrada

Doble

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Este valor se genera a partir de System. Photo. MaxApertureNumerator y System. Photo. MaxApertureDenominator. No se puede escribir directamente. Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 37381} |             |
| 2     | /xmp/exif:MaxApertureValue    |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 37381} |             |
| 2     | /xmp/exif:MaxApertureValue    |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                          |
|-------|-------------------------------|
| 1     | /app1/IFD/Exif/{ushort = 37381} |
| 2     | /xmp/exif:maxaperturevalue    |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                           | Formato de disco |
|-------|--------------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 37381}       |             |
| 2     | /ifd/xmp/exif:MaxApertureValue |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                           | Formato de disco |
|-------|--------------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 37381}       |             |
| 2     | /ifd/xmp/exif:MaxApertureValue |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                           |
|-------|--------------------------------|
| 1     | /IFD/Exif/{ushort = 37381}       |
| 2     | /ifd/xmp/exif:maxaperturevalue |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Photo. MaxAperture](../properties/props-system-photo-maxaperture.md)
</dt> </dl>

 

 
