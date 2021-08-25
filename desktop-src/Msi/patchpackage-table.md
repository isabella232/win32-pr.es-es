---
description: En la tabla PatchPackage se describen todos los paquetes de revisión que se han aplicado a este producto. Para cada paquete de revisión, se proporciona el identificador único de la revisión junto con información sobre la imagen multimedia en la que se encuentra la revisión.
ms.assetid: 212d99dd-c80c-42ca-9dfa-819ae1813006
title: Tabla PatchPackage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da4027913854436072330a69a788ca9dc9b1365a71b82fd1727227e33d8a203b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926125"
---
# <a name="patchpackage-table"></a>Tabla PatchPackage

En la tabla PatchPackage se describen todos los paquetes de revisión que se han aplicado a este producto. Para cada paquete de revisión, se proporciona el identificador único de la revisión junto con información sobre la imagen multimedia en la que se encuentra la revisión.

La tabla PatchPackage tiene las columnas siguientes.



| Columna  | Tipo                   | Clave | Nullable |
|---------|------------------------|-----|----------|
| PatchId | [GUID](guid.md)       | Y   | N        |
| Medios\_ | [Entero](integer.md) | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="PatchId"></span><span id="patchid"></span><span id="PATCHID"></span>PatchId
</dt> <dd>

Esta columna contiene un identificador único para esta revisión concreta.

</dd> <dt>

<span id="Media_"></span><span id="media_"></span><span id="MEDIA_"></span>Medio\_
</dt> <dd>

Esta columna es una clave externa para la columna DiskId de la [tabla](media-table.md) multimedia e indica el disco que contiene el paquete de revisión.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La tabla PatchPackage es necesaria en cada paquete de revisión. Si falta la tabla, se produce un error al intentar instalar la revisión con el mensaje "Error 2768: La transformación en el paquete de revisión no es válida". Normalmente, esta tabla se agrega al paquete de instalación mediante una transformación de un paquete de revisión. Normalmente no se ha escrito directamente en un paquete de instalación.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



