---
description: ICE13 valida que los cuadros de diálogo de las tablas de secuencia aparecen en las tablas AdminUISequence o InstallUISequence. Los cuadros de diálogo no deben aparecer en las tablas InstallExecuteSequence, AdminExecuteSequence o AdvtExecuteSequence.
ms.assetid: 51542a8f-2fb6-4021-b52d-6f7a2b0294d6
title: ICE13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fff440217ccffe41d5e4036f4ea0d03d1eabb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002254"
---
# <a name="ice13"></a><span data-ttu-id="65117-104">ICE13</span><span class="sxs-lookup"><span data-stu-id="65117-104">ICE13</span></span>

<span data-ttu-id="65117-105">ICE13 valida que los cuadros de diálogo de las tablas de secuencia aparecen en las tablas [AdminUISequence](adminuisequence-table.md)o [InstallUISequence](installuisequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="65117-105">ICE13 validates that dialogs in sequence tables appear in the [AdminUISequence](adminuisequence-table.md), or [InstallUISequence](installuisequence-table.md) tables.</span></span> <span data-ttu-id="65117-106">Los cuadros de diálogo no deben aparecer en las tablas [InstallExecuteSequence](installexecutesequence-table.md), [AdminExecuteSequence](adminexecutesequence-table.md)o [AdvtExecuteSequence](advtexecutesequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="65117-106">Dialogs must not be listed in the [InstallExecuteSequence](installexecutesequence-table.md), [AdminExecuteSequence](adminexecutesequence-table.md), or [AdvtExecuteSequence](advtexecutesequence-table.md) tables.</span></span>

## <a name="result"></a><span data-ttu-id="65117-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="65117-107">Result</span></span>

<span data-ttu-id="65117-108">ICE13 envía un mensaje de error si aparece un cuadro de diálogo en una tabla de secuencia de ejecución.</span><span class="sxs-lookup"><span data-stu-id="65117-108">ICE13 posts an error message if a dialog appears in an execute sequence table.</span></span>

## <a name="example"></a><span data-ttu-id="65117-109">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="65117-109">Example</span></span>

<span data-ttu-id="65117-110">En el ejemplo siguiente, ICE13 envía un mensaje de error que indica que no se puede enumerar ' WelcomeDialog ' en la tabla ' InstallExecuteSequence '.</span><span class="sxs-lookup"><span data-stu-id="65117-110">For the following example, ICE13 posts an error message stating that the 'WelcomeDialog' cannot be listed in the 'InstallExecuteSequence' table.</span></span>

<span data-ttu-id="65117-111">[Tabla InstallExecuteSequence](installexecutesequence-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="65117-111">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="65117-112">Acción</span><span class="sxs-lookup"><span data-stu-id="65117-112">Action</span></span>          |
|-----------------|
| <span data-ttu-id="65117-113">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="65117-113">InstallFinalize</span></span> |
| <span data-ttu-id="65117-114">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="65117-114">CostFinalize</span></span>    |
| <span data-ttu-id="65117-115">WelcomeDialog</span><span class="sxs-lookup"><span data-stu-id="65117-115">WelcomeDialog</span></span>   |



 

<span data-ttu-id="65117-116">[Tabla InstallUISequence](installuisequence-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="65117-116">[InstallUISequence Table](installuisequence-table.md) (partial)</span></span>



| <span data-ttu-id="65117-117">Acción</span><span class="sxs-lookup"><span data-stu-id="65117-117">Action</span></span>         |
|----------------|
| <span data-ttu-id="65117-118">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="65117-118">CostFinalize</span></span>   |
| <span data-ttu-id="65117-119">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="65117-119">CostInitialize</span></span> |
| <span data-ttu-id="65117-120">BrowseDialog</span><span class="sxs-lookup"><span data-stu-id="65117-120">BrowseDialog</span></span>   |



 

<span data-ttu-id="65117-121">[Tabla de cuadro de diálogo](dialog-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="65117-121">[Dialog Table](dialog-table.md) (partial)</span></span>



| <span data-ttu-id="65117-122">Diálogo</span><span class="sxs-lookup"><span data-stu-id="65117-122">Dialog</span></span>        |
|---------------|
| <span data-ttu-id="65117-123">BrowseDialog</span><span class="sxs-lookup"><span data-stu-id="65117-123">BrowseDialog</span></span>  |
| <span data-ttu-id="65117-124">WelcomeDialog</span><span class="sxs-lookup"><span data-stu-id="65117-124">WelcomeDialog</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="65117-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="65117-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65117-126">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="65117-126">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



