---
description: Los desarrolladores de paquetes de Windows Installer pueden optar por usar un tipo de acción personalizada 19 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: c6df5462-e20e-4486-8480-8c747193c5d9
title: Tipo de acción personalizada 19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 695f86db0848bd65884ce5e233b4d9a249275c1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105670002"
---
# <a name="custom-action-type-19"></a><span data-ttu-id="acfdf-103">Tipo de acción personalizada 19</span><span class="sxs-lookup"><span data-stu-id="acfdf-103">Custom Action Type 19</span></span>

<span data-ttu-id="acfdf-104">Esta acción personalizada muestra un mensaje de error especificado, devuelve un error y, a continuación, finaliza la instalación.</span><span class="sxs-lookup"><span data-stu-id="acfdf-104">This custom action displays a specified error message, returns failure, and then terminates the installation.</span></span> <span data-ttu-id="acfdf-105">El mensaje de error mostrado se puede proporcionar como una cadena o como un índice en la [tabla de errores](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="acfdf-105">The error message displayed can be supplied as a string or as an index into the [Error table](error-table.md).</span></span>

## <a name="source"></a><span data-ttu-id="acfdf-106">Source</span><span class="sxs-lookup"><span data-stu-id="acfdf-106">Source</span></span>

<span data-ttu-id="acfdf-107">Deje en blanco la columna de origen de la [tabla CustomAction](customaction-table.md) .</span><span class="sxs-lookup"><span data-stu-id="acfdf-107">Leave the Source column of the [CustomAction table](customaction-table.md) blank.</span></span>

## <a name="type-value"></a><span data-ttu-id="acfdf-108">Valor de tipo</span><span class="sxs-lookup"><span data-stu-id="acfdf-108">Type Value</span></span>

<span data-ttu-id="acfdf-109">Incluya el siguiente valor en la columna Type de la tabla CustomAction para especificar el tipo numérico básico.</span><span class="sxs-lookup"><span data-stu-id="acfdf-109">Include the following value in the Type column of the CustomAction table to specify the basic numeric type.</span></span>



| <span data-ttu-id="acfdf-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="acfdf-110">Constants</span></span>                                                               | <span data-ttu-id="acfdf-111">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="acfdf-111">Hexadecimal</span></span> | <span data-ttu-id="acfdf-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="acfdf-112">Decimal</span></span> |
|-------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="acfdf-113">**msidbCustomActionTypeTextData**  +  **msidbCustomActionTypeSourceFile**</span><span class="sxs-lookup"><span data-stu-id="acfdf-113">**msidbCustomActionTypeTextData** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="acfdf-114">0x013</span><span class="sxs-lookup"><span data-stu-id="acfdf-114">0x013</span></span>       | <span data-ttu-id="acfdf-115">19</span><span class="sxs-lookup"><span data-stu-id="acfdf-115">19</span></span>      |



 

## <a name="target"></a><span data-ttu-id="acfdf-116">Destino</span><span class="sxs-lookup"><span data-stu-id="acfdf-116">Target</span></span>

<span data-ttu-id="acfdf-117">La columna de destino de la [tabla CustomAction](customaction-table.md) contiene una cadena de texto con el formato de la funcionalidad especificada en [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (sin los especificadores de campo numérico).</span><span class="sxs-lookup"><span data-stu-id="acfdf-117">The Target column of the [CustomAction table](customaction-table.md) contains a text string formatted using the functionality specified in [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (without the numeric field specifiers).</span></span> <span data-ttu-id="acfdf-118">Los parámetros que se van a reemplazar se incluyen entre corchetes, \[ ... \] y pueden ser propiedades, variables de entorno (% Prefix), rutas de acceso de archivo ( \# prefijo) o rutas de acceso de directorio de componentes ($ Prefix).</span><span class="sxs-lookup"><span data-stu-id="acfdf-118">Parameters to be replaced are enclosed in square brackets, \[…\], and may be properties, environment variables (% prefix), file paths (\# prefix), or component directory paths ($ prefix).</span></span> <span data-ttu-id="acfdf-119">Si después de dar formato a la cadena se evalúa como un entero, ese entero se utiliza como índice en la [tabla de errores](error-table.md) para recuperar el mensaje que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="acfdf-119">If after formatting the string evaluates to an integer, that integer is used as an index into the [Error table](error-table.md) to retrieve the message to display.</span></span> <span data-ttu-id="acfdf-120">Si después de dar formato a la cadena contiene caracteres no numéricos, la propia cadena se muestra como el mensaje.</span><span class="sxs-lookup"><span data-stu-id="acfdf-120">If after formatting the string contains non-numeric characters, the string itself is displayed as the message.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="acfdf-121">Opciones de procesamiento de valores devueltos</span><span class="sxs-lookup"><span data-stu-id="acfdf-121">Return Processing Options</span></span>

<span data-ttu-id="acfdf-122">La acción personalizada no usa ninguna opción.</span><span class="sxs-lookup"><span data-stu-id="acfdf-122">The custom action does not use any options.</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="acfdf-123">Opciones de programación de ejecución</span><span class="sxs-lookup"><span data-stu-id="acfdf-123">Execution Scheduling Options</span></span>

<span data-ttu-id="acfdf-124">La acción personalizada no usa ninguna opción.</span><span class="sxs-lookup"><span data-stu-id="acfdf-124">The custom action does not use any options.</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="acfdf-125">Opciones de ejecución de In-Script</span><span class="sxs-lookup"><span data-stu-id="acfdf-125">In-Script Execution Options</span></span>

<span data-ttu-id="acfdf-126">La acción personalizada no usa ninguna opción.</span><span class="sxs-lookup"><span data-stu-id="acfdf-126">The custom action does not use any options.</span></span>

## <a name="return-values"></a><span data-ttu-id="acfdf-127">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="acfdf-127">Return Values</span></span>

<span data-ttu-id="acfdf-128">Vea [valores devueltos de la acción personalizada](custom-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="acfdf-128">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="acfdf-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="acfdf-129">Remarks</span></span>

<span data-ttu-id="acfdf-130">Por ejemplo, las acciones personalizadas CAError1, CAError2, CAError3 y CAError4 devuelven estos mensajes.</span><span class="sxs-lookup"><span data-stu-id="acfdf-130">For example, the custom actions CAError1, CAError2, CAError3, and CAError4 return these messages.</span></span>

[<span data-ttu-id="acfdf-131">Tabla CustomAction</span><span class="sxs-lookup"><span data-stu-id="acfdf-131">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="acfdf-132">Acción</span><span class="sxs-lookup"><span data-stu-id="acfdf-132">Action</span></span>   | <span data-ttu-id="acfdf-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="acfdf-133">Type</span></span> | <span data-ttu-id="acfdf-134">Source</span><span class="sxs-lookup"><span data-stu-id="acfdf-134">Source</span></span> | <span data-ttu-id="acfdf-135">Destino</span><span class="sxs-lookup"><span data-stu-id="acfdf-135">Target</span></span>                              |
|----------|------|--------|-------------------------------------|
| <span data-ttu-id="acfdf-136">CAError1</span><span class="sxs-lookup"><span data-stu-id="acfdf-136">CAError1</span></span> | <span data-ttu-id="acfdf-137">19</span><span class="sxs-lookup"><span data-stu-id="acfdf-137">19</span></span>   |        | <span data-ttu-id="acfdf-138">\[Prop1\]</span><span class="sxs-lookup"><span data-stu-id="acfdf-138">\[Prop1\]</span></span>                           |
| <span data-ttu-id="acfdf-139">CAError2</span><span class="sxs-lookup"><span data-stu-id="acfdf-139">CAError2</span></span> | <span data-ttu-id="acfdf-140">19</span><span class="sxs-lookup"><span data-stu-id="acfdf-140">19</span></span>   |        | <span data-ttu-id="acfdf-141">Error de instalación debido a Error2.</span><span class="sxs-lookup"><span data-stu-id="acfdf-141">Installation failure due to Error2.</span></span> |
| <span data-ttu-id="acfdf-142">CAError3</span><span class="sxs-lookup"><span data-stu-id="acfdf-142">CAError3</span></span> | <span data-ttu-id="acfdf-143">19</span><span class="sxs-lookup"><span data-stu-id="acfdf-143">19</span></span>   |        | <span data-ttu-id="acfdf-144">25000</span><span class="sxs-lookup"><span data-stu-id="acfdf-144">25000</span></span>                               |
| <span data-ttu-id="acfdf-145">CAError4</span><span class="sxs-lookup"><span data-stu-id="acfdf-145">CAError4</span></span> | <span data-ttu-id="acfdf-146">19</span><span class="sxs-lookup"><span data-stu-id="acfdf-146">19</span></span>   |        | <span data-ttu-id="acfdf-147">\[Prop2\]</span><span class="sxs-lookup"><span data-stu-id="acfdf-147">\[Prop2\]</span></span>                           |



 

[<span data-ttu-id="acfdf-148">Tabla de propiedades</span><span class="sxs-lookup"><span data-stu-id="acfdf-148">Property Table</span></span>](property-table.md)



| <span data-ttu-id="acfdf-149">Propiedad</span><span class="sxs-lookup"><span data-stu-id="acfdf-149">Property</span></span> | <span data-ttu-id="acfdf-150">Value</span><span class="sxs-lookup"><span data-stu-id="acfdf-150">Value</span></span>                                 |
|----------|---------------------------------------|
| <span data-ttu-id="acfdf-151">Prop1</span><span class="sxs-lookup"><span data-stu-id="acfdf-151">Prop1</span></span>    | <span data-ttu-id="acfdf-152">"Error de instalación debido a Error1".</span><span class="sxs-lookup"><span data-stu-id="acfdf-152">"Installation failure due to Error1."</span></span> |
| <span data-ttu-id="acfdf-153">Prop2</span><span class="sxs-lookup"><span data-stu-id="acfdf-153">Prop2</span></span>    | <span data-ttu-id="acfdf-154">"25100"</span><span class="sxs-lookup"><span data-stu-id="acfdf-154">"25100"</span></span>                               |



 

[<span data-ttu-id="acfdf-155">Tabla de errores</span><span class="sxs-lookup"><span data-stu-id="acfdf-155">Error Table</span></span>](error-table.md)



| <span data-ttu-id="acfdf-156">Código</span><span class="sxs-lookup"><span data-stu-id="acfdf-156">Code</span></span>  | <span data-ttu-id="acfdf-157">Message</span><span class="sxs-lookup"><span data-stu-id="acfdf-157">Message</span></span>                             |
|-------|-------------------------------------|
| <span data-ttu-id="acfdf-158">25000</span><span class="sxs-lookup"><span data-stu-id="acfdf-158">25000</span></span> | <span data-ttu-id="acfdf-159">Error de instalación debido a error3.</span><span class="sxs-lookup"><span data-stu-id="acfdf-159">Installation failure due to Error3.</span></span> |
| <span data-ttu-id="acfdf-160">25100</span><span class="sxs-lookup"><span data-stu-id="acfdf-160">25100</span></span> | <span data-ttu-id="acfdf-161">Error de instalación debido a Error4.</span><span class="sxs-lookup"><span data-stu-id="acfdf-161">Installation failure due to Error4.</span></span> |



 

<span data-ttu-id="acfdf-162">Estas acciones personalizadas devuelven los siguientes mensajes de error:</span><span class="sxs-lookup"><span data-stu-id="acfdf-162">These custom actions return the following error messages:</span></span>



| <span data-ttu-id="acfdf-163">Acción personalizada</span><span class="sxs-lookup"><span data-stu-id="acfdf-163">Custom action</span></span> | <span data-ttu-id="acfdf-164">Cadena de mensaje devuelta</span><span class="sxs-lookup"><span data-stu-id="acfdf-164">Returned message string</span></span>             |
|---------------|-------------------------------------|
| <span data-ttu-id="acfdf-165">CAError1</span><span class="sxs-lookup"><span data-stu-id="acfdf-165">CAError1</span></span>      | <span data-ttu-id="acfdf-166">Error de instalación debido a Error1.</span><span class="sxs-lookup"><span data-stu-id="acfdf-166">Installation failure due to Error1.</span></span> |
| <span data-ttu-id="acfdf-167">CAError2</span><span class="sxs-lookup"><span data-stu-id="acfdf-167">CAError2</span></span>      | <span data-ttu-id="acfdf-168">Error de instalación debido a Error2.</span><span class="sxs-lookup"><span data-stu-id="acfdf-168">Installation failure due to Error2.</span></span> |
| <span data-ttu-id="acfdf-169">CAError3</span><span class="sxs-lookup"><span data-stu-id="acfdf-169">CAError3</span></span>      | <span data-ttu-id="acfdf-170">Error de instalación debido a error3.</span><span class="sxs-lookup"><span data-stu-id="acfdf-170">Installation failure due to Error3.</span></span> |
| <span data-ttu-id="acfdf-171">CAError4</span><span class="sxs-lookup"><span data-stu-id="acfdf-171">CAError4</span></span>      | <span data-ttu-id="acfdf-172">Error de instalación debido a Error4.</span><span class="sxs-lookup"><span data-stu-id="acfdf-172">Installation failure due to Error4.</span></span> |



 

<span data-ttu-id="acfdf-173">Tenga en cuenta que, dado que el orden de evaluación de las condiciones de inicio no se puede garantizar mediante la creación de la [tabla LaunchCondition](launchcondition-table.md), debe usar las acciones personalizadas del tipo de acción personalizada 19 en la instalación para evaluar las condiciones en un orden específico.</span><span class="sxs-lookup"><span data-stu-id="acfdf-173">Note that because the order of evaluation of launch conditions cannot be guaranteed by authoring the [LaunchCondition table](launchcondition-table.md), you should use Custom Action Type 19 custom actions in your installation to evaluate conditions in a specific order.</span></span>

## <a name="related-topics"></a><span data-ttu-id="acfdf-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="acfdf-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acfdf-175">\_Acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="acfdf-175">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



