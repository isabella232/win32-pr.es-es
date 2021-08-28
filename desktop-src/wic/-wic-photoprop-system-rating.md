---
description: Directiva de metadatos de fotos para la propiedad System.Rating.
ms.assetid: e4d2c12e-617a-431e-9062-62acf6ef21c8
title: Directiva de metadatos de fotos System.Rating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25278ad7d881a0acadc5199fd07227bb650aaae4da2b6342070a64d69fd75240
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086988"
---
# <a name="systemrating-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Rating

Directiva de metadatos de fotos para la [propiedad System.Rating.](../properties/props-system-rating.md)

### <a name="pkey"></a>Pkey

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



| Pedido | Ruta de acceso                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /app1/ifd/{ushort=18249}   | ushort      |
| 2     | /xmp/MicrosoftPhoto:Rating | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /app1/ifd/{ushort=18249}   | ushort      |
| 2     | /xmp/MicrosoftPhoto:Rating | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                       |
|-------|----------------------------|
| 1     | /app1/ifd/{ushort=18249}   |
| 2     | /xmp/microsoftphoto:rating |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                           | Formato de disco |
|-------|--------------------------------|-------------|
| 1     | /ifd/{ushort=18249}            | ushort      |
| 2     | /ifd/xmp/MicrosoftPhoto:Rating | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                           | Formato de disco |
|-------|--------------------------------|-------------|
| 1     | /ifd/{ushort=18249}            | ushort      |
| 2     | /ifd/xmp/MicrosoftPhoto:Rating | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                           |
|-------|--------------------------------|
| 1     | /ifd/{ushort=18249}            |
| 2     | /ifd/xmp/microsoftphoto:rating |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Rating](../properties/props-system-rating.md)
</dt> </dl>

 

 
