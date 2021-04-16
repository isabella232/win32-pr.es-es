---
description: Los desarrolladores de paquetes de Windows Installer pueden optar por usar un tipo de acción personalizada 54 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: ab348a8e-f5df-4e03-a1b7-1ab1a7fbcb3b
title: Tipo de acción personalizada 54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 623e8d4ffe955c73ef95a5948aa6e043702a35f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497872"
---
# <a name="custom-action-type-54"></a><span data-ttu-id="78314-103">Tipo de acción personalizada 54</span><span class="sxs-lookup"><span data-stu-id="78314-103">Custom Action Type 54</span></span>

<span data-ttu-id="78314-104">Esta acción personalizada se escribe en VBScript.</span><span class="sxs-lookup"><span data-stu-id="78314-104">This custom action is written in VBScript.</span></span> <span data-ttu-id="78314-105">Vea también [scripts](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="78314-105">See also [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="78314-106">Source</span><span class="sxs-lookup"><span data-stu-id="78314-106">Source</span></span>

<span data-ttu-id="78314-107">El campo de origen de la [tabla CustomAction](customaction-table.md) contiene un nombre de propiedad o una clave a la [tabla de propiedades](property-table.md) de una propiedad que contiene el texto del script.</span><span class="sxs-lookup"><span data-stu-id="78314-107">The Source field of the [CustomAction table](customaction-table.md) contains a property name or a key to the [Property table](property-table.md) for a property containing the script text.</span></span>

## <a name="type-value"></a><span data-ttu-id="78314-108">Valor de tipo</span><span class="sxs-lookup"><span data-stu-id="78314-108">Type Value</span></span>

<span data-ttu-id="78314-109">Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico de una acción personalizada de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="78314-109">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="78314-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="78314-110">Constants</span></span>                                                             | <span data-ttu-id="78314-111">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="78314-111">Hexadecimal</span></span> | <span data-ttu-id="78314-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="78314-112">Decimal</span></span> |
|-----------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="78314-113">**msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeProperty**</span><span class="sxs-lookup"><span data-stu-id="78314-113">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeProperty**</span></span> | <span data-ttu-id="78314-114">0x036</span><span class="sxs-lookup"><span data-stu-id="78314-114">0x036</span></span>       | <span data-ttu-id="78314-115">54</span><span class="sxs-lookup"><span data-stu-id="78314-115">54</span></span>      |



 

<span data-ttu-id="78314-116">Windows Installer puede usar las acciones personalizadas de 64 bits en sistemas operativos de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="78314-116">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="78314-117">Una acción personalizada de 64 bits basada en scripts debe incluir el bit **msidbCustomActionType64BitScript** en su tipo numérico.</span><span class="sxs-lookup"><span data-stu-id="78314-117">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="78314-118">Para obtener información, consulte [acciones personalizadas de 64 bits](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="78314-118">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="78314-119">Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico de una acción personalizada de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="78314-119">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="78314-120">Constantes</span><span class="sxs-lookup"><span data-stu-id="78314-120">Constants</span></span>                                                                                                    | <span data-ttu-id="78314-121">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="78314-121">Hexadecimal</span></span> | <span data-ttu-id="78314-122">Decimal</span><span class="sxs-lookup"><span data-stu-id="78314-122">Decimal</span></span> |
|--------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="78314-123">**msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeProperty**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="78314-123">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeProperty** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="78314-124">0x0001036</span><span class="sxs-lookup"><span data-stu-id="78314-124">0x0001036</span></span>   | <span data-ttu-id="78314-125">4150</span><span class="sxs-lookup"><span data-stu-id="78314-125">4150</span></span>    |



 

## <a name="target"></a><span data-ttu-id="78314-126">Destino</span><span class="sxs-lookup"><span data-stu-id="78314-126">Target</span></span>

<span data-ttu-id="78314-127">El campo de destino de la [tabla CustomAction](customaction-table.md) contiene una función de script opcional.</span><span class="sxs-lookup"><span data-stu-id="78314-127">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="78314-128">El procesamiento primero envía el script para el análisis y, a continuación, llama a la función de script opcional.</span><span class="sxs-lookup"><span data-stu-id="78314-128">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="78314-129">Opciones de procesamiento de valores devueltos</span><span class="sxs-lookup"><span data-stu-id="78314-129">Return Processing Options</span></span>

<span data-ttu-id="78314-130">Incluya bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de procesamiento de valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="78314-130">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="78314-131">Para obtener una descripción de las opciones y los valores, vea [Opciones de procesamiento de devolución de acción personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="78314-131">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="78314-132">Opciones de programación de ejecución</span><span class="sxs-lookup"><span data-stu-id="78314-132">Execution Scheduling Options</span></span>

<span data-ttu-id="78314-133">Incluya los bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de programación de la ejecución.</span><span class="sxs-lookup"><span data-stu-id="78314-133">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="78314-134">Estas opciones controlan la ejecución múltiple de acciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="78314-134">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="78314-135">Para obtener una descripción de las opciones, vea opciones de programación de la [ejecución de acciones personalizadas](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="78314-135">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="78314-136">Opciones de ejecución de In-Script</span><span class="sxs-lookup"><span data-stu-id="78314-136">In-Script Execution Options</span></span>

<span data-ttu-id="78314-137">Incluya bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar una opción de ejecución en el script.</span><span class="sxs-lookup"><span data-stu-id="78314-137">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="78314-138">Estas opciones copian el código de acción en el script de ejecución, reversión o confirmación.</span><span class="sxs-lookup"><span data-stu-id="78314-138">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="78314-139">Para obtener una descripción de las opciones, vea [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="78314-139">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="78314-140">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="78314-140">Return Values</span></span>

<span data-ttu-id="78314-141">Las funciones opcionales escritas en el script deben devolver uno de los valores descritos en [valores devueltos de las acciones personalizadas de JScript y VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="78314-141">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="78314-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="78314-142">Remarks</span></span>

<span data-ttu-id="78314-143">Una acción personalizada escrita en JScript o VBScript requiere el objeto de [**sesión**](session-object.md) de instalación.</span><span class="sxs-lookup"><span data-stu-id="78314-143">A custom action that is written in JScript or VBScript requires the install [**Session**](session-object.md) object.</span></span> <span data-ttu-id="78314-144">El instalador adjunta el **objeto de sesión** al script con la *sesión* de nombre.</span><span class="sxs-lookup"><span data-stu-id="78314-144">The installer attaches the **Session Object** to the script with the name *Session*.</span></span> <span data-ttu-id="78314-145">Dado que es posible que el objeto de **sesión** no exista durante una reversión de la instalación, una acción personalizada diferida escrita en el script debe usar uno de los métodos o propiedades del objeto de **sesión** que se describe en la sección [obtener información de contexto para las acciones personalizadas de ejecución aplazada](obtaining-context-information-for-deferred-execution-custom-actions.md) para recuperar su contexto.</span><span class="sxs-lookup"><span data-stu-id="78314-145">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="78314-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="78314-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78314-147">\_Acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="78314-147">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



