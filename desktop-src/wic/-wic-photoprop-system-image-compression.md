---
description: La Directiva de metadatos de la fotografía para la propiedad System. Image. Compression.
ms.assetid: 0fada41f-f6f8-43b3-ad65-79785e859c9c
title: Directiva de metadatos de foto de System. Image. Compression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32fdc55e2a6a962b1a3dfd9057ef25c89d942f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687662"
---
# <a name="systemimagecompression-photo-metadata-policy"></a>Directiva de metadatos de foto de System. Image. Compression

La Directiva de metadatos de la fotografía para la propiedad [System. Image. Compression](../properties/props-system-image-compression.md) .

### <a name="pkey"></a>PKEY

\_Compresión de imagen PKEY \_

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ UI2

### <a name="input-type"></a>Tipo de entrada

UShort

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /app1/IFD/{ushort = 259} | ushort      |
| 2     | /XMP/TIFF: compresión  | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /app1/IFD/{ushort = 259} | ushort      |
| 2     | /XMP/TIFF: compresión  | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                   |
|-------|------------------------|
| 1     | /app1/IFD/{ushort = 259} |
| 2     | /XMP/TIFF: compresión  |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/{ushort = 259}         | ushort      |
| 2     | /IFD/XMP/TIFF: compresión | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/{ushort = 259}         | ushort      |
| 2     | /IFD/XMP/TIFF: compresión | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                      |
|-------|---------------------------|
| 1     | /IFD/{ushort = 259}         |
| 2     | /IFD/XMP/TIFF: compresión |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Image. Compression](../properties/props-system-image-compression.md)
</dt> </dl>

 

 
