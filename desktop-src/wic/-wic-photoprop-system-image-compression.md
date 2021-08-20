---
description: Directiva de metadatos de fotos para la propiedad System.Image.Compression.
ms.assetid: 0fada41f-f6f8-43b3-ad65-79785e859c9c
title: Directiva de metadatos de fotos System.Image.Compression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aecc3c216cc3aa4d80fe2185065cf68da2fd05b663ddb217941ed930df5caf00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117667625"
---
# <a name="systemimagecompression-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Image.Compression

Directiva de metadatos de fotos para [la propiedad System.Image.Compression.](../properties/props-system-image-compression.md)

### <a name="pkey"></a>Pkey

Compresión de imagen PKEY \_ \_

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ UI2

### <a name="input-type"></a>Tipo de entrada

UShort

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /app1/ifd/{ushort=259} | ushort      |
| 2     | /xmp/tiff:Compression  | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /app1/ifd/{ushort=259} | ushort      |
| 2     | /xmp/tiff:Compression  | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                   |
|-------|------------------------|
| 1     | /app1/ifd/{ushort=259} |
| 2     | /xmp/tiff:compression  |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /ifd/{ushort=259}         | ushort      |
| 2     | /ifd/xmp/tiff:Compression | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /ifd/{ushort=259}         | ushort      |
| 2     | /ifd/xmp/tiff:Compression | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                      |
|-------|---------------------------|
| 1     | /ifd/{ushort=259}         |
| 2     | /ifd/xmp/tiff:compression |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Image.Compression](../properties/props-system-image-compression.md)
</dt> </dl>

 

 
