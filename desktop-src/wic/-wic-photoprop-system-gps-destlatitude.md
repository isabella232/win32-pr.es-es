---
description: Directiva de metadatos de fotos para la propiedad System.GPS.DestLatitude.
ms.assetid: 05284291-977d-49b8-ad92-365f68384960
title: Directiva de metadatos de fotos System.GPS.DestLatitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d57cce67b13235933816e244e17b5c761e1f0d230055eb82d683eb610579e5aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882355"
---
# <a name="systemgpsdestlatitude-photo-metadata-policy"></a>Directiva de metadatos de fotos System.GPS.DestLatitude

Directiva de metadatos de fotos para [la propiedad System.GPS.DestLatitude.](../properties/props-system-gps-destlatitude.md)

### <a name="pkey"></a>Pkey

PKEY \_ GPS \_ DestLatitude

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

Sí

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ VECTOR \| VT \_ R8

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT de entrada

VT \_ VECTOR \| VT \_ R8

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Este valor se genera a partir de System.GPS.DestLatitudeNumerator y System.GPS.DestLatitudeDenominator. No se puede escribir directamente. Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=20} |             |
| 2     | /xmp/exif:GPSDestLatitude |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                      | Formato de disco |
|-------|---------------------------|-------------|
| 1     | /app1/ifd/gps/{ushort=20} |             |
| 2     | /xmp/exif:GPSDestLatitude |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                      |
|-------|---------------------------|
| 1     | /app1/ifd/gps/{ushort=20} |
| 2     | /xmp/exif:gpsdestlatitude |



 

### <a name="tiff-policies"></a>Directivas TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta de acceso                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /ifd/gps/{ushort=20}          |             |
| 2     | /ifd/xmp/exif:GPSDestLatitude |             |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                          | Formato de disco |
|-------|-------------------------------|-------------|
| 1     | /ifd/gps/{ushort=20}          |             |
| 2     | /ifd/xmp/exif:GPSDestLatitude |             |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                          |
|-------|-------------------------------|
| 1     | /ifd/gps/{ushort=20}          |
| 2     | /ifd/xmp/exif:gpsdestlatitude |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.GPS.DestLatitude](../properties/props-system-gps-destlatitude.md)
</dt> </dl>

 

 
