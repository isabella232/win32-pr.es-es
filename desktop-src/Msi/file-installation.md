---
description: 'Una vez completado el costo de los archivos, el instalador tiene toda la información necesaria para procesar las dos acciones de manipulación de archivos: DuplicateFiles y MoveFiles.'
ms.assetid: 2e6d6eb3-1e71-46e6-a946-d9cc0b209325
title: Instalación de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472c58db3dc2e9094a26d57f871359a38930877b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156632"
---
# <a name="file-installation"></a>Instalación de archivos

Una vez completado el costo de los [archivos](file-costing.md) , el instalador tiene toda la información necesaria para procesar las dos acciones de manipulación de archivos: [DuplicateFiles](duplicatefiles-action.md) y [MoveFiles](movefiles-action.md).

Use la [acción DuplicateFiles](duplicatefiles-action.md) para especificar los archivos que el instalador va a duplicar en la [tabla DuplicateFile](duplicatefile-table.md). Use la [acción MoveFiles](movefiles-action.md)para determinar qué archivos se van a trasladar consultando la [tabla MoveFile](movefile-table.md).

Tenga en cuenta que el campo de opciones de la [tabla MoveFile](movefile-table.md) especifica si el archivo original se va a eliminar o no de su ubicación actual. Los archivos que se mueven o copian mediante la acción MoveFiles no se eliminan cuando se desinstala el producto.

La [acción InstallFiles](installfiles-action.md) se llama una vez completadas todas las demás operaciones de manipulación de archivos. La acción InstallFiles procesa la [tabla de medios](media-table.md), la [tabla de archivos](file-table.md)y la tabla de [componentes](component-table.md) para determinar qué archivos se copiarán del origen al destino.

La [acción InstallFiles](installfiles-action.md) crea la estructura de directorios necesaria para instalar todos los archivos. Si se requiere la instalación de una carpeta vacía explícitamente, se puede llamar a la [acción CreateFolders](createfolders-action.md) para crearla.

 

 



