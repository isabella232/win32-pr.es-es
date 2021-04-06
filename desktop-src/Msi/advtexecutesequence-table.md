---
description: En la tabla AdvtExecuteSequence se enumeran las acciones que el instalador llama cuando se ejecuta la acción de anuncio de nivel superior.
ms.assetid: 8873c161-a709-48b8-a66f-fe2ee9be859f
title: Tabla AdvtExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b68a3f69cc7473b2364f169545743941d752f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909122"
---
# <a name="advtexecutesequence-table"></a><span data-ttu-id="363fc-103">Tabla AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="363fc-103">AdvtExecuteSequence Table</span></span>

<span data-ttu-id="363fc-104">En la tabla AdvtExecuteSequence se enumeran las acciones que el instalador llama cuando se ejecuta la [acción de anuncio](advertise-action.md) de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="363fc-104">The AdvtExecuteSequence table lists actions the installer calls when the top-level [ADVERTISE action](advertise-action.md) is executed.</span></span>

<span data-ttu-id="363fc-105">Solo se pueden usar las siguientes acciones en la tabla AdvtExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="363fc-105">Only the following actions can be used in the AdvtExecuteSequence table.</span></span> <span data-ttu-id="363fc-106">No se pueden usar acciones personalizadas en esta tabla.</span><span class="sxs-lookup"><span data-stu-id="363fc-106">Custom actions cannot be used in this table.</span></span>

[<span data-ttu-id="363fc-107">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="363fc-107">CostFinalize</span></span>](costfinalize-action.md)

[<span data-ttu-id="363fc-108">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="363fc-108">CostInitialize</span></span>](costinitialize-action.md)

[<span data-ttu-id="363fc-109">CreateShortcuts</span><span class="sxs-lookup"><span data-stu-id="363fc-109">CreateShortcuts</span></span>](createshortcuts-action.md)

[<span data-ttu-id="363fc-110">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="363fc-110">InstallFinalize</span></span>](installfinalize-action.md)

[<span data-ttu-id="363fc-111">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="363fc-111">InstallInitialize</span></span>](installinitialize-action.md)

[<span data-ttu-id="363fc-112">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="363fc-112">InstallValidate</span></span>](installvalidate-action.md)

[<span data-ttu-id="363fc-113">MsiPublishAssemblies</span><span class="sxs-lookup"><span data-stu-id="363fc-113">MsiPublishAssemblies</span></span>](msipublishassemblies-action.md)

[<span data-ttu-id="363fc-114">PublishComponents</span><span class="sxs-lookup"><span data-stu-id="363fc-114">PublishComponents</span></span>](publishcomponents-action.md)

[<span data-ttu-id="363fc-115">PublishFeatures</span><span class="sxs-lookup"><span data-stu-id="363fc-115">PublishFeatures</span></span>](publishfeatures-action.md)

[<span data-ttu-id="363fc-116">PublishProduct</span><span class="sxs-lookup"><span data-stu-id="363fc-116">PublishProduct</span></span>](publishproduct-action.md)

[<span data-ttu-id="363fc-117">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="363fc-117">RegisterClassInfo</span></span>](registerclassinfo-action.md)

[<span data-ttu-id="363fc-118">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="363fc-118">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)

