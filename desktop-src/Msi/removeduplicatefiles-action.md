---
description: La acción RemoveDuplicateFiles elimina los archivos instalados por la acción DuplicateFiles.
ms.assetid: 3d8ba4c5-775f-471e-a479-32fa6f7a1bf0
title: Acción RemoveDuplicateFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7527e7bd4dc66fe4d57f8c23654f1138e781a33064fc0a4a2694987c7ccdb66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074625"
---
# <a name="removeduplicatefiles-action"></a>Acción RemoveDuplicateFiles

La acción RemoveDuplicateFiles elimina los archivos instalados por la [acción DuplicateFiles.](duplicatefiles-action.md)

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción RemoveDuplicateFiles debe producirse después de la acción [InstallValidate](installvalidate-action.md) y antes de [la acción InstallFiles.](installfiles-action.md)

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                    |
|-------|-----------------------------------------------|
| \[1\] | Identificador del archivo quitado.                   |
| \[9\] | Identificador del directorio que contiene el archivo quitado. |



 

## <a name="remarks"></a>Comentarios

Para eliminar un archivo duplicado con la acción [DuplicateFiles](duplicatefiles-action.md) mediante la acción RemoveDuplicateFiles, se debe seleccionar el componente asociado a la entrada del archivo en la tabla DuplicateFile para su eliminación.

Use la columna DestFolder de la tabla [DuplicateFile para](duplicatefile-table.md) especificar el nombre de propiedad cuyo valor identifica la carpeta de destino.

 

 



