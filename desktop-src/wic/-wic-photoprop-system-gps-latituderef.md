---
description: Directiva de metadatos de fotos para la propiedad System.GPS.LatitudeRef.
ms.assetid: 057015fd-38b7-4053-b611-72565975cc58
title: Directiva de metadatos de fotos System.GPS.LatitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04412af5359e39eaf8e033b059b1c5460e33f6d7537c4763b009b11010fbe87a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119087253"
---
# <a name="systemgpslatituderef-photo-metadata-policy"></a>Directiva de metadatos de fotos System.GPS.LatitudeRef

Directiva de metadatos de fotos [para la propiedad System.GPS.LatitudeRef.](../properties/props-system-gps-latitude.md)

### <a name="pkey"></a>Pkey

PKEY \_ GPS \_ LatitudeRef

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ LPWSTR

### <a name="input-type"></a>Tipo de entrada

Se \_ prefiere VT LPWSTR, pero también \_ se acepta VT LPSTR.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="precedence-of-paths-jpeg"></a>Prioridad de las rutas de acceso (JPEG)

Si el archivo está en formato JPEG, el controlador leerá, escribirá y quitará los datos en el orden siguiente:



| Pedido | Ruta de acceso                         | Formato de disco | Requerido |
|-------|------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSLatitudeRef     | Unicode     | Sí      |
| 2     | /app1/ifd/gps/ \\ {ushort=1 \\ } | ASCII       | No       |



 

### <a name="precedence-of-paths-tiff"></a>Precedencia de rutas de acceso (TIFF)

Si el archivo está en formato TIFF, el controlador leerá, escribirá y quitará los datos en el orden siguiente:



| Pedido | Ruta de acceso                         | Formato de disco | Requerido |
|-------|------------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSLatitudeRef | Unicode     | Sí      |
| 2     | /ifd/gps/ \\ {ushort=1 \\ }      | ASCII       | No       |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.GPS.LatitudeRef](../properties/props-system-gps-latitude.md)
</dt> </dl>

 

 
