---
description: La acción RemoveFiles quita los archivos instalados previamente por la acción InstallFiles.
ms.assetid: 1079be89-515c-443e-8927-46ddf7891a59
title: Acción RemoveFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b50e23a7d2eb3c9bb23575d83d000b053f0de06907541777e43b5476f8c722ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626455"
---
# <a name="removefiles-action"></a>Acción RemoveFiles

La acción RemoveFiles quita los archivos instalados previamente por [la acción InstallFiles.](installfiles-action.md) Cada uno de estos archivos se programa mediante un vínculo a una entrada de la [tabla Component.](component-table.md) Solo se quitan los archivos con componentes resueltos en el estado *msiInstallStateAbsent* o en el *estado msiInstallStateLocal* si el componente está instalado localmente.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Se debe llamar a la acción [InstallValidate](installvalidate-action.md) antes de llamar a RemoveFiles. Si se [usa una acción InstallFiles,](installfiles-action.md) debe aparecer después de RemoveFiles.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                    |
|-------|-----------------------------------------------|
| \[1\] | Identificador del archivo quitado.                   |
| \[9\] | Identificador del directorio que contiene el archivo quitado. |



 

## <a name="remarks"></a>Comentarios

La [tabla RemoveFile](removefile-table.md) se puede omitir en la base de datos del instalador si no hay archivos varios para quitar.

La acción RemoveFiles también puede quitar archivos especificados por el autor que no están instalados por la acción InstallFiles. Estos archivos se especifican en la [tabla RemoveFile.](removefile-table.md) Cada uno de estos archivos se programa mediante un vínculo a una entrada de la [tabla Component.](component-table.md) Los archivos cuyos componentes se resuelven en cualquier estado de acción activo (es decir, no en el estado Desactivado o Nulo) se quitan si el archivo existe en el directorio especificado. La eliminación de los archivos especificados en la tabla RemoveFile se intenta cuando se instala por primera vez el componente vinculado, durante una reinstalación y de nuevo cuando se quita el componente vinculado.

La acción RemoveFiles también puede quitar carpetas. Se quita una carpeta vacía si el valor de la columna FileName de la tabla RemoveFile es NULL.

Al quitar archivos instalados previamente, la acción RemoveFiles consulta los mismos campos de las mismas tablas que [](media-table.md) los que consulta la acción [InstallFiles](installfiles-action.md) con la excepción de que la acción RemoveFiles no usa la tabla Media.

El nombre del archivo de destino se puede especificar en texto localizado en la columna FileName de la tabla RemoveFile.

 

 



