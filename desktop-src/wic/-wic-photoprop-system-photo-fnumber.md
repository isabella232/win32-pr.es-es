---
description: Directiva de metadatos de fotos para la propiedad System.Photo.FNumber.
ms.assetid: 434d52cb-c98d-4860-87f7-4aedab7f8188
title: Directiva de metadatos de fotos System.Photo.FNumber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85443b849d9f810709f3e75c3082738e5377092f
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443626"
---
# <a name="systemphotofnumber-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Photo.FNumber

Directiva de metadatos de fotos para [la propiedad System.Photo.FNumber.](../properties/props-system-photo-fnumber.md)

### <a name="pkey"></a>Pkey

PKEY \_ Photo \_ FNumber

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ R8

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Este valor se genera a partir de System.Photo.FNumberNumerator y System.Photo.FNumberDenominator. No se puede escribir directamente. Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=33437} |             |
| 2     | /xmp/exif:FNumber             |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=33437} |             |
| 2     | /xmp/exif:FNumber             |             | 
 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=33437} |
| 2     | /xmp/exif:fnumber             |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort=33437} |             |
| 2     | /ifd/xmp/exif:FNumber    |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                     | Formato de disco |
|-------|--------------------------|-------------|
| 1     | /ifd/exif/{ushort=33437} |             |
| 2     | /ifd/xmp/exif:FNumber    |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                     |
|-------|--------------------------|
| 1     | /ifd/exif/{ushort=33437} |
| 2     | /ifd/xmp/exif:fnumber    |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.FNumber](../properties/props-system-photo-fnumber.md)
</dt> </dl>

 

 
