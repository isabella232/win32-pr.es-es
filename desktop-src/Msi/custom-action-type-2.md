---
description: Los desarrolladores de paquetes de Windows Installer pueden optar por usar una acción personalizada tipo 2 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: 79ae0582-c991-4c0a-860b-0f5197ad0c7c
title: Tipo de acción personalizada 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0497b2a76dc2fac7f5e56f7347b50deac867757f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652890"
---
# <a name="custom-action-type-2"></a><span data-ttu-id="251e2-103">Tipo de acción personalizada 2</span><span class="sxs-lookup"><span data-stu-id="251e2-103">Custom Action Type 2</span></span>

<span data-ttu-id="251e2-104">Esta acción personalizada llama a un ejecutable iniciado con una línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="251e2-104">This custom action calls an executable launched with a command line.</span></span>

## <a name="source"></a><span data-ttu-id="251e2-105">Source</span><span class="sxs-lookup"><span data-stu-id="251e2-105">Source</span></span>

<span data-ttu-id="251e2-106">El ejecutable se genera a partir de una secuencia binaria temporal.</span><span class="sxs-lookup"><span data-stu-id="251e2-106">The executable is generated from a temporary binary stream.</span></span> <span data-ttu-id="251e2-107">El campo de origen de la [tabla CustomAction](customaction-table.md) contiene una clave para la [tabla binaria](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="251e2-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Binary table](binary-table.md).</span></span> <span data-ttu-id="251e2-108">La columna de datos de la tabla binaria contiene los datos de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="251e2-108">The Data column in the Binary table contains the stream data.</span></span> <span data-ttu-id="251e2-109">Se asigna una secuencia independiente para cada fila.</span><span class="sxs-lookup"><span data-stu-id="251e2-109">A separate stream is allocated for each row.</span></span>

<span data-ttu-id="251e2-110">Se pueden insertar nuevos datos binarios de un archivo mediante [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) seguido de [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) para insertar el registro en la tabla.</span><span class="sxs-lookup"><span data-stu-id="251e2-110">New binary data can be inserted from a file by using [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) followed by [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the record into the table.</span></span> <span data-ttu-id="251e2-111">Cuando se invoca la acción personalizada, los datos de la secuencia se copian en un archivo temporal, que se procesa en función del tipo de acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="251e2-111">When the custom action is invoked, the stream data is copied to a temporary file, which is then processed depending upon the type of custom action.</span></span>

## <a name="type-value"></a><span data-ttu-id="251e2-112">Valor de tipo</span><span class="sxs-lookup"><span data-stu-id="251e2-112">Type Value</span></span>

<span data-ttu-id="251e2-113">Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico.</span><span class="sxs-lookup"><span data-stu-id="251e2-113">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="251e2-114">Constantes</span><span class="sxs-lookup"><span data-stu-id="251e2-114">Constants</span></span>                                                          | <span data-ttu-id="251e2-115">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="251e2-115">Hexadecimal</span></span> | <span data-ttu-id="251e2-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="251e2-116">Decimal</span></span> |
|--------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="251e2-117">**msidbCustomActionTypeExe**  +  **msidbCustomActionTypeBinaryData**</span><span class="sxs-lookup"><span data-stu-id="251e2-117">**msidbCustomActionTypeExe** + **msidbCustomActionTypeBinaryData**</span></span> | <span data-ttu-id="251e2-118">0x002</span><span class="sxs-lookup"><span data-stu-id="251e2-118">0x002</span></span>       | <span data-ttu-id="251e2-119">2</span><span class="sxs-lookup"><span data-stu-id="251e2-119">2</span></span>       |



 

## <a name="target"></a><span data-ttu-id="251e2-120">Destino</span><span class="sxs-lookup"><span data-stu-id="251e2-120">Target</span></span>

<span data-ttu-id="251e2-121">La columna de destino de la [tabla CustomAction](customaction-table.md) contiene la cadena de línea de comandos para el ejecutable denominado en la columna de origen.</span><span class="sxs-lookup"><span data-stu-id="251e2-121">The Target column of the [CustomAction table](customaction-table.md) contains the command line string for the executable named in the Source column.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="251e2-122">Opciones de procesamiento de valores devueltos</span><span class="sxs-lookup"><span data-stu-id="251e2-122">Return Processing Options</span></span>

<span data-ttu-id="251e2-123">Incluya bits de marca opcionales en la columna tipo de la tabla CustomAction para especificar las opciones de procesamiento de valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="251e2-123">Include optional flag bits in the Type column of the CustomAction table to specify return processing options.</span></span> <span data-ttu-id="251e2-124">Para obtener una descripción de las opciones y los valores, vea [Opciones de procesamiento de devolución de acción personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="251e2-124">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="251e2-125">Opciones de programación de ejecución</span><span class="sxs-lookup"><span data-stu-id="251e2-125">Execution Scheduling Options</span></span>

<span data-ttu-id="251e2-126">Incluya los bits de marca opcionales en la columna tipo de la tabla CustomAction para especificar las opciones de programación de la ejecución.</span><span class="sxs-lookup"><span data-stu-id="251e2-126">Include optional flag bits in the Type column of the CustomAction table to specify execution scheduling options.</span></span> <span data-ttu-id="251e2-127">Estas opciones controlan la ejecución múltiple de acciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="251e2-127">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="251e2-128">Para obtener una descripción de las opciones, vea opciones de programación de la [ejecución de acciones personalizadas](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="251e2-128">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="251e2-129">Opciones de ejecución de In-Script</span><span class="sxs-lookup"><span data-stu-id="251e2-129">In-Script Execution Options</span></span>

<span data-ttu-id="251e2-130">Incluya bits de marca opcionales en la columna tipo de la tabla CustomAction para especificar una opción de ejecución en el script.</span><span class="sxs-lookup"><span data-stu-id="251e2-130">Include optional flag bits in the Type column of the CustomAction table to specify an in-script execution option.</span></span> <span data-ttu-id="251e2-131">Estas opciones copian el código de acción en el script de ejecución, reversión o confirmación.</span><span class="sxs-lookup"><span data-stu-id="251e2-131">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="251e2-132">Para obtener una descripción de las opciones, vea [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="251e2-132">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="251e2-133">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="251e2-133">Return Values</span></span>

<span data-ttu-id="251e2-134">Las acciones personalizadas que son [archivos ejecutables](executable-files.md) deben devolver un valor de 0 para que se ejecute correctamente.</span><span class="sxs-lookup"><span data-stu-id="251e2-134">Custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="251e2-135">El instalador interpreta cualquier otro valor devuelto como error.</span><span class="sxs-lookup"><span data-stu-id="251e2-135">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="251e2-136">Para omitir los valores devueltos, establezca la marca de bits **msidbCustomActionTypeContinue** en el campo Type de la tabla CustomAction.</span><span class="sxs-lookup"><span data-stu-id="251e2-136">To ignore return values, set the **msidbCustomActionTypeContinue** bit flag in the Type field of the CustomAction table.</span></span>

## <a name="remarks"></a><span data-ttu-id="251e2-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="251e2-137">Remarks</span></span>

<span data-ttu-id="251e2-138">Una acción personalizada que inicia un ejecutable toma una línea de comandos, que normalmente contiene las propiedades que se designan dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="251e2-138">A custom action that launches an executable takes a command line, which commonly contains properties that are designated dynamically.</span></span> <span data-ttu-id="251e2-139">Si esta es también una [acción personalizada de ejecución aplazada](deferred-execution-custom-actions.md), el instalador usa [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) o [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) para crear el proceso cuando se invoca la acción personalizada desde el script de instalación.</span><span class="sxs-lookup"><span data-stu-id="251e2-139">If this is also a [deferred execution custom action](deferred-execution-custom-actions.md), the installer uses [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) or [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) to create the process when the custom action is invoked from the installation script.</span></span>

<span data-ttu-id="251e2-140">Cuando se exporta una tabla de base de datos, cada secuencia se escribe como un archivo independiente en la subcarpeta con el nombre de la tabla, utilizando la clave principal como el nombre de archivo (columna Name de la tabla binaria), con una extensión predeterminada de ". ibd".</span><span class="sxs-lookup"><span data-stu-id="251e2-140">When a database table is exported, each stream is written as a separate file in the subfolder named after the table, using the primary key as the file name (Name column for the Binary table), with a default extension of ".ibd".</span></span> <span data-ttu-id="251e2-141">El nombre debe usar el formato 8,3 si el sistema de archivos o el sistema de control de versiones no admiten nombres de archivo largos.</span><span class="sxs-lookup"><span data-stu-id="251e2-141">The name should use the 8.3 format if the file system or version control system does not support long file names.</span></span> <span data-ttu-id="251e2-142">El archivo de almacenamiento persistente reemplaza los datos de la secuencia por el nombre de archivo usado, de modo que los datos se pueden encontrar al importar la tabla.</span><span class="sxs-lookup"><span data-stu-id="251e2-142">The persistent archive file replaces the stream data with the file name used, so that the data can be located when the table is imported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="251e2-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="251e2-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="251e2-144">\_Acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="251e2-144">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="251e2-145">Archivos ejecutables</span><span class="sxs-lookup"><span data-stu-id="251e2-145">Executable Files</span></span>](executable-files.md)
</dt> </dl>

 

 
