---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. SpeedRef.
ms.assetid: 45fea6be-1e63-4244-a93d-d446e315ddd4
title: Directiva de metadatos de la foto System. GPS. SpeedRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c454a016dd77345c0a85e0ca3df1ae52694bd81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697492"
---
# <a name="systemgpsspeedref-photo-metadata-policy"></a>Directiva de metadatos de la foto System. GPS. SpeedRef

La Directiva de metadatos de la fotografía para la propiedad [System. GPS. SpeedRef](../properties/props-system-gps-speedref.md) .

### <a name="pkey"></a>PKEY

PKEY \_ GPS \_ SpeedRef

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

### <a name="jpeg-policies"></a>Directivas JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/IFD/GPS/{ushort = 12} | ascii       |
| 2     | /xmp/exif:GPSSpeedRef     | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/IFD/GPS/{ushort = 12} | ascii       |
| 2     | /xmp/exif:GPSSpeedRef     | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/IFD/GPS/{ushort = 12} |             |
| 2     | /xmp/exif:gpsspeedref     |             |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                      |         |
|-------|---------------------------|---------|
| 1     | /IFD/GPS/{ushort = 12}      | ascii   |
| 2     | /ifd/xmp/exif:GPSSpeedRef | unicode |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 12}      | ascii       |
| 2     | /ifd/xmp/exif:GPSSpeedRef | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                      |
|-------|---------------------------|
| 1     | /IFD/GPS/{ushort = 12}      |
| 2     | /ifd/xmp/exif:gpsspeedref |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. GPS. SpeedRef](../properties/props-system-gps-speedref.md)
</dt> </dl>

 

 
