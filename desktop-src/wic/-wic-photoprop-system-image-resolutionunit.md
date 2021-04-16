---
description: La Directiva de metadatos de la fotografía para la propiedad System. Image. ResolutionUnit.
ms.assetid: b8b744bd-976b-4648-a04b-33607467d6ac
title: Directiva de metadatos de la foto de System. Image. ResolutionUnit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d954df0b7efe9501cf25c33a54cd4296fb03f3c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706400"
---
# <a name="systemimageresolutionunit-photo-metadata-policy"></a>Directiva de metadatos de la foto de System. Image. ResolutionUnit

La Directiva de metadatos de la fotografía para la propiedad [System. Image. ResolutionUnit](../properties/props-system-image-resolutionunit.md) .

### <a name="pkey"></a>PKEY

PKEY \_ Image \_ ResolutionUnit

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí.

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

I2 de VT \_

### <a name="input-type"></a>Tipo de entrada

UShort

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /app1/IFD/{ushort = 296}   | ushort      |
| 2     | /xmp/tiff:ResolutionUnit | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /app1/IFD/{ushort = 296}   | ushort      |
| 2     | /xmp/tiff:ResolutionUnit | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                     |
|-------|--------------------------|
| 1     | /app1/IFD/{ushort = 296}   |
| 2     | /xmp/tiff:resolutionunit |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /IFD/{ushort = 296}            | ushort      |
| 2     | /ifd/xmp/tiff:ResolutionUnit | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                         | Formato de disco |
|-------|------------------------------|-------------|
| 1     | /IFD/{ushort = 296}            | ushort      |
| 2     | /ifd/xmp/tiff:ResolutionUnit | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                         |
|-------|------------------------------|
| 1     | /IFD/{ushort = 296}            |
| 2     | /ifd/xmp/tiff:resolutionunit |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Image. ResolutionUnit](../properties/props-system-image-resolutionunit.md)
</dt> </dl>

 

 
