---
description: Directiva de metadatos de fotos para la propiedad System.SimpleRating.
ms.assetid: d932a251-f238-4582-a1c4-cf4855f26fb3
title: System.SimpleRating Photo Metadata Policy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63b91e41a0684c8e395992683e0a1d4fe43306a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359986"
---
# <a name="systemsimplerating-photo-metadata-policy"></a>System.SimpleRating Photo Metadata Policy

Directiva de metadatos de fotos para [la propiedad System.SimpleRating.](../properties/props-system-simplerating.md)

### <a name="pkey"></a>PKEY

PKEY \_ SimpleRating

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ UI4

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT de entrada

Puede ser VT \_ UI1, VT \_ UI2 o VT \_ UI4. El valor entero puede oscilar entre 0 y 5.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Path                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/{ushort=18246} | ushort      |
| 2     | /xmp/xmp:Rating          | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Path                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /app1/ifd/{ushort=18246} | ushort      |
| 2     | /xmp/xmp:Rating          | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                     |
|-------|--------------------------|
| 1     | /app1/ifd/{ushort=18246} |
| 2     | /xmp/xmp:rating          |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Path                | Formato de disco |
|-------|---------------------|-------------|
| 1     | /ifd/{ushort=18246} | ushort      |
| 2     | /ifd/xmp/xmp:Rating | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Path                | Formato de disco |
|-------|---------------------|-------------|
| 1     | /ifd/{ushort=18246} | ushort      |
| 2     | /ifd/xmp/xmp:Rating | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                |
|-------|---------------------|
| 1     | /ifd/{ushort=18246} |
| 2     | /ifd/xmp/xmp:rating |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.SimpleRating](../properties/props-system-simplerating.md)
</dt> </dl>

 

 
