---
description: Los desarrolladores de paquetes de Windows Installer pueden optar por usar una acción personalizada tipo 21 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: 0b28ad22-4e3a-49f2-8eed-2341a91eb67c
title: Tipo de acción personalizada 21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5bb7482c2f7c7b6cbd85af7a6f01cc83edbb89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361398"
---
# <a name="custom-action-type-21"></a><span data-ttu-id="79fd4-103">Tipo de acción personalizada 21</span><span class="sxs-lookup"><span data-stu-id="79fd4-103">Custom Action Type 21</span></span>

<span data-ttu-id="79fd4-104">Esta acción personalizada se escribe en JScript, como ECMA 262.</span><span class="sxs-lookup"><span data-stu-id="79fd4-104">This custom action is written in JScript, such as ECMA 262.</span></span> <span data-ttu-id="79fd4-105">Windows Installer no admite JScript 1,0.</span><span class="sxs-lookup"><span data-stu-id="79fd4-105">Windows Installer does not support JScript 1.0.</span></span> <span data-ttu-id="79fd4-106">Para obtener más información, vea [scripts](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="79fd4-106">For more information, see [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="79fd4-107">Source</span><span class="sxs-lookup"><span data-stu-id="79fd4-107">Source</span></span>

<span data-ttu-id="79fd4-108">El script se instala con la aplicación durante la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="79fd4-108">The script is installed with the application during the current session.</span></span> <span data-ttu-id="79fd4-109">El campo de origen de la [tabla CustomAction](customaction-table.md) contiene una clave para la [tabla de archivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="79fd4-109">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [File table](file-table.md).</span></span> <span data-ttu-id="79fd4-110">La ubicación del código de acción personalizada viene determinada por la resolución de la ruta de acceso de destino para este archivo; por lo tanto, se debe llamar a esta acción personalizada después de haber instalado el archivo y antes de quitarlo.</span><span class="sxs-lookup"><span data-stu-id="79fd4-110">The location of the custom action code is determined by the resolution of the target path for this file; therefore this custom action must be called after the file has been installed and before it is removed.</span></span>

## <a name="type-value"></a><span data-ttu-id="79fd4-111">Valor de tipo</span><span class="sxs-lookup"><span data-stu-id="79fd4-111">Type Value</span></span>

<span data-ttu-id="79fd4-112">Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico de una acción personalizada de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="79fd4-112">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="79fd4-113">Constantes</span><span class="sxs-lookup"><span data-stu-id="79fd4-113">Constants</span></span>                                                              | <span data-ttu-id="79fd4-114">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="79fd4-114">Hexadecimal</span></span> | <span data-ttu-id="79fd4-115">Decimal</span><span class="sxs-lookup"><span data-stu-id="79fd4-115">Decimal</span></span> |
|------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="79fd4-116">**msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeSourceFile**</span><span class="sxs-lookup"><span data-stu-id="79fd4-116">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="79fd4-117">0x015</span><span class="sxs-lookup"><span data-stu-id="79fd4-117">0x015</span></span>       | <span data-ttu-id="79fd4-118">21</span><span class="sxs-lookup"><span data-stu-id="79fd4-118">21</span></span>      |



 

<span data-ttu-id="79fd4-119">Windows Installer puede usar [las acciones personalizadas de 64 bits](64-bit-custom-actions.md) en sistemas operativos de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="79fd4-119">Windows Installer may use [64-bit Custom Actions](64-bit-custom-actions.md) on 64-bit operating systems.</span></span> <span data-ttu-id="79fd4-120">Una acción personalizada de 64 bits basada en scripts debe incluir el bit **msidbCustomActionType64BitScript** en su tipo numérico.</span><span class="sxs-lookup"><span data-stu-id="79fd4-120">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="79fd4-121">Para obtener información, consulte acciones personalizadas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="79fd4-121">For information see 64-bit Custom Actions.</span></span> <span data-ttu-id="79fd4-122">Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico de una acción personalizada de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="79fd4-122">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="79fd4-123">Constantes</span><span class="sxs-lookup"><span data-stu-id="79fd4-123">Constants</span></span>                                                                                                     | <span data-ttu-id="79fd4-124">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="79fd4-124">Hexadecimal</span></span> | <span data-ttu-id="79fd4-125">Decimal</span><span class="sxs-lookup"><span data-stu-id="79fd4-125">Decimal</span></span> |
|---------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="79fd4-126">**msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeSourceFile**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="79fd4-126">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeSourceFile** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="79fd4-127">0x0001015</span><span class="sxs-lookup"><span data-stu-id="79fd4-127">0x0001015</span></span>   | <span data-ttu-id="79fd4-128">4117</span><span class="sxs-lookup"><span data-stu-id="79fd4-128">4117</span></span>    |



 

## <a name="target"></a><span data-ttu-id="79fd4-129">Destino</span><span class="sxs-lookup"><span data-stu-id="79fd4-129">Target</span></span>

<span data-ttu-id="79fd4-130">El campo de destino de la [tabla CustomAction](customaction-table.md) contiene una función de script opcional.</span><span class="sxs-lookup"><span data-stu-id="79fd4-130">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="79fd4-131">El procesamiento primero envía el script para el análisis y, a continuación, llama a la función de script opcional.</span><span class="sxs-lookup"><span data-stu-id="79fd4-131">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="79fd4-132">Opciones de procesamiento de valores devueltos</span><span class="sxs-lookup"><span data-stu-id="79fd4-132">Return Processing Options</span></span>

<span data-ttu-id="79fd4-133">Incluya bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de procesamiento de valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="79fd4-133">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="79fd4-134">Para obtener una descripción de las opciones y los valores, vea [Opciones de procesamiento de devolución de acción personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="79fd4-134">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="79fd4-135">Opciones de programación de ejecución</span><span class="sxs-lookup"><span data-stu-id="79fd4-135">Execution Scheduling Options</span></span>

<span data-ttu-id="79fd4-136">Incluya los bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de programación de la ejecución.</span><span class="sxs-lookup"><span data-stu-id="79fd4-136">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="79fd4-137">Estas opciones controlan la ejecución múltiple de acciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="79fd4-137">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="79fd4-138">Para obtener una descripción de las opciones, vea opciones de programación de la [ejecución de acciones personalizadas](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="79fd4-138">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="79fd4-139">Opciones de ejecución de In-Script</span><span class="sxs-lookup"><span data-stu-id="79fd4-139">In-Script Execution Options</span></span>

<span data-ttu-id="79fd4-140">Incluya bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar una opción de ejecución en el script.</span><span class="sxs-lookup"><span data-stu-id="79fd4-140">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="79fd4-141">Estas opciones copian el código de acción en el script de ejecución, reversión o confirmación.</span><span class="sxs-lookup"><span data-stu-id="79fd4-141">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="79fd4-142">Para obtener una descripción de las opciones, vea [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="79fd4-142">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="79fd4-143">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="79fd4-143">Return Values</span></span>

<span data-ttu-id="79fd4-144">Las funciones opcionales escritas en el script deben devolver uno de los valores descritos en [valores devueltos de las acciones personalizadas de JScript y VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="79fd4-144">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="79fd4-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79fd4-145">Remarks</span></span>

<span data-ttu-id="79fd4-146">Una acción personalizada escrita en JScript o VBScript requiere el objeto de [**sesión**](session-object.md) de instalación.</span><span class="sxs-lookup"><span data-stu-id="79fd4-146">A custom action that is written in JScript or VBScript requires the installation [**Session**](session-object.md) object.</span></span> <span data-ttu-id="79fd4-147">El instalador adjunta el **objeto de sesión** al script con el nombre "session".</span><span class="sxs-lookup"><span data-stu-id="79fd4-147">The installer attaches the **Session Object** to the script with the name "Session".</span></span> <span data-ttu-id="79fd4-148">Dado que es posible que el objeto de **sesión** no exista durante una reversión de la instalación, una acción personalizada diferida escrita en el script debe usar uno de los métodos o propiedades del objeto de **sesión** que se describe en la sección [obtener información de contexto para las acciones personalizadas de ejecución aplazada](obtaining-context-information-for-deferred-execution-custom-actions.md) para recuperar su contexto.</span><span class="sxs-lookup"><span data-stu-id="79fd4-148">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

<span data-ttu-id="79fd4-149">Las acciones personalizadas que hacen referencia a un archivo instalado como origen, como el tipo de acción personalizada 21 (JScript), deben cumplir las siguientes restricciones de secuenciación:</span><span class="sxs-lookup"><span data-stu-id="79fd4-149">Custom actions that reference an installed file as their source, such as Custom Action Type 21 (JScript), must adhere to the following sequencing restrictions:</span></span>

-   <span data-ttu-id="79fd4-150">La acción personalizada se debe secuenciar después de la [acción CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="79fd4-150">The custom action must be sequenced after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="79fd4-151">Esto es para que la acción personalizada pueda resolver la ruta de acceso necesaria para buscar el archivo de código fuente que contiene JScript.</span><span class="sxs-lookup"><span data-stu-id="79fd4-151">This is so that the custom action can resolve the path needed to locate the source file containing the JScript.</span></span>
-   <span data-ttu-id="79fd4-152">Si el archivo de código fuente no está ya instalado en el equipo, las acciones personalizadas diferidas (en script) de este tipo deben secuenciarse después de la [acción InstallFiles](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="79fd4-152">If the source file is not already installed on the computer, deferred (in-script) custom actions of this type must be sequenced after the [InstallFiles action](installfiles-action.md).</span></span>
-   <span data-ttu-id="79fd4-153">Si el archivo de código fuente no está ya instalado en el equipo, las acciones personalizadas no diferidas de este tipo se deben secuenciar después de la [acción InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="79fd4-153">If the source file is not already installed on the computer, non-deferred custom actions of this type must be sequenced after the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="79fd4-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="79fd4-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79fd4-155">\_Acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="79fd4-155">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



