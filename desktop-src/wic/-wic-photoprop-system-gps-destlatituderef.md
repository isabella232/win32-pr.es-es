---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. DestLatitudeRef.
ms.assetid: 8a13642a-0d29-4193-9784-f716bc428c72
title: Directiva de metadatos de la foto System. GPS. DestLatitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838e4688f0c3342091e5995885689a44fab38739
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687873"
---
# <a name="systemgpsdestlatituderef-photo-metadata-policy"></a>Directiva de metadatos de la foto System. GPS. DestLatitudeRef

La Directiva de metadatos de la fotografía para la propiedad [System. GPS. DestLatitudeRef](../properties/props-system-gps-destlatituderef.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ DestLatitudeRef

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ LPWStr

### <a name="input-type"></a>Tipo de entrada

\_Se prefiere VT LPWStr, pero \_ se acepta VT LPSTR.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="precedence-of-paths-jpeg"></a>Prioridad de las rutas de acceso (JPEG)

Si el archivo está en formato JPEG, el controlador leerá, escribirá y quitará los datos en el siguiente orden:



| Pedido | Ruta                          | Formato de disco | Obligatorio |
|-------|-------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSDestLatitudeRef  | Unicode     | Sí      |
| 2     | /app1/IFD/GPS/ \\ {ushort = 19 \\ } | ASCII       | No       |



 

### <a name="precedence-of-paths-tiff"></a>Prioridad de las rutas de acceso (TIFF)

Si el archivo está en formato TIFF, el controlador leerá, escribirá y quitará los datos en el siguiente orden:



| Pedido | Ruta                             | Formato de disco | Obligatorio |
|-------|----------------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSDestLatitudeRef | Unicode     | Sí      |
| 2     | /IFD/GPS/ \\ {ushort = 19 \\ }         | ASCII       | No       |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. GPS. DestLatitudeRef](../properties/props-system-gps-destlatituderef.md)
</dt> </dl>

 

 
