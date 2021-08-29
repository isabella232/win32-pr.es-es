---
description: Directiva de metadatos de fotos para la propiedad System.Photo.CameraSerialNumber.
ms.assetid: 85f78f45-5e76-4d52-88a2-ac3c9e2b6a1e
title: Directiva de metadatos de fotos System.Photo.CameraSerialNumber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a730df8041534a377262d9bb55a19c9b109b35ab03e47d1b7e8cb88014987b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710142"
---
# <a name="systemphotocameraserialnumber-photo-metadata-policy"></a>Directiva de metadatos de fotos System.Photo.CameraSerialNumber

Directiva de metadatos de fotos para [la propiedad System.Photo.CameraSerialNumber.](../properties/props-system-photo-cameraserialnumber.md)

### <a name="pkey"></a>Pkey

PKEY \_ Photo \_ CameraSerialNumber

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

Si el archivo está en formato JPEG, el controlador leerá, escribirá y quitará los datos de la ruta de acceso siguiente:



| Pedido | Ruta de acceso                                   | Formato de disco | Requerido |
|-------|----------------------------------------|-------------|----------|
| 1     | /xmp/MicrosoftPhoto:CameraSerialNumber | Unicode     | Sí      |



 

### <a name="precedence-of-paths-tiff"></a>Precedencia de rutas de acceso (TIFF)

Si el archivo está en formato TIFF, el controlador leerá, escribirá y quitará los datos de la ruta de acceso siguiente.



| Pedido | Ruta de acceso                                       | Formato de disco | Requerido |
|-------|--------------------------------------------|-------------|----------|
| 1     | /ifd/xmp/MicrosoftPhoto:CameraSerialNumber | Unicode     | Sí      |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Photo.CameraSerialNumber](../properties/props-system-photo-cameraserialnumber.md)
</dt> </dl>

 

 
