---
description: Los directorios de la tabla de directorio especifican el diseño de una instalación de.
ms.assetid: 59f6ae09-d013-46d7-a1a7-0543f31ac487
title: Usar una propiedad de directorio en una ruta de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2789f6442072f3db6a96c0abb7db301038673f83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678460"
---
# <a name="using-a-directory-property-in-a-path"></a><span data-ttu-id="37ec4-103">Usar una propiedad de directorio en una ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="37ec4-103">Using a Directory Property in a Path</span></span>

<span data-ttu-id="37ec4-104">Los directorios de la [tabla de directorio](directory-table.md) especifican el diseño de una instalación de.</span><span class="sxs-lookup"><span data-stu-id="37ec4-104">The directories in the [Directory table](directory-table.md) specify the layout of an installation.</span></span> <span data-ttu-id="37ec4-105">Cuando el Windows Installer resuelve estos directorios durante la [acción CostFinalize](costfinalize-action.md), las claves de la tabla de directorio se convierten en [propiedades](properties.md) establecidas en rutas de acceso de directorio.</span><span class="sxs-lookup"><span data-stu-id="37ec4-105">When the Windows Installer resolves these directories during the [CostFinalize action](costfinalize-action.md), the keys in the Directory table become [properties](properties.md) set to directory paths.</span></span> <span data-ttu-id="37ec4-106">El instalador también establece siempre un número de [propiedades de carpeta del sistema](property-reference.md) estándar en las rutas de acceso a las carpetas del sistema.</span><span class="sxs-lookup"><span data-stu-id="37ec4-106">The installer also always sets a number of standard [System Folder Properties](property-reference.md) to system folder paths.</span></span>

<span data-ttu-id="37ec4-107">Se garantiza que los valores de las propiedades de la [carpeta del sistema](property-reference.md) terminan en un separador de directorios.</span><span class="sxs-lookup"><span data-stu-id="37ec4-107">The values of the [System Folder Properties](property-reference.md) are guaranteed to end in a directory separator.</span></span> <span data-ttu-id="37ec4-108">Solo se garantiza que los valores de todas las demás propiedades especificadas en la [tabla de directorio](directory-table.md) terminen en un separador de directorios después de que el instalador haya ejecutado la [acción CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="37ec4-108">The values of all other properties entered in the [Directory table](directory-table.md) are only guaranteed to end in a directory separator after the installer has run the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="37ec4-109">Antes de que se haya completado el costo, es posible que los valores de las propiedades especificadas en la tabla del directorio que no sean propiedades de la [carpeta del sistema](property-reference.md) no terminen en un separador de directorios.</span><span class="sxs-lookup"><span data-stu-id="37ec4-109">Before costing has completed, the values of properties entered in the Directory table which are not [System Folder Properties](property-reference.md) may not end in a directory separator.</span></span> <span data-ttu-id="37ec4-110">Por lo tanto, si la instalación establece las propiedades del directorio mediante [acciones personalizadas](custom-actions.md) en el paquete, los valores en referencia podrían no terminar con un separador de directorios.</span><span class="sxs-lookup"><span data-stu-id="37ec4-110">Therefore, if your installation sets directory properties using [custom actions](custom-actions.md) in the package, the values on reference might not end with a directory separator.</span></span>

<span data-ttu-id="37ec4-111">Por lo tanto, las propiedades de directorio que finalizan con un separador de directorio se pueden usar en una cadena de ruta de acceso sin incluir explícitamente el separador de directorios.</span><span class="sxs-lookup"><span data-stu-id="37ec4-111">Directory properties ending with a directory separator can therefore be used in a path string without explicitly including the directory separator.</span></span> <span data-ttu-id="37ec4-112">Por ejemplo, si el valor de DirectoryProperty termina con un separador de directorios, la cadena siguiente especifica correctamente la ruta de acceso al *archivo* en el *subdirectorio* .</span><span class="sxs-lookup"><span data-stu-id="37ec4-112">For example, if the value of DirectoryProperty ends with a directory separator, the following string correctly specifies the path to *file* in *subdirectory*</span></span>

``` syntax
[DirectoryProperty]subdirectory\file
```

<span data-ttu-id="37ec4-113">y la cadena de ruta de acceso siguiente es incorrecta.</span><span class="sxs-lookup"><span data-stu-id="37ec4-113">and the following path string is incorrect.</span></span>

``` syntax
[DirectoryProperty]\subdirectory\file
```

 

 



