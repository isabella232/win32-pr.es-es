---
description: Los desarrolladores de paquetes de Windows Installer pueden optar por usar un tipo de acción personalizada 50 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: fc8a875d-21e3-452a-8455-80835b52b256
title: Tipo de acción personalizada 50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5f3a80de730eb727c40c871070ab9e5b2470f98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652923"
---
# <a name="custom-action-type-50"></a><span data-ttu-id="7a018-103">Tipo de acción personalizada 50</span><span class="sxs-lookup"><span data-stu-id="7a018-103">Custom Action Type 50</span></span>

<span data-ttu-id="7a018-104">Esta acción personalizada llama a un ejecutable iniciado con una línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="7a018-104">This custom action calls an executable launched with a command line.</span></span>

<span data-ttu-id="7a018-105">Vea también [archivos ejecutables](executable-files.md).</span><span class="sxs-lookup"><span data-stu-id="7a018-105">See also [Executable Files](executable-files.md).</span></span>

## <a name="source"></a><span data-ttu-id="7a018-106">Source</span><span class="sxs-lookup"><span data-stu-id="7a018-106">Source</span></span>

<span data-ttu-id="7a018-107">El ejecutable se genera a partir de un archivo existente.</span><span class="sxs-lookup"><span data-stu-id="7a018-107">The executable is generated from an existing file.</span></span> <span data-ttu-id="7a018-108">El campo de origen de la [tabla CustomAction](customaction-table.md) contiene una clave para la [tabla de propiedades](property-table.md) de una propiedad que contiene la ruta de acceso completa al archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="7a018-108">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Property table](property-table.md) for a property that contains the full path to the executable file.</span></span>

## <a name="type-value"></a><span data-ttu-id="7a018-109">Valor de tipo</span><span class="sxs-lookup"><span data-stu-id="7a018-109">Type Value</span></span>

<span data-ttu-id="7a018-110">Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico.</span><span class="sxs-lookup"><span data-stu-id="7a018-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="7a018-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="7a018-111">Constants</span></span>                                                        | <span data-ttu-id="7a018-112">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="7a018-112">Hexadecimal</span></span> | <span data-ttu-id="7a018-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="7a018-113">Decimal</span></span> |
|------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="7a018-114">**msidbCustomActionTypeExe**  +  **msidbCustomActionTypeProperty**</span><span class="sxs-lookup"><span data-stu-id="7a018-114">**msidbCustomActionTypeExe** + **msidbCustomActionTypeProperty**</span></span> | <span data-ttu-id="7a018-115">0x032</span><span class="sxs-lookup"><span data-stu-id="7a018-115">0x032</span></span>       | <span data-ttu-id="7a018-116">50</span><span class="sxs-lookup"><span data-stu-id="7a018-116">50</span></span>      |



 

## <a name="target"></a><span data-ttu-id="7a018-117">Destino</span><span class="sxs-lookup"><span data-stu-id="7a018-117">Target</span></span>

<span data-ttu-id="7a018-118">La columna de destino de la [tabla CustomAction](customaction-table.md) contiene la cadena de línea de comandos para el ejecutable identificado en la columna de origen.</span><span class="sxs-lookup"><span data-stu-id="7a018-118">The Target column of the [CustomAction table](customaction-table.md) contains the command line string for the executable identified in the Source column.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="7a018-119">Opciones de procesamiento de valores devueltos</span><span class="sxs-lookup"><span data-stu-id="7a018-119">Return Processing Options</span></span>

<span data-ttu-id="7a018-120">Incluya bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de procesamiento de valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="7a018-120">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="7a018-121">Para obtener una descripción de las opciones y los valores, vea [Opciones de procesamiento de devolución de acción personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="7a018-121">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="7a018-122">Opciones de programación de ejecución</span><span class="sxs-lookup"><span data-stu-id="7a018-122">Execution Scheduling Options</span></span>

<span data-ttu-id="7a018-123">Incluya los bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de programación de la ejecución.</span><span class="sxs-lookup"><span data-stu-id="7a018-123">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="7a018-124">Estas opciones controlan la ejecución múltiple de acciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="7a018-124">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="7a018-125">Para obtener una descripción de las opciones, vea opciones de programación de la [ejecución de acciones personalizadas](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="7a018-125">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="7a018-126">Opciones de ejecución de In-Script</span><span class="sxs-lookup"><span data-stu-id="7a018-126">In-Script Execution Options</span></span>

<span data-ttu-id="7a018-127">Incluya bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar una opción de ejecución en el script.</span><span class="sxs-lookup"><span data-stu-id="7a018-127">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="7a018-128">Estas opciones copian el código de acción en el script de ejecución, reversión o confirmación.</span><span class="sxs-lookup"><span data-stu-id="7a018-128">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="7a018-129">Para obtener una descripción de las opciones, vea [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="7a018-129">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="7a018-130">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="7a018-130">Return Values</span></span>

<span data-ttu-id="7a018-131">Las acciones personalizadas que son [archivos ejecutables](executable-files.md) deben devolver un valor de 0 para que se ejecute correctamente.</span><span class="sxs-lookup"><span data-stu-id="7a018-131">Custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="7a018-132">El instalador interpreta cualquier otro valor devuelto como error.</span><span class="sxs-lookup"><span data-stu-id="7a018-132">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="7a018-133">Para omitir los valores devueltos, establezca la marca de bits **msidbCustomActionTypeContinue** en el campo Type de la tabla CustomAction.</span><span class="sxs-lookup"><span data-stu-id="7a018-133">To ignore return values set the **msidbCustomActionTypeContinue** bit flag in the Type field of the CustomAction table.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a018-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7a018-134">Remarks</span></span>

<span data-ttu-id="7a018-135">Una acción personalizada que inicia un ejecutable toma una línea de comandos, que normalmente contiene las propiedades que se designan dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="7a018-135">A custom action that launches an executable takes a command line, which commonly contains properties that are designated dynamically.</span></span> <span data-ttu-id="7a018-136">Si esta es también una [acción personalizada de ejecución aplazada](deferred-execution-custom-actions.md), el instalador usa CreateProcessAsUser o CreateProcess para crear el proceso cuando se invoca la acción personalizada desde el script de instalación.</span><span class="sxs-lookup"><span data-stu-id="7a018-136">If this is also a [deferred execution custom action](deferred-execution-custom-actions.md), the installer uses CreateProcessAsUser or CreateProcess to create the process when the custom action is invoked from the installation script.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a018-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7a018-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a018-138">\_Acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="7a018-138">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



