---
description: ICE34 valida que cada botón de radio de cada control RadioButtonGroup tiene una propiedad en la columna propiedad de la tabla RadioButton que especifica su grupo de botones de radio.
ms.assetid: 23a88a5a-89e9-47bc-9c0a-6101ce03123c
title: ICE34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7723cb530397eae66374b0f218db9ad8505195a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667755"
---
# <a name="ice34"></a><span data-ttu-id="4405d-103">ICE34</span><span class="sxs-lookup"><span data-stu-id="4405d-103">ICE34</span></span>

<span data-ttu-id="4405d-104">ICE34 valida que cada botón de radio de cada [control RadioButtonGroup](radiobuttongroup-control.md) tiene una propiedad en la columna propiedad de la [tabla RadioButton](radiobutton-table.md) que especifica su grupo de botones de radio.</span><span class="sxs-lookup"><span data-stu-id="4405d-104">ICE34 validates that each radio button on every [RadioButtonGroup Control](radiobuttongroup-control.md) has a property in the Property column of the [RadioButton table](radiobutton-table.md) that specifies its radio button group.</span></span> <span data-ttu-id="4405d-105">ICE34 valida que esta propiedad existe y está establecida en un valor predeterminado en la [tabla de propiedades](property-table.md) que es igual a uno de los valores de botón de radio del grupo en la columna valor de la tabla RadioButton.</span><span class="sxs-lookup"><span data-stu-id="4405d-105">ICE34 validates that this property exists and is set to a default value in the [Property table](property-table.md) which is equal to one of the group's radio button values in the Value column of the RadioButton table.</span></span>

<span data-ttu-id="4405d-106">Un grupo de botones de radio debe tener un valor predeterminado para que los usuarios puedan seleccionar una opción mediante la tecla TAB.</span><span class="sxs-lookup"><span data-stu-id="4405d-106">A radio button group must have a default for users to be able to select a choice using the TAB key.</span></span> <span data-ttu-id="4405d-107">Esto es necesario para que la accesibilidad de los usuarios sea correcta.</span><span class="sxs-lookup"><span data-stu-id="4405d-107">This is required for proper user accessibility.</span></span>

<span data-ttu-id="4405d-108">ICE34 informa de las tablas que faltan.</span><span class="sxs-lookup"><span data-stu-id="4405d-108">ICE34 reports missing tables.</span></span>

## <a name="result"></a><span data-ttu-id="4405d-109">Resultado</span><span class="sxs-lookup"><span data-stu-id="4405d-109">Result</span></span>

<span data-ttu-id="4405d-110">ICE34 expone un mensaje de error si hay un botón de radio que especifica una propiedad no válida.</span><span class="sxs-lookup"><span data-stu-id="4405d-110">ICE34 post an error message if there is a radio button that specifies an invalid property.</span></span>

## <a name="example"></a><span data-ttu-id="4405d-111">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4405d-111">Example</span></span>

<span data-ttu-id="4405d-112">ICE34 notifica los siguientes errores para el ejemplo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="4405d-112">ICE34 reports the following errors for the example shown.</span></span>



