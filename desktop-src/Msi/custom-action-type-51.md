---
description: Los desarrolladores de paquetes de Windows Installer pueden optar por usar un tipo de acción personalizada 51 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: cdad16ad-426c-4e04-8003-b32c67be7329
title: Tipo de acción personalizada 51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef3224add3a425131ee3308bc4f610b086cd99a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002565"
---
# <a name="custom-action-type-51"></a><span data-ttu-id="db257-103">Tipo de acción personalizada 51</span><span class="sxs-lookup"><span data-stu-id="db257-103">Custom Action Type 51</span></span>

<span data-ttu-id="db257-104">Esta acción personalizada establece una propiedad a partir de una cadena de texto con formato.</span><span class="sxs-lookup"><span data-stu-id="db257-104">This custom action sets a property from a formatted text string.</span></span>

<span data-ttu-id="db257-105">Para que afecte a una propiedad utilizada en una condición en un componente o característica, la acción personalizada debe estar antes de la [acción CostFinalize](costfinalize-action.md) en la secuencia de acción.</span><span class="sxs-lookup"><span data-stu-id="db257-105">To affect a property used in a condition on a component or feature, the custom action must come before the [CostFinalize action](costfinalize-action.md) in the action sequence.</span></span>

## <a name="source"></a><span data-ttu-id="db257-106">Source</span><span class="sxs-lookup"><span data-stu-id="db257-106">Source</span></span>

<span data-ttu-id="db257-107">El campo de origen de la [tabla CustomAction](customaction-table.md) puede contener el nombre de una propiedad o una clave de la [tabla de propiedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="db257-107">The Source field of the [CustomAction table](customaction-table.md) can contain either the name of a property or a key to the [Property table](property-table.md).</span></span> <span data-ttu-id="db257-108">Esta propiedad se establece mediante la cadena con formato en el campo de destino mediante [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya).</span><span class="sxs-lookup"><span data-stu-id="db257-108">This property is set by the formatted string in the Target field using [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya).</span></span>

## <a name="type-value"></a><span data-ttu-id="db257-109">Valor de tipo</span><span class="sxs-lookup"><span data-stu-id="db257-109">Type Value</span></span>

<span data-ttu-id="db257-110">Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico.</span><span class="sxs-lookup"><span data-stu-id="db257-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="db257-111">Constantes</span><span class="sxs-lookup"><span data-stu-id="db257-111">Constants</span></span>                                                             | <span data-ttu-id="db257-112">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="db257-112">Hexadecimal</span></span> | <span data-ttu-id="db257-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="db257-113">Decimal</span></span> |
|-----------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="db257-114">**msidbCustomActionTypeTextData**  +  **msidbCustomActionTypeProperty**</span><span class="sxs-lookup"><span data-stu-id="db257-114">**msidbCustomActionTypeTextData** + **msidbCustomActionTypeProperty**</span></span> | <span data-ttu-id="db257-115">0x033</span><span class="sxs-lookup"><span data-stu-id="db257-115">0x033</span></span>       | <span data-ttu-id="db257-116">51</span><span class="sxs-lookup"><span data-stu-id="db257-116">51</span></span>      |



 

## <a name="target"></a><span data-ttu-id="db257-117">Destino</span><span class="sxs-lookup"><span data-stu-id="db257-117">Target</span></span>

<span data-ttu-id="db257-118">La columna de destino de la [tabla CustomAction](customaction-table.md) contiene una cadena de texto con el formato de la funcionalidad especificada en [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (sin los especificadores de campo numérico).</span><span class="sxs-lookup"><span data-stu-id="db257-118">The Target column of the [CustomAction table](customaction-table.md) contains a text string formatted using the functionality specified in [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (without the numeric field specifiers).</span></span> <span data-ttu-id="db257-119">Los parámetros que se van a reemplazar se incluyen entre corchetes, \[ ... \] y pueden ser propiedades, variables de entorno (% Prefix), rutas de acceso de archivo ( \# prefijo) o rutas de acceso de directorio de componentes ($ Prefix).</span><span class="sxs-lookup"><span data-stu-id="db257-119">Parameters to be replaced are enclosed in square brackets, \[…\], and may be properties, environment variables (% prefix), file paths (\# prefix), or component directory paths ($ prefix).</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="db257-120">Opciones de procesamiento de valores devueltos</span><span class="sxs-lookup"><span data-stu-id="db257-120">Return Processing Options</span></span>

<span data-ttu-id="db257-121">La acción personalizada no utiliza estas opciones.</span><span class="sxs-lookup"><span data-stu-id="db257-121">The custom action does not use these options.</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="db257-122">Opciones de programación de ejecución</span><span class="sxs-lookup"><span data-stu-id="db257-122">Execution Scheduling Options</span></span>

<span data-ttu-id="db257-123">Incluya los bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de programación de la ejecución.</span><span class="sxs-lookup"><span data-stu-id="db257-123">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="db257-124">Estas opciones controlan la ejecución múltiple de acciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="db257-124">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="db257-125">Para obtener una descripción de las opciones, vea opciones de programación de la [ejecución de acciones personalizadas](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="db257-125">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="db257-126">Opciones de ejecución de In-Script</span><span class="sxs-lookup"><span data-stu-id="db257-126">In-Script Execution Options</span></span>

<span data-ttu-id="db257-127">La acción personalizada no utiliza estas opciones.</span><span class="sxs-lookup"><span data-stu-id="db257-127">The custom action does not use these options.</span></span>

## <a name="return-values"></a><span data-ttu-id="db257-128">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="db257-128">Return Values</span></span>

<span data-ttu-id="db257-129">Vea [valores devueltos de la acción personalizada](custom-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="db257-129">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="db257-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="db257-130">Remarks</span></span>

<span data-ttu-id="db257-131">Si establece una [propiedad privada](private-properties.md) en la secuencia de la interfaz de usuario mediante la creación de una acción personalizada en una de las tablas de secuencia de la interfaz de usuario, esa propiedad no se establece en la secuencia de ejecución.</span><span class="sxs-lookup"><span data-stu-id="db257-131">If you set a [private property](private-properties.md) in the UI sequence by authoring a custom action in one of the user interface sequence tables, that property is not set in the execution sequence.</span></span> <span data-ttu-id="db257-132">Para establecer la propiedad en la secuencia de ejecución, también debe colocar una acción personalizada en una tabla de secuencia de ejecución.</span><span class="sxs-lookup"><span data-stu-id="db257-132">To set the property in the execution sequence, you must also put a custom action in an execution sequence table.</span></span> <span data-ttu-id="db257-133">Como alternativa, puede convertir la propiedad en una [propiedad pública](public-properties.md) e incluirla en la [**propiedad SecureCustomProperties**](securecustomproperties.md).</span><span class="sxs-lookup"><span data-stu-id="db257-133">Alternatively, you can make the property a [public property](public-properties.md) and include it in the [**SecureCustomProperties property**](securecustomproperties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="db257-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="db257-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db257-135">\_Acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="db257-135">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="db257-136">Acciones personalizadas de texto con formato</span><span class="sxs-lookup"><span data-stu-id="db257-136">Formatted Text Custom Actions</span></span>](formatted-text-custom-actions.md)
</dt> </dl>

 

 



