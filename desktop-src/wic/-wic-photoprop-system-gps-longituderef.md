---
description: Directiva de metadatos de fotos para la propiedad System.GPS.LongitudeRef.
ms.assetid: 6e7b3b87-70e5-4c6a-a9b3-959eab38f1f0
title: Directiva de metadatos de fotos System.GPS.LongitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00908f0c76305c745e1146677f32bee7b9724c08510f273c1627ed56e139d02b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931735"
---
# <a name="systemgpslongituderef-photo-metadata-policy"></a>Directiva de metadatos de fotos System.GPS.LongitudeRef

Directiva de metadatos de fotos para [la propiedad System.GPS.LongitudeRef.](../properties/props-system-gps-longituderef.md)

### <a name="pkey"></a>Pkey

PKEY \_ GPS \_ LongitudeRef

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ LPWSTR

### <a name="input-type"></a>Tipo de entrada

String.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="precedence-of-paths-jpeg"></a>Prioridad de las rutas de acceso (JPEG)

Si el archivo está en formato JPEG, el controlador leerá, escribirá y quitará los datos en el orden siguiente:



| Pedido | Ruta de acceso                         | Formato de disco | Requerido |
|-------|------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSLongitudeRef    | Unicode     | Sí      |
| 2     | /app1/ifd/gps/ \\ {ushort=3 \\ } | ASCII       | No       |



 

### <a name="precedence-of-paths-tiff"></a>Precedencia de rutas de acceso (TIFF)

Si el archivo está en formato TIFF, el controlador leerá, escribirá y quitará los datos en el orden siguiente:



| Pedido | Ruta de acceso                          | Formato de disco | Requerido |
|-------|-------------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSLongitudeRef | Unicode     | Sí      |
| 2     | /ifd/gps/ \\ {ushort=3 \\ }       | ASCII       | No       |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.GPS.LongitudeRef](../properties/props-system-gps-longituderef.md)
</dt> </dl>

 

 
