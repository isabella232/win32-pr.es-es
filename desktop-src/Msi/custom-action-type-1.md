---
description: Los desarrolladores de paquetes de Windows Installer pueden optar por usar una acción personalizada tipo 1 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: 277b875f-37f1-4f4d-98ae-7a18131de4f0
title: Tipo de acción personalizada 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f72efd083b2cd547ff1dbd7f3bc81a617b5da88e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083355"
---
# <a name="custom-action-type-1"></a><span data-ttu-id="6295d-103">Tipo de acción personalizada 1</span><span class="sxs-lookup"><span data-stu-id="6295d-103">Custom Action Type 1</span></span>

<span data-ttu-id="6295d-104">Esta acción personalizada llama a una biblioteca de vínculos dinámicos (DLL) escrita en C o C++.</span><span class="sxs-lookup"><span data-stu-id="6295d-104">This custom action calls a dynamic link library (DLL) written in C or C++.</span></span>

## <a name="source"></a><span data-ttu-id="6295d-105">Source</span><span class="sxs-lookup"><span data-stu-id="6295d-105">Source</span></span>

<span data-ttu-id="6295d-106">El archivo DLL se genera a partir de una secuencia binaria temporal.</span><span class="sxs-lookup"><span data-stu-id="6295d-106">The DLL is generated from a temporary binary stream.</span></span> <span data-ttu-id="6295d-107">El campo de origen de la [tabla CustomAction](customaction-table.md) contiene una clave para la [tabla binaria](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="6295d-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Binary table](binary-table.md).</span></span>

<span data-ttu-id="6295d-108">La columna de datos de la tabla binaria contiene los datos de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="6295d-108">The Data column in the Binary table contains the stream data.</span></span> <span data-ttu-id="6295d-109">Se asigna una secuencia independiente para cada fila.</span><span class="sxs-lookup"><span data-stu-id="6295d-109">A separate stream is allocated for each row.</span></span> <span data-ttu-id="6295d-110">Se pueden insertar nuevos datos binarios de un archivo mediante [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) seguido de [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) para insertar el registro en la tabla.</span><span class="sxs-lookup"><span data-stu-id="6295d-110">New binary data can be inserted from a file by using [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) followed by [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the record into the table.</span></span> <span data-ttu-id="6295d-111">Cuando se invoca la acción personalizada, los datos de la secuencia se copian en un archivo temporal, que se procesa en función del tipo de acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="6295d-111">When the custom action is invoked, the stream data is copied to a temporary file, which is then processed depending upon the type of custom action.</span></span>

## <a name="type-value"></a><span data-ttu-id="6295d-112">Valor de tipo</span><span class="sxs-lookup"><span data-stu-id="6295d-112">Type Value</span></span>

<span data-ttu-id="6295d-113">Incluya los siguientes bits de marca en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico.</span><span class="sxs-lookup"><span data-stu-id="6295d-113">Include the following flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="6295d-114">Constantes</span><span class="sxs-lookup"><span data-stu-id="6295d-114">Constants</span></span>                                                          | <span data-ttu-id="6295d-115">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="6295d-115">Hexadecimal</span></span> | <span data-ttu-id="6295d-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="6295d-116">Decimal</span></span> |
|--------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="6295d-117">**msidbCustomActionTypeDll**  +  **msidbCustomActionTypeBinaryData**</span><span class="sxs-lookup"><span data-stu-id="6295d-117">**msidbCustomActionTypeDll** + **msidbCustomActionTypeBinaryData**</span></span> | <span data-ttu-id="6295d-118">0x001</span><span class="sxs-lookup"><span data-stu-id="6295d-118">0x001</span></span>       | <span data-ttu-id="6295d-119">1</span><span class="sxs-lookup"><span data-stu-id="6295d-119">1</span></span>       |



 

## <a name="target"></a><span data-ttu-id="6295d-120">Destino</span><span class="sxs-lookup"><span data-stu-id="6295d-120">Target</span></span>

<span data-ttu-id="6295d-121">Se llama a la DLL a través del punto de entrada denominado en el campo de destino de la [tabla CustomAction](customaction-table.md), pasando un solo argumento que es el identificador de la sesión de instalación actual.</span><span class="sxs-lookup"><span data-stu-id="6295d-121">The DLL is called through the entry point named in the Target field of the [CustomAction table](customaction-table.md), passing a single argument that is the handle to the current install session.</span></span> <span data-ttu-id="6295d-122">El nombre del punto de entrada especificado en la tabla debe coincidir con el exportado desde el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="6295d-122">The entry point name specified in the table must match that exported from the DLL.</span></span> <span data-ttu-id="6295d-123">Tenga en cuenta que si la función de entrada no se especifica mediante un. Archivo DEF o una especificación/EXPORT: linker, el nombre puede tener un carácter de subrayado inicial y un @4 sufijo "".</span><span class="sxs-lookup"><span data-stu-id="6295d-123">Note that if the entry function is not specified by a .DEF file or by a /EXPORT: linker specification, the name may have a leading underscore and a "@4" suffix.</span></span> <span data-ttu-id="6295d-124">La función llamada debe especificar la \_ \_ Convención de llamada Stdcall.</span><span class="sxs-lookup"><span data-stu-id="6295d-124">The called function must specify the \_\_stdcall calling convention.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="6295d-125">Opciones de procesamiento de valores devueltos</span><span class="sxs-lookup"><span data-stu-id="6295d-125">Return Processing Options</span></span>

<span data-ttu-id="6295d-126">Incluya bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de procesamiento de valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="6295d-126">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="6295d-127">Para obtener una descripción de las opciones y los valores, vea [Opciones de procesamiento de devolución de acción personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="6295d-127">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="6295d-128">Opciones de programación de ejecución</span><span class="sxs-lookup"><span data-stu-id="6295d-128">Execution Scheduling Options</span></span>

<span data-ttu-id="6295d-129">Incluya los bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de programación de la ejecución.</span><span class="sxs-lookup"><span data-stu-id="6295d-129">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="6295d-130">Estas opciones controlan la ejecución múltiple de acciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="6295d-130">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="6295d-131">Para obtener una descripción de las opciones, vea opciones de programación de la [ejecución de acciones personalizadas](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="6295d-131">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="6295d-132">Opciones de ejecución de In-Script</span><span class="sxs-lookup"><span data-stu-id="6295d-132">In-Script Execution Options</span></span>

<span data-ttu-id="6295d-133">Incluya bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar una opción de ejecución en el script.</span><span class="sxs-lookup"><span data-stu-id="6295d-133">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="6295d-134">Estas opciones copian el código de acción en el script de ejecución, reversión o confirmación.</span><span class="sxs-lookup"><span data-stu-id="6295d-134">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="6295d-135">Para obtener una descripción de las opciones, vea [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="6295d-135">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="6295d-136">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="6295d-136">Return Values</span></span>

<span data-ttu-id="6295d-137">Vea [valores devueltos de la acción personalizada](custom-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="6295d-137">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6295d-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6295d-138">Remarks</span></span>

<span data-ttu-id="6295d-139">Una acción personalizada que llama a una biblioteca de vínculos dinámicos (DLL) requiere un identificador para la sesión de instalación.</span><span class="sxs-lookup"><span data-stu-id="6295d-139">A custom action that calls a dynamic-link library (DLL) requires a handle to the installation session.</span></span> <span data-ttu-id="6295d-140">Si esta es también una acción personalizada de ejecución aplazada, es posible que la sesión ya no exista durante la ejecución del script de instalación.</span><span class="sxs-lookup"><span data-stu-id="6295d-140">If this is also a deferred execution custom action, the session may no longer exist during execution of the installation script.</span></span> <span data-ttu-id="6295d-141">Para obtener información sobre cómo una acción personalizada de este tipo puede obtener información de contexto, vea [obtener información de contexto para las acciones personalizadas de ejecución aplazada](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="6295d-141">For information on how a custom action of this type can obtain context information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

<span data-ttu-id="6295d-142">Cuando se exporta una tabla de base de datos, cada secuencia se escribe como un archivo independiente en la subcarpeta con el nombre de la tabla, utilizando la clave principal como el nombre de archivo (columna Name de la tabla binaria), con una extensión predeterminada de ". ibd".</span><span class="sxs-lookup"><span data-stu-id="6295d-142">When a database table is exported, each stream is written as a separate file in the subfolder named after the table, using the primary key as the file name (Name column for the Binary table), with a default extension of ".ibd".</span></span> <span data-ttu-id="6295d-143">El nombre debe usar el formato 8,3 si el sistema de archivos o el sistema de control de versiones no admiten nombres de archivo largos.</span><span class="sxs-lookup"><span data-stu-id="6295d-143">The name should use the 8.3 format if the file system or version control system does not support long file names.</span></span> <span data-ttu-id="6295d-144">El archivo de almacenamiento persistente reemplaza los datos de la secuencia por el nombre de archivo usado, de modo que los datos se pueden encontrar al importar la tabla.</span><span class="sxs-lookup"><span data-stu-id="6295d-144">The persistent archive file replaces the stream data with the file name used, so that the data can be located when the table is imported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6295d-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6295d-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6295d-146">\_Acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="6295d-146">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="6295d-147">Bibliotecas de vínculos dinámicos</span><span class="sxs-lookup"><span data-stu-id="6295d-147">Dynamic-Link Libraries</span></span>](dynamic-link-libraries.md)
</dt> <dt>

[<span data-ttu-id="6295d-148">Obtener información de contexto para las acciones personalizadas de ejecución aplazada</span><span class="sxs-lookup"><span data-stu-id="6295d-148">Obtaining Context Information for Deferred Execution Custom Actions</span></span>](obtaining-context-information-for-deferred-execution-custom-actions.md)
</dt> </dl>

 

 



