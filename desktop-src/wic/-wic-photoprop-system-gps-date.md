---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. Date.
ms.assetid: 75047658-b6f3-454e-961a-89016c244bf6
title: Directiva de metadatos de la foto System. GPS. Date
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c736c79cd76d2d070d727dc024925717b386cac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278839"
---
# <a name="systemgpsdate-photo-metadata-policy"></a>Directiva de metadatos de la foto System. GPS. Date

La Directiva de metadatos de la fotografía para la propiedad [System. GPS. Date](../properties/props-system-gps-date.md) .

### <a name="pkey"></a>PKEY

Fecha de PKEY \_ GPS \_

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="input-type"></a>Tipo de entrada

String.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policies"></a>Directivas JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/IFD/GPS/{ushort = 29} | ascii       |
| 2     | /xmp/exif:GPSTimeStamp    | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/IFD/GPS/{ushort = 29} | ascii       |
| 2     | /xmp/exif:GPSTimeStamp    | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                      |
|-------|---------------------------|
| 1     | /app1/IFD/GPS/{ushort = 29} |
| 2     | /xmp/exif:GPSTimeStamp    |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 29}       | ascii       |
| 2     | /ifd/xmp/exif:GPSTimeStamp | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 29}       | ascii       |
| 2     | /ifd/xmp/exif:GPSTimeStamp | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                       |
|-------|----------------------------|
| 1     | /IFD/GPS/{ushort = 29}       |
| 2     | /ifd/xmp/exif:GPSTimeStamp |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. GPS. Date](../properties/props-system-gps-date.md)
</dt> </dl>

 

 
