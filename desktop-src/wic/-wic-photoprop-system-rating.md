---
description: La Directiva de metadatos de la fotografía para la propiedad System. Rating.
ms.assetid: e4d2c12e-617a-431e-9062-62acf6ef21c8
title: Directiva de metadatos de la foto System. Rating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c4f7d89b1ff1ea8326c2d26fba0d331db1eab1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361034"
---
# <a name="systemrating-photo-metadata-policy"></a>Directiva de metadatos de la foto System. Rating

La Directiva de metadatos de la fotografía para la propiedad [System. Rating](../properties/props-system-rating.md) .

### <a name="pkey"></a>PKEY

\_Clasificación PKEY

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ UI4

### <a name="input-propvariant-type"></a>Tipo de PROPVARIANT de entrada

Puede ser VT \_ UI1, VT \_ UI2 o VT \_ UI4. El valor puede oscilar entre 0 y 99.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /app1/IFD/{ushort = 18249}   | ushort      |
| 2     | /xmp/MicrosoftPhoto: clasificación | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                       | Formato de disco |
|-------|----------------------------|-------------|
| 1     | /app1/IFD/{ushort = 18249}   | ushort      |
| 2     | /xmp/MicrosoftPhoto: clasificación | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                       |
|-------|----------------------------|
| 1     | /app1/IFD/{ushort = 18249}   |
| 2     | /XMP/microsoftphoto: clasificación |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                           | Formato de disco |
|-------|--------------------------------|-------------|
| 1     | /IFD/{ushort = 18249}            | ushort      |
| 2     | /ifd/xmp/MicrosoftPhoto: clasificación | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                           | Formato de disco |
|-------|--------------------------------|-------------|
| 1     | /IFD/{ushort = 18249}            | ushort      |
| 2     | /ifd/xmp/MicrosoftPhoto: clasificación | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                           |
|-------|--------------------------------|
| 1     | /IFD/{ushort = 18249}            |
| 2     | /IFD/XMP/microsoftphoto: clasificación |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Rating](../properties/props-system-rating.md)
</dt> </dl>

 

 
