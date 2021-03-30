---
description: La Directiva de metadatos de fotos para la propiedad System. Photo. isospeed.
ms.assetid: 22b5552c-41b1-4090-a827-b920dcbba5e9
title: Directiva de metadatos de fotografía de System. Photo. isospeed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2988f774f70721ab1817ffaf605098ab1164316a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360919"
---
# <a name="systemphotoisospeed-photo-metadata-policy"></a>Directiva de metadatos de fotografía de System. Photo. isospeed

La Directiva de metadatos de fotos para la propiedad [System. Photo. isospeed](../properties/props-system-photo-focallengthinfilm.md) .

### <a name="pkey"></a>PKEY

Isovelocidad de la \_ foto PKEY \_

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



| Pedido | Ruta                                    | Formato de disco |
|-------|-----------------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 34855}           | ushort      |
| 2     | /XMP/ <xmpseq> Exif: ISOSpeedRatings | unicode     |
| 3     | /XMP/Exif: isospeed                      | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                                    | Formato de disco |
|-------|-----------------------------------------|-------------|
| 1     | /app1/IFD/Exif/{ushort = 34855}           | ushort      |
| 2     | /XMP/ <xmpseq> Exif: ISOSpeedRatings | unicode     |
| 3     | /XMP/Exif: isospeed                      | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                                    |
|-------|-----------------------------------------|
| 1     | /app1/IFD/Exif/{ushort = 34855}           |
| 2     | /XMP/ <xmpseq> Exif: isospeedratings |
| 3     | /XMP/Exif: isospeed                      |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                                        | Formato de disco |
|-------|---------------------------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 34855}                    | ushort      |
| 2     | /IFD/XMP/ <xmpseq> Exif: ISOSpeedRatings | unicode     |
| 3     | /IFD/XMP/Exif: isospeed                      | unicode     |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                                        | Formato de disco |
|-------|---------------------------------------------|-------------|
| 1     | /IFD/Exif/{ushort = 34855}                    | ushort      |
| 2     | /IFD/XMP/ <xmpseq> Exif: ISOSpeedRatings | unicode     |
| 3     | /IFD/XMP/Exif: isospeed                      | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                                        |
|-------|---------------------------------------------|
| 1     | /IFD/Exif/{ushort = 34855}                    |
| 2     | /IFD/XMP/ <xmpseq> Exif: isospeedratings |
| 3     | /IFD/XMP/Exif: isospeed                      |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Photo. isospeed](../properties/props-system-photo-focallengthinfilm.md)
</dt> </dl>

 

 
