---
description: En la tabla AdvtExecuteSequence se enumeran las acciones que llama el instalador cuando ejecuta la acción ANUNCIAnte de nivel superior. Vea Grupo de tablas de procedimientos de instalación, uso de una tabla de secuencia y el ejemplo detallado de la tabla de secuencia.
ms.assetid: 269bd28c-fa45-42b8-a610-1c4c5fcabc19
title: Importación de AdvtExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e4d7622670973a622b1376456ecfef445684cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815446"
---
# <a name="importing-the-advtexecutesequence"></a><span data-ttu-id="63265-104">Importación de AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="63265-104">Importing the AdvtExecuteSequence</span></span>

<span data-ttu-id="63265-105">En la [tabla AdvtExecuteSequence](advtexecutesequence-table.md) se enumeran las acciones que llama el instalador cuando ejecuta la [acción anunciante](advertise-action.md)de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="63265-105">The [AdvtExecuteSequence table](advtexecutesequence-table.md) lists actions the installer calls when it executes the top-level [ADVERTISE action](advertise-action.md).</span></span> <span data-ttu-id="63265-106">Vea [grupo de tablas de procedimientos de instalación](installation-procedure-tables-group.md), [uso de una tabla de secuencia](using-a-sequence-table.md)y el [ejemplo detallado](sequence-table-detailed-example.md)de la tabla de secuencia.</span><span class="sxs-lookup"><span data-stu-id="63265-106">See [Installation Procedure Tables Group](installation-procedure-tables-group.md), [Using a Sequence Table](using-a-sequence-table.md), and the [Sequence Table Detailed Example](sequence-table-detailed-example.md).</span></span>

<span data-ttu-id="63265-107">Si en la sección [importar una base de datos en blanco](importing-a-blank-database.md) usada uisample.msi del SDK de Windows Installer, las tablas de secuencia de la copia de MNP2000.msi ya contienen las secuencias de acción sugeridas que se describen en [uso de una tabla de secuencia](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="63265-107">If in the section [Importing a Blank Database](importing-a-blank-database.md) you used uisample.msi from the Windows Installer SDK, the sequence tables in your copy of MNP2000.msi already contains the suggested action sequences described in [Using a Sequence table](using-a-sequence-table.md).</span></span> <span data-ttu-id="63265-108">No es necesario realizar ningún cambio en estas secuencias para crear el paquete de instalación del ejemplo del Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="63265-108">No changes to these sequences should be necessary to author the Notepad sample installation package.</span></span>

<span data-ttu-id="63265-109">Utilice el editor de base de datos para abrir MNP2000.msi y escriba los datos siguientes en la [tabla AdvtExecuteSequence](advtexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="63265-109">Use your database editor to open MNP2000.msi and enter the following data into the [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span>

[<span data-ttu-id="63265-110">Tabla AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="63265-110">AdvtExecuteSequence Table</span></span>](advtexecutesequence-table.md)



| <span data-ttu-id="63265-111">Acción</span><span class="sxs-lookup"><span data-stu-id="63265-111">Action</span></span>                | <span data-ttu-id="63265-112">Condición</span><span class="sxs-lookup"><span data-stu-id="63265-112">Condition</span></span> | <span data-ttu-id="63265-113">Secuencia</span><span class="sxs-lookup"><span data-stu-id="63265-113">Sequence</span></span> |
|-----------------------|-----------|----------|
| <span data-ttu-id="63265-114">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="63265-114">CostFinalize</span></span>          |           | <span data-ttu-id="63265-115">1000</span><span class="sxs-lookup"><span data-stu-id="63265-115">1000</span></span>     |
| <span data-ttu-id="63265-116">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="63265-116">CostInitialize</span></span>        |           | <span data-ttu-id="63265-117">800</span><span class="sxs-lookup"><span data-stu-id="63265-117">800</span></span>      |
| <span data-ttu-id="63265-118">CreateShortcuts</span><span class="sxs-lookup"><span data-stu-id="63265-118">CreateShortcuts</span></span>       |           | <span data-ttu-id="63265-119">4500</span><span class="sxs-lookup"><span data-stu-id="63265-119">4500</span></span>     |
| <span data-ttu-id="63265-120">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="63265-120">InstallFinalize</span></span>       |           | <span data-ttu-id="63265-121">6600</span><span class="sxs-lookup"><span data-stu-id="63265-121">6600</span></span>     |
| <span data-ttu-id="63265-122">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="63265-122">InstallInitialize</span></span>     |           | <span data-ttu-id="63265-123">1.500</span><span class="sxs-lookup"><span data-stu-id="63265-123">1500</span></span>     |
| <span data-ttu-id="63265-124">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="63265-124">InstallValidate</span></span>       |           | <span data-ttu-id="63265-125">1400</span><span class="sxs-lookup"><span data-stu-id="63265-125">1400</span></span>     |
| <span data-ttu-id="63265-126">PublishComponents</span><span class="sxs-lookup"><span data-stu-id="63265-126">PublishComponents</span></span>     |           | <span data-ttu-id="63265-127">6200</span><span class="sxs-lookup"><span data-stu-id="63265-127">6200</span></span>     |
| <span data-ttu-id="63265-128">PublishFeatures</span><span class="sxs-lookup"><span data-stu-id="63265-128">PublishFeatures</span></span>       |           | <span data-ttu-id="63265-129">6300</span><span class="sxs-lookup"><span data-stu-id="63265-129">6300</span></span>     |
| <span data-ttu-id="63265-130">PublishProduct</span><span class="sxs-lookup"><span data-stu-id="63265-130">PublishProduct</span></span>        |           | <span data-ttu-id="63265-131">6400</span><span class="sxs-lookup"><span data-stu-id="63265-131">6400</span></span>     |
| <span data-ttu-id="63265-132">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="63265-132">RegisterClassInfo</span></span>     |           | <span data-ttu-id="63265-133">4600</span><span class="sxs-lookup"><span data-stu-id="63265-133">4600</span></span>     |
| <span data-ttu-id="63265-134">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="63265-134">RegisterExtensionInfo</span></span> |           | <span data-ttu-id="63265-135">4700</span><span class="sxs-lookup"><span data-stu-id="63265-135">4700</span></span>     |
| <span data-ttu-id="63265-136">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="63265-136">RegisterMIMEInfo</span></span>      |           | <span data-ttu-id="63265-137">4900</span><span class="sxs-lookup"><span data-stu-id="63265-137">4900</span></span>     |
| <span data-ttu-id="63265-138">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="63265-138">RegisterProgIdInfo</span></span>    |           | <span data-ttu-id="63265-139">4800</span><span class="sxs-lookup"><span data-stu-id="63265-139">4800</span></span>     |



 

<span data-ttu-id="63265-140">El instalador no utiliza la [tabla AdvtUISequence](advtuisequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="63265-140">The [AdvtUISequence table](advtuisequence-table.md) is not used by the installer.</span></span> <span data-ttu-id="63265-141">Esta tabla no debe existir o dejarse vacía en la base de datos de instalación.</span><span class="sxs-lookup"><span data-stu-id="63265-141">This table should not exist or be left empty in the installation database.</span></span>

[<span data-ttu-id="63265-142">Continuar</span><span class="sxs-lookup"><span data-stu-id="63265-142">Continue</span></span>](adding-summary-information.md)

 

 



