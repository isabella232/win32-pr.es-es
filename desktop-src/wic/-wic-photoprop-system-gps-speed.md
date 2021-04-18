---
description: La Directiva de metadatos de fotos para la propiedad System. GPS. Speed.
ms.assetid: 278826c2-3057-4da2-8c86-0e44471ad7b0
title: Directiva de metadatos de foto de System. GPS. Speed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26d89f755114a73ab17388a1718d5ad0cbdf5a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697493"
---
# <a name="systemgpsspeed-photo-metadata-policy"></a>Directiva de metadatos de foto de System. GPS. Speed

La Directiva de metadatos de fotos para la propiedad [System. GPS. Speed](../properties/props-system-gps-speed.md) .

### <a name="pkey"></a>PKEY

\_Velocidad de GPS de PKEY \_

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ R8

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Este valor se genera a partir de System. GPS. SpeedNumerator y System. GPS. SpeedDenominator. No se puede escribir directamente. Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/IFD/GPS/{ushort = 13} |             |
| 2     | /xmp/exif:GPSSpeed        |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/IFD/GPS/{ushort = 13} |             |
| 2     | /xmp/exif:GPSSpeed        |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                      |
|-------|---------------------------|
| 1     | /app1/IFD/GPS/{ushort = 13} |
| 2     | /xmp/exif:gpsspeed        |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 13}   |             |
| 2     | /ifd/xmp/exif:GPSSpeed |             |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /IFD/GPS/{ushort = 13}   |             |
| 2     | /ifd/xmp/exif:GPSSpeed |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                   |
|-------|------------------------|
| 1     | /IFD/GPS/{ushort = 13}   |
| 2     | /ifd/xmp/exif:gpsspeed |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. GPS. Speed](../properties/props-system-gps-speed.md)
</dt> </dl>

 

 
