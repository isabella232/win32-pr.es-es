---
description: La acción RemoveDuplicateFiles elimina los archivos instalados por la acción DuplicateFiles.
ms.assetid: 3d8ba4c5-775f-471e-a479-32fa6f7a1bf0
title: Acción RemoveDuplicateFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 555379f3810770abc9f91fd449e71434e9fa6244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809493"
---
# <a name="removeduplicatefiles-action"></a>Acción RemoveDuplicateFiles

La acción RemoveDuplicateFiles elimina los archivos instalados por la acción [DuplicateFiles](duplicatefiles-action.md) .

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción RemoveDuplicateFiles debe producirse después de la acción [InstallValidate](installvalidate-action.md) y antes de la acción [InstallFiles](installfiles-action.md) .

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                    |
|-------|-----------------------------------------------|
| \[1\] | Identificador del archivo quitado.                   |
| \[9\] | Identificador del directorio que contiene el archivo quitado. |



 

## <a name="remarks"></a>Observaciones

Para eliminar un archivo duplicado con la [acción DuplicateFiles](duplicatefiles-action.md) mediante la acción RemoveDuplicateFiles, se debe seleccionar el componente asociado a la entrada del archivo en la tabla DuplicateFile para su eliminación.

Use la columna DestFolder de la [tabla DuplicateFile](duplicatefile-table.md) para especificar el nombre de la propiedad cuyo valor identifica la carpeta de destino.

 

 



