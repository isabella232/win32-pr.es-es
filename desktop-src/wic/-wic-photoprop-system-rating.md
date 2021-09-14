---
description: Directiva de metadatos de fotos para la propiedad System.Rating.
ms.assetid: e4d2c12e-617a-431e-9062-62acf6ef21c8
title: Directiva de metadatos de fotos System.Rating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c4f7d89b1ff1ea8326c2d26fba0d331db1eab1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360978"
---
# <a name="systemrating-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Rating

Directiva de metadatos de fotos para [la propiedad System.Rating.](../properties/props-system-rating.md)

### <a name="pkey"></a>PKEY

PKEY \_ Rating

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ UI4

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT de entrada

Puede ser VT \_ UI1, VT \_ UI2 o VT \_ UI4. El valor puede oscilar entre 0 y 99.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Path                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /app1/ifd/{ushort=18249}   | ushort      |
| 2     | /xmp/MicrosoftPhoto:Rating | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Path                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /app1/ifd/{ushort=18249}   | ushort      |
| 2     | /xmp/MicrosoftPhoto:Rating | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                       |
|-------|----------------------------|
| 1     | /app1/ifd/{ushort=18249}   |
| 2     | /xmp/microsoftphoto:rating |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Path                           | Formato de disco |
|-------|--------------------------------|-------------|
| 1     | /ifd/{ushort=18249}            | ushort      |
| 2     | /ifd/xmp/MicrosoftPhoto:Rating | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Path                           | Formato de disco |
|-------|--------------------------------|-------------|
| 1     | /ifd/{ushort=18249}            | ushort      |
| 2     | /ifd/xmp/MicrosoftPhoto:Rating | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                           |
|-------|--------------------------------|
| 1     | /ifd/{ushort=18249}            |
| 2     | /ifd/xmp/microsoftphoto:rating |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Rating](../properties/props-system-rating.md)
</dt> </dl>

 

 
