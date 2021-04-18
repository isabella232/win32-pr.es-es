---
description: Los desarrolladores de paquetes de Windows Installer pueden optar por usar una acción personalizada tipo 22 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: 6838f59b-e1bc-42c6-a7fe-3d32791adfac
title: Tipo de acción personalizada 22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a00b4772b1d2532c0291223cc5c4b6a63ead9324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361725"
---
# <a name="custom-action-type-22"></a><span data-ttu-id="69c60-103">Tipo de acción personalizada 22</span><span class="sxs-lookup"><span data-stu-id="69c60-103">Custom Action Type 22</span></span>

<span data-ttu-id="69c60-104">Esta acción personalizada se escribe en VBScript.</span><span class="sxs-lookup"><span data-stu-id="69c60-104">This custom action is written in VBScript.</span></span> <span data-ttu-id="69c60-105">Vea también [scripts](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="69c60-105">See also [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="69c60-106">Source</span><span class="sxs-lookup"><span data-stu-id="69c60-106">Source</span></span>

<span data-ttu-id="69c60-107">El script se instala con la aplicación durante la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="69c60-107">The script is installed with the application during the current session.</span></span> <span data-ttu-id="69c60-108">El campo de origen de la [tabla CustomAction](customaction-table.md) contiene una clave para la [tabla de archivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="69c60-108">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [File table](file-table.md).</span></span> <span data-ttu-id="69c60-109">La ubicación del código de acción personalizada viene determinada por la resolución de la ruta de acceso de destino para este archivo; por lo tanto, se debe llamar a esta acción personalizada después de haber instalado el archivo y antes de quitarlo.</span><span class="sxs-lookup"><span data-stu-id="69c60-109">The location of the custom action code is determined by the resolution of the target path for this file; therefore this custom action must be called after the file has been installed and before it is removed.</span></span>

## <a name="type-value"></a><span data-ttu-id="69c60-110">Valor de tipo</span><span class="sxs-lookup"><span data-stu-id="69c60-110">Type Value</span></span>

<span data-ttu-id="69c60-111">Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico de una acción personalizada de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="69c60-111">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="69c60-112">Constantes</span><span class="sxs-lookup"><span data-stu-id="69c60-112">Constants</span></span>                                                               | <span data-ttu-id="69c60-113">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="69c60-113">Hexadecimal</span></span> | <span data-ttu-id="69c60-114">Decimal</span><span class="sxs-lookup"><span data-stu-id="69c60-114">Decimal</span></span> |
|-------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="69c60-115">**msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeSourceFile**</span><span class="sxs-lookup"><span data-stu-id="69c60-115">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="69c60-116">0x016</span><span class="sxs-lookup"><span data-stu-id="69c60-116">0x016</span></span>       | <span data-ttu-id="69c60-117">22</span><span class="sxs-lookup"><span data-stu-id="69c60-117">22</span></span>      |



 

<span data-ttu-id="69c60-118">Windows Installer puede usar las acciones personalizadas de 64 bits en sistemas operativos de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="69c60-118">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="69c60-119">Una acción personalizada de 64 bits basada en scripts debe incluir el bit **msidbCustomActionType64BitScript** en su tipo numérico.</span><span class="sxs-lookup"><span data-stu-id="69c60-119">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="69c60-120">Para obtener información, consulte [acciones personalizadas de 64 bits](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="69c60-120">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="69c60-121">Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico de una acción personalizada de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="69c60-121">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="69c60-122">Constantes</span><span class="sxs-lookup"><span data-stu-id="69c60-122">Constants</span></span>                                                                                                      | <span data-ttu-id="69c60-123">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="69c60-123">Hexadecimal</span></span> | <span data-ttu-id="69c60-124">Decimal</span><span class="sxs-lookup"><span data-stu-id="69c60-124">Decimal</span></span> |
|----------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="69c60-125">**msidbCustomActionTypeVBScript**  +  **msidbCustomActionTypeSourceFile**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="69c60-125">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeSourceFile** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="69c60-126">0x0001016</span><span class="sxs-lookup"><span data-stu-id="69c60-126">0x0001016</span></span>   | <span data-ttu-id="69c60-127">4118</span><span class="sxs-lookup"><span data-stu-id="69c60-127">4118</span></span>    |



 

## <a name="target"></a><span data-ttu-id="69c60-128">Destino</span><span class="sxs-lookup"><span data-stu-id="69c60-128">Target</span></span>

<span data-ttu-id="69c60-129">El campo de destino de la [tabla CustomAction](customaction-table.md) contiene una función de script opcional.</span><span class="sxs-lookup"><span data-stu-id="69c60-129">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="69c60-130">El procesamiento primero envía el script para el análisis y, a continuación, llama a la función de script opcional.</span><span class="sxs-lookup"><span data-stu-id="69c60-130">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="69c60-131">Opciones de procesamiento de valores devueltos</span><span class="sxs-lookup"><span data-stu-id="69c60-131">Return Processing Options</span></span>

<span data-ttu-id="69c60-132">Incluya bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de procesamiento de valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="69c60-132">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="69c60-133">Para obtener una descripción de las opciones y los valores, vea [Opciones de procesamiento de devolución de acción personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="69c60-133">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="69c60-134">Opciones de programación de ejecución</span><span class="sxs-lookup"><span data-stu-id="69c60-134">Execution Scheduling Options</span></span>

<span data-ttu-id="69c60-135">Incluya los bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de programación de la ejecución.</span><span class="sxs-lookup"><span data-stu-id="69c60-135">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="69c60-136">Estas opciones controlan la ejecución múltiple de acciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="69c60-136">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="69c60-137">Para obtener una descripción de las opciones, vea opciones de programación de la [ejecución de acciones personalizadas](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="69c60-137">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="69c60-138">Opciones de ejecución de In-Script</span><span class="sxs-lookup"><span data-stu-id="69c60-138">In-Script Execution Options</span></span>

<span data-ttu-id="69c60-139">Incluya bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar una opción de ejecución en el script.</span><span class="sxs-lookup"><span data-stu-id="69c60-139">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="69c60-140">Estas opciones copian el código de acción en el script de ejecución, reversión o confirmación.</span><span class="sxs-lookup"><span data-stu-id="69c60-140">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="69c60-141">Para obtener una descripción de las opciones, vea [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="69c60-141">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="69c60-142">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="69c60-142">Return Values</span></span>

<span data-ttu-id="69c60-143">Las funciones opcionales escritas en el script deben devolver uno de los valores descritos en [valores devueltos de las acciones personalizadas de JScript y VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="69c60-143">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="69c60-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69c60-144">Remarks</span></span>

<span data-ttu-id="69c60-145">Una acción personalizada escrita en JScript o VBScript requiere el [**objeto de sesión**](session-object.md)de instalación.</span><span class="sxs-lookup"><span data-stu-id="69c60-145">A custom action that is written in JScript or VBScript requires the install [**Session Object**](session-object.md).</span></span> <span data-ttu-id="69c60-146">Este es el objeto de **sesión** de tipo y el instalador lo adjunta al script con el nombre "session".</span><span class="sxs-lookup"><span data-stu-id="69c60-146">This is of the type **Session Object** and the installer attaches it to the script with the name "Session".</span></span> <span data-ttu-id="69c60-147">Dado que es posible que el objeto de **sesión** no exista durante una reversión de la instalación, una acción personalizada diferida escrita en el script debe usar uno de los métodos o propiedades del objeto de **sesión** que se describe en la sección [obtener información de contexto para las acciones personalizadas de ejecución aplazada](obtaining-context-information-for-deferred-execution-custom-actions.md) para recuperar su contexto.</span><span class="sxs-lookup"><span data-stu-id="69c60-147">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

<span data-ttu-id="69c60-148">Las acciones personalizadas que hacen referencia a un archivo instalado como origen, como el tipo de acción personalizada 22 (VBcript), deben cumplir las siguientes restricciones de secuenciación:</span><span class="sxs-lookup"><span data-stu-id="69c60-148">Custom actions that reference an installed file as their source, such as Custom Action Type 22 (VBcript), must adhere to the following sequencing restrictions:</span></span>

-   <span data-ttu-id="69c60-149">La acción personalizada se debe secuenciar después de la [acción CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="69c60-149">The custom action must be sequenced after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="69c60-150">Esto es para que la acción personalizada pueda resolver la ruta de acceso necesaria para buscar el archivo de código fuente que contiene VBScript.</span><span class="sxs-lookup"><span data-stu-id="69c60-150">This is so that the custom action can resolve the path needed to locate the source file containing the VBScript.</span></span>
-   <span data-ttu-id="69c60-151">Si el archivo de código fuente no está ya instalado en el equipo, las acciones personalizadas diferidas (en script) de este tipo deben secuenciarse después de la [acción InstallFiles](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="69c60-151">If the source file is not already installed on the computer, deferred (in-script) custom actions of this type must be sequenced after the [InstallFiles action](installfiles-action.md).</span></span>
-   <span data-ttu-id="69c60-152">Si el archivo de código fuente no está ya instalado en el equipo, las acciones personalizadas no diferidas de este tipo se deben secuenciar después de la [acción InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="69c60-152">If the source file is not already installed on the computer, non-deferred custom actions of this type must be sequenced after the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="69c60-153">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="69c60-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69c60-154">\_Acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="69c60-154">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



