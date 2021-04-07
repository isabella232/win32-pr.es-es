---
description: Los desarrolladores de paquetes de Windows Installer pueden optar por usar una acción personalizada tipo 18 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: 8a7311a6-41c6-431e-982d-60bacf06454e
title: Tipo de acción personalizada 18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a669fe3caa532b3a365f1056ca2b36f490ab95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002926"
---
# <a name="custom-action-type-18"></a><span data-ttu-id="e5f04-103">Tipo de acción personalizada 18</span><span class="sxs-lookup"><span data-stu-id="e5f04-103">Custom Action Type 18</span></span>

<span data-ttu-id="e5f04-104">Esta acción personalizada llama a un ejecutable iniciado con una línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="e5f04-104">This custom action calls an executable launched with a command line.</span></span>

## <a name="source"></a><span data-ttu-id="e5f04-105">Source</span><span class="sxs-lookup"><span data-stu-id="e5f04-105">Source</span></span>

<span data-ttu-id="e5f04-106">El ejecutable se genera a partir de un archivo instalado con la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e5f04-106">The executable is generated from a file installed with the application.</span></span> <span data-ttu-id="e5f04-107">El campo de origen de la [tabla CustomAction](customaction-table.md) contiene una clave para la [tabla de archivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="e5f04-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [File table](file-table.md).</span></span> <span data-ttu-id="e5f04-108">La ubicación del código de acción personalizada viene determinada por la resolución de la ruta de acceso de destino para este archivo; por lo tanto, se debe llamar a esta acción personalizada después de haber instalado el archivo y antes de quitarlo.</span><span class="sxs-lookup"><span data-stu-id="e5f04-108">The location of the custom action code is determined by the resolution of the target path for this file; therefore this custom action must be called after the file has been installed and before it is removed.</span></span>

## <a name="type-value"></a><span data-ttu-id="e5f04-109">Valor de tipo</span><span class="sxs-lookup"><span data-stu-id="e5f04-109">Type Value</span></span>

<span data-ttu-id="e5f04-110">Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico.</span><span class="sxs-lookup"><span data-stu-id="e5f04-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="e5f04-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="e5f04-111">Constants</span></span>                                                          | <span data-ttu-id="e5f04-112">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="e5f04-112">Hexadecimal</span></span> | <span data-ttu-id="e5f04-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="e5f04-113">Decimal</span></span> |
|--------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="e5f04-114">**msidbCustomActionTypeExe**  +  **msidbCustomActionTypeSourceFile**</span><span class="sxs-lookup"><span data-stu-id="e5f04-114">**msidbCustomActionTypeExe** + **msidbCustomActionTypeSourceFile**</span></span> | <span data-ttu-id="e5f04-115">0x012</span><span class="sxs-lookup"><span data-stu-id="e5f04-115">0x012</span></span>       | <span data-ttu-id="e5f04-116">18</span><span class="sxs-lookup"><span data-stu-id="e5f04-116">18</span></span>      |



 

## <a name="target"></a><span data-ttu-id="e5f04-117">Destino</span><span class="sxs-lookup"><span data-stu-id="e5f04-117">Target</span></span>

<span data-ttu-id="e5f04-118">La columna de destino de la [tabla CustomAction](customaction-table.md) contiene la cadena de línea de comandos para el ejecutable identificado en la columna de origen.</span><span class="sxs-lookup"><span data-stu-id="e5f04-118">The Target column of the [CustomAction table](customaction-table.md) contains the command line string for the executable identified in the Source column.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="e5f04-119">Opciones de procesamiento de valores devueltos</span><span class="sxs-lookup"><span data-stu-id="e5f04-119">Return Processing Options</span></span>

