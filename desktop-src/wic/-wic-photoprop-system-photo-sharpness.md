---
description: La Directiva de metadatos de la foto de la propiedad System. Photo. Sharpity.
ms.assetid: 0fda4832-940b-4b5a-bd20-7e48c7800925
title: Directiva de metadatos de foto de System. Photo. nitidez
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d635691f0b0e0801c1e37a006faa686aff0a8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678223"
---
# <a name="systemphotosharpness-photo-metadata-policy"></a>Directiva de metadatos de foto de System. Photo. nitidez

La Directiva de metadatos de la foto de la propiedad [System. Photo. sharpity](../properties/props-system-photo-sharpness.md) .

### <a name="pkey"></a>PKEY

PKEY \_ foto \_

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ UI4

### <a name="input-type"></a>Tipo de entrada

UShort

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 41994} | ushort      |
| 2     | /XMP/Exif: nitidez           | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 41994} | ushort      |
| 2     | /XMP/Exif: nitidez           | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                          |
|-------|-------------------------------|
| 1     | /app1/IFD/Exif/{ushort = 41994} |
| 2     | /XMP/Exif: nitidez           |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 41994} | ushort      |
| 2     | /IFD/XMP/Exif: nitidez  | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 41994} | ushort      |
| 2     | /IFD/XMP/Exif: nitidez  | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                     |
|-------|--------------------------|
| 1     | /IFD/Exif/{ushort = 41994} |
| 2     | /IFD/XMP/Exif: nitidez  |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Photo. nitidez](../properties/props-system-photo-sharpness.md)
</dt> </dl>

 

 
