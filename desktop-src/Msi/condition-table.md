---
description: La tabla de condiciones se puede usar para modificar el estado de selección de cualquier entrada en la tabla de características basada en una expresión condicional.
ms.assetid: 8e2d7c8d-5734-49aa-ad29-16d4d32cccb4
title: Tabla de condiciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74d9a3c27d43b7d71bc8e5b0593771bc86a3ca4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000953"
---
# <a name="condition-table"></a><span data-ttu-id="49b14-103">Tabla de condiciones</span><span class="sxs-lookup"><span data-stu-id="49b14-103">Condition Table</span></span>

<span data-ttu-id="49b14-104">La tabla de condiciones se puede usar para modificar el estado de selección de cualquier entrada en la [tabla de características](feature-table.md) basada en una expresión condicional.</span><span class="sxs-lookup"><span data-stu-id="49b14-104">The Condition table can be used to modify the selection state of any entry in the [Feature table](feature-table.md) based on a conditional expression.</span></span>

<span data-ttu-id="49b14-105">La tabla de condiciones tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="49b14-105">The Condition table has the following columns.</span></span>



| <span data-ttu-id="49b14-106">Columna</span><span class="sxs-lookup"><span data-stu-id="49b14-106">Column</span></span>    | <span data-ttu-id="49b14-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="49b14-107">Type</span></span>                         | <span data-ttu-id="49b14-108">Clave</span><span class="sxs-lookup"><span data-stu-id="49b14-108">Key</span></span> | <span data-ttu-id="49b14-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="49b14-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="49b14-110">Característica\_</span><span class="sxs-lookup"><span data-stu-id="49b14-110">Feature\_</span></span> | [<span data-ttu-id="49b14-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="49b14-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="49b14-112">Y</span><span class="sxs-lookup"><span data-stu-id="49b14-112">Y</span></span>   | <span data-ttu-id="49b14-113">N</span><span class="sxs-lookup"><span data-stu-id="49b14-113">N</span></span>        |
| <span data-ttu-id="49b14-114">Nivel</span><span class="sxs-lookup"><span data-stu-id="49b14-114">Level</span></span>     | [<span data-ttu-id="49b14-115">Entero</span><span class="sxs-lookup"><span data-stu-id="49b14-115">Integer</span></span>](integer.md)       | <span data-ttu-id="49b14-116">Y</span><span class="sxs-lookup"><span data-stu-id="49b14-116">Y</span></span>   | <span data-ttu-id="49b14-117">N</span><span class="sxs-lookup"><span data-stu-id="49b14-117">N</span></span>        |
| <span data-ttu-id="49b14-118">Condición</span><span class="sxs-lookup"><span data-stu-id="49b14-118">Condition</span></span> | [<span data-ttu-id="49b14-119">Condition</span><span class="sxs-lookup"><span data-stu-id="49b14-119">Condition</span></span>](condition.md)   | <span data-ttu-id="49b14-120">N</span><span class="sxs-lookup"><span data-stu-id="49b14-120">N</span></span>   | <span data-ttu-id="49b14-121">Y</span><span class="sxs-lookup"><span data-stu-id="49b14-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="49b14-122">Columnas</span><span class="sxs-lookup"><span data-stu-id="49b14-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="49b14-123"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Ofrecen\_</span><span class="sxs-lookup"><span data-stu-id="49b14-123"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="49b14-124">Clave externa en la columna uno de la tabla de características.</span><span class="sxs-lookup"><span data-stu-id="49b14-124">External key into column one of the Feature table.</span></span>

</dd> <dt>

<span data-ttu-id="49b14-125"><span id="Level"></span><span id="level"></span><span id="LEVEL"></span>Dosis</span><span class="sxs-lookup"><span data-stu-id="49b14-125"><span id="Level"></span><span id="level"></span><span id="LEVEL"></span>Level</span></span>
</dt> <dd>

<span data-ttu-id="49b14-126">Un nivel de instalación condicional para la característica en la \_ columna de característica de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="49b14-126">A conditional install level for the feature in the Feature\_ column of this table.</span></span> <span data-ttu-id="49b14-127">El instalador establece el nivel de instalación de esta característica en el nivel especificado en esta columna si la expresión de la columna condition se evalúa como TRUE.</span><span class="sxs-lookup"><span data-stu-id="49b14-127">The installer sets the install level of this feature to the level specified in this column if the expression in the Condition column evaluates to TRUE.</span></span>

</dd> <dt>

<span data-ttu-id="49b14-128"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Cumple</span><span class="sxs-lookup"><span data-stu-id="49b14-128"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="49b14-129">Si esta expresión condicional se evalúa como TRUE, la columna LEVEL de la tabla de características se establece en el nivel de instalación condicional.</span><span class="sxs-lookup"><span data-stu-id="49b14-129">If this conditional expression evaluates to TRUE, then the Level column in the Feature table is set to the conditional install level.</span></span>

<span data-ttu-id="49b14-130">La expresión de la columna condición no debe contener una referencia al estado instalado de cualquier característica o componente.</span><span class="sxs-lookup"><span data-stu-id="49b14-130">The expression in the Condition column should not contain reference to the installed state of any feature or component.</span></span> <span data-ttu-id="49b14-131">Esto se debe a que las expresiones de la columna condición se evalúan antes de que el instalador evalúe los Estados instalados de características y componentes.</span><span class="sxs-lookup"><span data-stu-id="49b14-131">This is because the expressions in the Condition column are evaluated before the installer evaluates the installed states of features and components.</span></span> <span data-ttu-id="49b14-132">Cualquier expresión de la tabla de condiciones que intenta comprobar el estado instalado de una característica o componente siempre se evalúa como false.</span><span class="sxs-lookup"><span data-stu-id="49b14-132">Any expression in the Condition table that attempts to check the installed state of a feature or component always evaluates to false.</span></span>

