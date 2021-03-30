---
description: Los desarrolladores de paquetes de Windows Installer pueden optar por usar un tipo de acción personalizada 53 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: d024c73e-c2dc-4187-a8ae-ed96dc7c107e
title: Tipo de acción personalizada 53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a016d3b3f5a282567b909215d6ab7b32759417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002280"
---
# <a name="custom-action-type-53"></a><span data-ttu-id="bdf42-103">Tipo de acción personalizada 53</span><span class="sxs-lookup"><span data-stu-id="bdf42-103">Custom Action Type 53</span></span>

<span data-ttu-id="bdf42-104">Esta acción personalizada se escribe en JScript, como ECMA 262.</span><span class="sxs-lookup"><span data-stu-id="bdf42-104">This custom action is written in JScript, such as ECMA 262.</span></span> <span data-ttu-id="bdf42-105">Windows Installer no admite JScript 1,0.</span><span class="sxs-lookup"><span data-stu-id="bdf42-105">Windows Installer does not support JScript 1.0.</span></span> <span data-ttu-id="bdf42-106">Para obtener más información, vea [scripts](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="bdf42-106">For more information, see [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="bdf42-107">Source</span><span class="sxs-lookup"><span data-stu-id="bdf42-107">Source</span></span>

<span data-ttu-id="bdf42-108">El campo de origen de la [tabla CustomAction](customaction-table.md) contiene un nombre de propiedad o una clave a la [tabla de propiedades](property-table.md) de una propiedad que contiene el texto del script.</span><span class="sxs-lookup"><span data-stu-id="bdf42-108">The Source field of the [CustomAction table](customaction-table.md) contains a property name or a key to the [Property table](property-table.md) for a property containing the script text.</span></span>

## <a name="type-value"></a><span data-ttu-id="bdf42-109">Valor de tipo</span><span class="sxs-lookup"><span data-stu-id="bdf42-109">Type Value</span></span>

<span data-ttu-id="bdf42-110">Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico de una acción personalizada de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="bdf42-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="bdf42-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="bdf42-111">Constants</span></span>                                                            | <span data-ttu-id="bdf42-112">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="bdf42-112">Hexadecimal</span></span> | <span data-ttu-id="bdf42-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="bdf42-113">Decimal</span></span> |
|----------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="bdf42-114">**msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeProperty**</span><span class="sxs-lookup"><span data-stu-id="bdf42-114">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeProperty**</span></span> | <span data-ttu-id="bdf42-115">0x035</span><span class="sxs-lookup"><span data-stu-id="bdf42-115">0x035</span></span>       | <span data-ttu-id="bdf42-116">53</span><span class="sxs-lookup"><span data-stu-id="bdf42-116">53</span></span>      |



 

<span data-ttu-id="bdf42-117">Windows Installer puede usar las acciones personalizadas de 64 bits en sistemas operativos de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="bdf42-117">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="bdf42-118">Una acción personalizada de 64 bits basada en scripts debe incluir el bit **msidbCustomActionType64BitScript** en su tipo numérico.</span><span class="sxs-lookup"><span data-stu-id="bdf42-118">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="bdf42-119">Para obtener información, consulte [acciones personalizadas de 64 bits](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="bdf42-119">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="bdf42-120">Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico de una acción personalizada de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="bdf42-120">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="bdf42-121">Constantes</span><span class="sxs-lookup"><span data-stu-id="bdf42-121">Constants</span></span>                                                                                                   | <span data-ttu-id="bdf42-122">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="bdf42-122">Hexadecimal</span></span> | <span data-ttu-id="bdf42-123">Decimal</span><span class="sxs-lookup"><span data-stu-id="bdf42-123">Decimal</span></span> |
|-------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="bdf42-124">**msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeProperty**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="bdf42-124">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeProperty** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="bdf42-125">0x0001035</span><span class="sxs-lookup"><span data-stu-id="bdf42-125">0x0001035</span></span>   | <span data-ttu-id="bdf42-126">4149</span><span class="sxs-lookup"><span data-stu-id="bdf42-126">4149</span></span>    |



 

## <a name="target"></a><span data-ttu-id="bdf42-127">Destino</span><span class="sxs-lookup"><span data-stu-id="bdf42-127">Target</span></span>

<span data-ttu-id="bdf42-128">El campo de destino de la [tabla CustomAction](customaction-table.md) contiene una función de script opcional.</span><span class="sxs-lookup"><span data-stu-id="bdf42-128">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="bdf42-129">El procesamiento primero envía el script para el análisis y, a continuación, llama a la función de script opcional.</span><span class="sxs-lookup"><span data-stu-id="bdf42-129">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="bdf42-130">Opciones de procesamiento de valores devueltos</span><span class="sxs-lookup"><span data-stu-id="bdf42-130">Return Processing Options</span></span>

<span data-ttu-id="bdf42-131">Incluya bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de procesamiento de valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="bdf42-131">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="bdf42-132">Para obtener una descripción de las opciones y los valores, vea [Opciones de procesamiento de devolución de acción personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="bdf42-132">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="bdf42-133">Opciones de programación de ejecución</span><span class="sxs-lookup"><span data-stu-id="bdf42-133">Execution Scheduling Options</span></span>

<span data-ttu-id="bdf42-134">Incluya los bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de programación de la ejecución.</span><span class="sxs-lookup"><span data-stu-id="bdf42-134">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="bdf42-135">Estas opciones controlan la ejecución múltiple de acciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="bdf42-135">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="bdf42-136">Para obtener una descripción de las opciones, vea opciones de programación de la [ejecución de acciones personalizadas](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="bdf42-136">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="bdf42-137">Opciones de ejecución de In-Script</span><span class="sxs-lookup"><span data-stu-id="bdf42-137">In-Script Execution Options</span></span>

<span data-ttu-id="bdf42-138">Incluya bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar una opción de ejecución en el script.</span><span class="sxs-lookup"><span data-stu-id="bdf42-138">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="bdf42-139">Estas opciones copian el código de acción en el script de ejecución, reversión o confirmación.</span><span class="sxs-lookup"><span data-stu-id="bdf42-139">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="bdf42-140">Para obtener una descripción de las opciones, vea [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="bdf42-140">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="bdf42-141">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="bdf42-141">Return Values</span></span>

<span data-ttu-id="bdf42-142">Las funciones opcionales escritas en el script deben devolver uno de los valores descritos en [valores devueltos de las acciones personalizadas de JScript y VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="bdf42-142">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bdf42-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bdf42-143">Remarks</span></span>

<span data-ttu-id="bdf42-144">Una acción personalizada que se escribe en JScript requiere el objeto de [**sesión**](session-object.md) de instalación.</span><span class="sxs-lookup"><span data-stu-id="bdf42-144">A custom action that is written in JScript requires the installation [**Session**](session-object.md) object.</span></span> <span data-ttu-id="bdf42-145">Dado que es posible que el objeto de **sesión** no exista durante la reversión de la instalación, una acción personalizada diferida escrita en el script usa uno de los métodos descritos en [obtener información de contexto para las acciones personalizadas de ejecución aplazada](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="bdf42-145">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script uses one of the methods described in [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bdf42-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bdf42-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdf42-147">\_Acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="bdf42-147">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



