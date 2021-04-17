---
description: Los desarrolladores de paquetes de Windows Installer pueden optar por usar una acción personalizada tipo 5 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: 32b10271-44b1-4c5d-9c8b-eed1b4cd31e2
title: Tipo de acción personalizada 5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85460c9a41dca060ca2634c013999c2c340ddfa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667622"
---
# <a name="custom-action-type-5"></a><span data-ttu-id="dd3bc-103">Tipo de acción personalizada 5</span><span class="sxs-lookup"><span data-stu-id="dd3bc-103">Custom Action Type 5</span></span>

<span data-ttu-id="dd3bc-104">Esta acción personalizada se escribe en JScript, como ECMA 262.</span><span class="sxs-lookup"><span data-stu-id="dd3bc-104">This custom action is written in JScript, such as ECMA 262.</span></span> <span data-ttu-id="dd3bc-105">Windows Installer no admite JScript 1,0.</span><span class="sxs-lookup"><span data-stu-id="dd3bc-105">Windows Installer does not support JScript 1.0.</span></span> <span data-ttu-id="dd3bc-106">Para obtener más información, vea [scripts](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="dd3bc-106">For more information, see [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="dd3bc-107">Source</span><span class="sxs-lookup"><span data-stu-id="dd3bc-107">Source</span></span>

<span data-ttu-id="dd3bc-108">El script se genera a partir de una secuencia binaria temporal.</span><span class="sxs-lookup"><span data-stu-id="dd3bc-108">The script is generated from a temporary binary stream.</span></span> <span data-ttu-id="dd3bc-109">El campo de origen de la [tabla CustomAction](customaction-table.md) contiene una clave para la [tabla binaria](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="dd3bc-109">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Binary table](binary-table.md).</span></span> <span data-ttu-id="dd3bc-110">La columna de datos de la tabla binaria contiene los datos de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="dd3bc-110">The Data column in the Binary table contains the stream data.</span></span> <span data-ttu-id="dd3bc-111">Se asigna una secuencia independiente para cada fila.</span><span class="sxs-lookup"><span data-stu-id="dd3bc-111">A separate stream is allocated for each row.</span></span>

<span data-ttu-id="dd3bc-112">Se pueden insertar nuevos datos binarios de un archivo mediante [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) seguido de [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) para insertar el registro en la tabla.</span><span class="sxs-lookup"><span data-stu-id="dd3bc-112">New binary data can be inserted from a file by using [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) followed by [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the record into the table.</span></span> <span data-ttu-id="dd3bc-113">Cuando se invoca la acción personalizada, los datos de la secuencia se copian en un archivo temporal, que se procesa según el tipo de acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="dd3bc-113">When the custom action is invoked, the stream data is copied to a temporary file, which is then processed according to the type of custom action.</span></span>

## <a name="type-value"></a><span data-ttu-id="dd3bc-114">Valor de tipo</span><span class="sxs-lookup"><span data-stu-id="dd3bc-114">Type Value</span></span>

<span data-ttu-id="dd3bc-115">Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico de la acción personalizada de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="dd3bc-115">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of 32-bit custom action.</span></span>



| <span data-ttu-id="dd3bc-116">Constantes</span><span class="sxs-lookup"><span data-stu-id="dd3bc-116">Constants</span></span>                                                              | <span data-ttu-id="dd3bc-117">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="dd3bc-117">Hexadecimal</span></span> | <span data-ttu-id="dd3bc-118">Decimal</span><span class="sxs-lookup"><span data-stu-id="dd3bc-118">Decimal</span></span> |
|------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="dd3bc-119">**msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeBinaryData**</span><span class="sxs-lookup"><span data-stu-id="dd3bc-119">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeBinaryData**</span></span> | <span data-ttu-id="dd3bc-120">0x05</span><span class="sxs-lookup"><span data-stu-id="dd3bc-120">0x05</span></span>        | <span data-ttu-id="dd3bc-121">5</span><span class="sxs-lookup"><span data-stu-id="dd3bc-121">5</span></span>       |



 

<span data-ttu-id="dd3bc-122">Windows Installer puede usar las acciones personalizadas de 64 bits en sistemas operativos de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="dd3bc-122">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="dd3bc-123">Una acción personalizada de 64 bits basada en scripts debe incluir el bit **msidbCustomActionType64BitScript** en su tipo numérico.</span><span class="sxs-lookup"><span data-stu-id="dd3bc-123">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="dd3bc-124">Para obtener información, consulte [acciones personalizadas de 64 bits](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="dd3bc-124">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="dd3bc-125">Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico de una acción personalizada de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="dd3bc-125">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="dd3bc-126">Constantes</span><span class="sxs-lookup"><span data-stu-id="dd3bc-126">Constants</span></span>                                                                                                     | <span data-ttu-id="dd3bc-127">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="dd3bc-127">Hexadecimal</span></span> | <span data-ttu-id="dd3bc-128">Decimal</span><span class="sxs-lookup"><span data-stu-id="dd3bc-128">Decimal</span></span> |
|---------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="dd3bc-129">**msidbCustomActionTypeJScript**  +  **msidbCustomActionTypeBinaryData**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="dd3bc-129">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeBinaryData** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="dd3bc-130">0x0001005</span><span class="sxs-lookup"><span data-stu-id="dd3bc-130">0x0001005</span></span>   | <span data-ttu-id="dd3bc-131">4101</span><span class="sxs-lookup"><span data-stu-id="dd3bc-131">4101</span></span>    |



 

## <a name="target"></a><span data-ttu-id="dd3bc-132">Destino</span><span class="sxs-lookup"><span data-stu-id="dd3bc-132">Target</span></span>

<span data-ttu-id="dd3bc-133">El campo de destino de la [tabla CustomAction](customaction-table.md) contiene una función de script opcional.</span><span class="sxs-lookup"><span data-stu-id="dd3bc-133">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="dd3bc-134">El procesamiento primero envía el script para el análisis y, a continuación, llama a la función de script opcional.</span><span class="sxs-lookup"><span data-stu-id="dd3bc-134">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="dd3bc-135">Opciones de procesamiento de valores devueltos</span><span class="sxs-lookup"><span data-stu-id="dd3bc-135">Return Processing Options</span></span>

<span data-ttu-id="dd3bc-136">Incluya bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de procesamiento de valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="dd3bc-136">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="dd3bc-137">Para obtener una descripción de las opciones y los valores, vea [Opciones de procesamiento de devolución de acción personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="dd3bc-137">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="dd3bc-138">Opciones de programación de ejecución</span><span class="sxs-lookup"><span data-stu-id="dd3bc-138">Execution Scheduling Options</span></span>

<span data-ttu-id="dd3bc-139">Incluya los bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de programación de la ejecución.</span><span class="sxs-lookup"><span data-stu-id="dd3bc-139">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="dd3bc-140">Estas opciones controlan la ejecución múltiple de acciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="dd3bc-140">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="dd3bc-141">Para obtener una descripción de las opciones, vea opciones de programación de la [ejecución de acciones personalizadas](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="dd3bc-141">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="dd3bc-142">Opciones de ejecución de In-Script</span><span class="sxs-lookup"><span data-stu-id="dd3bc-142">In-Script Execution Options</span></span>

<span data-ttu-id="dd3bc-143">Incluya bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar una opción de ejecución en el script.</span><span class="sxs-lookup"><span data-stu-id="dd3bc-143">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="dd3bc-144">Estas opciones copian el código de acción en el script de ejecución, reversión o confirmación.</span><span class="sxs-lookup"><span data-stu-id="dd3bc-144">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="dd3bc-145">Para obtener una descripción de las opciones, vea [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="dd3bc-145">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="dd3bc-146">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="dd3bc-146">Return Values</span></span>

<span data-ttu-id="dd3bc-147">Las funciones opcionales escritas en el script deben devolver uno de los valores descritos en [valores devueltos de las acciones personalizadas de JScript y VBScript](return-values-of-jscript-and-vbscript-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="dd3bc-147">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="dd3bc-148">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dd3bc-148">Remarks</span></span>

<span data-ttu-id="dd3bc-149">Una acción personalizada escrita en JScript o VBScript requiere la instalación del objeto de [**sesión**](session-object.md).</span><span class="sxs-lookup"><span data-stu-id="dd3bc-149">A custom action that is written in JScript or VBScript requires the installation of [**Session Object**](session-object.md).</span></span> <span data-ttu-id="dd3bc-150">El instalador adjunta el objeto de **sesión** al script con la *sesión* de nombre.</span><span class="sxs-lookup"><span data-stu-id="dd3bc-150">The installer attaches the **Session** object to the script with the name *Session*.</span></span> <span data-ttu-id="dd3bc-151">Dado que es posible que el objeto de **sesión** no exista durante una reversión de la instalación, una acción personalizada diferida escrita en el script debe usar uno de los métodos o propiedades del objeto de **sesión** que se describe en la sección [obtener información de contexto para las acciones personalizadas de ejecución aplazada](obtaining-context-information-for-deferred-execution-custom-actions.md) para recuperar su contexto.</span><span class="sxs-lookup"><span data-stu-id="dd3bc-151">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

<span data-ttu-id="dd3bc-152">Cuando se exporta una tabla de base de datos, cada secuencia se escribe como un archivo independiente en la subcarpeta con el nombre de la tabla, utilizando la clave principal como el nombre de archivo (columna Name de la tabla binaria), con una extensión predeterminada de ". ibd".</span><span class="sxs-lookup"><span data-stu-id="dd3bc-152">When a database table is exported, each stream is written as a separate file in the subfolder named after the table, using the primary key as the file name (Name column for the Binary table), with a default extension of ".ibd".</span></span> <span data-ttu-id="dd3bc-153">El nombre debe usar el formato de nombre de archivo 8,3 si el sistema de archivos o el sistema de control de versiones no admiten nombres de archivo largos.</span><span class="sxs-lookup"><span data-stu-id="dd3bc-153">The name should use the 8.3 file name format if the file system or version control system does not support long file names.</span></span> <span data-ttu-id="dd3bc-154">El archivo de almacenamiento persistente reemplaza los datos de la secuencia por el nombre de archivo usado, de modo que los datos se pueden encontrar al importar la tabla.</span><span class="sxs-lookup"><span data-stu-id="dd3bc-154">The persistent archive file replaces the stream data with the file name used, so that the data can be located when the table is imported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd3bc-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dd3bc-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd3bc-156">\_Acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="dd3bc-156">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



