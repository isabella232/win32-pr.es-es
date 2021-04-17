---
description: En la tabla AdminUISequence se enumeran las acciones que el instalador llama cuando ejecuta la acción de administrador de nivel superior y el nivel de interfaz de usuario interna se establece en interfaz de usuario completa o en interfaz de usuario reducida.
ms.assetid: f23bd5c2-1d7f-485f-a22b-99436dfab6bf
title: Importación de AdminUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f1b9d2a91a350097ac043c186478e4933f6e81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652855"
---
# <a name="importing-the-adminuisequence"></a><span data-ttu-id="655fe-103">Importación de AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="655fe-103">Importing the AdminUISequence</span></span>

<span data-ttu-id="655fe-104">En la [tabla AdminUISequence](adminuisequence-table.md) se enumeran las acciones que el instalador llama cuando ejecuta la [acción de administrador](admin-action.md) de nivel superior y el nivel de interfaz de usuario interna se establece en interfaz de usuario completa o en interfaz de usuario reducida.</span><span class="sxs-lookup"><span data-stu-id="655fe-104">The [AdminUISequence table](adminuisequence-table.md) lists actions that the installer calls when it executes the top-level [ADMIN action](admin-action.md) and the internal user interface level is set to full UI or reduced UI.</span></span> <span data-ttu-id="655fe-105">El instalador omite las acciones de esta tabla si el nivel de la interfaz de usuario se establece en la interfaz de usuario básica o en ninguna interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="655fe-105">The installer skips the actions in this table if the user interface level is set to basic UI or no UI.</span></span> <span data-ttu-id="655fe-106">Vea [los niveles](user-interface-levels.md)de interfaz [de usuario y](user-interface.md) interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="655fe-106">See [User Interface](user-interface.md) and [User Interface Levels](user-interface-levels.md).</span></span> <span data-ttu-id="655fe-107">Vea [grupo de tablas de procedimientos de instalación](installation-procedure-tables-group.md), [uso de una tabla de secuencia](using-a-sequence-table.md)y el [ejemplo detallado](sequence-table-detailed-example.md)de la tabla de secuencia.</span><span class="sxs-lookup"><span data-stu-id="655fe-107">See [Installation Procedure Tables Group](installation-procedure-tables-group.md), [Using a Sequence Table](using-a-sequence-table.md), and the [Sequence Table Detailed Example](sequence-table-detailed-example.md).</span></span>

<span data-ttu-id="655fe-108">Si en la sección [importar una base de datos en blanco](importing-a-blank-database.md) usada uisample.msi del SDK de Windows Installer, las tablas de secuencia de la copia de MNP2000.msi ya contienen las secuencias de acción sugeridas que se describen en [uso de una tabla de secuencia](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="655fe-108">If in the section [Importing a Blank Database](importing-a-blank-database.md) you used uisample.msi from the Windows Installer SDK, the sequence tables in your copy of MNP2000.msi already contains the suggested action sequences described in [Using a Sequence Table](using-a-sequence-table.md).</span></span> <span data-ttu-id="655fe-109">No es necesario realizar ningún cambio en estas secuencias para instalar el ejemplo de Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="655fe-109">No changes to these sequences should be necessary to install the Notepad sample.</span></span>

<span data-ttu-id="655fe-110">Utilice el editor de base de datos para abrir MNP2000.msi y escriba los datos siguientes en la tabla AdminExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="655fe-110">Use your database editor to open MNP2000.msi and enter the following data into the AdminExecuteSequence table.</span></span>

[<span data-ttu-id="655fe-111">Tabla AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="655fe-111">AdminUISequence Table</span></span>](adminuisequence-table.md)



| <span data-ttu-id="655fe-112">Acción</span><span class="sxs-lookup"><span data-stu-id="655fe-112">Action</span></span>          | <span data-ttu-id="655fe-113">Condición</span><span class="sxs-lookup"><span data-stu-id="655fe-113">Condition</span></span> | <span data-ttu-id="655fe-114">Secuencia</span><span class="sxs-lookup"><span data-stu-id="655fe-114">Sequence</span></span> |
|-----------------|-----------|----------|
| <span data-ttu-id="655fe-115">AdminWelcomeDlg</span><span class="sxs-lookup"><span data-stu-id="655fe-115">AdminWelcomeDlg</span></span> |           | <span data-ttu-id="655fe-116">1230</span><span class="sxs-lookup"><span data-stu-id="655fe-116">1230</span></span>     |
| <span data-ttu-id="655fe-117">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="655fe-117">CostFinalize</span></span>    |           | <span data-ttu-id="655fe-118">1000</span><span class="sxs-lookup"><span data-stu-id="655fe-118">1000</span></span>     |
| <span data-ttu-id="655fe-119">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="655fe-119">CostInitialize</span></span>  |           | <span data-ttu-id="655fe-120">800</span><span class="sxs-lookup"><span data-stu-id="655fe-120">800</span></span>      |
| <span data-ttu-id="655fe-121">ExecuteAction</span><span class="sxs-lookup"><span data-stu-id="655fe-121">ExecuteAction</span></span>   |           | <span data-ttu-id="655fe-122">1300</span><span class="sxs-lookup"><span data-stu-id="655fe-122">1300</span></span>     |
| <span data-ttu-id="655fe-123">ExitDlg</span><span class="sxs-lookup"><span data-stu-id="655fe-123">ExitDlg</span></span>         |           | <span data-ttu-id="655fe-124">-1</span><span class="sxs-lookup"><span data-stu-id="655fe-124">-1</span></span>       |
| <span data-ttu-id="655fe-125">FatalErrorDlg</span><span class="sxs-lookup"><span data-stu-id="655fe-125">FatalErrorDlg</span></span>   |           | <span data-ttu-id="655fe-126">-3</span><span class="sxs-lookup"><span data-stu-id="655fe-126">-3</span></span>       |
| <span data-ttu-id="655fe-127">FileCost</span><span class="sxs-lookup"><span data-stu-id="655fe-127">FileCost</span></span>        |           | <span data-ttu-id="655fe-128">900</span><span class="sxs-lookup"><span data-stu-id="655fe-128">900</span></span>      |
| <span data-ttu-id="655fe-129">PrepareDlg</span><span class="sxs-lookup"><span data-stu-id="655fe-129">PrepareDlg</span></span>      |           | <span data-ttu-id="655fe-130">140</span><span class="sxs-lookup"><span data-stu-id="655fe-130">140</span></span>      |
| <span data-ttu-id="655fe-131">ProgressDlg</span><span class="sxs-lookup"><span data-stu-id="655fe-131">ProgressDlg</span></span>     |           | <span data-ttu-id="655fe-132">1280</span><span class="sxs-lookup"><span data-stu-id="655fe-132">1280</span></span>     |
| <span data-ttu-id="655fe-133">UserExitDlg</span><span class="sxs-lookup"><span data-stu-id="655fe-133">UserExitDlg</span></span>     |           | <span data-ttu-id="655fe-134">-2</span><span class="sxs-lookup"><span data-stu-id="655fe-134">-2</span></span>       |



 

[<span data-ttu-id="655fe-135">Continuar</span><span class="sxs-lookup"><span data-stu-id="655fe-135">Continue</span></span>](importing-the-advtexecutesequence.md)

 

 



