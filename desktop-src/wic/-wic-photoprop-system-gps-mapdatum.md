---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. MapDatum.
ms.assetid: be31e98f-5114-4693-a9ef-37fea334875b
title: Directiva de metadatos de la foto System. GPS. MapDatum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb7a279c79da3d2b1dd20563af35bd34233a1a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678367"
---
# <a name="systemgpsmapdatum-photo-metadata-policy"></a>Directiva de metadatos de la foto System. GPS. MapDatum

La Directiva de metadatos de la fotografía para la propiedad [System. GPS. MapDatum](../properties/props-system-gps-mapdatum.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ MapDatum

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ LPWStr

### <a name="input-type"></a>Tipo de entrada

\_Se prefiere VT LPWStr, pero \_ también se acepta VT LPSTR

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="precedence-of-paths-jpeg"></a>Prioridad de las rutas de acceso (JPEG)

Si el archivo está en formato JPEG, el controlador leerá, escribirá y quitará los datos en el siguiente orden:



| Pedido | Ruta                          | Formato de disco | Obligatorio |
|-------|-------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSMapDatum         | Unicode     | Sí      |
| 2     | /app1/IFD/GPS/ \\ {ushort = 18 \\ } | ASCII       | No       |



 

### <a name="precedence-of-paths-tiff"></a>Prioridad de las rutas de acceso (TIFF)

Si el archivo está en formato TIFF, el controlador leerá, escribirá y quitará los datos en el siguiente orden:



| Pedido | Ruta                      | Formato de disco | Obligatorio |
|-------|---------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSMapDatum | Unicode     | Sí      |
| 2     | /IFD/GPS/ \\ {ushort = 18 \\ }  | ASCII       | No       |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. GPS. MapDatum](../properties/props-system-gps-mapdatum.md)
</dt> </dl>

 

 
