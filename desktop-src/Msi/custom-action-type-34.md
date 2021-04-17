---
description: Los desarrolladores de paquetes de Windows Installer pueden optar por usar un tipo de acción personalizada 34 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: 4d0e4f01-0530-4202-bc78-b6e52670b8e5
title: Tipo de acción personalizada 34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ba17c9a4dc5b35d8d03e9cca2707079cb15bf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652889"
---
# <a name="custom-action-type-34"></a><span data-ttu-id="2e46a-103">Tipo de acción personalizada 34</span><span class="sxs-lookup"><span data-stu-id="2e46a-103">Custom Action Type 34</span></span>

<span data-ttu-id="2e46a-104">Esta acción personalizada llama a un ejecutable iniciado con una línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="2e46a-104">This custom action calls an executable launched with a command line.</span></span> <span data-ttu-id="2e46a-105">Para obtener más información, vea [archivos ejecutables](executable-files.md).</span><span class="sxs-lookup"><span data-stu-id="2e46a-105">For more information, see [Executable Files](executable-files.md).</span></span>

## <a name="source"></a><span data-ttu-id="2e46a-106">Source</span><span class="sxs-lookup"><span data-stu-id="2e46a-106">Source</span></span>

<span data-ttu-id="2e46a-107">El ejecutable se genera a partir de un archivo.</span><span class="sxs-lookup"><span data-stu-id="2e46a-107">The executable is generated from a file.</span></span> <span data-ttu-id="2e46a-108">El campo de origen de la tabla [CustomAction](customaction-table.md) contiene una clave en la tabla de [directorios](directory-table.md) .</span><span class="sxs-lookup"><span data-stu-id="2e46a-108">The Source field of the [CustomAction](customaction-table.md) table contains a key into the [Directory](directory-table.md) table.</span></span> <span data-ttu-id="2e46a-109">La entrada de la tabla de directorios a la que se hace referencia se usa para resolver la ruta de acceso completa a un directorio de trabajo.</span><span class="sxs-lookup"><span data-stu-id="2e46a-109">The referenced Directory table entry is used to resolve the full path to a working directory.</span></span> <span data-ttu-id="2e46a-110">No es necesario que sea la ruta de acceso al directorio que contiene el archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="2e46a-110">This is not required to be the path to the directory containing the executable.</span></span>

## <a name="type-value"></a><span data-ttu-id="2e46a-111">Valor de tipo</span><span class="sxs-lookup"><span data-stu-id="2e46a-111">Type Value</span></span>

<span data-ttu-id="2e46a-112">Incluya el siguiente valor en la columna Type de la tabla [CustomAction](customaction-table.md) para especificar el tipo numérico básico.</span><span class="sxs-lookup"><span data-stu-id="2e46a-112">Include the following value in the Type column of the [CustomAction](customaction-table.md) table to specify the basic numeric type.</span></span>



| <span data-ttu-id="2e46a-113">Constantes</span><span class="sxs-lookup"><span data-stu-id="2e46a-113">Constants</span></span>                                                         | <span data-ttu-id="2e46a-114">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="2e46a-114">Hexadecimal</span></span> | <span data-ttu-id="2e46a-115">Decimal</span><span class="sxs-lookup"><span data-stu-id="2e46a-115">Decimal</span></span> |
|-------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="2e46a-116">**msidbCustomActionTypeExe**  +  **msidbCustomActionTypeDirectory**</span><span class="sxs-lookup"><span data-stu-id="2e46a-116">**msidbCustomActionTypeExe** + **msidbCustomActionTypeDirectory**</span></span> | <span data-ttu-id="2e46a-117">0x022</span><span class="sxs-lookup"><span data-stu-id="2e46a-117">0x022</span></span>       | <span data-ttu-id="2e46a-118">34</span><span class="sxs-lookup"><span data-stu-id="2e46a-118">34</span></span>      |



 

## <a name="target"></a><span data-ttu-id="2e46a-119">Destino</span><span class="sxs-lookup"><span data-stu-id="2e46a-119">Target</span></span>

