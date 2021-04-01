---
description: La acción PatchFiles consulta la tabla patch para determinar qué revisiones se van a aplicar. La acción PatchFiles también realiza la revisión en bytes de los archivos.
ms.assetid: 4026755e-a006-40c0-8816-de5358f4582e
title: Acción PatchFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53583a93089444f014d9cc837fb18acf21cec82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909830"
---
# <a name="patchfiles-action"></a>Acción PatchFiles

La acción PatchFiles consulta la [tabla patch](patch-table.md) para determinar qué revisiones se van a aplicar. La acción PatchFiles también realiza la revisión en bytes de los archivos.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Si el archivo que se va a revisar no está instalado, la acción PatchFiles debe aparecer después de la [acción InstallFiles](installfiles-action.md) que instala el archivo. Los archivos instalados anteriormente se pueden revisar en cualquier momento de la secuencia de acciones. La [acción DuplicateFiles](duplicatefiles-action.md) debe aparecer después de la acción PatchFiles para evitar la duplicación de la versión no revisada del archivo.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                    |
|-------|-----------------------------------------------|
| \[1\] | Identificador del archivo revisado.                   |
| \[2\] | Identificador del directorio que contiene el archivo revisado. |
| \[3\] | Tamaño de la revisión en bytes.                       |



 

 

 



