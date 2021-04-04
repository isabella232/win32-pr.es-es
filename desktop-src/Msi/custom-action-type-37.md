---
description: Los desarrolladores de paquetes de Windows Installer pueden optar por usar un tipo de acción personalizada 37 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: 1c1e4f4f-1ccb-444c-940a-a1963d97714d
title: Tipo de acción personalizada 37
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30a42d4837af6fe2878f33624251d9c06550855b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083096"
---
# <a name="custom-action-type-37"></a><span data-ttu-id="94b98-103">Tipo de acción personalizada 37</span><span class="sxs-lookup"><span data-stu-id="94b98-103">Custom Action Type 37</span></span>

<span data-ttu-id="94b98-104">Esta acción personalizada se escribe en JScript, como ECMA 262.</span><span class="sxs-lookup"><span data-stu-id="94b98-104">This custom action is written in JScript, such as ECMA 262.</span></span> <span data-ttu-id="94b98-105">Windows Installer no admite JScript 1,0.</span><span class="sxs-lookup"><span data-stu-id="94b98-105">Windows Installer does not support JScript 1.0.</span></span> <span data-ttu-id="94b98-106">Para obtener más información, vea [scripts](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="94b98-106">For more information, see [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="94b98-107">Source</span><span class="sxs-lookup"><span data-stu-id="94b98-107">Source</span></span>

<span data-ttu-id="94b98-108">El campo de origen de la [tabla CustomAction](customaction-table.md) contiene el valor null.</span><span class="sxs-lookup"><span data-stu-id="94b98-108">The Source field of the [CustomAction table](customaction-table.md) contains the null value.</span></span> <span data-ttu-id="94b98-109">El código de script de la acción personalizada se almacena como una cadena de texto de script literal en el campo de destino.</span><span class="sxs-lookup"><span data-stu-id="94b98-109">The script code for the custom action is stored as a string of literal script text in the Target field.</span></span>

## <a name="type-value"></a><span data-ttu-id="94b98-110">Valor de tipo</span><span class="sxs-lookup"><span data-stu-id="94b98-110">Type Value</span></span>

<span data-ttu-id="94b98-111">Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico de una acción personalizada de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="94b98-111">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="94b98-112">Constantes</span><span class="sxs-lookup"><span data-stu-id="94b98-112">Constants</span></span>                                                             | <span data-ttu-id="94b98-113">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="94b98-113">Hexadecimal</span></span> | <span data-ttu-id="94b98-114">Decimal</span><span class="sxs-lookup"><span data-stu-id="94b98-114">Decimal</span></span> |
|-----------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="94b98-115">**msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeDirectory**</span><span class="sxs-lookup"><span data-stu-id="94b98-115">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeDirectory**</span></span> | <span data-ttu-id="94b98-116">0x025</span><span class="sxs-lookup"><span data-stu-id="94b98-116">0x025</span></span>       | <span data-ttu-id="94b98-117">37</span><span class="sxs-lookup"><span data-stu-id="94b98-117">37</span></span>      |



 

<span data-ttu-id="94b98-118">Windows Installer puede usar las acciones personalizadas de 64 bits en sistemas operativos de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="94b98-118">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="94b98-119">Una acción personalizada de 64 bits basada en scripts debe incluir el bit **msidbCustomActionType64BitScript** en su tipo numérico.</span><span class="sxs-lookup"><span data-stu-id="94b98-119">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="94b98-120">Para obtener información, consulte [acciones personalizadas de 64 bits](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="94b98-120">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="94b98-121">Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico de una acción personalizada de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="94b98-121">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="94b98-122">Constantes</span><span class="sxs-lookup"><span data-stu-id="94b98-122">Constants</span></span>                                                                                                    | <span data-ttu-id="94b98-123">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="94b98-123">Hexadecimal</span></span> | <span data-ttu-id="94b98-124">Decimal</span><span class="sxs-lookup"><span data-stu-id="94b98-124">Decimal</span></span> |
|--------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="94b98-125">**msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeDirectory**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="94b98-125">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeDirectory** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="94b98-126">0x0001025</span><span class="sxs-lookup"><span data-stu-id="94b98-126">0x0001025</span></span>   | <span data-ttu-id="94b98-127">4133</span><span class="sxs-lookup"><span data-stu-id="94b98-127">4133</span></span>    |



 

## <a name="target"></a><span data-ttu-id="94b98-128">Destino</span><span class="sxs-lookup"><span data-stu-id="94b98-128">Target</span></span>

<span data-ttu-id="94b98-129">El campo de destino de la [tabla CustomAction](customaction-table.md) contiene el código de script para la acción personalizada como una cadena de texto de script literal.</span><span class="sxs-lookup"><span data-stu-id="94b98-129">The Target field of the [CustomAction table](customaction-table.md) contains the script code for the custom action as a string of literal script text.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="94b98-130">Opciones de procesamiento de valores devueltos</span><span class="sxs-lookup"><span data-stu-id="94b98-130">Return Processing Options</span></span>

<span data-ttu-id="94b98-131">Incluya bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de procesamiento de valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="94b98-131">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="94b98-132">Para obtener una descripción de las opciones y los valores, vea [Opciones de procesamiento de devolución de acción personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="94b98-132">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="94b98-133">Opciones de programación de ejecución</span><span class="sxs-lookup"><span data-stu-id="94b98-133">Execution Scheduling Options</span></span>

<span data-ttu-id="94b98-134">Incluya los bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de programación de la ejecución.</span><span class="sxs-lookup"><span data-stu-id="94b98-134">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="94b98-135">Estas opciones controlan la ejecución múltiple de acciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="94b98-135">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="94b98-136">Para obtener una descripción de las opciones, vea opciones de programación de la [ejecución de acciones personalizadas](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="94b98-136">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="94b98-137">Opciones de ejecución de In-Script</span><span class="sxs-lookup"><span data-stu-id="94b98-137">In-Script Execution Options</span></span>

<span data-ttu-id="94b98-138">Incluya bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar una opción de ejecución en el script.</span><span class="sxs-lookup"><span data-stu-id="94b98-138">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="94b98-139">Estas opciones copian el código de acción en el script de ejecución, reversión o confirmación.</span><span class="sxs-lookup"><span data-stu-id="94b98-139">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="94b98-140">Para obtener una descripción de las opciones, vea [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="94b98-140">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="94b98-141">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="94b98-141">Return Values</span></span>

<span data-ttu-id="94b98-142">Este tipo de acción personalizada siempre devuelve SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="94b98-142">This custom action type always returns success.</span></span>

## <a name="remarks"></a><span data-ttu-id="94b98-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94b98-143">Remarks</span></span>

<span data-ttu-id="94b98-144">Una acción personalizada escrita en JScript o VBScript requiere el objeto de [**sesión**](session-object.md) de instalación.</span><span class="sxs-lookup"><span data-stu-id="94b98-144">A custom action that is written in JScript or VBScript requires the install [**Session**](session-object.md) object.</span></span> <span data-ttu-id="94b98-145">El instalador adjunta el **objeto de sesión** al script con el nombre "session".</span><span class="sxs-lookup"><span data-stu-id="94b98-145">The installer attaches the **Session Object** to the script with the name "Session".</span></span> <span data-ttu-id="94b98-146">Dado que es posible que el objeto de **sesión** no exista durante una reversión de la instalación, una acción personalizada diferida escrita en el script debe usar uno de los métodos o propiedades del objeto de **sesión** que se describe en la sección [obtener información de contexto para las acciones personalizadas de ejecución aplazada](obtaining-context-information-for-deferred-execution-custom-actions.md) para recuperar su contexto.</span><span class="sxs-lookup"><span data-stu-id="94b98-146">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94b98-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="94b98-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94b98-148">\_Acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="94b98-148">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



