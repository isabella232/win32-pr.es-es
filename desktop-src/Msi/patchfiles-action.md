---
description: La acción PatchFiles consulta la tabla Patch para determinar qué revisiones se van a aplicar. La acción PatchFiles también realiza la aplicación de revisiones de bytes de los archivos.
ms.assetid: 4026755e-a006-40c0-8816-de5358f4582e
title: Acción PatchFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6186f150df1871e424b1dc6e4f466d148a1ce2ed51ffd9cd8170a1221e2f0b7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082675"
---
# <a name="patchfiles-action"></a>Acción PatchFiles

La acción PatchFiles consulta la [tabla Patch para](patch-table.md) determinar qué revisiones se van a aplicar. La acción PatchFiles también realiza la aplicación de revisiones de bytes de los archivos.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Si el archivo al que se va a aplicar la revisión no está instalado, la acción PatchFiles debe ir después de la acción [InstallFiles](installfiles-action.md) que instala el archivo. Los archivos instalados anteriormente se pueden aplicar revisiones en cualquier punto de la secuencia de acciones. La [acción DuplicateFiles debe](duplicatefiles-action.md) ir después de la acción PatchFiles para evitar duplicar la versión sin revisiones del archivo.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                    |
|-------|-----------------------------------------------|
| \[1\] | Identificador del archivo con revisión.                   |
| \[2\] | Identificador del directorio que contiene el archivo con revisión. |
| \[3\] | Tamaño de la revisión en bytes.                       |



 

 

 