[<span data-ttu-id="363fc-119">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="363fc-119">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

[<span data-ttu-id="363fc-120">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="363fc-120">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)

<span data-ttu-id="363fc-121">Las columnas son idénticas a las de la [tabla InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="363fc-121">The columns are identical to those of the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="363fc-122">La tabla AdvtExecuteSequence tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="363fc-122">The AdvtExecuteSequence table has the following columns.</span></span>



| <span data-ttu-id="363fc-123">Columna</span><span class="sxs-lookup"><span data-stu-id="363fc-123">Column</span></span>    | <span data-ttu-id="363fc-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="363fc-124">Type</span></span>                         | <span data-ttu-id="363fc-125">Clave</span><span class="sxs-lookup"><span data-stu-id="363fc-125">Key</span></span> | <span data-ttu-id="363fc-126">Nullable</span><span class="sxs-lookup"><span data-stu-id="363fc-126">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="363fc-127">Acción</span><span class="sxs-lookup"><span data-stu-id="363fc-127">Action</span></span>    | [<span data-ttu-id="363fc-128">Identificador</span><span class="sxs-lookup"><span data-stu-id="363fc-128">Identifier</span></span>](identifier.md) | <span data-ttu-id="363fc-129">Y</span><span class="sxs-lookup"><span data-stu-id="363fc-129">Y</span></span>   | <span data-ttu-id="363fc-130">N</span><span class="sxs-lookup"><span data-stu-id="363fc-130">N</span></span>        |
| <span data-ttu-id="363fc-131">Condición</span><span class="sxs-lookup"><span data-stu-id="363fc-131">Condition</span></span> | [<span data-ttu-id="363fc-132">Condition</span><span class="sxs-lookup"><span data-stu-id="363fc-132">Condition</span></span>](condition.md)   | <span data-ttu-id="363fc-133">N</span><span class="sxs-lookup"><span data-stu-id="363fc-133">N</span></span>   | <span data-ttu-id="363fc-134">Y</span><span class="sxs-lookup"><span data-stu-id="363fc-134">Y</span></span>        |
| <span data-ttu-id="363fc-135">Secuencia</span><span class="sxs-lookup"><span data-stu-id="363fc-135">Sequence</span></span>  | [<span data-ttu-id="363fc-136">Entero</span><span class="sxs-lookup"><span data-stu-id="363fc-136">Integer</span></span>](integer.md)       | <span data-ttu-id="363fc-137">N</span><span class="sxs-lookup"><span data-stu-id="363fc-137">N</span></span>   | <span data-ttu-id="363fc-138">Y</span><span class="sxs-lookup"><span data-stu-id="363fc-138">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="363fc-139">Columnas</span><span class="sxs-lookup"><span data-stu-id="363fc-139">Columns</span></span>

<dl> <dt>

<span data-ttu-id="363fc-140"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Actuar</span><span class="sxs-lookup"><span data-stu-id="363fc-140"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="363fc-141">Nombre de la [acción estándar](standard-actions.md) que va a ejecutar el instalador.</span><span class="sxs-lookup"><span data-stu-id="363fc-141">Name of the [standard action](standard-actions.md) the installer is to execute.</span></span> <span data-ttu-id="363fc-142">Esta es la clave principal de la tabla.</span><span class="sxs-lookup"><span data-stu-id="363fc-142">This is the primary key of the table.</span></span>

</dd> <dt>

<span data-ttu-id="363fc-143"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Cumple</span><span class="sxs-lookup"><span data-stu-id="363fc-143"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="363fc-144">Expresión lógica.</span><span class="sxs-lookup"><span data-stu-id="363fc-144">Logical expression.</span></span> <span data-ttu-id="363fc-145">Si la expresión se evalúa como false, se omite la acción.</span><span class="sxs-lookup"><span data-stu-id="363fc-145">If the expression evaluates to false, the action is skipped.</span></span> <span data-ttu-id="363fc-146">Si la sintaxis de la expresión no es válida, la secuencia finaliza y devuelve iesBadActionData.</span><span class="sxs-lookup"><span data-stu-id="363fc-146">If the expression syntax is invalid, the sequence terminates, returning iesBadActionData.</span></span> <span data-ttu-id="363fc-147">Para obtener información sobre la sintaxis de las instrucciones condicionales, vea sintaxis de la [instrucción condicional](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="363fc-147">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="363fc-148"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>SPRJ</span><span class="sxs-lookup"><span data-stu-id="363fc-148"><span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequence</span></span>
</dt> <dd>

<span data-ttu-id="363fc-149">Un valor positivo indica la posición de la secuencia de la acción.</span><span class="sxs-lookup"><span data-stu-id="363fc-149">A positive value indicates the sequence position of the action.</span></span> <span data-ttu-id="363fc-150">Los siguientes valores negativos indican que se llama a la acción si el instalador devuelve la marca de finalización.</span><span class="sxs-lookup"><span data-stu-id="363fc-150">The following negative values indicate that the action is called if the installer returns the termination flag.</span></span> <span data-ttu-id="363fc-151">Cada marca de finalización (valor negativo) se puede usar sin más de una acción.</span><span class="sxs-lookup"><span data-stu-id="363fc-151">Each termination flag (negative value) can be used with no more than one action.</span></span> <span data-ttu-id="363fc-152">Varias acciones pueden tener marcas de finalización, pero deben ser marcas diferentes.</span><span class="sxs-lookup"><span data-stu-id="363fc-152">Multiple actions can have termination flags, but they must be different flags.</span></span> <span data-ttu-id="363fc-153">Las marcas de finalización (valores negativos) suelen usarse con [cuadros de diálogo](dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="363fc-153">Termination flags (negative values) are typically used with [Dialog Boxes](dialog-boxes.md).</span></span>



| <span data-ttu-id="363fc-154">Marca de terminación</span><span class="sxs-lookup"><span data-stu-id="363fc-154">Termination flag</span></span>          | <span data-ttu-id="363fc-155">Value</span><span class="sxs-lookup"><span data-stu-id="363fc-155">Value</span></span> | <span data-ttu-id="363fc-156">Descripción</span><span class="sxs-lookup"><span data-stu-id="363fc-156">Description</span></span>                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="363fc-157">msiDoActionStatusSuccess</span><span class="sxs-lookup"><span data-stu-id="363fc-157">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="363fc-158">-1</span><span class="sxs-lookup"><span data-stu-id="363fc-158">-1</span></span>    | <span data-ttu-id="363fc-159">Finalización correcta.</span><span class="sxs-lookup"><span data-stu-id="363fc-159">Successful completion.</span></span> <span data-ttu-id="363fc-160">Se usa con los cuadros de diálogo de [salida](exit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="363fc-160">Used with [Exit](exit-dialog.md) dialog boxes.</span></span>               |
| <span data-ttu-id="363fc-161">msiDoActionStatusUserExit</span><span class="sxs-lookup"><span data-stu-id="363fc-161">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="363fc-162">-2</span><span class="sxs-lookup"><span data-stu-id="363fc-162">-2</span></span>    | <span data-ttu-id="363fc-163">El usuario finaliza la instalación.</span><span class="sxs-lookup"><span data-stu-id="363fc-163">User terminates install.</span></span> <span data-ttu-id="363fc-164">Se usa con los cuadros de diálogo de [UserExit](userexit-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="363fc-164">Used with [UserExit](userexit-dialog.md) dialog boxes.</span></span>     |
| <span data-ttu-id="363fc-165">msiDoActionStatusFailure</span><span class="sxs-lookup"><span data-stu-id="363fc-165">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="363fc-166">-3</span><span class="sxs-lookup"><span data-stu-id="363fc-166">-3</span></span>    | <span data-ttu-id="363fc-167">Se termina la salida grave.</span><span class="sxs-lookup"><span data-stu-id="363fc-167">Fatal exit terminates.</span></span> <span data-ttu-id="363fc-168">Se usa con un cuadro de diálogo de [FatalError](fatalerror-dialog.md) .</span><span class="sxs-lookup"><span data-stu-id="363fc-168">Used with a [FatalError](fatalerror-dialog.md) dialog boxes.</span></span> |
| <span data-ttu-id="363fc-169">msiDoActionStatusSuspend</span><span class="sxs-lookup"><span data-stu-id="363fc-169">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="363fc-170">-4</span><span class="sxs-lookup"><span data-stu-id="363fc-170">-4</span></span>    | <span data-ttu-id="363fc-171">La instalación está suspendida.</span><span class="sxs-lookup"><span data-stu-id="363fc-171">Install is suspended.</span></span>                                                                |



 

<span data-ttu-id="363fc-172">Cero, todos los demás números negativos o un valor null indican que nunca se llama a la acción.</span><span class="sxs-lookup"><span data-stu-id="363fc-172">Zero, all other negative numbers, or a null value indicate that the action is never called.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="363fc-173">Validación</span><span class="sxs-lookup"><span data-stu-id="363fc-173">Validation</span></span>

<dl>

[<span data-ttu-id="363fc-174">ICE03</span><span class="sxs-lookup"><span data-stu-id="363fc-174">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="363fc-175">ICE06</span><span class="sxs-lookup"><span data-stu-id="363fc-175">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="363fc-176">ICE12</span><span class="sxs-lookup"><span data-stu-id="363fc-176">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="363fc-177">ICE13</span><span class="sxs-lookup"><span data-stu-id="363fc-177">ICE13</span></span>](ice13.md)  
[<span data-ttu-id="363fc-178">ICE27</span><span class="sxs-lookup"><span data-stu-id="363fc-178">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="363fc-179">ICE46</span><span class="sxs-lookup"><span data-stu-id="363fc-179">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="363fc-180">ICE72</span><span class="sxs-lookup"><span data-stu-id="363fc-180">ICE72</span></span>](ice72.md)  
[<span data-ttu-id="363fc-181">ICE79</span><span class="sxs-lookup"><span data-stu-id="363fc-181">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="363fc-182">ICE82</span><span class="sxs-lookup"><span data-stu-id="363fc-182">ICE82</span></span>](ice82.md)  
[<span data-ttu-id="363fc-183">ICE83</span><span class="sxs-lookup"><span data-stu-id="363fc-183">ICE83</span></span>](ice83.md)  
[<span data-ttu-id="363fc-184">ICE84</span><span class="sxs-lookup"><span data-stu-id="363fc-184">ICE84</span></span>](ice84.md)  
[<span data-ttu-id="363fc-185">ICE86</span><span class="sxs-lookup"><span data-stu-id="363fc-185">ICE86</span></span>](ice86.md)  
[<span data-ttu-id="363fc-186">ICEM04</span><span class="sxs-lookup"><span data-stu-id="363fc-186">ICEM04</span></span>](icem04.md)  
</dl>

 

 



