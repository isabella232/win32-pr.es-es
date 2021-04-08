---
description: La tabla ControlCondition permite que un autor especifique acciones especiales que se aplicarán a los controles basándose en el resultado de una instrucción condicional. Por ejemplo, al usar esta tabla, el autor podría optar por ocultar un control basado en la propiedad VersionNT.
ms.assetid: e36d20ec-cd7b-494f-b517-c07b40d2a338
title: Tabla ControlCondition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 671dcdee6e2ed1067c51a04084693c276b8db2d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002371"
---
# <a name="controlcondition-table"></a><span data-ttu-id="2f1bd-104">Tabla ControlCondition</span><span class="sxs-lookup"><span data-stu-id="2f1bd-104">ControlCondition Table</span></span>

<span data-ttu-id="2f1bd-105">La tabla ControlCondition permite que un autor especifique acciones especiales que se aplicarán a los controles basándose en el resultado de una instrucción condicional.</span><span class="sxs-lookup"><span data-stu-id="2f1bd-105">The ControlCondition table enables an author to specify special actions to be applied to controls based on the result of a conditional statement.</span></span> <span data-ttu-id="2f1bd-106">Por ejemplo, al usar esta tabla, el autor podría optar por ocultar un control basado en la propiedad [**VersionNT**](versionnt.md) .</span><span class="sxs-lookup"><span data-stu-id="2f1bd-106">For example, using this table the author could choose to hide a control based on the [**VersionNT**](versionnt.md) property.</span></span>

<span data-ttu-id="2f1bd-107">La tabla ControlCondition tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="2f1bd-107">The ControlCondition table has the following columns.</span></span>