<span data-ttu-id="2e46a-120">La columna de destino de la tabla [CustomAction](customaction-table.md) contiene la ruta de acceso completa y el nombre del archivo ejecutable seguidos de argumentos opcionales para el ejecutable.</span><span class="sxs-lookup"><span data-stu-id="2e46a-120">The Target column of the [CustomAction](customaction-table.md) table contains the full path and name of the executable file followed by optional arguments to the executable.</span></span> <span data-ttu-id="2e46a-121">Se requiere la ruta de acceso completa y el nombre del archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="2e46a-121">The full path and name to the executable file is required.</span></span> <span data-ttu-id="2e46a-122">Las comillas deben usarse en torno a nombres de archivo largos o rutas de acceso.</span><span class="sxs-lookup"><span data-stu-id="2e46a-122">Quotation marks must be used around long file names or paths.</span></span> <span data-ttu-id="2e46a-123">El valor se trata como texto [con formato](formatted.md) y puede contener referencias a propiedades, archivos, directorios u otros atributos de texto con formato.</span><span class="sxs-lookup"><span data-stu-id="2e46a-123">The value is treated as [formatted](formatted.md) text and may contain references to properties, files, directories, or other formatted text attributes.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="2e46a-124">Opciones de procesamiento de valores devueltos</span><span class="sxs-lookup"><span data-stu-id="2e46a-124">Return Processing Options</span></span>

<span data-ttu-id="2e46a-125">Incluya bits de marca opcionales en la columna tipo de la tabla [CustomAction](customaction-table.md) para especificar las opciones de procesamiento de valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="2e46a-125">Include optional flag bits in the Type column of the [CustomAction](customaction-table.md) table to specify return processing options.</span></span> <span data-ttu-id="2e46a-126">Para obtener una descripción de las opciones y los valores, vea [Opciones de procesamiento de devolución de acción personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="2e46a-126">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="2e46a-127">Opciones de programación de ejecución</span><span class="sxs-lookup"><span data-stu-id="2e46a-127">Execution Scheduling Options</span></span>

<span data-ttu-id="2e46a-128">Incluya los bits de marca opcionales en la columna tipo de la tabla [CustomAction](customaction-table.md) para especificar las opciones de programación de la ejecución.</span><span class="sxs-lookup"><span data-stu-id="2e46a-128">Include optional flag bits in the Type column of the [CustomAction](customaction-table.md) table to specify execution scheduling options.</span></span> <span data-ttu-id="2e46a-129">Estas opciones controlan la ejecución múltiple de acciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="2e46a-129">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="2e46a-130">Para obtener una descripción de las opciones, vea opciones de programación de la [ejecución de acciones personalizadas](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="2e46a-130">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="2e46a-131">Opciones de ejecución de In-Script</span><span class="sxs-lookup"><span data-stu-id="2e46a-131">In-Script Execution Options</span></span>

<span data-ttu-id="2e46a-132">Incluya bits de marca opcionales en la columna tipo de la tabla [CustomAction](customaction-table.md) para especificar una opción de ejecución en el script.</span><span class="sxs-lookup"><span data-stu-id="2e46a-132">Include optional flag bits in the Type column of the [CustomAction](customaction-table.md) table to specify an in-script execution option.</span></span> <span data-ttu-id="2e46a-133">Estas opciones copian el código de acción en el script de ejecución, reversión o confirmación.</span><span class="sxs-lookup"><span data-stu-id="2e46a-133">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="2e46a-134">Para obtener una descripción de las opciones, vea [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="2e46a-134">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="2e46a-135">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="2e46a-135">Return Values</span></span>

<span data-ttu-id="2e46a-136">Las acciones personalizadas que son [archivos ejecutables](executable-files.md) deben devolver un valor de 0 para que se ejecute correctamente.</span><span class="sxs-lookup"><span data-stu-id="2e46a-136">Custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="2e46a-137">El instalador interpreta cualquier otro valor devuelto como error.</span><span class="sxs-lookup"><span data-stu-id="2e46a-137">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="2e46a-138">Para omitir los valores devueltos, establezca la marca de bits **msidbCustomActionTypeContinue** en el campo Type de la tabla [CustomAction](customaction-table.md) .</span><span class="sxs-lookup"><span data-stu-id="2e46a-138">To ignore return values set the **msidbCustomActionTypeContinue** bit flag in the Type field of the [CustomAction](customaction-table.md) table.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e46a-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e46a-139">Remarks</span></span>

<span data-ttu-id="2e46a-140">Una acción personalizada que inicia un ejecutable toma una línea de comandos, que normalmente contiene las propiedades que se designan dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="2e46a-140">A custom action that launches an executable takes a command line, which commonly contains properties that are designated dynamically.</span></span> <span data-ttu-id="2e46a-141">Si esta es también una [acción personalizada de ejecución aplazada](deferred-execution-custom-actions.md), el instalador usa [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) o [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) para crear el proceso cuando se invoca la acción personalizada desde el script de instalación.</span><span class="sxs-lookup"><span data-stu-id="2e46a-141">If this is also a [deferred execution custom action](deferred-execution-custom-actions.md), the installer uses [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) or [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) to create the process when the custom action is invoked from the installation script.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e46a-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2e46a-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e46a-143">\_Acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="2e46a-143">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 
