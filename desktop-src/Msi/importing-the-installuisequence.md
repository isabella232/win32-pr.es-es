---
description: La secuencia de la interfaz de usuario se importa en la base de datos de ejemplo.
ms.assetid: 750e4dc6-91ff-4d9a-a968-abc2515e3b7c
title: Importación de InstallUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f20de59a752da6d24a5f3e7fed94e00aa4f0048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277743"
---
# <a name="importing-the-installuisequence"></a><span data-ttu-id="396fc-103">Importación de InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="396fc-103">Importing the InstallUISequence</span></span>

<span data-ttu-id="396fc-104">En la [tabla InstallUISequence](installuisequence-table.md) se enumeran las acciones que se ejecutan cuando se ejecuta la [acción de instalación](install-action.md) de nivel superior y el nivel interno de la interfaz de usuario se establece en interfaz de usuario completa o en interfaz de usuario reducida.</span><span class="sxs-lookup"><span data-stu-id="396fc-104">The [InstallUISequence table](installuisequence-table.md) lists actions that are executed when the top-level [INSTALL action](install-action.md) is executed and the internal user interface level is set to full UI or reduced UI.</span></span> <span data-ttu-id="396fc-105">El instalador omite las acciones de esta tabla si el nivel de la interfaz de usuario se establece en la interfaz de usuario básica o en ninguna interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="396fc-105">The installer skips the actions in this table if the user interface level is set to basic UI or to no UI.</span></span> <span data-ttu-id="396fc-106">Vea [los niveles](user-interface-levels.md)de interfaz [de usuario y](user-interface.md) interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="396fc-106">See [User Interface](user-interface.md) and [User Interface Levels](user-interface-levels.md).</span></span> <span data-ttu-id="396fc-107">Vea [grupo de tablas de procedimientos de instalación](installation-procedure-tables-group.md), [uso de una tabla de secuencia](using-a-sequence-table.md)y el [ejemplo detallado](sequence-table-detailed-example.md)de la tabla de secuencia.</span><span class="sxs-lookup"><span data-stu-id="396fc-107">See [Installation Procedure Tables Group](installation-procedure-tables-group.md), [Using a Sequence Table](using-a-sequence-table.md), and the [Sequence Table Detailed Example](sequence-table-detailed-example.md).</span></span>

