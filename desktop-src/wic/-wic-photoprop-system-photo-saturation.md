---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. saturación.
ms.assetid: 1dbb7515-7022-404c-928a-9eb09e43e7a7
title: Directiva de metadatos de la foto System. Photo. saturación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcb2b199458f063f2c28d7f6780a6ea907f76f90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083166"
---
# <a name="systemphotosaturation-photo-metadata-policy"></a>Directiva de metadatos de la foto System. Photo. saturación

La Directiva de metadatos de fotos para la propiedad [System. Photo. saturación](../properties/props-system-photo-saturation.md) .

### <a name="pkey"></a>PKEY

Saturación de la fotografía de PKEY \_ \_

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ UI4

### <a name="input-type"></a>Tipo de entrada

UShort

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 41993} | ushort      |
| 2     | /XMP/Exif: saturación          | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 41993} | ushort      |
| 2     | /XMP/Exif: saturación          | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                          |
|-------|-------------------------------|
| 1     | /app1/IFD/Exif/{ushort = 41993} |
| 2     | /XMP/Exif: saturación          |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 41993} | ushort      |
| 2     | /IFD/XMP/Exif: saturación | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 41993} | ushort      |
| 2     | /IFD/XMP/Exif: saturación | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                     |
|-------|--------------------------|
| 1     | /IFD/Exif/{ushort = 41993} |
| 2     | /IFD/XMP/Exif: saturación |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Photo. saturación](../properties/props-system-photo-saturation.md)
</dt> </dl>

 

 
