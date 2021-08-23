---
description: Directiva de metadatos de fotos para la propiedad System.GPS.DestLongitudeRef.
ms.assetid: 2a0abb9b-41e3-49ba-a60b-3096d9c032bd
title: Directiva de metadatos de fotos System.GPS.DestLongitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fca1095138b35767da94e2eeed85a11892ba6edea3fa32f37ea6bd85fb76462
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964954"
---
# <a name="systemgpsdestlongituderef-photo-metadata-policy"></a>Directiva de metadatos de fotos System.GPS.DestLongitudeRef

Directiva de metadatos de fotos [para la propiedad System.GPS.DestLongitudeRef.](../properties/props-system-gps-destlongituderef.md)

### <a name="pkey"></a>Pkey

PKEY \_ GPS. DestLongitudeRef

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT de entrada

Se \_ prefiere VT LPWSTR, pero también \_ se acepta VT LPSTR.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="precedence-of-paths-jpeg"></a>Prioridad de las rutas de acceso (JPEG)

Si el archivo está en formato JPEG, el controlador leerá, escribirá y quitará los datos en el orden siguiente:



| Pedido | Ruta de acceso                          | Formato de disco | Requerido |
|-------|-------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSDestLongitudeRef | Unicode     | Sí      |
| 2     | /app1/ifd/gps/ \\ {ushort=21 \\ } | ASCII       | No       |



 

### <a name="precedence-of-paths-tiff"></a>Precedencia de rutas de acceso (TIFF)

Si el archivo está en formato TIFF, el controlador leerá, escribirá y quitará los datos en el orden siguiente:



| Pedido | Ruta de acceso                              | Formato de disco | Requerido |
|-------|-----------------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSDestLongitudeRef | Unicode     | Sí      |
| 2     | /ifd/gps/ \\ {ushort=21 \\ }          | ASCII       | No       |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.GPS.DestLongitudeRef](../properties/props-system-gps-destlongituderef.md)
</dt> </dl>

 

 
