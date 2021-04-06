---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. DOP.
ms.assetid: 62efd1cc-a2ae-4e53-a0f2-4822b8c91c42
title: Directiva de metadatos de foto de System. GPS. DOP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c33f3bfc6b958593748396124a8cfd1a7de73fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002874"
---
# <a name="systemgpsdop-photo-metadata-policy"></a>Directiva de metadatos de foto de System. GPS. DOP

La Directiva de metadatos de la fotografía para la propiedad [System. GPS. DOP](../properties/props-system-gps-dop.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ DOP

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ R8

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Este valor se puede escribir escribiendo en System. GPS. DOPNumerator y System. GPS. DOPDenominator. No se puede escribir directamente. Se reconcilian los valores de los distintos esquemas.

### <a name="precedence-of-paths-jpeg"></a>Prioridad de las rutas de acceso (JPEG)

Si el archivo está en formato JPEG, el controlador leerá, escribirá y quitará los datos en el siguiente orden:



| Pedido | Ruta                          | Formato de disco   | Obligatorio |
|-------|-------------------------------|---------------|----------|
| 1     | /xmp/exif:GPSDOP              | XMP Rational  | Sí      |
| 2     | /app1/IFD/GPS/ \\ {ushort = 11 \\ } | Racional EXIF | No       |



 

### <a name="precedence-of-paths-tiff"></a>Prioridad de las rutas de acceso (TIFF)

Si el archivo está en formato TIFF, el controlador leerá, escribirá y quitará los datos en el siguiente orden:



| Pedido | Ruta                     | Formato de disco   | Obligatorio |
|-------|--------------------------|---------------|----------|
| 1     | /ifd/xmp/exif:GPSDop     | XMP Rational  | Sí      |
| 2     | /IFD/GPS/ \\ {ushort = 11 \\ } | Racional EXIF | No       |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. GPS. DOP](../properties/props-system-gps-dop.md)
</dt> </dl>

 

 
