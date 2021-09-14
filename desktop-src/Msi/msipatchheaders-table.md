---
description: La tabla MsiPatchHeaders contiene los flujos de encabezado de revisión binarios que se usan para la validación de revisiones.
ms.assetid: aefdd365-1681-43e4-8470-04a5d6efd993
title: Tabla MsiPatchHeaders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a3fa4e037a31f3e913f13ff9c96735ed6760dc4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169794"
---
# <a name="msipatchheaders-table"></a>Tabla MsiPatchHeaders

La tabla MsiPatchHeaders contiene los flujos de encabezado de revisión binarios que se usan para la validación de revisiones.

La tabla MsiPatchHeaders se [](file-table.md) usa cuando las claves de tabla de archivos largas generan un error al generar la secuencia de encabezado de revisión en la [tabla Patch](patch-table.md). Esto puede deberse a la limitación del nombre de secuencia descrita en [Limitaciones de OLE Secuencias](ole-limitations-on-streams.md). En este caso, la tabla Patch puede hacer referencia a la tabla MsiPatchHeaders para crear el flujo de encabezado de revisión.

La tabla MsiPatchHeaders tiene las columnas siguientes.



| Columna    | Tipo                         | Clave | Nullable |
|-----------|------------------------------|-----|----------|
| StreamRef | [Identificador](identifier.md) | Y   | No        |
| Encabezado    | [Binario](binary.md)         | No   | No        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="StreamRef"></span><span id="streamref"></span><span id="STREAMREF"></span>StreamRef
</dt> <dd>

Clave principal de la tabla que identifica de forma única un encabezado de revisión determinado.

</dd> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>Rúbrica
</dt> <dd>

Esta columna es el encabezado de revisión de flujo binario usado para la validación de revisiones.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta tabla se procesa mediante la [acción PatchFiles](patchfiles-action.md). Normalmente, esta tabla se agrega al paquete de instalación mediante una transformación de un paquete de revisión. Normalmente no se ha escrito directamente en un paquete de instalación.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
</dl>

 

 



