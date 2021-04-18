---
description: La Directiva de metadatos de la fotografía para la propiedad System. Subject.
ms.assetid: 5ab7c74b-8a5e-4329-8a49-291470d406cc
title: Directiva de metadatos de la foto System. Subject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceabbab95a52a1155db949dbc60b4525dd5f9d73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706834"
---
# <a name="systemsubject-photo-metadata-policy"></a>Directiva de metadatos de la foto System. Subject

La Directiva de metadatos de la fotografía para la propiedad [System. Subject](../properties/props-system-subject.md) .

### <a name="pkey"></a>PKEY

\_Asunto PKEY

### <a name="containers"></a>Contenedores

JPEG, TIFF

### <a name="read-only"></a>Solo lectura

No

### <a name="output-propvariant-type"></a>Tipo de PROPVARIANT de salida

VT \_ LPWStr

### <a name="input-propvariant-type"></a>Tipo de PROPVARIANT de entrada

VT \_ LPWStr o VT \_ LPWStr

### <a name="conflict-resolution-policy"></a>Directiva de resolución de conflictos

Se reconcilian los valores de los distintos esquemas.

### <a name="jpeg-policy"></a>Directiva JPEG

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                     | Formato de disco    |
|-------|--------------------------|----------------|
| 1     | /app1/IFD/{ushort = 40095} | \_bytes Unicode |
| 2     | /app1/IFD/{ushort = 270}   | ascii          |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                     | Formato de disco    |
|-------|--------------------------|----------------|
| 1     | /app1/IFD/{ushort = 40095} | \_bytes Unicode |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                     |
|-------|--------------------------|
| 1     | /app1/IFD/{ushort = 40095} |
| 2     | /app1/IFD/{ushort = 270}   |



 

### <a name="tiff-policy"></a>Directiva TIFF

### <a name="read-paths"></a>Leer rutas de acceso



| Pedido | Ruta                | Formato de disco    |
|-------|---------------------|----------------|
| 1     | /IFD/{ushort = 40095} | \_bytes Unicode |
| 2     | /IFD/{ushort = 270}   | ascii          |



 

### <a name="write-paths"></a>Escribir rutas de acceso



| Pedido | Ruta                | Formato de disco    |
|-------|---------------------|----------------|
| 1     | /IFD/{ushort = 40095} | \_bytes Unicode |



 

### <a name="remove-paths"></a>Quitar rutas de acceso



| Pedido | Ruta                |
|-------|---------------------|
| 1     | /IFD/{ushort = 40095} |
| 2     | /IFD/{ushort = 270}   |



 

## <a name="remarks"></a>Observaciones

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[System. Subject](../properties/props-system-subject.md)
</dt> </dl>

 

 
