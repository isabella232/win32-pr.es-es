---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. Contrast.
ms.assetid: c5e2589d-507c-4b92-9ada-7d64e7c45dd8
title: Directiva de metadatos de fotografía de System. Photo. Contrast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d6ed34854b525e9eaac2ff5ac7339a75ad10e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547043"
---
# <a name="systemphotocontrast-photo-metadata-policy"></a>Directiva de metadatos de fotografía de System. Photo. Contrast

La Directiva de metadatos de fotos para la propiedad [System. Photo. Contrast](../properties/props-system-photo-contrast.md) .

### <a name="pkey"></a>PKEY

PKEY \_ contraste de fotografía \_

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
| 1     | /app1/IFD/Exif/{ushort = 41992} | ushort      |
| 2     | /XMP/Exif: contraste            | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 41992} | ushort      |
| 2     | /XMP/Exif: contraste            | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                          |
|-------|-------------------------------|
| 1     | /app1/IFD/Exif/{ushort = 41992} |
| 2     | /XMP/Exif: contraste            |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 41992} | ushort      |
| 2     | /IFD/XMP/Exif: contraste   | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 41992} | ushort      |
| 2     | /IFD/XMP/Exif: contraste   | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                     |
|-------|--------------------------|
| 1     | /IFD/Exif/{ushort = 41992} |
| 2     | /IFD/XMP/Exif: contraste   |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Photo. Contrast](../properties/props-system-photo-contrast.md)
</dt> </dl>

 

 
