---
description: Los desarrolladores de paquetes de Windows Installer pueden optar por usar un tipo de acción personalizada 35 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: b88b5f48-5353-4876-9dda-2eeda288fa4b
title: Tipo de acción personalizada 35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8401f26f40ccc7de811ea0d290d556789284680f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669749"
---
# <a name="custom-action-type-35"></a><span data-ttu-id="43062-103">Tipo de acción personalizada 35</span><span class="sxs-lookup"><span data-stu-id="43062-103">Custom Action Type 35</span></span>

<span data-ttu-id="43062-104">Esta acción personalizada establece el directorio de instalación desde una cadena de texto con formato.</span><span class="sxs-lookup"><span data-stu-id="43062-104">This custom action sets the install directory from a formatted text string.</span></span> <span data-ttu-id="43062-105">Para obtener más información, consulte [cambiar la ubicación de destino de un directorio](changing-the-target-location-for-a-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="43062-105">For more information, see [Changing the Target Location for a Directory](changing-the-target-location-for-a-directory.md)</span></span>

## <a name="source"></a><span data-ttu-id="43062-106">Source</span><span class="sxs-lookup"><span data-stu-id="43062-106">Source</span></span>

<span data-ttu-id="43062-107">El campo de origen de la [tabla CustomAction](customaction-table.md) contiene una clave para la [tabla de directorios](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="43062-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Directory table](directory-table.md).</span></span> <span data-ttu-id="43062-108">El directorio designado se establece mediante la cadena con formato en el campo de destino mediante [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha).</span><span class="sxs-lookup"><span data-stu-id="43062-108">The designated directory is set by the formatted string in the Target field using [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha).</span></span> <span data-ttu-id="43062-109">Esto establece la ruta de acceso de destino y la propiedad asociada en el valor expandido de la cadena de texto con formato en el campo de destino.</span><span class="sxs-lookup"><span data-stu-id="43062-109">This sets the target path and associated property to the expanded value of the formatted text string in the Target field.</span></span> <span data-ttu-id="43062-110">No intente cambiar la ubicación de un directorio de destino durante una [instalación de mantenimiento](maintenance-installation.md).</span><span class="sxs-lookup"><span data-stu-id="43062-110">Do not attempt to change the location of a target directory during a [maintenance installation](maintenance-installation.md).</span></span> <span data-ttu-id="43062-111">No intente cambiar la ruta de acceso del directorio de destino si algunos componentes que usan esa ruta de acceso ya están instalados para cualquier usuario.</span><span class="sxs-lookup"><span data-stu-id="43062-111">Do not attempt to change the target directory path if some components using that path are already installed for any user.</span></span>

## <a name="type-value"></a><span data-ttu-id="43062-112">Valor de tipo</span><span class="sxs-lookup"><span data-stu-id="43062-112">Type Value</span></span>

<span data-ttu-id="43062-113">Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico.</span><span class="sxs-lookup"><span data-stu-id="43062-113">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="43062-114">Constantes</span><span class="sxs-lookup"><span data-stu-id="43062-114">Constants</span></span>                                                              | <span data-ttu-id="43062-115">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="43062-115">Hexadecimal</span></span> | <span data-ttu-id="43062-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="43062-116">Decimal</span></span> |
|------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="43062-117">**msidbCustomActionTypeTextData**  +  **msidbCustomActionTypeDirectory**</span><span class="sxs-lookup"><span data-stu-id="43062-117">**msidbCustomActionTypeTextData** + **msidbCustomActionTypeDirectory**</span></span> | <span data-ttu-id="43062-118">0x023</span><span class="sxs-lookup"><span data-stu-id="43062-118">0x023</span></span>       | <span data-ttu-id="43062-119">35</span><span class="sxs-lookup"><span data-stu-id="43062-119">35</span></span>      |



 

## <a name="target"></a><span data-ttu-id="43062-120">Destino</span><span class="sxs-lookup"><span data-stu-id="43062-120">Target</span></span>

<span data-ttu-id="43062-121">La columna de destino de la [tabla CustomAction](customaction-table.md) contiene una cadena de texto con el formato de la funcionalidad especificada en [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (sin los especificadores de campo numérico).</span><span class="sxs-lookup"><span data-stu-id="43062-121">The Target column of the [CustomAction table](customaction-table.md) contains a text string formatted using the functionality specified in [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (without the numeric field specifiers).</span></span> <span data-ttu-id="43062-122">Los parámetros que se van a reemplazar se incluyen entre corchetes \[ ... \] y pueden ser propiedades, variables de entorno (% Prefix), rutas de acceso de archivo ( \# prefijo) o rutas de acceso del directorio de componentes ($ Prefix).</span><span class="sxs-lookup"><span data-stu-id="43062-122">Parameters to be replaced are enclosed in square brackets \[…\], and may be properties, environment variables (% prefix), file paths (\# prefix), or component directory paths ($ prefix).</span></span> <span data-ttu-id="43062-123">Tenga en cuenta que las rutas de acceso de directorio siempre finalizan con un separador de directorios.</span><span class="sxs-lookup"><span data-stu-id="43062-123">Note that directory paths always end with a directory separator.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="43062-124">Opciones de procesamiento de valores devueltos</span><span class="sxs-lookup"><span data-stu-id="43062-124">Return Processing Options</span></span>

<span data-ttu-id="43062-125">La acción personalizada no utiliza estas opciones.</span><span class="sxs-lookup"><span data-stu-id="43062-125">The custom action does not use these options.</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="43062-126">Opciones de programación de ejecución</span><span class="sxs-lookup"><span data-stu-id="43062-126">Execution Scheduling Options</span></span>

<span data-ttu-id="43062-127">Incluya los bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de programación de la ejecución.</span><span class="sxs-lookup"><span data-stu-id="43062-127">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="43062-128">Estas opciones controlan la ejecución múltiple de acciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="43062-128">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="43062-129">Para obtener una descripción de las opciones, vea opciones de programación de la [ejecución de acciones personalizadas](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="43062-129">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="43062-130">Opciones de ejecución de In-Script</span><span class="sxs-lookup"><span data-stu-id="43062-130">In-Script Execution Options</span></span>

<span data-ttu-id="43062-131">La acción personalizada no utiliza estas opciones.</span><span class="sxs-lookup"><span data-stu-id="43062-131">The custom action does not use these options.</span></span>

## <a name="return-values"></a><span data-ttu-id="43062-132">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="43062-132">Return Values</span></span>

<span data-ttu-id="43062-133">Vea [valores devueltos de la acción personalizada](custom-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="43062-133">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="43062-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="43062-134">Remarks</span></span>

<span data-ttu-id="43062-135">Si establece una [propiedad privada](private-properties.md) en la secuencia de la interfaz de usuario mediante la creación de una acción personalizada en una de las tablas de secuencia de la interfaz de usuario, esa propiedad no se establece en la secuencia de ejecución.</span><span class="sxs-lookup"><span data-stu-id="43062-135">If you set a [private property](private-properties.md) in the UI sequence by authoring a custom action in one of the user interface sequence tables, that property is not set in the execution sequence.</span></span> <span data-ttu-id="43062-136">Para establecer la propiedad en la secuencia de ejecución, también debe colocar una acción personalizada en una tabla de secuencia de ejecución.</span><span class="sxs-lookup"><span data-stu-id="43062-136">To set the property in the execution sequence you must also put a custom action in an execution sequence table.</span></span> <span data-ttu-id="43062-137">Como alternativa, puede convertir la propiedad en una [propiedad pública](public-properties.md) e incluirla en la [**propiedad SecureCustomProperties**](securecustomproperties.md).</span><span class="sxs-lookup"><span data-stu-id="43062-137">Alternatively, you can make the property a [public property](public-properties.md) and include it in the [**SecureCustomProperties property**](securecustomproperties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="43062-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="43062-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43062-139">\_Acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="43062-139">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="43062-140">Acciones personalizadas de texto con formato</span><span class="sxs-lookup"><span data-stu-id="43062-140">Formatted Text Custom Actions</span></span>](formatted-text-custom-actions.md)
</dt> </dl>

 

 



