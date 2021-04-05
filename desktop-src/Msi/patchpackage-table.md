---
description: La tabla PatchPackage describe todos los paquetes de revisiones que se han aplicado a este producto. Para cada paquete de revisión, se proporciona el identificador único de la revisión junto con información sobre la imagen multimedia en la que se encuentra la revisión.
ms.assetid: 212d99dd-c80c-42ca-9dfa-819ae1813006
title: Tabla PatchPackage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13bf9fc03012ca54a0b2144e97c828c968c68da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279328"
---
# <a name="patchpackage-table"></a>Tabla PatchPackage

La tabla PatchPackage describe todos los paquetes de revisiones que se han aplicado a este producto. Para cada paquete de revisión, se proporciona el identificador único de la revisión junto con información sobre la imagen multimedia en la que se encuentra la revisión.

La tabla PatchPackage tiene las columnas siguientes.



| Columna  | Tipo                   | Clave | Nullable |
|---------|------------------------|-----|----------|
| PatchId | [GUID](guid.md)       | Y   | N        |
| Medios\_ | [Entero](integer.md) | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="PatchId"></span><span id="patchid"></span><span id="PATCHID"></span>PatchId
</dt> <dd>

Esta columna contiene un identificador único para esta revisión en particular.

</dd> <dt>

<span id="Media_"></span><span id="media_"></span><span id="MEDIA_"></span>Soporte\_
</dt> <dd>

Esta columna es una clave externa de la columna de dipatine de la [tabla de medios](media-table.md) e indica el disco que contiene el paquete de revisión.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La tabla PatchPackage es necesaria en cada paquete de revisión. Si falta la tabla, se producirá un error en los intentos de instalación de la revisión con el mensaje "error 2768: la transformación del paquete de revisión no es válida". Esta tabla normalmente se agrega al paquete de instalación mediante una transformación de un paquete de revisión. Normalmente no se crea directamente en un paquete de instalación.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



