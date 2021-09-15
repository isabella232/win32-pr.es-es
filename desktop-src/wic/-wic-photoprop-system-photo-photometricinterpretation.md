---
description: Directiva de metadatos de fotos para la propiedad System.Photo.PhotometricInterpretation.
ms.assetid: ff36b2c3-8763-4640-a049-b5880fd26929
title: Directiva de metadatos de fotos System.Photo.PhotometricInterpretation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b371ce9257d526f941f3fdb33949e8788a7112
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247538"
---
# <a name="systemphotophotometricinterpretation-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Photo.PhotometricInterpretation

Directiva de metadatos de fotos para [la propiedad System.Photo.PhotometricInterpretation.](../properties/props-system-photo-photometricinterpretation.md)

### <a name="pkey"></a>PKEY

PKEY \_ Photo \_ PhotometricInterpretation

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ UI2

### <a name="input-type"></a>Tipo de entrada

UShort

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Path                                | Formato de disco |
|-------|-------------------------------------|-------------|
| 1     | /app1/ifd/{ushort=262}              | ushort      |
| 2     | /xmp/tiff:PhotometricInterpretation | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Path                                | Formato de disco |
|-------|-------------------------------------|-------------|
| 1     | /app1/ifd/{ushort=262}              | ushort      |
| 2     | /xmp/tiff:PhotometricInterpretation | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                                |
|-------|-------------------------------------|
| 1     | /app1/ifd/{ushort=262}              |
| 2     | /xmp/tiff:photometricinterpretation |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Path                                    | Formato de disco |
|-------|-----------------------------------------|-------------|
| 1     | /ifd/{ushort=262}                       | ushort      |
| 2     | /ifd/xmp/tiff:PhotometricInterpretation | unicode     |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Path                                    | Formato de disco |
|-------|-----------------------------------------|-------------|
| 1     | /ifd/{ushort=262}                       | ushort      |
| 2     | /ifd/xmp/tiff:PhotometricInterpretation | unicode     |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Path                                    |
|-------|-----------------------------------------|
| 1     | /ifd/{ushort=262}                       |
| 2     | /ifd/xmp/tiff:photometricinterpretation |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.PhotometricInterpretation](../properties/props-system-photo-photometricinterpretation.md)
</dt> </dl>

 

 
