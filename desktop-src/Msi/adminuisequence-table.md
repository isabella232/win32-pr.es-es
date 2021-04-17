---
description: En la tabla AdminUISequence se enumeran las acciones que el instalador llama en secuencia cuando se ejecuta la acción de administrador de nivel superior y el nivel de interfaz de usuario interno se establece en interfaz de usuario completa o en interfaz de usuario reducida.
ms.assetid: 7227846d-b755-4af9-acc3-e27742a5097a
title: Tabla AdminUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8fb460f65d223e75ebd50a7587f5b3f4adeced8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652622"
---
# <a name="adminuisequence-table"></a><span data-ttu-id="35c6c-103">Tabla AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="35c6c-103">AdminUISequence Table</span></span>

<span data-ttu-id="35c6c-104">En la tabla AdminUISequence se enumeran las acciones que el instalador llama en secuencia cuando se ejecuta la [acción de administrador](admin-action.md) de nivel superior y el nivel de interfaz de usuario interno se establece en interfaz de usuario completa o en interfaz de usuario reducida.</span><span class="sxs-lookup"><span data-stu-id="35c6c-104">The AdminUISequence table lists actions that the installer calls in sequence when the top-level [ADMIN action](admin-action.md) is executed and the internal user interface level is set to full UI or reduced UI.</span></span> <span data-ttu-id="35c6c-105">El instalador omite las acciones de esta tabla si el nivel de la interfaz de usuario se establece en la interfaz de usuario básica o en ninguna interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="35c6c-105">The installer skips the actions in this table if the user interface level is set to basic UI or no UI.</span></span> <span data-ttu-id="35c6c-106">Vea [acerca de la interfaz de usuario](about-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="35c6c-106">See [About the User Interface](about-the-user-interface.md).</span></span>

<span data-ttu-id="35c6c-107">Las acciones de administración de la secuencia de instalación hasta la [acción InstallValidate](installvalidate-action.md)y los cuadros de diálogo de salida se encuentran en la tabla AdminUISequence.</span><span class="sxs-lookup"><span data-stu-id="35c6c-107">ADMIN actions in the install sequence up to the [InstallValidate action](installvalidate-action.md), and any exit dialog boxes, are located in the AdminUISequence table.</span></span> <span data-ttu-id="35c6c-108">Todas las acciones de InstallValidate hasta el final de la secuencia de instalación se encuentran en la [tabla AdminExecuteSequence](adminexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="35c6c-108">All actions from the InstallValidate through the end of the install sequence are in the [AdminExecuteSequence table](adminexecutesequence-table.md).</span></span> <span data-ttu-id="35c6c-109">Dado que la tabla AdminExecuteSequence debe ser independiente, también contiene las acciones de inicialización necesarias, como [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md)y [CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="35c6c-109">Because the AdminExecuteSequence table needs to stand alone, it also contains any necessary initialization actions such as [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md), and [CostFinalize](costfinalize-action.md).</span></span> <span data-ttu-id="35c6c-110">También tiene la [acción ExecuteAction](executeaction-action.md).</span><span class="sxs-lookup"><span data-stu-id="35c6c-110">It also has the [ExecuteAction action](executeaction-action.md).</span></span>

<span data-ttu-id="35c6c-111">Las columnas son idénticas a las de la [tabla InstallUISequence](installuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="35c6c-111">The columns are identical to those of the [InstallUISequence table](installuisequence-table.md).</span></span> <span data-ttu-id="35c6c-112">La tabla AdminUISequence tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="35c6c-112">The AdminUISequence table has the following columns.</span></span>



| <span data-ttu-id="35c6c-113">Columna</span><span class="sxs-lookup"><span data-stu-id="35c6c-113">Column</span></span>    | <span data-ttu-id="35c6c-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="35c6c-114">Type</span></span>                         | <span data-ttu-id="35c6c-115">Clave</span><span class="sxs-lookup"><span data-stu-id="35c6c-115">Key</span></span> | <span data-ttu-id="35c6c-116">Nullable</span><span class="sxs-lookup"><span data-stu-id="35c6c-116">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="35c6c-117">Acción</span><span class="sxs-lookup"><span data-stu-id="35c6c-117">Action</span></span>    | [<span data-ttu-id="35c6c-118">Identificador</span><span class="sxs-lookup"><span data-stu-id="35c6c-118">Identifier</span></span>](identifier.md) | <span data-ttu-id="35c6c-119">Y</span><span class="sxs-lookup"><span data-stu-id="35c6c-119">Y</span></span>   | <span data-ttu-id="35c6c-120">N</span><span class="sxs-lookup"><span data-stu-id="35c6c-120">N</span></span>        |
| <span data-ttu-id="35c6c-121">Condición</span><span class="sxs-lookup"><span data-stu-id="35c6c-121">Condition</span></span> | [<span data-ttu-id="35c6c-122">Condition</span><span class="sxs-lookup"><span data-stu-id="35c6c-122">Condition</span></span>](condition.md)   | <span data-ttu-id="35c6c-123">N</span><span class="sxs-lookup"><span data-stu-id="35c6c-123">N</span></span>   | <span data-ttu-id="35c6c-124">Y</span><span class="sxs-lookup"><span data-stu-id="35c6c-124">Y</span></span>        |
| <span data-ttu-id="35c6c-125">Secuencia</span><span class="sxs-lookup"><span data-stu-id="35c6c-125">Sequence</span></span>  | [<span data-ttu-id="35c6c-126">Entero</span><span class="sxs-lookup"><span data-stu-id="35c6c-126">Integer</span></span>](integer.md)       | <span data-ttu-id="35c6c-127">N</span><span class="sxs-lookup"><span data-stu-id="35c6c-127">N</span></span>   | <span data-ttu-id="35c6c-128">Y</span><span class="sxs-lookup"><span data-stu-id="35c6c-128">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="35c6c-129">Columnas</span><span class="sxs-lookup"><span data-stu-id="35c6c-129">Columns</span></span>

<dl> <dt>

<span data-ttu-id="35c6c-130"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Actuar</span><span class="sxs-lookup"><span data-stu-id="35c6c-130"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="35c6c-131">Nombre de la acción que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="35c6c-131">Name of the action to execute.</span></span> <span data-ttu-id="35c6c-132">Se trata de una acción estándar, un asistente para interfaz de usuario o una acción personalizada que se muestra en la [tabla CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="35c6c-132">This is either a standard action, a user interface wizard, or a custom action listed in the [CustomAction table](customaction-table.md).</span></span>

<span data-ttu-id="35c6c-133">Clave de la tabla principal.</span><span class="sxs-lookup"><span data-stu-id="35c6c-133">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="35c6c-134"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Cumple</span><span class="sxs-lookup"><span data-stu-id="35c6c-134"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="35c6c-135">Expresión lógica.</span><span class="sxs-lookup"><span data-stu-id="35c6c-135">Logical expression.</span></span> <span data-ttu-id="35c6c-136">Si la expresión se evalúa como false, se omite la acción.</span><span class="sxs-lookup"><span data-stu-id="35c6c-136">If the expression evaluates to false, the action is skipped.</span></span> <span data-ttu-id="35c6c-137">Si la sintaxis de la expresión no es válida, la secuencia finaliza y devuelve iesBadActionData.</span><span class="sxs-lookup"><span data-stu-id="35c6c-137">If the expression syntax is invalid, the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="35c6c-138">Para obtener información sobre la sintaxis de las instrucciones condicionales, vea sintaxis de la [instrucción condicional](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="35c6c-138">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="35c6c-139"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>SPRJ</span><span class="sxs-lookup"><span data-stu-id="35c6c-139"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="35c6c-140">Un valor positivo indica la posición de la secuencia de la acción.</span><span class="sxs-lookup"><span data-stu-id="35c6c-140">A positive value indicates the sequence position of the action.</span></span> <span data-ttu-id="35c6c-141">Los siguientes valores negativos indican que se llama a la acción si el instalador devuelve la marca de finalización.</span><span class="sxs-lookup"><span data-stu-id="35c6c-141">The following negative values indicate that the action is called if the installer returns the termination flag.</span></span> <span data-ttu-id="35c6c-142">Cada marca de finalización (valor negativo) se puede usar sin más de una acción.</span><span class="sxs-lookup"><span data-stu-id="35c6c-142">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="35c6c-143">Varias acciones pueden tener marcas de finalización, pero deben ser marcas diferentes.</span><span class="sxs-lookup"><span data-stu-id="35c6c-143">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="35c6c-144">Las marcas de finalización (valores negativos) suelen usarse con [cuadros de diálogo](dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="35c6c-144">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="35c6c-145">Marca de terminación</span><span class="sxs-lookup"><span data-stu-id="35c6c-145">Termination flag</span></span>          | <span data-ttu-id="35c6c-146">Value</span><span class="sxs-lookup"><span data-stu-id="35c6c-146">Value</span></span> | <span data-ttu-id="35c6c-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="35c6c-147">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="35c6c-148">msiDoActionStatusSuccess</span><span class="sxs-lookup"><span data-stu-id="35c6c-148">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="35c6c-149">-1</span><span class="sxs-lookup"><span data-stu-id="35c6c-149">-1</span></span>    | <span data-ttu-id="35c6c-150">Finalización correcta.</span><span class="sxs-lookup"><span data-stu-id="35c6c-150">Successful completion.</span></span> <span data-ttu-id="35c6c-151">Se usa con los cuadros de diálogo de [salida](exit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="35c6c-151">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="35c6c-152">msiDoActionStatusUserExit</span><span class="sxs-lookup"><span data-stu-id="35c6c-152">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="35c6c-153">-2</span><span class="sxs-lookup"><span data-stu-id="35c6c-153">-2</span></span>    | <span data-ttu-id="35c6c-154">El usuario finaliza la instalación.</span><span class="sxs-lookup"><span data-stu-id="35c6c-154">User terminates install.</span></span> <span data-ttu-id="35c6c-155">Se usa con los cuadros de diálogo de [UserExit](userexit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="35c6c-155">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="35c6c-156">msiDoActionStatusFailure</span><span class="sxs-lookup"><span data-stu-id="35c6c-156">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="35c6c-157">-3</span><span class="sxs-lookup"><span data-stu-id="35c6c-157">-3</span></span>    | <span data-ttu-id="35c6c-158">Se termina la salida grave.</span><span class="sxs-lookup"><span data-stu-id="35c6c-158">Fatal exit terminates.</span></span> <span data-ttu-id="35c6c-159">Se usa con un cuadro de diálogo de [FatalError](fatalerror-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="35c6c-159">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="35c6c-160">msiDoActionStatusSuspend</span><span class="sxs-lookup"><span data-stu-id="35c6c-160">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="35c6c-161">-4</span><span class="sxs-lookup"><span data-stu-id="35c6c-161">-4</span></span>    | <span data-ttu-id="35c6c-162">La instalación está suspendida.</span><span class="sxs-lookup"><span data-stu-id="35c6c-162">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="35c6c-163">Cero, todos los demás números negativos o un valor null indican que nunca se llama a la acción.</span><span class="sxs-lookup"><span data-stu-id="35c6c-163">Zero, all other negative numbers, or a null value indicate that the action is never called.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="35c6c-164">Validación</span><span class="sxs-lookup"><span data-stu-id="35c6c-164">Validation</span></span>

<dl>

[<span data-ttu-id="35c6c-165">ICE03</span><span class="sxs-lookup"><span data-stu-id="35c6c-165">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="35c6c-166">ICE06</span><span class="sxs-lookup"><span data-stu-id="35c6c-166">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="35c6c-167">ICE12</span><span class="sxs-lookup"><span data-stu-id="35c6c-167">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="35c6c-168">ICE13</span><span class="sxs-lookup"><span data-stu-id="35c6c-168">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="35c6c-169">ICE20</span><span class="sxs-lookup"><span data-stu-id="35c6c-169">ICE20</span></span>](ice20.md)  
[<span data-ttu-id="35c6c-170">ICE26</span><span class="sxs-lookup"><span data-stu-id="35c6c-170">ICE26</span></span>](ice26.md)  
[<span data-ttu-id="35c6c-171">ICE27</span><span class="sxs-lookup"><span data-stu-id="35c6c-171">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="35c6c-172">ICE28</span><span class="sxs-lookup"><span data-stu-id="35c6c-172">ICE28</span></span>](ice28.md)  
[<span data-ttu-id="35c6c-173">ICE46</span><span class="sxs-lookup"><span data-stu-id="35c6c-173">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="35c6c-174">ICE75</span><span class="sxs-lookup"><span data-stu-id="35c6c-174">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="35c6c-175">ICE79</span><span class="sxs-lookup"><span data-stu-id="35c6c-175">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="35c6c-176">ICE82</span><span class="sxs-lookup"><span data-stu-id="35c6c-176">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="35c6c-177">ICE84</span><span class="sxs-lookup"><span data-stu-id="35c6c-177">ICE84</span></span>](ice84.md)  
[<span data-ttu-id="35c6c-178">ICE86</span><span class="sxs-lookup"><span data-stu-id="35c6c-178">ICE86</span></span>](ice86.md)  
[<span data-ttu-id="35c6c-179">ICE96</span><span class="sxs-lookup"><span data-stu-id="35c6c-179">ICE96</span></span>](ice96.md)  
[<span data-ttu-id="35c6c-180">ICEM04</span><span class="sxs-lookup"><span data-stu-id="35c6c-180">ICEM04</span></span>](icem04.md)  
</dl>

 

 



