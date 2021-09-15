---
description: Directiva de metadatos de fotos para la propiedad System.GPS.DOP.
ms.assetid: 62efd1cc-a2ae-4e53-a0f2-4822b8c91c42
title: Directiva de metadatos de fotos System.GPS.DOP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c33f3bfc6b958593748396124a8cfd1a7de73fd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579400"
---
# <a name="systemgpsdop-photo-metadata-policy"></a>Directiva de metadatos de fotos System.GPS.DOP

Directiva de metadatos de fotos para [la propiedad System.GPS.DOP.](../properties/props-system-gps-dop.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ DOP

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ R8

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Este valor se puede escribir escribiendo en System.GPS.DOPNumerator y System.GPS.DOPDenominator. No se puede escribir directamente. Los valores de esquemas diferentes se concilian.

### <a name="precedence-of-paths-jpeg"></a>Prioridad de las rutas de acceso (JPEG)

Si el archivo está en formato JPEG, el controlador leerá, escribirá y quitará los datos en el orden siguiente:



| Pedido | Path                          | Formato de disco   | Obligatorio |
|-------|-------------------------------|---------------|----------|
| 1     | /xmp/exif:GPSDOP              | Racionalización de XMP  | Sí      |
| 2     | /app1/ifd/gps/ \\ {ushort=11 \\ } | Exif rational | No       |



 

### <a name="precedence-of-paths-tiff"></a>Precedencia de rutas de acceso (TIFF)

Si el archivo está en formato TIFF, el controlador leerá, escribirá y quitará los datos en el orden siguiente:



| Pedido | Path                     | Formato de disco   | Obligatorio |
|-------|--------------------------|---------------|----------|
| 1     | /ifd/xmp/exif:GPSDop     | Racionalización de XMP  | Sí      |
| 2     | /ifd/gps/ \\ {ushort=11 \\ } | Exif rational | No       |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.GPS.DOP](../properties/props-system-gps-dop.md)
</dt> </dl>

 

 
