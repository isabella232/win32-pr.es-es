---
description: Directiva de metadatos de fotos para la propiedad System.GPS.MapDatum.
ms.assetid: be31e98f-5114-4693-a9ef-37fea334875b
title: Directiva de metadatos de fotos System.GPS.MapDatum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8bbd3671ec9e025dd2c5ea98fc36f4937abab315b09a2227fb6249d74e577da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882345"
---
# <a name="systemgpsmapdatum-photo-metadata-policy"></a>Directiva de metadatos de fotos System.GPS.MapDatum

Directiva de metadatos de fotos para [la propiedad System.GPS.MapDatum.](../properties/props-system-gps-mapdatum.md)

### <a name="pkey"></a>Pkey

PKEY \_ GPS \_ MapDatum

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ LPWSTR

### <a name="input-type"></a>Tipo de entrada

Se \_ prefiere VT LPWSTR, pero también se acepta \_ VT LPSTR.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="precedence-of-paths-jpeg"></a>Prioridad de las rutas de acceso (JPEG)

Si el archivo está en formato JPEG, el controlador leerá, escribirá y quitará los datos en el orden siguiente:



| Pedido | Ruta de acceso                          | Formato de disco | Requerido |
|-------|-------------------------------|-------------|----------|
| 1     | /xmp/exif:GPSMapDatum         | Unicode     | Sí      |
| 2     | /app1/ifd/gps/ \\ {ushort=18 \\ } | ASCII       | No       |



 

### <a name="precedence-of-paths-tiff"></a>Precedencia de rutas de acceso (TIFF)

Si el archivo está en formato TIFF, el controlador leerá, escribirá y quitará los datos en el orden siguiente:



| Pedido | Ruta de acceso                      | Formato de disco | Requerido |
|-------|---------------------------|-------------|----------|
| 1     | /ifd/xmp/exif:GPSMapDatum | Unicode     | Sí      |
| 2     | /ifd/gps/ \\ {ushort=18 \\ }  | ASCII       | No       |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.GPS.MapDatum](../properties/props-system-gps-mapdatum.md)
</dt> </dl>

 

 
