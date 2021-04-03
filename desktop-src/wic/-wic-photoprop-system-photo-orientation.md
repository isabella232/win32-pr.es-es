---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. Orientation.
ms.assetid: 27e6d4f5-39d5-4cb4-88bc-b0d61ccaa2f3
title: Directiva de metadatos de foto de System. Photo. Orientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a28f4f350cd1a4c24d71ec737b4679aea2f7cab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083167"
---
# <a name="systemphotoorientation-photo-metadata-policy"></a>Directiva de metadatos de foto de System. Photo. Orientation

La Directiva de metadatos de fotos para la propiedad [System. Photo. Orientation](../properties/props-system-photo-meteringmode.md) .

### <a name="pkey"></a>PKEY

PKEY \_ orientación de la foto \_

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

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
| 1     | /app1/IFD/{ushort = 274} | ushort      |
| 2     | /XMP/TIFF: orientación  | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                   | Formato de disco |
|-------|------------------------|-------------|
| 1     | /app1/IFD/{ushort = 274} | ushort      |
| 2     | /XMP/TIFF: orientación  | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                   |
|-------|------------------------|
| 1     | /app1/IFD/{ushort = 274} |
| 2     | /XMP/TIFF: orientación  |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/{ushort = 274}         | ushort      |
| 2     | /IFD/XMP/TIFF: orientación | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /IFD/{ushort = 274}         | ushort      |
| 2     | /IFD/XMP/TIFF: orientación | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                      |
|-------|---------------------------|
| 1     | /IFD/{ushort = 274}         |
| 2     | /IFD/XMP/TIFF: orientación |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Photo. Orientation](../properties/props-system-photo-meteringmode.md)
</dt> </dl>

 

 
