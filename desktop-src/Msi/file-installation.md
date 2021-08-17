---
description: 'Una vez completado el costo de los archivos, el instalador tiene toda la información necesaria para procesar las dos acciones de manipulación de archivos: DuplicateFiles y MoveFiles.'
ms.assetid: 2e6d6eb3-1e71-46e6-a946-d9cc0b209325
title: Instalación de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 005a987a7e61f646f58abd0ec699ce03bd29d85dfa2ddb01e8f693750acda740
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636703"
---
# <a name="file-installation"></a>Instalación de archivos

Una [vez completado el](file-costing.md) costo de los archivos, el instalador tiene toda la información necesaria para procesar las dos acciones de manipulación de archivos: [DuplicateFiles](duplicatefiles-action.md) y [MoveFiles.](movefiles-action.md)

Use la [acción DuplicateFiles](duplicatefiles-action.md) para especificar los archivos que el instalador debe duplicar en la [tabla DuplicateFile](duplicatefile-table.md). Use la [acción MoveFiles para](movefiles-action.md)determinar qué archivos se deben mover consultando la [tabla MoveFile](movefile-table.md).

Tenga en cuenta que el campo Opciones de la [tabla MoveFile](movefile-table.md) especifica si el archivo original se va a eliminar o no de su ubicación actual. Los archivos que se mueven o copian mediante la acción MoveFiles no se eliminan cuando se desinstala el producto.

Se [llama a la acción InstallFiles](installfiles-action.md) una vez que se han completado todas las demás operaciones de manipulación de archivos. La acción InstallFiles procesa la tabla [Media](media-table.md), la tabla [File](file-table.md)y la tabla [Component](component-table.md) para determinar qué archivos se copiarán del origen al destino.

La [acción InstallFiles crea](installfiles-action.md) la estructura de directorios necesaria para instalar todos los archivos. Si es necesario instalar una carpeta vacía explícitamente, se puede llamar a la [acción CreateFolders](createfolders-action.md) para crearla.

 

 