| <span data-ttu-id="2f1bd-108">Columna</span><span class="sxs-lookup"><span data-stu-id="2f1bd-108">Column</span></span>    | <span data-ttu-id="2f1bd-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="2f1bd-109">Type</span></span>                         | <span data-ttu-id="2f1bd-110">Clave</span><span class="sxs-lookup"><span data-stu-id="2f1bd-110">Key</span></span> | <span data-ttu-id="2f1bd-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="2f1bd-111">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="2f1bd-112">Diálogo\_</span><span class="sxs-lookup"><span data-stu-id="2f1bd-112">Dialog\_</span></span>  | [<span data-ttu-id="2f1bd-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="2f1bd-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="2f1bd-114">Y</span><span class="sxs-lookup"><span data-stu-id="2f1bd-114">Y</span></span>   | <span data-ttu-id="2f1bd-115">N</span><span class="sxs-lookup"><span data-stu-id="2f1bd-115">N</span></span>        |
| <span data-ttu-id="2f1bd-116">control\_</span><span class="sxs-lookup"><span data-stu-id="2f1bd-116">Control\_</span></span> | [<span data-ttu-id="2f1bd-117">Identificador</span><span class="sxs-lookup"><span data-stu-id="2f1bd-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="2f1bd-118">Y</span><span class="sxs-lookup"><span data-stu-id="2f1bd-118">Y</span></span>   | <span data-ttu-id="2f1bd-119">N</span><span class="sxs-lookup"><span data-stu-id="2f1bd-119">N</span></span>        |
| <span data-ttu-id="2f1bd-120">Acción</span><span class="sxs-lookup"><span data-stu-id="2f1bd-120">Action</span></span>    | [<span data-ttu-id="2f1bd-121">Texto</span><span class="sxs-lookup"><span data-stu-id="2f1bd-121">Text</span></span>](text.md)             | <span data-ttu-id="2f1bd-122">Y</span><span class="sxs-lookup"><span data-stu-id="2f1bd-122">Y</span></span>   | <span data-ttu-id="2f1bd-123">N</span><span class="sxs-lookup"><span data-stu-id="2f1bd-123">N</span></span>        |
| <span data-ttu-id="2f1bd-124">Condición</span><span class="sxs-lookup"><span data-stu-id="2f1bd-124">Condition</span></span> | [<span data-ttu-id="2f1bd-125">Condition</span><span class="sxs-lookup"><span data-stu-id="2f1bd-125">Condition</span></span>](condition.md)   | <span data-ttu-id="2f1bd-126">Y</span><span class="sxs-lookup"><span data-stu-id="2f1bd-126">Y</span></span>   | <span data-ttu-id="2f1bd-127">N</span><span class="sxs-lookup"><span data-stu-id="2f1bd-127">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="2f1bd-128">Columnas</span><span class="sxs-lookup"><span data-stu-id="2f1bd-128">Columns</span></span>

<dl> <dt>

<span data-ttu-id="2f1bd-129"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Diálogo\_</span><span class="sxs-lookup"><span data-stu-id="2f1bd-129"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialog\_</span></span>
</dt> <dd>

<span data-ttu-id="2f1bd-130">Una clave externa a la primera columna de la [tabla del cuadro de diálogo](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="2f1bd-130">An external key to the first column of the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="2f1bd-131">La combinación de este campo con el campo de control \_ identifica un control único.</span><span class="sxs-lookup"><span data-stu-id="2f1bd-131">Combining this field with the Control\_ field identifies a unique control.</span></span>

</dd> <dt>

<span data-ttu-id="2f1bd-132"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Control\_</span><span class="sxs-lookup"><span data-stu-id="2f1bd-132"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Control\_</span></span>
</dt> <dd>

<span data-ttu-id="2f1bd-133">Una clave externa a la segunda columna de la [tabla de control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="2f1bd-133">An external key to the second column of the [Control table](control-table.md).</span></span> <span data-ttu-id="2f1bd-134">Al combinar este campo, el campo del cuadro de diálogo \_ identifica un control único.</span><span class="sxs-lookup"><span data-stu-id="2f1bd-134">Combining this field the Dialog\_ field identifies a unique control.</span></span>

</dd> <dt>

<span data-ttu-id="2f1bd-135"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Actuar</span><span class="sxs-lookup"><span data-stu-id="2f1bd-135"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="2f1bd-136">Acción que se va a realizar en el control.</span><span class="sxs-lookup"><span data-stu-id="2f1bd-136">The action that is to be taken on the control.</span></span> <span data-ttu-id="2f1bd-137">En la tabla siguiente se muestran las acciones posibles.</span><span class="sxs-lookup"><span data-stu-id="2f1bd-137">The possible actions are shown in the following table.</span></span>



| <span data-ttu-id="2f1bd-138">Value</span><span class="sxs-lookup"><span data-stu-id="2f1bd-138">Value</span></span>   | <span data-ttu-id="2f1bd-139">Significado</span><span class="sxs-lookup"><span data-stu-id="2f1bd-139">Meaning</span></span>                     |
|---------|-----------------------------|
| <span data-ttu-id="2f1bd-140">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="2f1bd-140">Default</span></span> | <span data-ttu-id="2f1bd-141">Establecer el control como el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="2f1bd-141">Set control as the default.</span></span> |
| <span data-ttu-id="2f1bd-142">Disable</span><span class="sxs-lookup"><span data-stu-id="2f1bd-142">Disable</span></span> | <span data-ttu-id="2f1bd-143">Deshabilite el control.</span><span class="sxs-lookup"><span data-stu-id="2f1bd-143">Disable the control.</span></span>        |
| <span data-ttu-id="2f1bd-144">Habilitar</span><span class="sxs-lookup"><span data-stu-id="2f1bd-144">Enable</span></span>  | <span data-ttu-id="2f1bd-145">Habilite el control.</span><span class="sxs-lookup"><span data-stu-id="2f1bd-145">Enable the control.</span></span>         |
| <span data-ttu-id="2f1bd-146">Ocultar</span><span class="sxs-lookup"><span data-stu-id="2f1bd-146">Hide</span></span>    | <span data-ttu-id="2f1bd-147">Oculte el control.</span><span class="sxs-lookup"><span data-stu-id="2f1bd-147">Hide the control.</span></span>           |
| <span data-ttu-id="2f1bd-148">Mostrar</span><span class="sxs-lookup"><span data-stu-id="2f1bd-148">Show</span></span>    | <span data-ttu-id="2f1bd-149">Mostrar el control.</span><span class="sxs-lookup"><span data-stu-id="2f1bd-149">Display the control.</span></span>        |



 

</dd> <dt>

<span data-ttu-id="2f1bd-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Cumple</span><span class="sxs-lookup"><span data-stu-id="2f1bd-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="2f1bd-151">Instrucción condicional que especifica en qué condiciones se debe desencadenar la acción.</span><span class="sxs-lookup"><span data-stu-id="2f1bd-151">A conditional statement that specifies under which conditions the action should be triggered.</span></span> <span data-ttu-id="2f1bd-152">Esta columna no se puede dejar en blanco.</span><span class="sxs-lookup"><span data-stu-id="2f1bd-152">This column may not be left blank.</span></span> <span data-ttu-id="2f1bd-153">Si esta instrucción no se evalúa como TRUE, la acción no tiene lugar.</span><span class="sxs-lookup"><span data-stu-id="2f1bd-153">If this statement does not evaluate to TRUE, the action does not take place.</span></span> <span data-ttu-id="2f1bd-154">Si se establece en 1, siempre se aplica la acción.</span><span class="sxs-lookup"><span data-stu-id="2f1bd-154">If it is set to 1, the action is always applied.</span></span> <span data-ttu-id="2f1bd-155">Para obtener información sobre la sintaxis de las instrucciones condicionales, vea sintaxis de la [instrucción condicional](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="2f1bd-155">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f1bd-156">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f1bd-156">Remarks</span></span>

<span data-ttu-id="2f1bd-157">Si desea ocultar y deshabilitar un control [Pushbutton](pushbutton-control.md) o un [control de casilla](checkbox-control.md) basado en una instrucción condicional en el campo condición de la tabla ControlCondition, debe usar cuatro registros para que cada control se deshabilite y oculte el control.</span><span class="sxs-lookup"><span data-stu-id="2f1bd-157">If you want to hide and disable a [PushButton control](pushbutton-control.md) or [CheckBox control](checkbox-control.md) based on a conditional statement in the Condition field of the ControlCondition table, you should use four records for each control to disable as well as hide the control.</span></span> <span data-ttu-id="2f1bd-158">Todavía se puede tener acceso a los controles de pulsador o casilla que solo se han ocultado mediante teclas de método abreviado.</span><span class="sxs-lookup"><span data-stu-id="2f1bd-158">PushButton or CheckBox controls that have only been hidden can still be accessed by shortcut keys.</span></span>

<span data-ttu-id="2f1bd-159">Por ejemplo, los registros siguientes ocultan y deshabilitan controla en el cuadro de diálogo cuando se instala el producto.</span><span class="sxs-lookup"><span data-stu-id="2f1bd-159">For example, the following records hide and disable ControlA on DialogA when the product is installed.</span></span> <span data-ttu-id="2f1bd-160">El control estará visible y habilitado cuando el producto no esté instalado.</span><span class="sxs-lookup"><span data-stu-id="2f1bd-160">The control will be visible and enabled when the product is not installed.</span></span>



| <span data-ttu-id="2f1bd-161">Diálogo</span><span class="sxs-lookup"><span data-stu-id="2f1bd-161">Dialog</span></span>  | <span data-ttu-id="2f1bd-162">Control</span><span class="sxs-lookup"><span data-stu-id="2f1bd-162">Control</span></span>  | <span data-ttu-id="2f1bd-163">Acción</span><span class="sxs-lookup"><span data-stu-id="2f1bd-163">Action</span></span>  | <span data-ttu-id="2f1bd-164">Condición</span><span class="sxs-lookup"><span data-stu-id="2f1bd-164">Condition</span></span>                      |
|---------|----------|---------|--------------------------------|
| <span data-ttu-id="2f1bd-165">Cuadro de diálogo</span><span class="sxs-lookup"><span data-stu-id="2f1bd-165">DialogA</span></span> | <span data-ttu-id="2f1bd-166">ControlA</span><span class="sxs-lookup"><span data-stu-id="2f1bd-166">ControlA</span></span> | <span data-ttu-id="2f1bd-167">Ocultar</span><span class="sxs-lookup"><span data-stu-id="2f1bd-167">Hide</span></span>    | [<span data-ttu-id="2f1bd-168">**Instalado**</span><span class="sxs-lookup"><span data-stu-id="2f1bd-168">**Installed**</span></span>](installed.md) |
| <span data-ttu-id="2f1bd-169">Cuadro de diálogo</span><span class="sxs-lookup"><span data-stu-id="2f1bd-169">DialogA</span></span> | <span data-ttu-id="2f1bd-170">ControlA</span><span class="sxs-lookup"><span data-stu-id="2f1bd-170">ControlA</span></span> | <span data-ttu-id="2f1bd-171">Disable</span><span class="sxs-lookup"><span data-stu-id="2f1bd-171">Disable</span></span> | <span data-ttu-id="2f1bd-172">Instalado</span><span class="sxs-lookup"><span data-stu-id="2f1bd-172">Installed</span></span>                      |
| <span data-ttu-id="2f1bd-173">Cuadro de diálogo</span><span class="sxs-lookup"><span data-stu-id="2f1bd-173">DialogA</span></span> | <span data-ttu-id="2f1bd-174">ControlA</span><span class="sxs-lookup"><span data-stu-id="2f1bd-174">ControlA</span></span> | <span data-ttu-id="2f1bd-175">Mostrar</span><span class="sxs-lookup"><span data-stu-id="2f1bd-175">Show</span></span>    | <span data-ttu-id="2f1bd-176">NO instalado</span><span class="sxs-lookup"><span data-stu-id="2f1bd-176">NOT Installed</span></span>                  |
| <span data-ttu-id="2f1bd-177">Cuadro de diálogo</span><span class="sxs-lookup"><span data-stu-id="2f1bd-177">DialogA</span></span> | <span data-ttu-id="2f1bd-178">ControlA</span><span class="sxs-lookup"><span data-stu-id="2f1bd-178">ControlA</span></span> | <span data-ttu-id="2f1bd-179">Habilitar</span><span class="sxs-lookup"><span data-stu-id="2f1bd-179">Enable</span></span>  | <span data-ttu-id="2f1bd-180">NO instalado</span><span class="sxs-lookup"><span data-stu-id="2f1bd-180">NOT Installed</span></span>                  |



 

## <a name="validation"></a><span data-ttu-id="2f1bd-181">Validación</span><span class="sxs-lookup"><span data-stu-id="2f1bd-181">Validation</span></span>

<dl>

[<span data-ttu-id="2f1bd-182">ICE03</span><span class="sxs-lookup"><span data-stu-id="2f1bd-182">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="2f1bd-183">ICE06</span><span class="sxs-lookup"><span data-stu-id="2f1bd-183">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="2f1bd-184">ICE17</span><span class="sxs-lookup"><span data-stu-id="2f1bd-184">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="2f1bd-185">ICE32</span><span class="sxs-lookup"><span data-stu-id="2f1bd-185">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="2f1bd-186">ICE46</span><span class="sxs-lookup"><span data-stu-id="2f1bd-186">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="2f1bd-187">ICE79</span><span class="sxs-lookup"><span data-stu-id="2f1bd-187">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="2f1bd-188">ICE86</span><span class="sxs-lookup"><span data-stu-id="2f1bd-188">ICE86</span></span>](ice86.md)  
</dl>

 

 



