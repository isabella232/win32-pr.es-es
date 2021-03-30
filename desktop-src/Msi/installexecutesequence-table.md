---
description: En la tabla InstallExecuteSequence se enumeran las acciones que se ejecutan cuando se ejecuta la acción de instalación de nivel superior.
ms.assetid: 995d4159-bfc9-48b2-8328-3ae8251d785d
title: Tabla InstallExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7d110debacab19739c3da69abf3948d11bb7aa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907837"
---
# <a name="installexecutesequence-table"></a><span data-ttu-id="2ee69-103">Tabla InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="2ee69-103">InstallExecuteSequence Table</span></span>

<span data-ttu-id="2ee69-104">En la tabla InstallExecuteSequence se enumeran las acciones que se ejecutan cuando se ejecuta la [acción de instalación](install-action.md) de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="2ee69-104">The InstallExecuteSequence table lists actions that are executed when the top-level [INSTALL action](install-action.md) is executed.</span></span>

<span data-ttu-id="2ee69-105">Las acciones de la secuencia de instalación hasta la [acción InstallValidate](installvalidate-action.md)y los cuadros de diálogo de salida se encuentran en la [tabla InstallUISequence](installuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="2ee69-105">Actions in the install sequence up to the [InstallValidate action](installvalidate-action.md), and any exit dialog boxes, are located in the [InstallUISequence table](installuisequence-table.md).</span></span> <span data-ttu-id="2ee69-106">Todas las acciones de InstallValidate hasta el final de la secuencia de instalación se encuentran en la tabla InstallExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="2ee69-106">All actions from the InstallValidate through the end of the install sequence are in the InstallExecuteSequence table.</span></span> <span data-ttu-id="2ee69-107">Dado que la tabla InstallExecuteSequence debe ser independiente, tiene cualquier acción de inicialización necesaria, como las acciones [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md)y [CostFinalize](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="2ee69-107">Because the InstallExecuteSequence table needs to stand alone, it has any necessary initialization actions such as the [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md), and [CostFinalize](costfinalize-action.md) actions.</span></span>

<span data-ttu-id="2ee69-108">[Las acciones personalizadas](custom-actions.md) que requieren una interfaz de usuario deben utilizar [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) en lugar de los cuadros de diálogo creados mediante la [tabla de diálogo](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="2ee69-108">[Custom actions](custom-actions.md) requiring a user interface should use [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) instead of authored dialog boxes created using the [Dialog table](dialog-table.md).</span></span>

<span data-ttu-id="2ee69-109">La tabla InstallExecuteSequence tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="2ee69-109">The InstallExecuteSequence table has the following columns.</span></span>



| <span data-ttu-id="2ee69-110">Columna</span><span class="sxs-lookup"><span data-stu-id="2ee69-110">Column</span></span>    | <span data-ttu-id="2ee69-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="2ee69-111">Type</span></span>                         | <span data-ttu-id="2ee69-112">Clave</span><span class="sxs-lookup"><span data-stu-id="2ee69-112">Key</span></span> | <span data-ttu-id="2ee69-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="2ee69-113">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="2ee69-114">Acción</span><span class="sxs-lookup"><span data-stu-id="2ee69-114">Action</span></span>    | [<span data-ttu-id="2ee69-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="2ee69-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="2ee69-116">Y</span><span class="sxs-lookup"><span data-stu-id="2ee69-116">Y</span></span>   | <span data-ttu-id="2ee69-117">N</span><span class="sxs-lookup"><span data-stu-id="2ee69-117">N</span></span>        |
| <span data-ttu-id="2ee69-118">Condición</span><span class="sxs-lookup"><span data-stu-id="2ee69-118">Condition</span></span> | [<span data-ttu-id="2ee69-119">Condition</span><span class="sxs-lookup"><span data-stu-id="2ee69-119">Condition</span></span>](condition.md)   | <span data-ttu-id="2ee69-120">N</span><span class="sxs-lookup"><span data-stu-id="2ee69-120">N</span></span>   | <span data-ttu-id="2ee69-121">Y</span><span class="sxs-lookup"><span data-stu-id="2ee69-121">Y</span></span>        |
| <span data-ttu-id="2ee69-122">Secuencia</span><span class="sxs-lookup"><span data-stu-id="2ee69-122">Sequence</span></span>  | [<span data-ttu-id="2ee69-123">Entero</span><span class="sxs-lookup"><span data-stu-id="2ee69-123">Integer</span></span>](integer.md)       | <span data-ttu-id="2ee69-124">N</span><span class="sxs-lookup"><span data-stu-id="2ee69-124">N</span></span>   | <span data-ttu-id="2ee69-125">Y</span><span class="sxs-lookup"><span data-stu-id="2ee69-125">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="2ee69-126">Columnas</span><span class="sxs-lookup"><span data-stu-id="2ee69-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="2ee69-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Actuar</span><span class="sxs-lookup"><span data-stu-id="2ee69-127"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="2ee69-128">Nombre de la acción que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="2ee69-128">Name of the action to execute.</span></span> <span data-ttu-id="2ee69-129">Se trata de una acción integrada o una acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="2ee69-129">This is either a built-in action or a custom action.</span></span>

<span data-ttu-id="2ee69-130">Clave de la tabla principal.</span><span class="sxs-lookup"><span data-stu-id="2ee69-130">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="2ee69-131"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Cumple</span><span class="sxs-lookup"><span data-stu-id="2ee69-131"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="2ee69-132">Este campo contiene una expresión condicional.</span><span class="sxs-lookup"><span data-stu-id="2ee69-132">This field contains a conditional expression.</span></span> <span data-ttu-id="2ee69-133">Si la expresión se evalúa como false, se omite la acción.</span><span class="sxs-lookup"><span data-stu-id="2ee69-133">If the expression evaluates to False, then the action is skipped.</span></span> <span data-ttu-id="2ee69-134">Si la sintaxis de la expresión no es válida, la secuencia finaliza y devuelve iesBadActionData.</span><span class="sxs-lookup"><span data-stu-id="2ee69-134">If the expression syntax is invalid, then the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="2ee69-135">Para obtener información sobre la sintaxis de las instrucciones condicionales, vea sintaxis de la [instrucción condicional](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="2ee69-135">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ee69-136"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>SPRJ</span><span class="sxs-lookup"><span data-stu-id="2ee69-136"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="2ee69-137">Número que determina la posición de la secuencia en la que se va a ejecutar esta acción.</span><span class="sxs-lookup"><span data-stu-id="2ee69-137">Number that determines the sequence position in which this action is to be executed.</span></span>

<span data-ttu-id="2ee69-138">Un valor positivo representa la posición de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="2ee69-138">A positive value represents the sequence position.</span></span> <span data-ttu-id="2ee69-139">Un valor null indica que la acción no se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="2ee69-139">A Null value indicates that the action is not executed.</span></span> <span data-ttu-id="2ee69-140">Los siguientes valores negativos indican que esta acción se va a ejecutar si el instalador devuelve la marca de finalización asociada.</span><span class="sxs-lookup"><span data-stu-id="2ee69-140">The following negative values indicate that this action is to be executed if the installer returns the associated termination flag.</span></span> <span data-ttu-id="2ee69-141">Cada marca de finalización (valor negativo) se puede usar sin más de una acción.</span><span class="sxs-lookup"><span data-stu-id="2ee69-141">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="2ee69-142">Varias acciones pueden tener marcas de finalización, pero deben ser marcas diferentes.</span><span class="sxs-lookup"><span data-stu-id="2ee69-142">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="2ee69-143">Las marcas de finalización (valores negativos) suelen usarse con [cuadros de diálogo](dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="2ee69-143">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="2ee69-144">Marca de terminación</span><span class="sxs-lookup"><span data-stu-id="2ee69-144">Termination flag</span></span>          | <span data-ttu-id="2ee69-145">Value</span><span class="sxs-lookup"><span data-stu-id="2ee69-145">Value</span></span> | <span data-ttu-id="2ee69-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ee69-146">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2ee69-147">msiDoActionStatusSuccess</span><span class="sxs-lookup"><span data-stu-id="2ee69-147">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="2ee69-148">-1</span><span class="sxs-lookup"><span data-stu-id="2ee69-148">-1</span></span>    | <span data-ttu-id="2ee69-149">Finalización correcta.</span><span class="sxs-lookup"><span data-stu-id="2ee69-149">Successful completion.</span></span> <span data-ttu-id="2ee69-150">Se usa con los cuadros de diálogo de [salida](exit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="2ee69-150">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="2ee69-151">msiDoActionStatusUserExit</span><span class="sxs-lookup"><span data-stu-id="2ee69-151">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="2ee69-152">-2</span><span class="sxs-lookup"><span data-stu-id="2ee69-152">-2</span></span>    | <span data-ttu-id="2ee69-153">El usuario finaliza la instalación.</span><span class="sxs-lookup"><span data-stu-id="2ee69-153">User terminates install.</span></span> <span data-ttu-id="2ee69-154">Se usa con los cuadros de diálogo de [UserExit](userexit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="2ee69-154">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="2ee69-155">msiDoActionStatusFailure</span><span class="sxs-lookup"><span data-stu-id="2ee69-155">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="2ee69-156">-3</span><span class="sxs-lookup"><span data-stu-id="2ee69-156">-3</span></span>    | <span data-ttu-id="2ee69-157">Se termina la salida grave.</span><span class="sxs-lookup"><span data-stu-id="2ee69-157">Fatal exit terminates.</span></span> <span data-ttu-id="2ee69-158">Se usa con un cuadro de diálogo de [FatalError](fatalerror-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="2ee69-158">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="2ee69-159">msiDoActionStatusSuspend</span><span class="sxs-lookup"><span data-stu-id="2ee69-159">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="2ee69-160">-4</span><span class="sxs-lookup"><span data-stu-id="2ee69-160">-4</span></span>    | <span data-ttu-id="2ee69-161">La instalación está suspendida.</span><span class="sxs-lookup"><span data-stu-id="2ee69-161">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="2ee69-162">Cero, todos los demás números negativos o un valor nulo indican que la acción no se ejecuta nunca.</span><span class="sxs-lookup"><span data-stu-id="2ee69-162">Zero, all other negative numbers, or a Null value indicate that the action is never run.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2ee69-163">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2ee69-163">Remarks</span></span>

<span data-ttu-id="2ee69-164">El texto localizado para la presentación o el registro del progreso se especifica en la [tabla ActionText](actiontext-table.md).</span><span class="sxs-lookup"><span data-stu-id="2ee69-164">Localized text for progress display or logging is specified in the [ActionText table](actiontext-table.md).</span></span>

<span data-ttu-id="2ee69-165">Para obtener un ejemplo de una tabla de secuencia, vea [usar una tabla de secuencia](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="2ee69-165">For an example of a sequence table, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="2ee69-166">Validación</span><span class="sxs-lookup"><span data-stu-id="2ee69-166">Validation</span></span>

<dl>

[<span data-ttu-id="2ee69-167">ICE03</span><span class="sxs-lookup"><span data-stu-id="2ee69-167">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="2ee69-168">ICE06</span><span class="sxs-lookup"><span data-stu-id="2ee69-168">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="2ee69-169">ICE12</span><span class="sxs-lookup"><span data-stu-id="2ee69-169">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="2ee69-170">ICE13</span><span class="sxs-lookup"><span data-stu-id="2ee69-170">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="2ee69-171">ICE26</span><span class="sxs-lookup"><span data-stu-id="2ee69-171">ICE26</span></span>](ice26.md)  
[<span data-ttu-id="2ee69-172">ICE27</span><span class="sxs-lookup"><span data-stu-id="2ee69-172">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="2ee69-173">ICE28</span><span class="sxs-lookup"><span data-stu-id="2ee69-173">ICE28</span></span>](ice28.md)  
[<span data-ttu-id="2ee69-174">ICE46</span><span class="sxs-lookup"><span data-stu-id="2ee69-174">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="2ee69-175">ICE63</span><span class="sxs-lookup"><span data-stu-id="2ee69-175">ICE63</span></span>](ice63.md)  
[<span data-ttu-id="2ee69-176">ICE75</span><span class="sxs-lookup"><span data-stu-id="2ee69-176">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="2ee69-177">ICE77</span><span class="sxs-lookup"><span data-stu-id="2ee69-177">ICE77</span></span>](ice77.md)  
[<span data-ttu-id="2ee69-178">ICE79</span><span class="sxs-lookup"><span data-stu-id="2ee69-178">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="2ee69-179">ICE82</span><span class="sxs-lookup"><span data-stu-id="2ee69-179">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="2ee69-180">ICE83</span><span class="sxs-lookup"><span data-stu-id="2ee69-180">ICE83</span></span>](ice83.md)  
[<span data-ttu-id="2ee69-181">ICE84</span><span class="sxs-lookup"><span data-stu-id="2ee69-181">ICE84</span></span>](ice84.md)  
[<span data-ttu-id="2ee69-182">ICE86</span><span class="sxs-lookup"><span data-stu-id="2ee69-182">ICE86</span></span>](ice86.md)  
</dl>

 

 



