---
description: La Directiva de metadatos de la fotografía para la propiedad System. GPS. Differential.
ms.assetid: 330d1f88-5f54-4e29-b57f-eb7112203e04
title: Directiva de metadatos de fotografía de System. GPS. Differential
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc3f114683d324a067fe4ce4034e2de5cfc88da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361314"
---
# <a name="systemgpsdifferential-photo-metadata-policy"></a>Directiva de metadatos de fotografía de System. GPS. Differential

La Directiva de metadatos de la fotografía para la propiedad [System. GPS. Differential](../properties/props-system-gps-differential.md) .

### <a name="pkey"></a>PKEY

\_Diferencial de GPS de PKEY \_

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ UI2

### <a name="input-propvariant-type"></a>Tipo de PROPVARIANT de entrada

VT \_ UI1, VT \_ UI2 y VT \_ UI4 se aceptan.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policies"></a>Directivas JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/IFD/GPS/{ushort = 30} | ushort      |
| 2     | /xmp/exif:GPSDifferential | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/IFD/GPS/{ushort = 30} | ushort      |
| 2     | /xmp/exif:GPSDifferential | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                      |
|-------|---------------------------|
| 1     | /app1/IFD/GPS/{ushort = 30} |
| 2     | /xmp/exif:gpsdifferential |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 30}          | ushort      |
| 2     | /ifd/xmp/exif:GPSDifferential | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 30}          | ushort      |
| 2     | /ifd/xmp/exif:GPSDifferential | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                          |
|-------|-------------------------------|
| 1     | /IFD/GPS/{ushort = 30}          |
| 2     | /ifd/xmp/exif:gpsdifferential |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. GPS. Differential](../properties/props-system-gps-differential.md)
</dt> </dl>

 

 
