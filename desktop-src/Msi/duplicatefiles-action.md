---
description: La acción DuplicateFiles duplica los archivos instalados por la acción InstallFiles. Los archivos duplicados se pueden copiar en el mismo directorio con un nombre diferente o en otro directorio con el nombre original.
ms.assetid: 51cc0b3f-aa01-4f4d-9a4d-add832698061
title: Acción DuplicateFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7969440aed4361ad264baa0d30a9c1d16f0ca673c72a2a7c3c1326e5d393ffc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637717"
---
# <a name="duplicatefiles-action"></a>Acción DuplicateFiles

La acción DuplicateFiles duplica los archivos instalados por [la acción InstallFiles.](installfiles-action.md) Los archivos duplicados se pueden copiar en el mismo directorio con un nombre diferente o en otro directorio con el nombre original.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción DuplicateFiles debe ir después de [la acción InstallFiles](installfiles-action.md). La acción DuplicateFiles también debe ir después de la acción [PatchFiles](patchfiles-action.md) para evitar duplicar la versión sin revisiones del archivo.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                       |
|-------|--------------------------------------------------|
| \[1\] | Identificador del archivo duplicado.                   |
| \[6\] | Tamaño del archivo duplicado.                         |
| \[9\] | Identificador del directorio que contiene el archivo duplicado. |



 

## <a name="remarks"></a>Comentarios

La acción DuplicateFiles procesa una entrada de tabla [DuplicateFile](duplicatefile-table.md) solo si el componente vinculado a esa entrada se instala localmente. Para obtener más información, vea [Tabla de componentes](component-table.md).

La cadena del campo DestFolder es un nombre de propiedad cuyo valor se espera que se resuelva en una ruta de acceso completa. Esta propiedad puede ser cualquiera de las entradas de directorio de la tabla [Directory,](directory-table.md) cualquier propiedad de carpeta predefinida [**(CommonFilesFolder**](commonfilesfolder.md), por ejemplo) o una propiedad establecida por cualquier entrada de la tabla [AppSearch.](appsearch-table.md) Si la **propiedad DestFolder** no se evalúa como una ruta de acceso válida, la acción DuplicateFiles no hace nada para esa entrada.

Si el nombre del archivo de destino de la columna DestName de la tabla DuplicateFile se deja en blanco, el nombre del archivo de destino será el mismo que el nombre de archivo original.

Los archivos instalados por la acción DuplicateFiles se quitan mediante [la acción RemoveDuplicateFiles](removeduplicatefiles-action.md) cuando corresponda.

 

 



