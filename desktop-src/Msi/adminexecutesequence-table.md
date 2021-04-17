---
description: En la tabla AdminExecuteSequence se enumeran las acciones que el instalador llama en secuencia cuando se ejecuta la acción de administrador de nivel superior.
ms.assetid: 33a2ef50-519b-424e-b510-55c21c5706a3
title: Tabla AdminExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c62ae43f8436ab210765e5402751c5722b78b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667051"
---
# <a name="adminexecutesequence-table"></a><span data-ttu-id="2ef3f-103">Tabla AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="2ef3f-103">AdminExecuteSequence Table</span></span>

<span data-ttu-id="2ef3f-104">En la tabla AdminExecuteSequence se enumeran las acciones que el instalador llama en secuencia cuando se ejecuta la [acción de administrador](admin-action.md) de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="2ef3f-104">The AdminExecuteSequence table lists actions that the installer calls in sequence when the top-level [ADMIN action](admin-action.md) is executed.</span></span>

<span data-ttu-id="2ef3f-105">Las acciones de administración de la secuencia de instalación, hasta la [acción InstallValidate](installvalidate-action.md) y cualquier cuadro de diálogo de salida, se encuentran en la [tabla AdminUISequence](adminuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="2ef3f-105">ADMIN actions in the install sequence, up to the [InstallValidate action](installvalidate-action.md) and any exit dialog boxes, are located in the [AdminUISequence table](adminuisequence-table.md).</span></span>

<span data-ttu-id="2ef3f-106">Las acciones de administración de la acción InstallValidate hasta el final de la secuencia de instalación se encuentran en la tabla AdminExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="2ef3f-106">ADMIN actions from the InstallValidate action through the end of the install sequence are in the AdminExecuteSequence table.</span></span> <span data-ttu-id="2ef3f-107">Dado que la tabla AdminExecuteSequence debe ser independiente, también contiene las acciones de inicialización necesarias, como [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md)y [CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="2ef3f-107">Because the AdminExecuteSequence table needs to stand alone, it also contains any necessary initialization actions such as [LaunchConditions](launchconditions-action.md), [CostInitialize](costinitialize-action.md), [FileCost](filecost-action.md), and [CostFinalize](costfinalize-action.md).</span></span>

<span data-ttu-id="2ef3f-108">[Las acciones personalizadas](custom-actions.md) que requieren una interfaz de usuario deben utilizar [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) en lugar de los cuadros de diálogo creados mediante la [tabla de diálogo](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="2ef3f-108">[Custom actions](custom-actions.md) requiring a user interface should use [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) instead of authored dialog boxes created using the [Dialog table](dialog-table.md).</span></span>

<span data-ttu-id="2ef3f-109">Las columnas son idénticas a las de la [tabla InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="2ef3f-109">The columns are identical to those of the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="2ef3f-110">La tabla AdminExecuteSequence tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="2ef3f-110">The AdminExecuteSequence table has the following columns.</span></span>



| <span data-ttu-id="2ef3f-111">Columna</span><span class="sxs-lookup"><span data-stu-id="2ef3f-111">Column</span></span>    | <span data-ttu-id="2ef3f-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="2ef3f-112">Type</span></span>                         | <span data-ttu-id="2ef3f-113">Clave</span><span class="sxs-lookup"><span data-stu-id="2ef3f-113">Key</span></span> | <span data-ttu-id="2ef3f-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="2ef3f-114">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="2ef3f-115">Acción</span><span class="sxs-lookup"><span data-stu-id="2ef3f-115">Action</span></span>    | [<span data-ttu-id="2ef3f-116">Identificador</span><span class="sxs-lookup"><span data-stu-id="2ef3f-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="2ef3f-117">Y</span><span class="sxs-lookup"><span data-stu-id="2ef3f-117">Y</span></span>   | <span data-ttu-id="2ef3f-118">N</span><span class="sxs-lookup"><span data-stu-id="2ef3f-118">N</span></span>        |
| <span data-ttu-id="2ef3f-119">Condición</span><span class="sxs-lookup"><span data-stu-id="2ef3f-119">Condition</span></span> | [<span data-ttu-id="2ef3f-120">Condition</span><span class="sxs-lookup"><span data-stu-id="2ef3f-120">Condition</span></span>](condition.md)   | <span data-ttu-id="2ef3f-121">N</span><span class="sxs-lookup"><span data-stu-id="2ef3f-121">N</span></span>   | <span data-ttu-id="2ef3f-122">Y</span><span class="sxs-lookup"><span data-stu-id="2ef3f-122">Y</span></span>        |
| <span data-ttu-id="2ef3f-123">Secuencia</span><span class="sxs-lookup"><span data-stu-id="2ef3f-123">Sequence</span></span>  | [<span data-ttu-id="2ef3f-124">Entero</span><span class="sxs-lookup"><span data-stu-id="2ef3f-124">Integer</span></span>](integer.md)       | <span data-ttu-id="2ef3f-125">N</span><span class="sxs-lookup"><span data-stu-id="2ef3f-125">N</span></span>   | <span data-ttu-id="2ef3f-126">Y</span><span class="sxs-lookup"><span data-stu-id="2ef3f-126">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="2ef3f-127">Columnas</span><span class="sxs-lookup"><span data-stu-id="2ef3f-127">Columns</span></span>

<dl> <dt>

<span data-ttu-id="2ef3f-128"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Actuar</span><span class="sxs-lookup"><span data-stu-id="2ef3f-128"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="2ef3f-129">Nombre de la acción que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="2ef3f-129">Name of the action to execute.</span></span> <span data-ttu-id="2ef3f-130">Se trata de una acción estándar o una acción personalizada que se muestra en la [tabla CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="2ef3f-130">This is either a standard action or a custom action listed in the [CustomAction table](customaction-table.md).</span></span>

<span data-ttu-id="2ef3f-131">Clave de la tabla principal.</span><span class="sxs-lookup"><span data-stu-id="2ef3f-131">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="2ef3f-132"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Cumple</span><span class="sxs-lookup"><span data-stu-id="2ef3f-132"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="2ef3f-133">Expresión lógica.</span><span class="sxs-lookup"><span data-stu-id="2ef3f-133">Logical expression.</span></span> <span data-ttu-id="2ef3f-134">Si la expresión se evalúa como false, se omite la acción.</span><span class="sxs-lookup"><span data-stu-id="2ef3f-134">If the expression evaluates to false, the action is skipped.</span></span> <span data-ttu-id="2ef3f-135">Si la sintaxis de la expresión no es válida, la secuencia finaliza y devuelve iesBadActionData.</span><span class="sxs-lookup"><span data-stu-id="2ef3f-135">If the expression syntax is invalid, the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="2ef3f-136">Para obtener información sobre la sintaxis de las instrucciones condicionales, vea sintaxis de la [instrucción condicional](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="2ef3f-136">For information on the syntax of conditional statements see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ef3f-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>SPRJ</span><span class="sxs-lookup"><span data-stu-id="2ef3f-137"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="2ef3f-138">Un valor positivo indica la posición de la secuencia de la acción.</span><span class="sxs-lookup"><span data-stu-id="2ef3f-138">A positive value indicates the sequence position of the action.</span></span> <span data-ttu-id="2ef3f-139">Los siguientes valores negativos indican que se llama a la acción si el instalador devuelve la marca de finalización.</span><span class="sxs-lookup"><span data-stu-id="2ef3f-139">The following negative values indicate that the action is called if the installer returns the termination flag.</span></span> <span data-ttu-id="2ef3f-140">Cada marca de finalización (valor negativo) se puede usar sin más de una acción.</span><span class="sxs-lookup"><span data-stu-id="2ef3f-140">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="2ef3f-141">Varias acciones pueden tener marcas de finalización, pero deben ser marcas diferentes.</span><span class="sxs-lookup"><span data-stu-id="2ef3f-141">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="2ef3f-142">Las marcas de finalización (valores negativos) suelen usarse con [cuadros de diálogo](dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="2ef3f-142">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="2ef3f-143">Marca de terminación</span><span class="sxs-lookup"><span data-stu-id="2ef3f-143">Termination flag</span></span>          | <span data-ttu-id="2ef3f-144">Value</span><span class="sxs-lookup"><span data-stu-id="2ef3f-144">Value</span></span> | <span data-ttu-id="2ef3f-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ef3f-145">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2ef3f-146">msiDoActionStatusSuccess</span><span class="sxs-lookup"><span data-stu-id="2ef3f-146">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="2ef3f-147">-1</span><span class="sxs-lookup"><span data-stu-id="2ef3f-147">-1</span></span>    | <span data-ttu-id="2ef3f-148">Finalización correcta.</span><span class="sxs-lookup"><span data-stu-id="2ef3f-148">Successful completion.</span></span> <span data-ttu-id="2ef3f-149">Se usa con los cuadros de diálogo de [salida](exit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="2ef3f-149">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="2ef3f-150">msiDoActionStatusUserExit</span><span class="sxs-lookup"><span data-stu-id="2ef3f-150">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="2ef3f-151">-2</span><span class="sxs-lookup"><span data-stu-id="2ef3f-151">-2</span></span>    | <span data-ttu-id="2ef3f-152">El usuario finaliza la instalación.</span><span class="sxs-lookup"><span data-stu-id="2ef3f-152">User terminates install.</span></span> <span data-ttu-id="2ef3f-153">Se usa con los cuadros de diálogo de [UserExit](userexit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="2ef3f-153">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="2ef3f-154">msiDoActionStatusFailure</span><span class="sxs-lookup"><span data-stu-id="2ef3f-154">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="2ef3f-155">-3</span><span class="sxs-lookup"><span data-stu-id="2ef3f-155">-3</span></span>    | <span data-ttu-id="2ef3f-156">Se termina la salida grave.</span><span class="sxs-lookup"><span data-stu-id="2ef3f-156">Fatal exit terminates.</span></span> <span data-ttu-id="2ef3f-157">Se usa con un cuadro de diálogo de [FatalError](fatalerror-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="2ef3f-157">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="2ef3f-158">msiDoActionStatusSuspend</span><span class="sxs-lookup"><span data-stu-id="2ef3f-158">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="2ef3f-159">-4</span><span class="sxs-lookup"><span data-stu-id="2ef3f-159">-4</span></span>    | <span data-ttu-id="2ef3f-160">La instalación está suspendida.</span><span class="sxs-lookup"><span data-stu-id="2ef3f-160">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="2ef3f-161">Cero, todos los demás números negativos o un valor null indican que nunca se llama a la acción.</span><span class="sxs-lookup"><span data-stu-id="2ef3f-161">Zero, all other negative numbers, or a null value indicate that the action is never called.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="2ef3f-162">Validación</span><span class="sxs-lookup"><span data-stu-id="2ef3f-162">Validation</span></span>

<dl>

[<span data-ttu-id="2ef3f-163">ICE03</span><span class="sxs-lookup"><span data-stu-id="2ef3f-163">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="2ef3f-164">ICE06</span><span class="sxs-lookup"><span data-stu-id="2ef3f-164">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="2ef3f-165">ICE12</span><span class="sxs-lookup"><span data-stu-id="2ef3f-165">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="2ef3f-166">ICE13</span><span class="sxs-lookup"><span data-stu-id="2ef3f-166">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="2ef3f-167">ICE26</span><span class="sxs-lookup"><span data-stu-id="2ef3f-167">ICE26</span></span>](ice26.md)  
[<span data-ttu-id="2ef3f-168">ICE27</span><span class="sxs-lookup"><span data-stu-id="2ef3f-168">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="2ef3f-169">ICE28</span><span class="sxs-lookup"><span data-stu-id="2ef3f-169">ICE28</span></span>](ice28.md)  
[<span data-ttu-id="2ef3f-170">ICE75</span><span class="sxs-lookup"><span data-stu-id="2ef3f-170">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="2ef3f-171">ICE77</span><span class="sxs-lookup"><span data-stu-id="2ef3f-171">ICE77</span></span>](ice77.md)  
[<span data-ttu-id="2ef3f-172">ICE79</span><span class="sxs-lookup"><span data-stu-id="2ef3f-172">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="2ef3f-173">ICE82</span><span class="sxs-lookup"><span data-stu-id="2ef3f-173">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="2ef3f-174">ICE84</span><span class="sxs-lookup"><span data-stu-id="2ef3f-174">ICE84</span></span>](ice84.md)  
[<span data-ttu-id="2ef3f-175">ICE86</span><span class="sxs-lookup"><span data-stu-id="2ef3f-175">ICE86</span></span>](ice86.md)  
[<span data-ttu-id="2ef3f-176">ICEM04</span><span class="sxs-lookup"><span data-stu-id="2ef3f-176">ICEM04</span></span>](icem04.md)  
</dl>

 

 



