---
description: En la tabla AdminExecuteSequence se enumeran las acciones que ejecuta el instalador cuando llama a la acción de administrador de nivel superior. Vea Grupo de tablas de procedimientos de instalación, uso de una tabla de secuencia y el ejemplo detallado de la tabla de secuencia.
ms.assetid: 8b1da4a3-0b82-4b71-8a32-59e90025cbfa
title: Importación de AdminExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60e5cfef89ada780d9ce647f45667fdc34cc5b01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810736"
---
# <a name="importing-the-adminexecutesequence"></a><span data-ttu-id="90535-104">Importación de AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="90535-104">Importing the AdminExecuteSequence</span></span>

<span data-ttu-id="90535-105">En la [tabla AdminExecuteSequence](adminexecutesequence-table.md) se enumeran las acciones que ejecuta el instalador cuando llama a la [acción de administrador](admin-action.md)de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="90535-105">The [AdminExecuteSequence table](adminexecutesequence-table.md) lists actions that the installer executes when it calls the top-level [ADMIN action](admin-action.md).</span></span> <span data-ttu-id="90535-106">Vea [grupo de tablas de procedimientos de instalación](installation-procedure-tables-group.md), [uso de una tabla de secuencia](using-a-sequence-table.md)y el [ejemplo detallado](sequence-table-detailed-example.md)de la tabla de secuencia.</span><span class="sxs-lookup"><span data-stu-id="90535-106">See [Installation Procedure Tables Group](installation-procedure-tables-group.md), [Using a Sequence Table](using-a-sequence-table.md), and the [Sequence Table Detailed Example](sequence-table-detailed-example.md).</span></span>

<span data-ttu-id="90535-107">Si en la sección [importar una base de datos en blanco](importing-a-blank-database.md) usada uisample.msi del SDK de Windows Installer, las tablas de secuencia de la copia de MNP2000.msi ya contienen las secuencias de acción sugeridas que se describen en [uso de una tabla de secuencia](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="90535-107">If in the section [Importing a Blank Database](importing-a-blank-database.md) you used uisample.msi from the Windows Installer SDK, the sequence tables in your copy of MNP2000.msi already contains the suggested action sequences described in [Using a Sequence Table](using-a-sequence-table.md).</span></span> <span data-ttu-id="90535-108">No es necesario realizar ningún cambio en estas secuencias para crear el paquete de instalación del ejemplo del Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="90535-108">No changes to these sequences should be necessary to author the Notepad sample installation package.</span></span>

<span data-ttu-id="90535-109">Utilice el editor de base de datos para abrir MNP2000.msi y escriba los datos siguientes en la tabla AdminExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="90535-109">Use your database editor to open MNP2000.msi and enter the following data into the AdminExecuteSequence table.</span></span>

[<span data-ttu-id="90535-110">Tabla AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="90535-110">AdminExecuteSequence Table</span></span>](adminexecutesequence-table.md)



| <span data-ttu-id="90535-111">Acción</span><span class="sxs-lookup"><span data-stu-id="90535-111">Action</span></span>              | <span data-ttu-id="90535-112">Condición</span><span class="sxs-lookup"><span data-stu-id="90535-112">Condition</span></span> | <span data-ttu-id="90535-113">Secuencia</span><span class="sxs-lookup"><span data-stu-id="90535-113">Sequence</span></span> |
|---------------------|-----------|----------|
| <span data-ttu-id="90535-114">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="90535-114">CostFinalize</span></span>        |           | <span data-ttu-id="90535-115">1000</span><span class="sxs-lookup"><span data-stu-id="90535-115">1000</span></span>     |
| <span data-ttu-id="90535-116">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="90535-116">CostInitialize</span></span>      |           | <span data-ttu-id="90535-117">800</span><span class="sxs-lookup"><span data-stu-id="90535-117">800</span></span>      |
| <span data-ttu-id="90535-118">FileCost</span><span class="sxs-lookup"><span data-stu-id="90535-118">FileCost</span></span>            |           | <span data-ttu-id="90535-119">900</span><span class="sxs-lookup"><span data-stu-id="90535-119">900</span></span>      |
| <span data-ttu-id="90535-120">InstallAdminPackage</span><span class="sxs-lookup"><span data-stu-id="90535-120">InstallAdminPackage</span></span> |           | <span data-ttu-id="90535-121">3900</span><span class="sxs-lookup"><span data-stu-id="90535-121">3900</span></span>     |
| <span data-ttu-id="90535-122">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="90535-122">InstallFiles</span></span>        |           | <span data-ttu-id="90535-123">4000</span><span class="sxs-lookup"><span data-stu-id="90535-123">4000</span></span>     |
| <span data-ttu-id="90535-124">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="90535-124">InstallFinalize</span></span>     |           | <span data-ttu-id="90535-125">6600</span><span class="sxs-lookup"><span data-stu-id="90535-125">6600</span></span>     |
| <span data-ttu-id="90535-126">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="90535-126">InstallInitialize</span></span>   |           | <span data-ttu-id="90535-127">1.500</span><span class="sxs-lookup"><span data-stu-id="90535-127">1500</span></span>     |
| <span data-ttu-id="90535-128">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="90535-128">InstallValidate</span></span>     |           | <span data-ttu-id="90535-129">1400</span><span class="sxs-lookup"><span data-stu-id="90535-129">1400</span></span>     |



 

[<span data-ttu-id="90535-130">Continuar</span><span class="sxs-lookup"><span data-stu-id="90535-130">Continue</span></span>](importing-the-adminuisequence.md)

 

 



