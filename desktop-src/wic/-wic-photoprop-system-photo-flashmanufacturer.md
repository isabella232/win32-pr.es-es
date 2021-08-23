---
description: Directiva de metadatos de fotos para la propiedad System.Photo.FlashManufacturer.
ms.assetid: f62e85ec-2dc6-456b-a43b-7b76d162b608
title: Directiva de metadatos de fotos de System.Photo.FlashManufacturer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0d81a57967e5b3f1139b0efabd85266bec80d10e06fb18251b0a6b9ef61a1e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964814"
---
# <a name="systemphotoflashmanufacturer-photo-metadata-policy"></a>Directiva de metadatos de fotos de System.Photo.FlashManufacturer

Directiva de metadatos de fotos para [la propiedad System.Photo.FlashManufacturer.](../properties/props-system-photo-flashmanufacturer.md)

### <a name="pkey"></a>Pkey

PKEY \_ Photo \_ FlashManufacturer

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ LPWSTR

### <a name="input-type"></a>Tipo de entrada

String.

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="precedence-of-paths-jpeg"></a>Prioridad de las rutas de acceso (JPEG)

Si el archivo está en formato JPEG, el controlador usará la ruta de acceso siguiente al leer o escribir los datos.



| Pedido | Ruta de acceso                                  | Formato de disco | Formato de datos | Requerido |
|-------|---------------------------------------|-------------|-------------|----------|
| 1     | /xmp/MicrosoftPhoto:FlashManufacturer | Unicode     |             | Sí      |



 

### <a name="precedence-of-paths-tiff"></a>Precedencia de rutas de acceso (TIFF)

Si el archivo está en formato TIFF, el controlador usará el siguiente orden de prioridad al leer o escribir los datos.



| Pedido | Ruta de acceso                                      | Formato de disco | Formato de datos | Requerido |
|-------|-------------------------------------------|-------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:FlashManufacturer | Unicode     |             | Sí      |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.FlashManufacturer](../properties/props-system-photo-flashmanufacturer.md)
</dt> </dl>

 

 
