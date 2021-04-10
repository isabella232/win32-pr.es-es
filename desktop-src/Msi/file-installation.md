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
# <a name="file-installation"></a><span data-ttu-id="361d7-103">Instalación de archivos</span><span class="sxs-lookup"><span data-stu-id="361d7-103">File Installation</span></span>

<span data-ttu-id="361d7-104">Una vez completado el costo de los [archivos](file-costing.md) , el instalador tiene toda la información necesaria para procesar las dos acciones de manipulación de archivos: [DuplicateFiles](duplicatefiles-action.md) y [MoveFiles](movefiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="361d7-104">Once [file costing](file-costing.md) has been completed, the installer has all the information required to process the two file manipulation actions: [DuplicateFiles](duplicatefiles-action.md) and [MoveFiles](movefiles-action.md).</span></span>

<span data-ttu-id="361d7-105">Use la [acción DuplicateFiles](duplicatefiles-action.md) para especificar los archivos que el instalador va a duplicar en la [tabla DuplicateFile](duplicatefile-table.md).</span><span class="sxs-lookup"><span data-stu-id="361d7-105">Use the [DuplicateFiles action](duplicatefiles-action.md) to specify the files the installer is to duplicate in the [DuplicateFile table](duplicatefile-table.md).</span></span> <span data-ttu-id="361d7-106">Use la [acción MoveFiles](movefiles-action.md)para determinar qué archivos se van a trasladar consultando la [tabla MoveFile](movefile-table.md).</span><span class="sxs-lookup"><span data-stu-id="361d7-106">Use the [MoveFiles action](movefiles-action.md)to determine which files to move by querying the [MoveFile table](movefile-table.md).</span></span>

<span data-ttu-id="361d7-107">Tenga en cuenta que el campo de opciones de la [tabla MoveFile](movefile-table.md) especifica si el archivo original se va a eliminar o no de su ubicación actual.</span><span class="sxs-lookup"><span data-stu-id="361d7-107">Note that the Options field of the [MoveFile table](movefile-table.md) specifies whether or not the original file is to be deleted from its current location.</span></span> <span data-ttu-id="361d7-108">Los archivos que se mueven o copian mediante la acción MoveFiles no se eliminan cuando se desinstala el producto.</span><span class="sxs-lookup"><span data-stu-id="361d7-108">Files that are moved or copied by the MoveFiles action are not deleted when the product is uninstalled.</span></span>

<span data-ttu-id="361d7-109">La [acción InstallFiles](installfiles-action.md) se llama una vez completadas todas las demás operaciones de manipulación de archivos.</span><span class="sxs-lookup"><span data-stu-id="361d7-109">The [InstallFiles action](installfiles-action.md) is called once all other file manipulation operations have completed.</span></span> <span data-ttu-id="361d7-110">La acción InstallFiles procesa la [tabla de medios](media-table.md), la [tabla de archivos](file-table.md)y la tabla de [componentes](component-table.md) para determinar qué archivos se copiarán del origen al destino.</span><span class="sxs-lookup"><span data-stu-id="361d7-110">The InstallFiles action processes the [Media table](media-table.md), the [File table](file-table.md), and the [Component table](component-table.md) to determine which files will be copied from the source to the destination.</span></span>

<span data-ttu-id="361d7-111">La [acción InstallFiles](installfiles-action.md) crea la estructura de directorios necesaria para instalar todos los archivos.</span><span class="sxs-lookup"><span data-stu-id="361d7-111">The [InstallFiles action](installfiles-action.md) creates the directory structure necessary to install all files.</span></span> <span data-ttu-id="361d7-112">Si se requiere la instalación de una carpeta vacía explícitamente, se puede llamar a la [acción CreateFolders](createfolders-action.md) para crearla.</span><span class="sxs-lookup"><span data-stu-id="361d7-112">If an explicitly empty folder is required to be installed, the [CreateFolders action](createfolders-action.md) may be called to create it.</span></span>

 

 



