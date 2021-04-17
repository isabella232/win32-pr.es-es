---
description: La acción DuplicateFiles duplica los archivos instalados por la acción InstallFiles. Los archivos duplicados se pueden copiar en el mismo directorio con un nombre diferente o en otro directorio con el nombre original.
ms.assetid: 51cc0b3f-aa01-4f4d-9a4d-add832698061
title: Acción DuplicateFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711f6bbd4716beb227dea348826bc302e2f4ba2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652754"
---
# <a name="duplicatefiles-action"></a>Acción DuplicateFiles

La acción DuplicateFiles duplica los archivos instalados por la acción [InstallFiles](installfiles-action.md) . Los archivos duplicados se pueden copiar en el mismo directorio con un nombre diferente o en otro directorio con el nombre original.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción DuplicateFiles debe aparecer después de la [acción InstallFiles](installfiles-action.md). La acción DuplicateFiles también debe aparecer después de la [acción PatchFiles](patchfiles-action.md) para evitar la duplicación de la versión no revisada del archivo.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                       |
|-------|--------------------------------------------------|
| \[1\] | Identificador del archivo duplicado.                   |
| \[6\] | Tamaño del archivo duplicado.                         |
| \[9\] | Identificador del directorio que contiene el archivo duplicado. |



 

## <a name="remarks"></a>Observaciones

La acción DuplicateFiles procesa una entrada de la [tabla DuplicateFile](duplicatefile-table.md) solo si el componente vinculado a esa entrada se está instalando localmente. Para obtener más información, vea [tabla de componentes](component-table.md).

La cadena en el campo DestFolder es un nombre de propiedad cuyo valor se espera que se resuelva como una ruta de acceso completa. Esta propiedad puede ser cualquiera de las entradas de directorio de la tabla de [directorio](directory-table.md) , cualquier propiedad de carpeta predefinida ([**CommonFilesFolder**](commonfilesfolder.md), por ejemplo) o una propiedad establecida por cualquier entrada de la tabla [AppSearch](appsearch-table.md) . Si la propiedad **DestFolder** no se evalúa como una ruta de acceso válida, la acción DuplicateFiles no hace nada para esa entrada.

Si el nombre del archivo de destino en la columna DestName de la tabla DuplicateFile se deja en blanco, el nombre de archivo de destino será el mismo que el nombre de archivo original.

La acción [RemoveDuplicateFiles](removeduplicatefiles-action.md) quita los archivos instalados por la acción DuplicateFiles cuando corresponda.

 

 



