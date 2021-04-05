---
description: El instalador mantiene información acerca de la estructura de directorios de instalación en la tabla de directorios.
ms.assetid: 31390138-b1d0-4f0b-9304-6e7c69e6a736
title: Especificar la estructura de directorios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a87880921799158559e28fed2c6dde97c9a331
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908120"
---
# <a name="specifying-directory-structure"></a><span data-ttu-id="fd036-103">Especificar la estructura de directorios</span><span class="sxs-lookup"><span data-stu-id="fd036-103">Specifying Directory Structure</span></span>

<span data-ttu-id="fd036-104">El instalador mantiene información acerca de la estructura de directorios de instalación en la [tabla de directorios](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="fd036-104">The installer keeps information about the installation directory structure in the [Directory Table](directory-table.md).</span></span> <span data-ttu-id="fd036-105">Vea el [Grupo tablas principales](core-tables-group.md).</span><span class="sxs-lookup"><span data-stu-id="fd036-105">See the [Core Tables Group](core-tables-group.md).</span></span> <span data-ttu-id="fd036-106">En esta sección, agregará información de la estructura de directorios para el ejemplo del Bloc de notas a la base de datos vacía que creó en la [importación de una base de datos en blanco](importing-a-blank-database.md).</span><span class="sxs-lookup"><span data-stu-id="fd036-106">In this section you add directory structure information for the Notepad sample to the empty database you created in [Importing a Blank Database](importing-a-blank-database.md).</span></span> <span data-ttu-id="fd036-107">Use el editor de bases de datos orca que se proporciona con el SDK u otro editor para abrir la tabla de directorio en MNP2000.msi.</span><span class="sxs-lookup"><span data-stu-id="fd036-107">Use the database editor Orca that is provided with the SDK, or another editor, to open the Directory Table in MNP2000.msi.</span></span> <span data-ttu-id="fd036-108">Utilice el editor de para escribir los datos siguientes en la tabla de directorios en blanco.</span><span class="sxs-lookup"><span data-stu-id="fd036-108">Use the editor to enter the following data into the blank Directory table.</span></span>

[<span data-ttu-id="fd036-109">Tabla de directorio</span><span class="sxs-lookup"><span data-stu-id="fd036-109">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="fd036-110">Directorio</span><span class="sxs-lookup"><span data-stu-id="fd036-110">Directory</span></span>                                        | <span data-ttu-id="fd036-111">Directorio \_ primario</span><span class="sxs-lookup"><span data-stu-id="fd036-111">Directory\_Parent</span></span>                                | <span data-ttu-id="fd036-112">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="fd036-112">DefaultDir</span></span>        |
|--------------------------------------------------|--------------------------------------------------|-------------------|
| [<span data-ttu-id="fd036-113">**TARGETDIR**</span><span class="sxs-lookup"><span data-stu-id="fd036-113">**TARGETDIR**</span></span>](targetdir.md)                   |                                                  | <span data-ttu-id="fd036-114">SourceDir</span><span class="sxs-lookup"><span data-stu-id="fd036-114">SourceDir</span></span>         |
| [<span data-ttu-id="fd036-115">**ProgramFilesFolder**</span><span class="sxs-lookup"><span data-stu-id="fd036-115">**ProgramFilesFolder**</span></span>](programfilesfolder.md) | [<span data-ttu-id="fd036-116">**TARGETDIR**</span><span class="sxs-lookup"><span data-stu-id="fd036-116">**TARGETDIR**</span></span>](targetdir.md)                   | <span data-ttu-id="fd036-117">.</span><span class="sxs-lookup"><span data-stu-id="fd036-117">.</span></span>                 |
| <span data-ttu-id="fd036-118">ARTSDIR</span><span class="sxs-lookup"><span data-stu-id="fd036-118">ARTSDIR</span></span>                                          | <span data-ttu-id="fd036-119">NOTEPADDIR</span><span class="sxs-lookup"><span data-stu-id="fd036-119">NOTEPADDIR</span></span>                                       | <span data-ttu-id="fd036-120">Arts: eventos</span><span class="sxs-lookup"><span data-stu-id="fd036-120">Arts:Events</span></span>       |
| <span data-ttu-id="fd036-121">HOLDIR</span><span class="sxs-lookup"><span data-stu-id="fd036-121">HOLDIR</span></span>                                           | <span data-ttu-id="fd036-122">MONDIR</span><span class="sxs-lookup"><span data-stu-id="fd036-122">MONDIR</span></span>                                           | <span data-ttu-id="fd036-123">.: Festivos</span><span class="sxs-lookup"><span data-stu-id="fd036-123">.:Holidays</span></span>        |
| <span data-ttu-id="fd036-124">MENUDIR</span><span class="sxs-lookup"><span data-stu-id="fd036-124">MENUDIR</span></span>                                          | <span data-ttu-id="fd036-125">NOTEPADDIR</span><span class="sxs-lookup"><span data-stu-id="fd036-125">NOTEPADDIR</span></span>                                       | <span data-ttu-id="fd036-126">Menú</span><span class="sxs-lookup"><span data-stu-id="fd036-126">Menu</span></span>              |
| <span data-ttu-id="fd036-127">MONDIR</span><span class="sxs-lookup"><span data-stu-id="fd036-127">MONDIR</span></span>                                           | <span data-ttu-id="fd036-128">NOTEPADDIR</span><span class="sxs-lookup"><span data-stu-id="fd036-128">NOTEPADDIR</span></span>                                       | <span data-ttu-id="fd036-129">Canaliza</span><span class="sxs-lookup"><span data-stu-id="fd036-129">Gate</span></span>              |
| <span data-ttu-id="fd036-130">NOTEPADDIR</span><span class="sxs-lookup"><span data-stu-id="fd036-130">NOTEPADDIR</span></span>                                       | [<span data-ttu-id="fd036-131">**ProgramFilesFolder**</span><span class="sxs-lookup"><span data-stu-id="fd036-131">**ProgramFilesFolder**</span></span>](programfilesfolder.md) | <span data-ttu-id="fd036-132">\_Estacionamiento rojo: Bloc de notas</span><span class="sxs-lookup"><span data-stu-id="fd036-132">Red\_Park:Notepad</span></span> |
| <span data-ttu-id="fd036-133">SPORTDIR</span><span class="sxs-lookup"><span data-stu-id="fd036-133">SPORTDIR</span></span>                                         | <span data-ttu-id="fd036-134">NOTEPADDIR</span><span class="sxs-lookup"><span data-stu-id="fd036-134">NOTEPADDIR</span></span>                                       | <span data-ttu-id="fd036-135">Deportes: eventos</span><span class="sxs-lookup"><span data-stu-id="fd036-135">Sports:Events</span></span>     |



 

<span data-ttu-id="fd036-136">Al escribir estos datos en la tabla de directorio se especifican las estructuras de directorio de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="fd036-136">Entering this data into the Directory table specifies the source and target directory structures.</span></span> <span data-ttu-id="fd036-137">Vea la [tabla de directorios](directory-table.md) y [el uso de los temas de la tabla de directorios](using-the-directory-table.md) .</span><span class="sxs-lookup"><span data-stu-id="fd036-137">See the [Directory Table](directory-table.md) and [Using the Directory Table](using-the-directory-table.md) topics.</span></span> <span data-ttu-id="fd036-138">Tenga en cuenta que la propiedad [**targetDir**](targetdir.md) debe ser el nombre de una raíz en la tabla de directorio de cada instalación.</span><span class="sxs-lookup"><span data-stu-id="fd036-138">Note that the [**TARGETDIR**](targetdir.md) property must be the name of one root in the Directory table of every installation.</span></span>

[<span data-ttu-id="fd036-139">Continuar</span><span class="sxs-lookup"><span data-stu-id="fd036-139">Continue</span></span>](specifying-components.md)

 

 



