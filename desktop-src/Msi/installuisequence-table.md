---
description: En la tabla InstallUISequence se enumeran las acciones que se ejecutan cuando se ejecuta la acción de instalación de nivel superior y el nivel interno de la interfaz de usuario se establece en interfaz de usuario completa o en interfaz de usuario reducida.
ms.assetid: 076d7c14-e302-4465-aed5-27a4b1f70ac8
title: Tabla InstallUISequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19a4d8d3033645ac1f414e3aff67be2a26d7a6ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688331"
---
# <a name="installuisequence-table"></a><span data-ttu-id="fa195-103">Tabla InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="fa195-103">InstallUISequence Table</span></span>

<span data-ttu-id="fa195-104">En la tabla InstallUISequence se enumeran las acciones que se ejecutan cuando se ejecuta la [acción de instalación](install-action.md) de nivel superior y el nivel interno de la interfaz de usuario se establece en interfaz de usuario completa o en interfaz de usuario reducida.</span><span class="sxs-lookup"><span data-stu-id="fa195-104">The InstallUISequence table lists actions that are executed when the top-level [INSTALL action](install-action.md) is executed and the internal user interface level is set to full UI or reduced UI.</span></span> <span data-ttu-id="fa195-105">El instalador omite las acciones de esta tabla si el nivel de la interfaz de usuario se establece en la interfaz de usuario básica o en ninguna interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="fa195-105">The installer skips the actions in this table if the user interface level is set to basic UI or no UI.</span></span> <span data-ttu-id="fa195-106">Vea [acerca de la interfaz de usuario](about-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="fa195-106">See [About the User Interface](about-the-user-interface.md).</span></span>

<span data-ttu-id="fa195-107">Las acciones de la secuencia de instalación hasta la [acción InstallValidate](installvalidate-action.md)y los cuadros de diálogo de salida se encuentran en la tabla InstallUISequence.</span><span class="sxs-lookup"><span data-stu-id="fa195-107">Actions in the install sequence up to the [InstallValidate action](installvalidate-action.md), and the exit dialog boxes, are located in the InstallUISequence table.</span></span> <span data-ttu-id="fa195-108">Todas las acciones de InstallValidate hasta el final de la secuencia de instalación se encuentran en la [tabla InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="fa195-108">All actions from the InstallValidate through the end of the install sequence are in the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="fa195-109">Dado que la tabla InstallExecuteSequence debe ser independiente, tiene cualquier acción de inicialización necesaria, como las acciones [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md)y [CostFinalize](costfinalize-action.md), y [ExecuteAction](executeaction-action.md).</span><span class="sxs-lookup"><span data-stu-id="fa195-109">Because the InstallExecuteSequence table needs to stand alone, it has any necessary initialization actions such as the [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md), and the [CostFinalize](costfinalize-action.md), and [ExecuteAction action](executeaction-action.md).</span></span>

<span data-ttu-id="fa195-110">La tabla InstallUISequence tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="fa195-110">The InstallUISequence table has the following columns.</span></span>



| <span data-ttu-id="fa195-111">Columna</span><span class="sxs-lookup"><span data-stu-id="fa195-111">Column</span></span>    | <span data-ttu-id="fa195-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="fa195-112">Type</span></span>                         | <span data-ttu-id="fa195-113">Clave</span><span class="sxs-lookup"><span data-stu-id="fa195-113">Key</span></span> | <span data-ttu-id="fa195-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="fa195-114">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="fa195-115">Acción</span><span class="sxs-lookup"><span data-stu-id="fa195-115">Action</span></span>    | [<span data-ttu-id="fa195-116">Identificador</span><span class="sxs-lookup"><span data-stu-id="fa195-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="fa195-117">Y</span><span class="sxs-lookup"><span data-stu-id="fa195-117">Y</span></span>   | <span data-ttu-id="fa195-118">N</span><span class="sxs-lookup"><span data-stu-id="fa195-118">N</span></span>        |
| <span data-ttu-id="fa195-119">Condición</span><span class="sxs-lookup"><span data-stu-id="fa195-119">Condition</span></span> | [<span data-ttu-id="fa195-120">Condition</span><span class="sxs-lookup"><span data-stu-id="fa195-120">Condition</span></span>](condition.md)   | <span data-ttu-id="fa195-121">N</span><span class="sxs-lookup"><span data-stu-id="fa195-121">N</span></span>   | <span data-ttu-id="fa195-122">Y</span><span class="sxs-lookup"><span data-stu-id="fa195-122">Y</span></span>        |
| <span data-ttu-id="fa195-123">Secuencia</span><span class="sxs-lookup"><span data-stu-id="fa195-123">Sequence</span></span>  | [<span data-ttu-id="fa195-124">Entero</span><span class="sxs-lookup"><span data-stu-id="fa195-124">Integer</span></span>](integer.md)       | <span data-ttu-id="fa195-125">N</span><span class="sxs-lookup"><span data-stu-id="fa195-125">N</span></span>   | <span data-ttu-id="fa195-126">Y</span><span class="sxs-lookup"><span data-stu-id="fa195-126">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="fa195-127">Columnas</span><span class="sxs-lookup"><span data-stu-id="fa195-127">Columns</span></span>

<dl> <dt>

<span data-ttu-id="fa195-128"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Actuar</span><span class="sxs-lookup"><span data-stu-id="fa195-128"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="fa195-129">Nombre de la acción que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="fa195-129">Name of the action to execute.</span></span> <span data-ttu-id="fa195-130">Se trata de una acción integrada, una acción personalizada o un asistente para interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="fa195-130">This is either a built-in action, a custom action, or a user interface wizard.</span></span>

<span data-ttu-id="fa195-131">Clave de la tabla principal.</span><span class="sxs-lookup"><span data-stu-id="fa195-131">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="fa195-132"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Cumple</span><span class="sxs-lookup"><span data-stu-id="fa195-132"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="fa195-133">Este campo contiene una expresión condicional.</span><span class="sxs-lookup"><span data-stu-id="fa195-133">This field contains a conditional expression.</span></span> <span data-ttu-id="fa195-134">Si la expresión se evalúa como false, se omite la acción.</span><span class="sxs-lookup"><span data-stu-id="fa195-134">If the expression evaluates to False, then the action is skipped.</span></span> <span data-ttu-id="fa195-135">Si la sintaxis de la expresión no es válida, la secuencia finaliza y devuelve iesBadActionData.</span><span class="sxs-lookup"><span data-stu-id="fa195-135">If the expression syntax is invalid, then the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="fa195-136">Para obtener información sobre la sintaxis de las instrucciones condicionales, vea sintaxis de la [instrucción condicional](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="fa195-136">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa195-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>SPRJ</span><span class="sxs-lookup"><span data-stu-id="fa195-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="fa195-138">El número de esta columna determina la posición de la secuencia en la que se ejecuta esta acción.</span><span class="sxs-lookup"><span data-stu-id="fa195-138">The number in this column determines the sequence position in which this action is run.</span></span>

<span data-ttu-id="fa195-139">Un valor positivo representa la posición de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="fa195-139">A positive value represents the sequence position.</span></span> <span data-ttu-id="fa195-140">Un valor null indica que la acción no se ejecuta nunca.</span><span class="sxs-lookup"><span data-stu-id="fa195-140">A Null value indicates that the action is never run.</span></span> <span data-ttu-id="fa195-141">Los siguientes valores negativos indican que esta acción se ejecuta si el instalador devuelve la marca de finalización asociada.</span><span class="sxs-lookup"><span data-stu-id="fa195-141">The following negative values indicate that this action is executed if the installer returns the associated termination flag.</span></span> <span data-ttu-id="fa195-142">Cada marca de finalización (valor negativo) se puede usar sin más de una acción.</span><span class="sxs-lookup"><span data-stu-id="fa195-142">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="fa195-143">Varias acciones pueden tener marcas de finalización, pero deben ser marcas diferentes.</span><span class="sxs-lookup"><span data-stu-id="fa195-143">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="fa195-144">Las marcas de finalización (valores negativos) suelen usarse con [cuadros de diálogo](dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="fa195-144">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="fa195-145">Marca de terminación</span><span class="sxs-lookup"><span data-stu-id="fa195-145">Termination flag</span></span>          | <span data-ttu-id="fa195-146">Value</span><span class="sxs-lookup"><span data-stu-id="fa195-146">Value</span></span> | <span data-ttu-id="fa195-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa195-147">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fa195-148">msiDoActionStatusSuccess</span><span class="sxs-lookup"><span data-stu-id="fa195-148">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="fa195-149">-1</span><span class="sxs-lookup"><span data-stu-id="fa195-149">-1</span></span>    | <span data-ttu-id="fa195-150">Finalización correcta.</span><span class="sxs-lookup"><span data-stu-id="fa195-150">Successful completion.</span></span> <span data-ttu-id="fa195-151">Se usa con los cuadros de diálogo de [salida](exit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="fa195-151">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="fa195-152">msiDoActionStatusUserExit</span><span class="sxs-lookup"><span data-stu-id="fa195-152">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="fa195-153">-2</span><span class="sxs-lookup"><span data-stu-id="fa195-153">-2</span></span>    | <span data-ttu-id="fa195-154">El usuario finaliza la instalación.</span><span class="sxs-lookup"><span data-stu-id="fa195-154">User terminates install.</span></span> <span data-ttu-id="fa195-155">Se usa con los cuadros de diálogo de [UserExit](userexit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="fa195-155">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="fa195-156">msiDoActionStatusFailure</span><span class="sxs-lookup"><span data-stu-id="fa195-156">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="fa195-157">-3</span><span class="sxs-lookup"><span data-stu-id="fa195-157">-3</span></span>    | <span data-ttu-id="fa195-158">Se termina la salida grave.</span><span class="sxs-lookup"><span data-stu-id="fa195-158">Fatal exit terminates.</span></span> <span data-ttu-id="fa195-159">Se usa con un cuadro de diálogo de [FatalError](fatalerror-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="fa195-159">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="fa195-160">msiDoActionStatusSuspend</span><span class="sxs-lookup"><span data-stu-id="fa195-160">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="fa195-161">-4</span><span class="sxs-lookup"><span data-stu-id="fa195-161">-4</span></span>    | <span data-ttu-id="fa195-162">La instalación está suspendida.</span><span class="sxs-lookup"><span data-stu-id="fa195-162">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="fa195-163">Cero, todos los demás números negativos o un valor nulo indican que la acción no se ejecuta nunca.</span><span class="sxs-lookup"><span data-stu-id="fa195-163">Zero, all other negative numbers, or a Null value indicate that the action is never run.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fa195-164">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fa195-164">Remarks</span></span>

<span data-ttu-id="fa195-165">El texto localizado asociado para la presentación o el registro de progreso se especifica en la [tabla ActionText](actiontext-table.md).</span><span class="sxs-lookup"><span data-stu-id="fa195-165">Associated localized text for progress display or logging is specified in the [ActionText table](actiontext-table.md).</span></span>

<span data-ttu-id="fa195-166">Para obtener un ejemplo de una tabla de secuencia, vea [usar una tabla de secuencia](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="fa195-166">For an example of a sequence table, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="fa195-167">Validación</span><span class="sxs-lookup"><span data-stu-id="fa195-167">Validation</span></span>

<dl>

[<span data-ttu-id="fa195-168">ICE03</span><span class="sxs-lookup"><span data-stu-id="fa195-168">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="fa195-169">ICE06</span><span class="sxs-lookup"><span data-stu-id="fa195-169">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="fa195-170">ICE12</span><span class="sxs-lookup"><span data-stu-id="fa195-170">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="fa195-171">ICE13</span><span class="sxs-lookup"><span data-stu-id="fa195-171">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="fa195-172">ICE20</span><span class="sxs-lookup"><span data-stu-id="fa195-172">ICE20</span></span>](ice20.md)  
[<span data-ttu-id="fa195-173">ICE26</span><span class="sxs-lookup"><span data-stu-id="fa195-173">ICE26</span></span>](ice26.md)  
[<span data-ttu-id="fa195-174">ICE27</span><span class="sxs-lookup"><span data-stu-id="fa195-174">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="fa195-175">ICE28</span><span class="sxs-lookup"><span data-stu-id="fa195-175">ICE28</span></span>](ice28.md)  
[<span data-ttu-id="fa195-176">ICE46</span><span class="sxs-lookup"><span data-stu-id="fa195-176">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="fa195-177">ICE75</span><span class="sxs-lookup"><span data-stu-id="fa195-177">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="fa195-178">ICE79</span><span class="sxs-lookup"><span data-stu-id="fa195-178">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="fa195-179">ICE82</span><span class="sxs-lookup"><span data-stu-id="fa195-179">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="fa195-180">ICE86</span><span class="sxs-lookup"><span data-stu-id="fa195-180">ICE86</span></span>](ice86.md)  
</dl>

 

 



