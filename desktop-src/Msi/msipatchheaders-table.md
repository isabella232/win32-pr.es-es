---
description: La tabla MsiPatchHeaders contiene las secuencias de encabezado de la revisión binaria que se usan para la validación de revisiones.
ms.assetid: aefdd365-1681-43e4-8470-04a5d6efd993
title: Tabla MsiPatchHeaders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a3fa4e037a31f3e913f13ff9c96735ed6760dc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277165"
---
# <a name="msipatchheaders-table"></a>Tabla MsiPatchHeaders

La tabla MsiPatchHeaders contiene las secuencias de encabezado de la revisión binaria que se usan para la validación de revisiones.

La tabla MsiPatchHeaders se utiliza cuando las claves de [tabla de archivos](file-table.md) largas producen un error al generar la secuencia de encabezado patch en la [tabla patch](patch-table.md). Esto puede deberse a la limitación del nombre de flujo que se describe en [limitaciones OLE en secuencias](ole-limitations-on-streams.md). En este caso, la tabla patch puede hacer referencia a la tabla MsiPatchHeaders para crear la secuencia de encabezado patch.

La tabla MsiPatchHeaders tiene las columnas siguientes.



| Columna    | Tipo                         | Clave | Nullable |
|-----------|------------------------------|-----|----------|
| StreamRef | [Identificador](identifier.md) | Y   | N        |
| Encabezado    | [Binario](binary.md)         | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="StreamRef"></span><span id="streamref"></span><span id="STREAMREF"></span>StreamRef
</dt> <dd>

La clave principal de la tabla que identifica de forma única un encabezado patch determinado.

</dd> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>Encabezado
</dt> <dd>

Esta columna es el encabezado de revisión de la secuencia binaria que se utiliza para la validación de revisiones.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La [acción PatchFiles](patchfiles-action.md)procesa esta tabla. Esta tabla normalmente se agrega al paquete de instalación mediante una transformación de un paquete de revisión. Normalmente no se crea directamente en un paquete de instalación.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
</dl>

 

 



