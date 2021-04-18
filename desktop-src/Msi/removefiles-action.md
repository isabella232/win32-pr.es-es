---
description: La acción RemoveFiles quita los archivos instalados previamente por la acción InstallFiles.
ms.assetid: 1079be89-515c-443e-8927-46ddf7891a59
title: Acción RemoveFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 174e477d512401c8ff6f1ff091b7c67f26e86f16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667939"
---
# <a name="removefiles-action"></a>Acción RemoveFiles

La acción RemoveFiles quita los archivos instalados previamente por la acción [InstallFiles](installfiles-action.md) . Cada uno de estos archivos se valida mediante un vínculo a una entrada en la tabla de [componentes](component-table.md) . Solo se quitarán los archivos con componentes que se resuelvan en el estado *msiInstallStateAbsent* o *msiInstallStateLocal* si el componente está instalado localmente.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Se debe llamar a la acción [InstallValidate](installvalidate-action.md) antes de llamar a RemoveFiles. Si se usa una acción [InstallFiles](installfiles-action.md) , debe aparecer después de RemoveFiles.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                    |
|-------|-----------------------------------------------|
| \[1\] | Identificador del archivo quitado.                   |
| \[9\] | Identificador del directorio que contiene el archivo quitado. |



 

## <a name="remarks"></a>Observaciones

La tabla [RemoveFile](removefile-table.md) se puede omitir en la base de datos del instalador si no hay archivos varios que quitar.

La acción RemoveFiles también puede quitar archivos especificados por el autor que no se instalan mediante la acción InstallFiles. Estos archivos se especifican en la tabla [RemoveFile](removefile-table.md) . Cada uno de estos archivos se valida mediante un vínculo a una entrada en la tabla de [componentes](component-table.md) . Los archivos cuyos componentes se resuelven en cualquier estado de acción activo (es decir, no en estado desactivado o nulo) se quitan si el archivo existe en el directorio especificado. La eliminación de los archivos especificados en la tabla RemoveFile se intenta cuando el componente vinculado se instala por primera vez, durante una reinstalación y de nuevo cuando se quita el componente vinculado.

La acción RemoveFiles también puede quitar carpetas. Si el valor de la columna FileName de la tabla RemoveFile es null, se quita una carpeta vacía.

Al quitar los archivos instalados anteriormente, la acción RemoveFiles consulta los mismos campos de las mismas tablas que los consultados por la acción [InstallFiles](installfiles-action.md) con la excepción de que la acción RemoveFiles no utiliza la [tabla de medios](media-table.md) .

El nombre de archivo de destino se puede especificar en texto localizado en la columna FileName de la tabla RemoveFile.

 

 



