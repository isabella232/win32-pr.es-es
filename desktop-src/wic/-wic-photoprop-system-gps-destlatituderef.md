---
description: Directiva de metadatos de fotos para la propiedad System.GPS.DestLatitudeRef.
ms.assetid: 8a13642a-0d29-4193-9784-f716bc428c72
title: Directiva de metadatos de fotos System.GPS.DestLatitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7abdd7cb7332a15040f329469ec774214840b8eb1a4a8d67ba42662ce3c2c3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118032889"
---
# <a name="systemgpsdestlatituderef-photo-metadata-policy"></a>Directiva de metadatos de fotos System.GPS.DestLatitudeRef

Directiva de metadatos de fotos [para la propiedad System.GPS.DestLatitudeRef.](../properties/props-system-gps-destlatituderef.md)

### <a name="pkey"></a>Pkey

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



| Pedido | Ruta de acceso                          | Formato de disco | Obligatorio |
|-------|-------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSDestLatitudeRef  | Unicode     | Sí      |
| 2     | /app1/ifd/gps/ \\ {ushort=19 \\ } | ASCII       | No       |



 

### <a name="precedence-of-paths-tiff"></a>Precedencia de rutas de acceso (TIFF)

Si el archivo está en formato TIFF, el controlador leerá, escribirá y quitará los datos en el orden siguiente:



| Pedido | Ruta de acceso                             | Formato de disco | Obligatorio |
|-------|----------------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSDestLatitudeRef | Unicode     | Sí      |
| 2     | /ifd/gps/ \\ {ushort=19 \\ }         | ASCII       | No       |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.GPS.DestLatitudeRef](../properties/props-system-gps-destlatituderef.md)
</dt> </dl>

 

 