| <span data-ttu-id="4405d-113">Error ICE34</span><span class="sxs-lookup"><span data-stu-id="4405d-113">ICE34 error</span></span>                                                                                                                                                                | <span data-ttu-id="4405d-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="4405d-114">Description</span></span>                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4405d-115">El control dialoga. Control2 debe tener una propiedad porque es de tipo RadioButtonGroup.</span><span class="sxs-lookup"><span data-stu-id="4405d-115">Control DialogA.Control2 must have a property because it is of type RadioButtonGroup.</span></span>                                                                                      | <span data-ttu-id="4405d-116">Hay un [control RadioButtonGroup](radiobuttongroup-control.md), sin el bit de [control indirecto](indirect-control-attribute.md) establecido en la columna Attributes de la [tabla de control](control-table.md), que no tiene una propiedad enumerada en la columna Property.</span><span class="sxs-lookup"><span data-stu-id="4405d-116">There is a [RadioButtonGroup control](radiobuttongroup-control.md), without the [Indirect control](indirect-control-attribute.md) bit set in the Attributes column of the [Control table](control-table.md), that does not have a property listed in the Property column.</span></span> |
| <span data-ttu-id="4405d-117">Quizás no es un valor predeterminado válido para RadioButtonGroup con la propiedad Property3.</span><span class="sxs-lookup"><span data-stu-id="4405d-117">Maybe is not a valid default value for the RadioButtonGroup using property Property3.</span></span> <span data-ttu-id="4405d-118">El valor debe aparecer como una opción en la tabla RadioButtonGroup.</span><span class="sxs-lookup"><span data-stu-id="4405d-118">The value must be listed as an option in the RadioButtonGroup table.</span></span>                 | <span data-ttu-id="4405d-119">Existe un valor predeterminado para una propiedad especificada en la columna valor de la [tabla de propiedades](property-table.md) que no es uno de los valores del grupo de botones de radio especificado en la columna valor de la [tabla RadioButton](radiobutton-table.md).</span><span class="sxs-lookup"><span data-stu-id="4405d-119">There is a default value for a property specified in the Value column of the [Property table](property-table.md) that is not one of the values for the radio button group specified in the Value column of the [RadioButton table](radiobutton-table.md).</span></span>                  |
| <span data-ttu-id="4405d-120">Se debe definir la propiedad PropertyB porque es una propiedad indirecta de un cuadro de diálogo de control RadioButtonGroup. Control4</span><span class="sxs-lookup"><span data-stu-id="4405d-120">Property PropertyB must be defined because it is an indirect property of a RadioButtonGroup control DialogA.Control4</span></span>                                                       | <span data-ttu-id="4405d-121">La propiedad a la que hace referencia este grupo RadioButton es una propiedad indirecta y el valor de la propiedad indirecta no es una de las opciones del grupo RadioButton.</span><span class="sxs-lookup"><span data-stu-id="4405d-121">The property referenced by this RadioButton group is an indirect property, and the value of the indirect property is not one of the choices for the RadioButton group.</span></span>                                                                                                       |
| <span data-ttu-id="4405d-122">Quizás no es un valor predeterminado válido para la propiedad propertya.</span><span class="sxs-lookup"><span data-stu-id="4405d-122">Maybe is not a valid default value for the property PropertyA.</span></span> <span data-ttu-id="4405d-123">La propiedad es una propiedad RadioButtonGroup indirecta de control dialoga. Control5 (a través de la propiedad Property5).</span><span class="sxs-lookup"><span data-stu-id="4405d-123">The property is an indirect RadioButtonGroup property of control DialogA.Control5 (via property Property5).</span></span> | <span data-ttu-id="4405d-124">El valor de la propiedad indirecta a la que se hace referencia a través del control no es ninguno de los valores predeterminados para ese RadioButtonGroup.</span><span class="sxs-lookup"><span data-stu-id="4405d-124">The value of the indirect property referenced via the control is not one of the default values for that RadioButtonGroup.</span></span>                                                                                                                                                    |



 

