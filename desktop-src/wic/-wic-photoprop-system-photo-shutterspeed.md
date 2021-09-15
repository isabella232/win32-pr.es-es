---
description: Directiva de metadatos de fotos para la propiedad System.Photo.Speed.
ms.assetid: f320944c-978d-4a3c-9bf8-5c5652123e29
title: Directiva de metadatos de fotos System.Photo.SpeedSpeed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8df8c9e7fda5643fed022f67c3b6b7846e7a72f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247527"
---
# <a name="systemphotoshutterspeed-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Photo.SpeedSpeed

Directiva de metadatos de fotos para [la propiedad System.Photo.Speed.](../properties/props-system-photo-shutterspeed.md)

### <a name="pkey"></a>PKEY

PKEY \_ \_ PhotoSpeed

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ R8

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Este valor se genera a partir de System.Photo.SpeedNumerator y System.Photo.SpeedDenominator. No se puede escribir directamente. Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Path                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37377} |             |
| 2     | /xmp/exif:SpeedValue   |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Path                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /app1/ifd/exif/{ushort=37377} |             |
| 2     | /xmp/exif:SpeedValue   |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                          |
|-------|-------------------------------|
| 1     | /app1/ifd/exif/{ushort=37377} |
| 2     | /xmp/exif:speedvalue   |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Path                            | Formato de disco |
|-------|---------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37377}        |             |
| 2     | /ifd/xmp/exif:SpeedValue |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Path                            | Formato de disco |
|-------|---------------------------------|-------------|
| 1     | /ifd/exif/{ushort=37377}        |             |
| 2     | /ifd/xmp/exif:SpeedValue |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                            |
|-------|---------------------------------|
| 1     | /ifd/exif/{ushort=37377}        |
| 2     | /ifd/xmp/exif:speedvalue |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.Speed](../properties/props-system-photo-shutterspeed.md)
</dt> </dl>

 

 