<span data-ttu-id="e5f04-120">Incluya bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de procesamiento de valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="e5f04-120">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="e5f04-121">Para obtener una descripción de las opciones y los valores, vea [Opciones de procesamiento de devolución de acción personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="e5f04-121">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="e5f04-122">Opciones de programación de ejecución</span><span class="sxs-lookup"><span data-stu-id="e5f04-122">Execution Scheduling Options</span></span>

<span data-ttu-id="e5f04-123">Incluya los bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de programación de la ejecución.</span><span class="sxs-lookup"><span data-stu-id="e5f04-123">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="e5f04-124">Estas opciones controlan la ejecución múltiple de acciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="e5f04-124">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="e5f04-125">Para obtener una descripción de las opciones, vea opciones de programación de la [ejecución de acciones personalizadas](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="e5f04-125">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="e5f04-126">Opciones de ejecución de In-Script</span><span class="sxs-lookup"><span data-stu-id="e5f04-126">In-Script Execution Options</span></span>

<span data-ttu-id="e5f04-127">Incluya bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar una opción de ejecución en el script.</span><span class="sxs-lookup"><span data-stu-id="e5f04-127">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="e5f04-128">Estas opciones copian el código de acción en el script de ejecución, reversión o confirmación.</span><span class="sxs-lookup"><span data-stu-id="e5f04-128">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="e5f04-129">Para obtener una descripción de las opciones, vea [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="e5f04-129">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="e5f04-130">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="e5f04-130">Return Values</span></span>

<span data-ttu-id="e5f04-131">Las acciones personalizadas que son [archivos ejecutables](executable-files.md) deben devolver un valor de 0 para que se ejecute correctamente.</span><span class="sxs-lookup"><span data-stu-id="e5f04-131">Custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="e5f04-132">El instalador interpreta cualquier otro valor devuelto como error.</span><span class="sxs-lookup"><span data-stu-id="e5f04-132">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="e5f04-133">Para omitir los valores devueltos, establezca la marca de bits **msidbCustomActionTypeContinue** en el campo Type de la tabla CustomAction.</span><span class="sxs-lookup"><span data-stu-id="e5f04-133">To ignore return values, set the **msidbCustomActionTypeContinue** bit flag in the Type field of the CustomAction table.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5f04-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e5f04-134">Remarks</span></span>

<span data-ttu-id="e5f04-135">Una acción personalizada que inicia un ejecutable toma una línea de comandos, que normalmente contiene las propiedades que se designan dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="e5f04-135">A custom action that launches an executable takes a command line, which commonly contains properties that are designated dynamically.</span></span> <span data-ttu-id="e5f04-136">Si esta es también una [acción personalizada de ejecución aplazada](deferred-execution-custom-actions.md), el instalador usa [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) o [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) para crear el proceso cuando se invoca la acción personalizada desde el script de instalación.</span><span class="sxs-lookup"><span data-stu-id="e5f04-136">If this is also a [deferred execution custom action](deferred-execution-custom-actions.md), the installer uses [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) or [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) to create the process when the custom action is invoked from the installation script.</span></span>

<span data-ttu-id="e5f04-137">Las acciones personalizadas que hacen referencia a un archivo instalado como origen, como el tipo de acción personalizada 18 (EXE), deben cumplir las siguientes restricciones de secuenciación:</span><span class="sxs-lookup"><span data-stu-id="e5f04-137">Custom actions that reference an installed file as their source, such as Custom Action Type 18 (EXE), must adhere to the following sequencing restrictions:</span></span>

-   <span data-ttu-id="e5f04-138">La acción personalizada se debe secuenciar después de la [acción CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="e5f04-138">The custom action must be sequenced after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="e5f04-139">Esto es para que la acción personalizada pueda resolver la ruta de acceso necesaria para localizar el archivo EXE.</span><span class="sxs-lookup"><span data-stu-id="e5f04-139">This is so that the custom action can resolve the path needed to locate the EXE.</span></span>
-   <span data-ttu-id="e5f04-140">Si el archivo de código fuente no está ya instalado en el equipo, las acciones personalizadas diferidas (en script) de este tipo deben secuenciarse después de la [acción InstallFiles](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="e5f04-140">If the source file is not already installed on the computer, deferred (in-script) custom actions of this type must be sequenced after the [InstallFiles action](installfiles-action.md).</span></span>
-   <span data-ttu-id="e5f04-141">Si el archivo de código fuente no está ya instalado en el equipo, las acciones personalizadas no diferidas de este tipo se deben secuenciar después de la [acción InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="e5f04-141">If the source file is not already installed on the computer, non-deferred custom actions of this type must be sequenced after the [InstallFinalize action](installfinalize-action.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5f04-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e5f04-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5f04-143">\_Acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="e5f04-143">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="e5f04-144">Archivos ejecutables</span><span class="sxs-lookup"><span data-stu-id="e5f04-144">Executable Files</span></span>](executable-files.md)
</dt> </dl>

 

 