<span data-ttu-id="396fc-108">Si en la sección [importar una base de datos en blanco](importing-a-blank-database.md) usada uisample.msi del SDK de Windows Installer, las tablas de secuencia de la copia de MNP2000.msi ya contienen las secuencias de acción sugeridas que se describen en [uso de una tabla de secuencia](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="396fc-108">If in the section [Importing a Blank Database](importing-a-blank-database.md) you used uisample.msi from the Windows Installer SDK, the sequence tables in your copy of MNP2000.msi already contains the suggested action sequences described in [Using a Sequence Table](using-a-sequence-table.md).</span></span> <span data-ttu-id="396fc-109">No es necesario realizar ningún cambio en estas secuencias para crear el paquete de instalación del Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="396fc-109">No changes to these sequences should be necessary to author the Notepad installation package.</span></span>

<span data-ttu-id="396fc-110">Utilice el editor de base de datos para abrir MNP2000.msi y escriba los datos siguientes en la tabla InstallUISequence.</span><span class="sxs-lookup"><span data-stu-id="396fc-110">Use your database editor to open MNP2000.msi and enter the following data into the InstallUISequence table.</span></span>

[<span data-ttu-id="396fc-111">Tabla InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="396fc-111">InstallUISequence Table</span></span>](installuisequence-table.md)



| <span data-ttu-id="396fc-112">Acción</span><span class="sxs-lookup"><span data-stu-id="396fc-112">Action</span></span>                | <span data-ttu-id="396fc-113">Condición</span><span class="sxs-lookup"><span data-stu-id="396fc-113">Condition</span></span>                                    | <span data-ttu-id="396fc-114">Secuencia</span><span class="sxs-lookup"><span data-stu-id="396fc-114">Sequence</span></span> |
|-----------------------|----------------------------------------------|----------|
| <span data-ttu-id="396fc-115">AppSearch</span><span class="sxs-lookup"><span data-stu-id="396fc-115">AppSearch</span></span>             |                                              | <span data-ttu-id="396fc-116">400</span><span class="sxs-lookup"><span data-stu-id="396fc-116">400</span></span>      |
| <span data-ttu-id="396fc-117">CCPSearch</span><span class="sxs-lookup"><span data-stu-id="396fc-117">CCPSearch</span></span>             | <span data-ttu-id="396fc-118">NO instalado</span><span class="sxs-lookup"><span data-stu-id="396fc-118">NOT Installed</span></span>                                | <span data-ttu-id="396fc-119">500</span><span class="sxs-lookup"><span data-stu-id="396fc-119">500</span></span>      |
| <span data-ttu-id="396fc-120">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="396fc-120">CostFinalize</span></span>          |                                              | <span data-ttu-id="396fc-121">1000</span><span class="sxs-lookup"><span data-stu-id="396fc-121">1000</span></span>     |
| <span data-ttu-id="396fc-122">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="396fc-122">CostInitialize</span></span>        |                                              | <span data-ttu-id="396fc-123">800</span><span class="sxs-lookup"><span data-stu-id="396fc-123">800</span></span>      |
| <span data-ttu-id="396fc-124">ExecuteAction</span><span class="sxs-lookup"><span data-stu-id="396fc-124">ExecuteAction</span></span>         |                                              | <span data-ttu-id="396fc-125">1300</span><span class="sxs-lookup"><span data-stu-id="396fc-125">1300</span></span>     |
| <span data-ttu-id="396fc-126">ExitDlg</span><span class="sxs-lookup"><span data-stu-id="396fc-126">ExitDlg</span></span>               |                                              | <span data-ttu-id="396fc-127">-1</span><span class="sxs-lookup"><span data-stu-id="396fc-127">-1</span></span>       |
| <span data-ttu-id="396fc-128">FatalErrorDlg</span><span class="sxs-lookup"><span data-stu-id="396fc-128">FatalErrorDlg</span></span>         |                                              | <span data-ttu-id="396fc-129">-3</span><span class="sxs-lookup"><span data-stu-id="396fc-129">-3</span></span>       |
| <span data-ttu-id="396fc-130">FileCost</span><span class="sxs-lookup"><span data-stu-id="396fc-130">FileCost</span></span>              |                                              | <span data-ttu-id="396fc-131">900</span><span class="sxs-lookup"><span data-stu-id="396fc-131">900</span></span>      |
| <span data-ttu-id="396fc-132">LaunchConditions</span><span class="sxs-lookup"><span data-stu-id="396fc-132">LaunchConditions</span></span>      |                                              | <span data-ttu-id="396fc-133">100</span><span class="sxs-lookup"><span data-stu-id="396fc-133">100</span></span>      |
| <span data-ttu-id="396fc-134">MaintenanceWelcomeDlg</span><span class="sxs-lookup"><span data-stu-id="396fc-134">MaintenanceWelcomeDlg</span></span> | <span data-ttu-id="396fc-135">Instalado, no REANUDAdo y no preseleccionado</span><span class="sxs-lookup"><span data-stu-id="396fc-135">Installed AND NOT RESUME AND NOT Preselected</span></span> | <span data-ttu-id="396fc-136">1250</span><span class="sxs-lookup"><span data-stu-id="396fc-136">1250</span></span>     |
| <span data-ttu-id="396fc-137">PrepareDlg</span><span class="sxs-lookup"><span data-stu-id="396fc-137">PrepareDlg</span></span>            |                                              | <span data-ttu-id="396fc-138">140</span><span class="sxs-lookup"><span data-stu-id="396fc-138">140</span></span>      |
| <span data-ttu-id="396fc-139">ProgressDlg</span><span class="sxs-lookup"><span data-stu-id="396fc-139">ProgressDlg</span></span>           |                                              | <span data-ttu-id="396fc-140">1280</span><span class="sxs-lookup"><span data-stu-id="396fc-140">1280</span></span>     |
| <span data-ttu-id="396fc-141">ResumeDlg</span><span class="sxs-lookup"><span data-stu-id="396fc-141">ResumeDlg</span></span>             | <span data-ttu-id="396fc-142">Instalado y (REANUDAr o preseleccionado)</span><span class="sxs-lookup"><span data-stu-id="396fc-142">Installed AND (RESUME OR Preselected)</span></span>        | <span data-ttu-id="396fc-143">1240</span><span class="sxs-lookup"><span data-stu-id="396fc-143">1240</span></span>     |
| <span data-ttu-id="396fc-144">RMCCPSearch</span><span class="sxs-lookup"><span data-stu-id="396fc-144">RMCCPSearch</span></span>           | <span data-ttu-id="396fc-145">NO instalado</span><span class="sxs-lookup"><span data-stu-id="396fc-145">NOT Installed</span></span>                                | <span data-ttu-id="396fc-146">600</span><span class="sxs-lookup"><span data-stu-id="396fc-146">600</span></span>      |
| <span data-ttu-id="396fc-147">UserExitDlg</span><span class="sxs-lookup"><span data-stu-id="396fc-147">UserExitDlg</span></span>           |                                              | <span data-ttu-id="396fc-148">-2</span><span class="sxs-lookup"><span data-stu-id="396fc-148">-2</span></span>       |
| <span data-ttu-id="396fc-149">WelcomeDlg</span><span class="sxs-lookup"><span data-stu-id="396fc-149">WelcomeDlg</span></span>            | <span data-ttu-id="396fc-150">NO instalado</span><span class="sxs-lookup"><span data-stu-id="396fc-150">NOT Installed</span></span>                                | <span data-ttu-id="396fc-151">1230</span><span class="sxs-lookup"><span data-stu-id="396fc-151">1230</span></span>     |
| <span data-ttu-id="396fc-152">MigrateFeatureStates</span><span class="sxs-lookup"><span data-stu-id="396fc-152">MigrateFeatureStates</span></span>  |                                              | <span data-ttu-id="396fc-153">1200</span><span class="sxs-lookup"><span data-stu-id="396fc-153">1200</span></span>     |
| <span data-ttu-id="396fc-154">FindRelatedProducts</span><span class="sxs-lookup"><span data-stu-id="396fc-154">FindRelatedProducts</span></span>   |                                              | <span data-ttu-id="396fc-155">200</span><span class="sxs-lookup"><span data-stu-id="396fc-155">200</span></span>      |



 

[<span data-ttu-id="396fc-156">Continuar</span><span class="sxs-lookup"><span data-stu-id="396fc-156">Continue</span></span>](importing-the-adminexecutesequence.md)

 

 