<span data-ttu-id="49b14-133">Para obtener información sobre la sintaxis de las instrucciones condicionales, vea sintaxis de la [instrucción condicional](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="49b14-133">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49b14-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="49b14-134">Remarks</span></span>

<span data-ttu-id="49b14-135">Una característica se puede deshabilitar permanentemente si se establece la columna LEVEL en 0.</span><span class="sxs-lookup"><span data-stu-id="49b14-135">A feature can be permanently disabled by setting the Level column to 0.</span></span>

<span data-ttu-id="49b14-136">El nivel se puede establecer en función de cualquier instrucción condicional, como una prueba para la plataforma, el sistema operativo o un valor de propiedad determinado.</span><span class="sxs-lookup"><span data-stu-id="49b14-136">The Level may be set based on any conditional statement, such as a test for platform, operating system, or a particular property setting.</span></span>

<span data-ttu-id="49b14-137">Las condiciones deben elegirse con cuidado para que una característica no esté habilitada en la instalación y deshabilitarse en la desinstalación.</span><span class="sxs-lookup"><span data-stu-id="49b14-137">Conditions should be carefully chosen so that a feature is not enabled on install and then disabled on uninstall.</span></span> <span data-ttu-id="49b14-138">Esto hará que la característica quede huérfana y el producto no podrá desinstalarse.</span><span class="sxs-lookup"><span data-stu-id="49b14-138">This will orphan the feature and the product will not be able to be uninstalled.</span></span>

<span data-ttu-id="49b14-139">Se hace referencia a esta tabla cuando se ejecuta la [acción CostFinalize](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="49b14-139">This table is referred to when the [CostFinalize action](costfinalize-action.md) is executed.</span></span>

<span data-ttu-id="49b14-140">Si la propiedad [**preseleccionada**](preselected.md) se ha establecido en 1, el instalador no evalúa la tabla de condiciones.</span><span class="sxs-lookup"><span data-stu-id="49b14-140">If the [**Preselected**](preselected.md) property has been set to 1, the installer does not evaluate the Condition table.</span></span> <span data-ttu-id="49b14-141">La tabla de condición solo afecta a la instalación de características cuando no se ha establecido ninguna de las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="49b14-141">The Condition table affects only the installation of features when none of the following properties have been set:</span></span>

<dl>

[<span data-ttu-id="49b14-142">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="49b14-142">**ADDLOCAL**</span></span>](addlocal.md)  
[<span data-ttu-id="49b14-143">**RETIRAR**</span><span class="sxs-lookup"><span data-stu-id="49b14-143">**REMOVE**</span></span>](remove.md)  
[<span data-ttu-id="49b14-144">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="49b14-144">**ADDSOURCE**</span></span>](addsource.md)  
[<span data-ttu-id="49b14-145">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="49b14-145">**ADDDEFAULT**</span></span>](adddefault.md)  
[<span data-ttu-id="49b14-146">**REINSTALAR**</span><span class="sxs-lookup"><span data-stu-id="49b14-146">**REINSTALL**</span></span>](reinstall.md)  
[<span data-ttu-id="49b14-147">**ANUNCIA**</span><span class="sxs-lookup"><span data-stu-id="49b14-147">**ADVERTISE**</span></span>](advertise.md)  
[<span data-ttu-id="49b14-148">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="49b14-148">**COMPADDLOCAL**</span></span>](compaddlocal.md)  
[<span data-ttu-id="49b14-149">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="49b14-149">**COMPADDSOURCE**</span></span>](compaddsource.md)  
[<span data-ttu-id="49b14-150">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="49b14-150">**COMPADDDEFAULT**</span></span>](compadddefault.md)  
[<span data-ttu-id="49b14-151">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="49b14-151">**FILEADDLOCAL**</span></span>](fileaddlocal.md)  
[<span data-ttu-id="49b14-152">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="49b14-152">**FILEADDSOURCE**</span></span>](fileaddsource.md)  
[<span data-ttu-id="49b14-153">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="49b14-153">**FILEADDDEFAULT**</span></span>](fileadddefault.md)  
</dl>

## <a name="validation"></a><span data-ttu-id="49b14-154">Validación</span><span class="sxs-lookup"><span data-stu-id="49b14-154">Validation</span></span>

<dl>

[<span data-ttu-id="49b14-155">ICE03</span><span class="sxs-lookup"><span data-stu-id="49b14-155">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="49b14-156">ICE06</span><span class="sxs-lookup"><span data-stu-id="49b14-156">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="49b14-157">ICE32</span><span class="sxs-lookup"><span data-stu-id="49b14-157">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="49b14-158">ICE46</span><span class="sxs-lookup"><span data-stu-id="49b14-158">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="49b14-159">ICE79</span><span class="sxs-lookup"><span data-stu-id="49b14-159">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="49b14-160">ICE86</span><span class="sxs-lookup"><span data-stu-id="49b14-160">ICE86</span></span>](ice86.md)  
</dl>

 

 



