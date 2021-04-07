---
description: El estado de instalación de un archivo complementario no depende de su propia información de versión del archivo, sino de la versión de su elemento primario complementario.
ms.assetid: 3c1e3507-8ed9-4ce8-8d38-6c8248a9e883
title: Archivos complementarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c927c377c7111e89c6f97b385610da9e09f8bdd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002483"
---
# <a name="companion-files"></a><span data-ttu-id="45d3a-103">Archivos complementarios</span><span class="sxs-lookup"><span data-stu-id="45d3a-103">Companion Files</span></span>

<span data-ttu-id="45d3a-104">El estado de instalación de un archivo complementario no depende de su propia información de versión del archivo, sino de la versión de su elemento primario complementario.</span><span class="sxs-lookup"><span data-stu-id="45d3a-104">The installation state of a companion file depends not on its own file versioning information, but on the versioning of its companion parent.</span></span> <span data-ttu-id="45d3a-105">Vea las [reglas de control de versiones de archivo](file-versioning-rules.md).</span><span class="sxs-lookup"><span data-stu-id="45d3a-105">See the [File Versioning Rules](file-versioning-rules.md).</span></span> <span data-ttu-id="45d3a-106">Para especificar un archivo complementario, la clave principal del elemento primario complementario de la [tabla de archivos](file-table.md) debe crearse en la columna versión del registro del complemento.</span><span class="sxs-lookup"><span data-stu-id="45d3a-106">To specify a companion file, the primary key of the companion parent in the [File table](file-table.md) must be authored into the Version column of the record for the companion.</span></span>

<span data-ttu-id="45d3a-107">En el ejemplo siguiente, Filea es el elemento primario Companion y FileB es el archivo complementario.</span><span class="sxs-lookup"><span data-stu-id="45d3a-107">In the following example, FileA is the companion parent and FileB is the companion file.</span></span>

<span data-ttu-id="45d3a-108">[Tabla de archivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="45d3a-108">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="45d3a-109">Archivo</span><span class="sxs-lookup"><span data-stu-id="45d3a-109">File</span></span>  | <span data-ttu-id="45d3a-110">Versión</span><span class="sxs-lookup"><span data-stu-id="45d3a-110">Version</span></span> |
|-------|---------|
| <span data-ttu-id="45d3a-111">Archivoa</span><span class="sxs-lookup"><span data-stu-id="45d3a-111">FileA</span></span> | <span data-ttu-id="45d3a-112">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="45d3a-112">1.0.0.0</span></span> |
| <span data-ttu-id="45d3a-113">FileB</span><span class="sxs-lookup"><span data-stu-id="45d3a-113">FileB</span></span> | <span data-ttu-id="45d3a-114">Archivoa</span><span class="sxs-lookup"><span data-stu-id="45d3a-114">FileA</span></span>   |



 

<span data-ttu-id="45d3a-115">En este ejemplo, el estado de instalación de FileB depende de las [reglas de control de versiones de archivo](file-versioning-rules.md) y de la información de versión de Filea.</span><span class="sxs-lookup"><span data-stu-id="45d3a-115">In this example, the installation state of FileB depends on the [File Versioning Rules](file-versioning-rules.md) and the versioning information for FileA.</span></span> <span data-ttu-id="45d3a-116">Si el instalador determina que la versión de Filea en el paquete debe instalarse en una versión anterior de Filea que ya existe en el equipo del usuario, también se instalará FileB desde el paquete, independientemente de la versión de cualquier FileB instalado.</span><span class="sxs-lookup"><span data-stu-id="45d3a-116">If the installer determines that the version of FileA in the package should be installed over an older version of FileA that already exists on the user's computer, it will also install FileB from the package regardless of the version of any installed FileB.</span></span>

<span data-ttu-id="45d3a-117">Tenga en cuenta que un archivo que es la ruta de acceso de la clave de su componente no debe ser un archivo complementario.</span><span class="sxs-lookup"><span data-stu-id="45d3a-117">Note that a file that is the key path for its component must not be a companion file.</span></span> <span data-ttu-id="45d3a-118">Como resultado, la lógica de control de versiones del archivo de ruta de acceso de la clave viene determinada por el archivo principal complementario.</span><span class="sxs-lookup"><span data-stu-id="45d3a-118">This would result in the versioning logic of the key path file being determined by the companion parent file.</span></span>

 

 



