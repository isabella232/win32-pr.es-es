---
description: La Directiva de metadatos de la fotografía para la propiedad System. SimpleRating.
ms.assetid: d932a251-f238-4582-a1c4-cf4855f26fb3
title: Directiva de metadatos de la foto System. SimpleRating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63b91e41a0684c8e395992683e0a1d4fe43306a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083162"
---
# <a name="systemsimplerating-photo-metadata-policy"></a>Directiva de metadatos de la foto System. SimpleRating

La Directiva de metadatos de la fotografía para la propiedad [System. SimpleRating](../properties/props-system-simplerating.md) .

### <a name="pkey"></a>PKEY

PKEY \_ SimpleRating

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ UI4

### <a name="input-propvariant-type"></a>Tipo de PROPVARIANT de entrada

Puede ser VT \_ UI1, VT \_ UI2 o VT \_ UI4. El valor entero puede oscilar entre 0 y 5.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /app1/IFD/{ushort = 18246} | ushort      |
| 2     | /XMP/XMP: clasificación          | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /app1/IFD/{ushort = 18246} | ushort      |
| 2     | /XMP/XMP: clasificación          | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                     |
|-------|--------------------------|
| 1     | /app1/IFD/{ushort = 18246} |
| 2     | /XMP/XMP: clasificación          |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                | Formato de disco |
|-------|---------------------|-------------|
| 1     | /IFD/{ushort = 18246} | ushort      |
| 2     | /IFD/XMP/XMP: clasificación | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                | Formato de disco |
|-------|---------------------|-------------|
| 1     | /IFD/{ushort = 18246} | ushort      |
| 2     | /IFD/XMP/XMP: clasificación | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                |
|-------|---------------------|
| 1     | /IFD/{ushort = 18246} |
| 2     | /IFD/XMP/XMP: clasificación |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. SimpleRating](../properties/props-system-simplerating.md)
</dt> </dl>

 

 
