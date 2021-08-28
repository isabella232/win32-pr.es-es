---
description: Directiva de metadatos de fotos para la propiedad System.Subject.
ms.assetid: 5ab7c74b-8a5e-4329-8a49-291470d406cc
title: Directiva de metadatos de fotos de System.Subject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9321e866c34027df3e932f84d532162def959cbaf365bb4020c19647d547adea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881975"
---
# <a name="systemsubject-photo-metadata-policy"></a>Directiva de metadatos de fotos de System.Subject

Directiva de metadatos de fotos para la [propiedad System.Subject.](../properties/props-system-subject.md)

### <a name="pkey"></a>Pkey

Asunto \_ PKEY

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo PROPVARIANT de salida

VT \_ LPWSTR

### <a name="input-propvariant-type"></a>Tipo PROPVARIANT de entrada

VT \_ LPWSTR o VT \_ LPWSTR

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Los valores de esquemas diferentes se concilian.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                     | Formato de disco    |
|-------|--------------------------|----------------|
| 1     | /app1/ifd/{ushort=40095} | bytes \_ unicode |
| 2     | /app1/ifd/{ushort=270}   | ascii          |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                     | Formato de disco    |
|-------|--------------------------|----------------|
| 1     | /app1/ifd/{ushort=40095} | bytes \_ unicode |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                     |
|-------|--------------------------|
| 1     | /app1/ifd/{ushort=40095} |
| 2     | /app1/ifd/{ushort=270}   |



 

### <a name="tiff-policy"></a>Directiva TIFF

### <a name="read-paths"></a>Rutas de acceso de lectura



| Pedido | Ruta de acceso                | Formato de disco    |
|-------|---------------------|----------------|
| 1     | /ifd/{ushort=40095} | bytes \_ unicode |
| 2     | /ifd/{ushort=270}   | ascii          |



 

### <a name="write-paths"></a>Rutas de acceso de escritura



| Pedido | Ruta de acceso                | Formato de disco    |
|-------|---------------------|----------------|
| 1     | /ifd/{ushort=40095} | bytes \_ unicode |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta de acceso                |
|-------|---------------------|
| 1     | /ifd/{ushort=40095} |
| 2     | /ifd/{ushort=270}   |



 

## <a name="remarks"></a>Comentarios

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System.Subject](../properties/props-system-subject.md)
</dt> </dl>

 

 
