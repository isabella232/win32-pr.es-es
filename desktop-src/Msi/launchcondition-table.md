---
description: La acción LaunchConditions usa la tabla LaunchCondition. Contiene una lista de condiciones que se deben satisfacer para que se inicie la instalación.
ms.assetid: 6e550cc7-c479-417e-ab89-882d8fece4e1
title: Tabla LaunchCondition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d67834f058575dde297454480040028ef9c5732
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686803"
---
# <a name="launchcondition-table"></a><span data-ttu-id="f247b-104">Tabla LaunchCondition</span><span class="sxs-lookup"><span data-stu-id="f247b-104">LaunchCondition Table</span></span>

<span data-ttu-id="f247b-105">La [acción LaunchConditions](launchconditions-action.md)usa la tabla LaunchCondition.</span><span class="sxs-lookup"><span data-stu-id="f247b-105">The LaunchCondition table is used by the [LaunchConditions action](launchconditions-action.md).</span></span> <span data-ttu-id="f247b-106">Contiene una lista de condiciones que se deben satisfacer para que se inicie la instalación.</span><span class="sxs-lookup"><span data-stu-id="f247b-106">It contains a list of conditions that all must be satisfied for the installation to begin.</span></span>

<span data-ttu-id="f247b-107">La tabla LaunchCondition tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="f247b-107">The LaunchCondition table has the following columns.</span></span>



| <span data-ttu-id="f247b-108">Columna</span><span class="sxs-lookup"><span data-stu-id="f247b-108">Column</span></span>      | <span data-ttu-id="f247b-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="f247b-109">Type</span></span>                       | <span data-ttu-id="f247b-110">Clave</span><span class="sxs-lookup"><span data-stu-id="f247b-110">Key</span></span> | <span data-ttu-id="f247b-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="f247b-111">Nullable</span></span> |
|-------------|----------------------------|-----|----------|
| <span data-ttu-id="f247b-112">Condición</span><span class="sxs-lookup"><span data-stu-id="f247b-112">Condition</span></span>   | [<span data-ttu-id="f247b-113">Condition</span><span class="sxs-lookup"><span data-stu-id="f247b-113">Condition</span></span>](condition.md) | <span data-ttu-id="f247b-114">Y</span><span class="sxs-lookup"><span data-stu-id="f247b-114">Y</span></span>   | <span data-ttu-id="f247b-115">N</span><span class="sxs-lookup"><span data-stu-id="f247b-115">N</span></span>        |
| <span data-ttu-id="f247b-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="f247b-116">Description</span></span> | [<span data-ttu-id="f247b-117">Formatea</span><span class="sxs-lookup"><span data-stu-id="f247b-117">Formatted</span></span>](formatted.md) | <span data-ttu-id="f247b-118">N</span><span class="sxs-lookup"><span data-stu-id="f247b-118">N</span></span>   | <span data-ttu-id="f247b-119">N</span><span class="sxs-lookup"><span data-stu-id="f247b-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="f247b-120">Columnas</span><span class="sxs-lookup"><span data-stu-id="f247b-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="f247b-121"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Cumple</span><span class="sxs-lookup"><span data-stu-id="f247b-121"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="f247b-122">Expresión que debe evaluarse como true para que se inicie la instalación.</span><span class="sxs-lookup"><span data-stu-id="f247b-122">Expression that must evaluate to True for installation to begin.</span></span>

</dd> <dt>

<span data-ttu-id="f247b-123"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Denominación</span><span class="sxs-lookup"><span data-stu-id="f247b-123"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="f247b-124">Texto localizable que se muestra cuando se produce un error en la condición y se debe terminar la instalación.</span><span class="sxs-lookup"><span data-stu-id="f247b-124">Localizable text to display when the condition fails and the installation must be terminated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f247b-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f247b-125">Remarks</span></span>

<span data-ttu-id="f247b-126">No se puede garantizar el orden en el que se evalúan las condiciones de inicio mediante la creación de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="f247b-126">You cannot guarantee the order in which the launch conditions are evaluated by authoring this table.</span></span> <span data-ttu-id="f247b-127">Si es necesario controlar el orden en el que se evalúan las condiciones, debe hacerlo con las acciones personalizadas del tipo de acción personalizada 19 en la instalación.</span><span class="sxs-lookup"><span data-stu-id="f247b-127">If it is necessary to control the order in which conditions are evaluated, you should do this by using Custom Action Type 19 custom actions in your installation.</span></span>

## <a name="validation"></a><span data-ttu-id="f247b-128">Validación</span><span class="sxs-lookup"><span data-stu-id="f247b-128">Validation</span></span>

<dl>

[<span data-ttu-id="f247b-129">ICE03</span><span class="sxs-lookup"><span data-stu-id="f247b-129">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="f247b-130">ICE06</span><span class="sxs-lookup"><span data-stu-id="f247b-130">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="f247b-131">ICE46</span><span class="sxs-lookup"><span data-stu-id="f247b-131">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="f247b-132">ICE79</span><span class="sxs-lookup"><span data-stu-id="f247b-132">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="f247b-133">ICE86</span><span class="sxs-lookup"><span data-stu-id="f247b-133">ICE86</span></span>](ice86.md)  
</dl>

 

 



