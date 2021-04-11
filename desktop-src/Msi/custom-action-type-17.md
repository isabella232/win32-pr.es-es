---
description: Los desarrolladores de paquetes de Windows Installer pueden optar por usar una acción personalizada tipo 17 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: 99efd6d5-e0a3-4e66-ae55-252d19090d31
title: Tipo de acción personalizada 17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b53d0046cb7515d701eb1bae3d10de0570ee5843
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361399"
---
# <a name="custom-action-type-17"></a><span data-ttu-id="44f94-103">Tipo de acción personalizada 17</span><span class="sxs-lookup"><span data-stu-id="44f94-103">Custom Action Type 17</span></span>

<span data-ttu-id="44f94-104">Esta acción personalizada llama a una biblioteca de vínculos dinámicos (DLL) escrita en C o C++.</span><span class="sxs-lookup"><span data-stu-id="44f94-104">This custom action calls a dynamic link library (DLL) written in C or C++.</span></span>

## <a name="source"></a><span data-ttu-id="44f94-105">Source</span><span class="sxs-lookup"><span data-stu-id="44f94-105">Source</span></span>

<span data-ttu-id="44f94-106">El archivo DLL se instala con la aplicación durante la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="44f94-106">The DLL is installed with the application during the current session.</span></span> <span data-ttu-id="44f94-107">El campo de origen de la [tabla CustomAction](customaction-table.md) contiene una clave para la [tabla de archivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="44f94-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [File table](file-table.md).</span></span> <span data-ttu-id="44f94-108">La ubicación del código de acción personalizada viene determinada por la resolución de la ruta de acceso de destino para este archivo; por lo tanto, se debe llamar a esta acción personalizada después de instalar el archivo y antes de quitarlo.</span><span class="sxs-lookup"><span data-stu-id="44f94-108">The location of the custom action code is determined by the resolution of the target path for this file; therefore this custom action must be called after that file has been installed and before it is removed.</span></span>

## <a name="type-value"></a><span data-ttu-id="44f94-109">Valor de tipo</span><span class="sxs-lookup"><span data-stu-id="44f94-109">Type Value</span></span>

<span data-ttu-id="44f94-110">Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico.</span><span class="sxs-lookup"><span data-stu-id="44f94-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="44f94-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="44f94-111">Constants</span></span>                                                          | <span data-ttu-id="44f94-112">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="44f94-112">Hexadecimal</span></span> | <span data-ttu-id="44f94-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="44f94-113">Decimal</span></span> |
|--------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="44f94-114">**msidbCustomActionTypeDll**  +  **msidbCustomActionTypeSourceFile**</span><span class="sxs-lookup"><span data-stu-id="44f94-114">**msidbCustomActionTypeDll** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="44f94-115">0x011</span><span class="sxs-lookup"><span data-stu-id="44f94-115">0x011</span></span>       | <span data-ttu-id="44f94-116">17</span><span class="sxs-lookup"><span data-stu-id="44f94-116">17</span></span>      |



 

## <a name="target"></a><span data-ttu-id="44f94-117">Destino</span><span class="sxs-lookup"><span data-stu-id="44f94-117">Target</span></span>

<span data-ttu-id="44f94-118">Se llama a la DLL a través del punto de entrada denominado en el campo de destino de la [tabla CustomAction](customaction-table.md), pasando un solo argumento que es el identificador de la sesión de instalación actual.</span><span class="sxs-lookup"><span data-stu-id="44f94-118">The DLL is called through the entry point named in the Target field of the [CustomAction table](customaction-table.md), passing a single argument that is the handle to the current install session.</span></span> <span data-ttu-id="44f94-119">El nombre del punto de entrada especificado en la tabla debe coincidir con el exportado desde el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="44f94-119">The entry point name specified in the table must match that exported from the DLL.</span></span> <span data-ttu-id="44f94-120">Tenga en cuenta que si la función de entrada no se especifica mediante un. Archivo DEF o una especificación/EXPORT: linker, el nombre puede tener un carácter de subrayado inicial y un @4 sufijo "".</span><span class="sxs-lookup"><span data-stu-id="44f94-120">Note that if the entry function is not specified by a .DEF file or by a /EXPORT: linker specification, the name may have a leading underscore and a "@4" suffix.</span></span> <span data-ttu-id="44f94-121">La función llamada debe especificar la \_ \_ Convención de llamada Stdcall.</span><span class="sxs-lookup"><span data-stu-id="44f94-121">The called function must specify the \_\_stdcall calling convention.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="44f94-122">Opciones de procesamiento de valores devueltos</span><span class="sxs-lookup"><span data-stu-id="44f94-122">Return Processing Options</span></span>

<span data-ttu-id="44f94-123">Incluya bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de procesamiento de valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="44f94-123">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="44f94-124">Para obtener una descripción de las opciones y los valores, vea [Opciones de procesamiento de devolución de acción personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="44f94-124">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="44f94-125">Opciones de programación de ejecución</span><span class="sxs-lookup"><span data-stu-id="44f94-125">Execution Scheduling Options</span></span>

<span data-ttu-id="44f94-126">Incluya los bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de programación de la ejecución.</span><span class="sxs-lookup"><span data-stu-id="44f94-126">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="44f94-127">Estas opciones controlan la ejecución múltiple de acciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="44f94-127">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="44f94-128">Para obtener una descripción de las opciones, vea opciones de programación de la [ejecución de acciones personalizadas](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="44f94-128">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="44f94-129">Opciones de ejecución de In-Script</span><span class="sxs-lookup"><span data-stu-id="44f94-129">In-Script Execution Options</span></span>

<span data-ttu-id="44f94-130">Incluya bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar una opción de ejecución en el script.</span><span class="sxs-lookup"><span data-stu-id="44f94-130">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="44f94-131">Estas opciones copian el código de acción en el script de ejecución, reversión o confirmación.</span><span class="sxs-lookup"><span data-stu-id="44f94-131">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="44f94-132">Para obtener una descripción de las opciones, vea [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="44f94-132">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="44f94-133">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="44f94-133">Return Values</span></span>

<span data-ttu-id="44f94-134">Vea [valores devueltos de la acción personalizada](custom-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="44f94-134">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="44f94-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="44f94-135">Remarks</span></span>

<span data-ttu-id="44f94-136">Una acción personalizada que llama a una biblioteca de vínculos dinámicos (DLL) requiere un identificador para la sesión de instalación.</span><span class="sxs-lookup"><span data-stu-id="44f94-136">A custom action that calls a dynamic-link library (DLL) requires a handle to the installation session.</span></span> <span data-ttu-id="44f94-137">Si esta es también una acción personalizada de ejecución aplazada, es posible que la sesión ya no exista durante la ejecución del script de instalación.</span><span class="sxs-lookup"><span data-stu-id="44f94-137">If this is also a deferred execution custom action, the session may no longer exist during execution of the installation script.</span></span> <span data-ttu-id="44f94-138">Para obtener información sobre cómo una acción personalizada de este tipo puede obtener información de contexto, vea [obtener información de contexto para las acciones personalizadas de ejecución aplazada](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="44f94-138">For information on how a custom action of this type can obtain context information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

<span data-ttu-id="44f94-139">Las acciones personalizadas se ejecutan en un subproceso independiente y pueden tener acceso limitado al sistema.</span><span class="sxs-lookup"><span data-stu-id="44f94-139">Custom actions execute in a separate thread, and may have limited access to the system.</span></span> <span data-ttu-id="44f94-140">Las acciones personalizadas que se ejecutan de forma asincrónica bloquean el subproceso principal a la finalización de la secuencia actual o de la sesión de instalación hasta que devuelvan.</span><span class="sxs-lookup"><span data-stu-id="44f94-140">Custom actions that run asynchronously block the main thread at the termination of either the current sequence or the install session until they return.</span></span>

<span data-ttu-id="44f94-141">Las acciones personalizadas que hacen referencia a un archivo instalado como origen, como el tipo de acción personalizada 17 (DLL), deben cumplir las siguientes restricciones de secuenciación:</span><span class="sxs-lookup"><span data-stu-id="44f94-141">Custom actions that reference an installed file as their source, such as Custom Action Type 17 (DLL), must adhere to the following sequencing restrictions:</span></span>

-   <span data-ttu-id="44f94-142">La acción personalizada se debe secuenciar después de la [acción CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="44f94-142">The custom action must be sequenced after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="44f94-143">Esto es para que la acción personalizada pueda resolver la ruta de acceso necesaria para buscar el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="44f94-143">This is so that the custom action can resolve the path needed to locate the DLL.</span></span>
-   <span data-ttu-id="44f94-144">Si el archivo de código fuente no está ya instalado en el equipo, las acciones personalizadas diferidas (en script) de este tipo deben secuenciarse después de la [acción InstallFiles](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="44f94-144">If the source file is not already installed on the computer, deferred (in-script) custom actions of this type must be sequenced after the [InstallFiles action](installfiles-action.md).</span></span>
-   <span data-ttu-id="44f94-145">Si el archivo de código fuente no está ya instalado en el equipo, las acciones personalizadas no diferidas de este tipo se deben secuenciar después de la [acción InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="44f94-145">If the source file is not already installed on the computer, non-deferred custom actions of this type must be sequenced after the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="44f94-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="44f94-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44f94-147">\_Acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="44f94-147">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="44f94-148">Acciones personalizadas de ejecución aplazada</span><span class="sxs-lookup"><span data-stu-id="44f94-148">Deferred Execution Custom Actions</span></span>](deferred-execution-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="44f94-149">Bibliotecas de vínculos dinámicos</span><span class="sxs-lookup"><span data-stu-id="44f94-149">Dynamic-Link Libraries</span></span>](dynamic-link-libraries.md)
</dt> </dl>

 

 