<span data-ttu-id="4405d-125">[Tabla de control](control-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="4405d-125">[Control Table](control-table.md) (partial)</span></span>



| <span data-ttu-id="4405d-126">Diálogo</span><span class="sxs-lookup"><span data-stu-id="4405d-126">Dialog</span></span>  | <span data-ttu-id="4405d-127">Control</span><span class="sxs-lookup"><span data-stu-id="4405d-127">Control</span></span>  | <span data-ttu-id="4405d-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="4405d-128">Type</span></span>             | <span data-ttu-id="4405d-129">Atributos</span><span class="sxs-lookup"><span data-stu-id="4405d-129">Attributes</span></span> | <span data-ttu-id="4405d-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4405d-130">Property</span></span>  |
|---------|----------|------------------|------------|-----------|
| <span data-ttu-id="4405d-131">Cuadro de diálogo</span><span class="sxs-lookup"><span data-stu-id="4405d-131">DialogA</span></span> | <span data-ttu-id="4405d-132">Control1</span><span class="sxs-lookup"><span data-stu-id="4405d-132">Control1</span></span> | <span data-ttu-id="4405d-133">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="4405d-133">RadioButtonGroup</span></span> | <span data-ttu-id="4405d-134">0</span><span class="sxs-lookup"><span data-stu-id="4405d-134">0</span></span>          | <span data-ttu-id="4405d-135">Property1</span><span class="sxs-lookup"><span data-stu-id="4405d-135">Property1</span></span> |
| <span data-ttu-id="4405d-136">Cuadro de diálogo</span><span class="sxs-lookup"><span data-stu-id="4405d-136">DialogA</span></span> | <span data-ttu-id="4405d-137">Control2</span><span class="sxs-lookup"><span data-stu-id="4405d-137">Control2</span></span> | <span data-ttu-id="4405d-138">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="4405d-138">RadioButtonGroup</span></span> | <span data-ttu-id="4405d-139">0</span><span class="sxs-lookup"><span data-stu-id="4405d-139">0</span></span>          |           |
| <span data-ttu-id="4405d-140">Cuadro de diálogo</span><span class="sxs-lookup"><span data-stu-id="4405d-140">DialogA</span></span> | <span data-ttu-id="4405d-141">Control3</span><span class="sxs-lookup"><span data-stu-id="4405d-141">Control3</span></span> | <span data-ttu-id="4405d-142">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="4405d-142">RadioButtonGroup</span></span> | <span data-ttu-id="4405d-143">0</span><span class="sxs-lookup"><span data-stu-id="4405d-143">0</span></span>          | <span data-ttu-id="4405d-144">Property3</span><span class="sxs-lookup"><span data-stu-id="4405d-144">Property3</span></span> |
| <span data-ttu-id="4405d-145">Cuadro de diálogo</span><span class="sxs-lookup"><span data-stu-id="4405d-145">DialogA</span></span> | <span data-ttu-id="4405d-146">Control4</span><span class="sxs-lookup"><span data-stu-id="4405d-146">Control4</span></span> | <span data-ttu-id="4405d-147">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="4405d-147">RadioButtonGroup</span></span> | <span data-ttu-id="4405d-148">8</span><span class="sxs-lookup"><span data-stu-id="4405d-148">8</span></span>          | <span data-ttu-id="4405d-149">Property4</span><span class="sxs-lookup"><span data-stu-id="4405d-149">Property4</span></span> |
| <span data-ttu-id="4405d-150">Cuadro de diálogo</span><span class="sxs-lookup"><span data-stu-id="4405d-150">DialogA</span></span> | <span data-ttu-id="4405d-151">Control5</span><span class="sxs-lookup"><span data-stu-id="4405d-151">Control5</span></span> | <span data-ttu-id="4405d-152">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="4405d-152">RadioButtonGroup</span></span> | <span data-ttu-id="4405d-153">8</span><span class="sxs-lookup"><span data-stu-id="4405d-153">8</span></span>          | <span data-ttu-id="4405d-154">Property5</span><span class="sxs-lookup"><span data-stu-id="4405d-154">Property5</span></span> |



 

<span data-ttu-id="4405d-155">[Tabla de propiedades](property-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="4405d-155">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="4405d-156">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4405d-156">Property</span></span>  | <span data-ttu-id="4405d-157">Value</span><span class="sxs-lookup"><span data-stu-id="4405d-157">Value</span></span>     |
|-----------|-----------|
| <span data-ttu-id="4405d-158">Property1</span><span class="sxs-lookup"><span data-stu-id="4405d-158">Property1</span></span> | <span data-ttu-id="4405d-159">Sí</span><span class="sxs-lookup"><span data-stu-id="4405d-159">Yes</span></span>       |
| <span data-ttu-id="4405d-160">Property3</span><span class="sxs-lookup"><span data-stu-id="4405d-160">Property3</span></span> | <span data-ttu-id="4405d-161">Es posible</span><span class="sxs-lookup"><span data-stu-id="4405d-161">Maybe</span></span>     |
| <span data-ttu-id="4405d-162">Property4</span><span class="sxs-lookup"><span data-stu-id="4405d-162">Property4</span></span> | <span data-ttu-id="4405d-163">PropertyB</span><span class="sxs-lookup"><span data-stu-id="4405d-163">PropertyB</span></span> |
| <span data-ttu-id="4405d-164">Property5</span><span class="sxs-lookup"><span data-stu-id="4405d-164">Property5</span></span> | <span data-ttu-id="4405d-165">Propiedad a</span><span class="sxs-lookup"><span data-stu-id="4405d-165">PropertyA</span></span> |
| <span data-ttu-id="4405d-166">Propiedad a</span><span class="sxs-lookup"><span data-stu-id="4405d-166">PropertyA</span></span> | <span data-ttu-id="4405d-167">Es posible</span><span class="sxs-lookup"><span data-stu-id="4405d-167">Maybe</span></span>     |



 

<span data-ttu-id="4405d-168">[Tabla RadioButton](radiobutton-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="4405d-168">[RadioButton Table](radiobutton-table.md) (partial)</span></span>



| <span data-ttu-id="4405d-169">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4405d-169">Property</span></span>  | <span data-ttu-id="4405d-170">Pedido</span><span class="sxs-lookup"><span data-stu-id="4405d-170">Order</span></span> | <span data-ttu-id="4405d-171">Value</span><span class="sxs-lookup"><span data-stu-id="4405d-171">Value</span></span> |
|-----------|-------|-------|
| <span data-ttu-id="4405d-172">Property1</span><span class="sxs-lookup"><span data-stu-id="4405d-172">Property1</span></span> | <span data-ttu-id="4405d-173">1</span><span class="sxs-lookup"><span data-stu-id="4405d-173">1</span></span>     | <span data-ttu-id="4405d-174">Sí</span><span class="sxs-lookup"><span data-stu-id="4405d-174">Yes</span></span>   |
| <span data-ttu-id="4405d-175">Property1</span><span class="sxs-lookup"><span data-stu-id="4405d-175">Property1</span></span> | <span data-ttu-id="4405d-176">2</span><span class="sxs-lookup"><span data-stu-id="4405d-176">2</span></span>     | <span data-ttu-id="4405d-177">Ahora</span><span class="sxs-lookup"><span data-stu-id="4405d-177">Now</span></span>   |
| <span data-ttu-id="4405d-178">Property2</span><span class="sxs-lookup"><span data-stu-id="4405d-178">Property2</span></span> | <span data-ttu-id="4405d-179">1</span><span class="sxs-lookup"><span data-stu-id="4405d-179">1</span></span>     | <span data-ttu-id="4405d-180">Sí</span><span class="sxs-lookup"><span data-stu-id="4405d-180">Yes</span></span>   |
| <span data-ttu-id="4405d-181">Property2</span><span class="sxs-lookup"><span data-stu-id="4405d-181">Property2</span></span> | <span data-ttu-id="4405d-182">2</span><span class="sxs-lookup"><span data-stu-id="4405d-182">2</span></span>     | <span data-ttu-id="4405d-183">No</span><span class="sxs-lookup"><span data-stu-id="4405d-183">No</span></span>    |
| <span data-ttu-id="4405d-184">Property3</span><span class="sxs-lookup"><span data-stu-id="4405d-184">Property3</span></span> | <span data-ttu-id="4405d-185">1</span><span class="sxs-lookup"><span data-stu-id="4405d-185">1</span></span>     | <span data-ttu-id="4405d-186">Sí</span><span class="sxs-lookup"><span data-stu-id="4405d-186">Yes</span></span>   |
| <span data-ttu-id="4405d-187">Property3</span><span class="sxs-lookup"><span data-stu-id="4405d-187">Property3</span></span> | <span data-ttu-id="4405d-188">2</span><span class="sxs-lookup"><span data-stu-id="4405d-188">2</span></span>     | <span data-ttu-id="4405d-189">No</span><span class="sxs-lookup"><span data-stu-id="4405d-189">No</span></span>    |
| <span data-ttu-id="4405d-190">Property4</span><span class="sxs-lookup"><span data-stu-id="4405d-190">Property4</span></span> | <span data-ttu-id="4405d-191">1</span><span class="sxs-lookup"><span data-stu-id="4405d-191">1</span></span>     | <span data-ttu-id="4405d-192">Sí</span><span class="sxs-lookup"><span data-stu-id="4405d-192">Yes</span></span>   |
| <span data-ttu-id="4405d-193">Property4</span><span class="sxs-lookup"><span data-stu-id="4405d-193">Property4</span></span> | <span data-ttu-id="4405d-194">2</span><span class="sxs-lookup"><span data-stu-id="4405d-194">2</span></span>     | <span data-ttu-id="4405d-195">No</span><span class="sxs-lookup"><span data-stu-id="4405d-195">No</span></span>    |
| <span data-ttu-id="4405d-196">Propiedad a</span><span class="sxs-lookup"><span data-stu-id="4405d-196">PropertyA</span></span> | <span data-ttu-id="4405d-197">1</span><span class="sxs-lookup"><span data-stu-id="4405d-197">1</span></span>     | <span data-ttu-id="4405d-198">Sí</span><span class="sxs-lookup"><span data-stu-id="4405d-198">Yes</span></span>   |
| <span data-ttu-id="4405d-199">Propiedad a</span><span class="sxs-lookup"><span data-stu-id="4405d-199">PropertyA</span></span> | <span data-ttu-id="4405d-200">2</span><span class="sxs-lookup"><span data-stu-id="4405d-200">2</span></span>     | <span data-ttu-id="4405d-201">No</span><span class="sxs-lookup"><span data-stu-id="4405d-201">No</span></span>    |
| <span data-ttu-id="4405d-202">PropertyB</span><span class="sxs-lookup"><span data-stu-id="4405d-202">PropertyB</span></span> | <span data-ttu-id="4405d-203">1</span><span class="sxs-lookup"><span data-stu-id="4405d-203">1</span></span>     | <span data-ttu-id="4405d-204">Sí</span><span class="sxs-lookup"><span data-stu-id="4405d-204">Yes</span></span>   |
| <span data-ttu-id="4405d-205">PropertyB</span><span class="sxs-lookup"><span data-stu-id="4405d-205">PropertyB</span></span> | <span data-ttu-id="4405d-206">2</span><span class="sxs-lookup"><span data-stu-id="4405d-206">2</span></span>     | <span data-ttu-id="4405d-207">No</span><span class="sxs-lookup"><span data-stu-id="4405d-207">No</span></span>    |



 

<span data-ttu-id="4405d-208">Para corregir los errores que se indican en esta ICE, compruebe lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="4405d-208">To fix the errors reported by this ICE, check the following:</span></span>

-   <span data-ttu-id="4405d-209">Cada entrada de control RadioButton sin el conjunto de atributos indirectos tiene una propiedad que aparece en la columna propiedad:</span><span class="sxs-lookup"><span data-stu-id="4405d-209">That every RadioButton control entry without the indirect attribute set has a property listed in the Property column:</span></span>
-   <span data-ttu-id="4405d-210">Que cada propiedad de este tipo tiene al menos una entrada correspondiente en la tabla RadioButton.</span><span class="sxs-lookup"><span data-stu-id="4405d-210">That every such property has at least one corresponding entry in the RadioButton table.</span></span>
-   <span data-ttu-id="4405d-211">Cada una de estas propiedades se define en la tabla de propiedades, con un valor que es una de las opciones de la tabla RadioButton.</span><span class="sxs-lookup"><span data-stu-id="4405d-211">That every such property is defined in the Property table, with a value that is one of the choices from the RadioButton table.</span></span>
-   <span data-ttu-id="4405d-212">Todas las propiedades a las que se hace referencia en la columna de propiedades de un control RadioButton con el conjunto de atributos indirecto se definen en la tabla de propiedades.</span><span class="sxs-lookup"><span data-stu-id="4405d-212">That every property referenced in the Property column of a RadioButton control with the indirect attribute set is defined in the Property table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4405d-213">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4405d-213">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4405d-214">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="4405d-214">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



