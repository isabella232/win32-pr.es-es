---
description: Directiva de metadatos de fotos para la propiedad System.GPS.DestLatitudeRef.
ms.assetid: 8a13642a-0d29-4193-9784-f716bc428c72
title: Directiva de metadatos de fotos System.GPS.DestLatitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838e4688f0c3342091e5995885689a44fab38739
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247551"
---
# <a name="systemgpsdestlatituderef-photo-metadata-policy"></a>Directiva de metadatos de fotos System.GPS.DestLatitudeRef

Directiva de metadatos de fotos [para la propiedad System.GPS.DestLatitudeRef.](../properties/props-system-gps-destlatituderef.md)

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ DestLatitudeRef

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ LPWSTR

### <a name="input-type"></a>Tipo de entrada

Se \_ prefiere VT LPWSTR, pero se \_ acepta VT LPSTR.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="precedence-of-paths-jpeg"></a>Prioridad de las rutas de acceso (JPEG)

Si el archivo está en formato JPEG, el controlador leerá, escribirá y quitará los datos en el orden siguiente:



| Pedido | Path                          | Formato de disco | Obligatorio |
|-------|-------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSDestLatitudeRef  | Unicode     | Sí      |
| 2     | /app1/ifd/gps/ \\ {ushort=19 \\ } | ASCII       | No       |



 

### <a name="precedence-of-paths-tiff"></a>Precedencia de rutas de acceso (TIFF)

Si el archivo está en formato TIFF, el controlador leerá, escribirá y quitará los datos en el orden siguiente:



| Pedido | Path                             | Formato de disco | Obligatorio |
|-------|----------------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSDestLatitudeRef | Unicode     | Sí      |
| 2     | /ifd/gps/ \\ {ushort=19 \\ }         | ASCII       | No       |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.GPS.DestLatitudeRef](../properties/props-system-gps-destlatituderef.md)
</dt> </dl>

 

 
