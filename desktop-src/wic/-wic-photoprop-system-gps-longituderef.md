---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. LongitudeRef.
ms.assetid: 6e7b3b87-70e5-4c6a-a9b3-959eab38f1f0
title: Directiva de metadatos de la foto System. GPS. LongitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a93d37b59ca7c77bc05e049860cf4e2608eb60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678368"
---
# <a name="systemgpslongituderef-photo-metadata-policy"></a>Directiva de metadatos de la foto System. GPS. LongitudeRef

La Directiva de metadatos de la fotografía para la propiedad [System. GPS. LongitudeRef](../properties/props-system-gps-longituderef.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ LongitudeRef

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ LPWStr

### <a name="input-type"></a>Tipo de entrada

String.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="precedence-of-paths-jpeg"></a>Prioridad de las rutas de acceso (JPEG)

Si el archivo está en formato JPEG, el controlador leerá, escribirá y quitará los datos en el siguiente orden:



| Pedido | Ruta                         | Formato de disco | Obligatorio |
|-------|------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSLongitudeRef    | Unicode     | Sí      |
| 2     | /app1/IFD/GPS/ \\ {ushort = 3 \\ } | ASCII       | No       |



 

### <a name="precedence-of-paths-tiff"></a>Prioridad de las rutas de acceso (TIFF)

Si el archivo está en formato TIFF, el controlador leerá, escribirá y quitará los datos en el siguiente orden:



| Pedido | Ruta                          | Formato de disco | Obligatorio |
|-------|-------------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSLongitudeRef | Unicode     | Sí      |
| 2     | /IFD/GPS/ \\ {ushort = 3 \\ }       | ASCII       | No       |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. GPS. LongitudeRef](../properties/props-system-gps-longituderef.md)
</dt> </dl>

 

 
