---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. DestLongitudeRef.
ms.assetid: 2a0abb9b-41e3-49ba-a60b-3096d9c032bd
title: Directiva de metadatos de la foto System. GPS. DestLongitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8139fcf5218d9863393888d7ab7b188a53e7f55f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716785"
---
# <a name="systemgpsdestlongituderef-photo-metadata-policy"></a>Directiva de metadatos de la foto System. GPS. DestLongitudeRef

La Directiva de metadatos de la fotografía para la propiedad [System. GPS. DestLongitudeRef](../properties/props-system-gps-destlongituderef.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS. DestLongitudeRef

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ LPWStr

### <a name="input-propvariant-type"></a>Tipo de PROPVARIANT de entrada

\_Se prefiere VT LPWStr, pero \_ también se acepta VT LPSTR.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="precedence-of-paths-jpeg"></a>Prioridad de las rutas de acceso (JPEG)

Si el archivo está en formato JPEG, el controlador leerá, escribirá y quitará los datos en el siguiente orden:



| Pedido | Ruta                          | Formato de disco | Obligatorio |
|-------|-------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSDestLongitudeRef | Unicode     | Sí      |
| 2     | /app1/IFD/GPS/ \\ {ushort = 21 \\ } | ASCII       | No       |



 

### <a name="precedence-of-paths-tiff"></a>Prioridad de las rutas de acceso (TIFF)

Si el archivo está en formato TIFF, el controlador leerá, escribirá y quitará los datos en el siguiente orden:



| Pedido | Ruta                              | Formato de disco | Obligatorio |
|-------|-----------------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSDestLongitudeRef | Unicode     | Sí      |
| 2     | /IFD/GPS/ \\ {ushort = 21 \\ }          | ASCII       | No       |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. GPS. DestLongitudeRef](../properties/props-system-gps-destlongituderef.md)
</dt> </dl>

 

 
