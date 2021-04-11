---
description: Los desarrolladores de paquetes de Windows Installer pueden optar por usar una acción personalizada tipo 7 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: 4a8f35f9-58a8-417e-b72e-159f4af7d83f
title: Tipo de acción personalizada 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d3cc1c68fae098c6ef70797ed87df887ff898a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082787"
---
# <a name="custom-action-type-7"></a><span data-ttu-id="f9151-103">Tipo de acción personalizada 7</span><span class="sxs-lookup"><span data-stu-id="f9151-103">Custom Action Type 7</span></span>

<span data-ttu-id="f9151-104">El tipo de acción personalizada 7 se usa con instalaciones simultáneas.</span><span class="sxs-lookup"><span data-stu-id="f9151-104">The Custom Action Type 7 is used with concurrent installations.</span></span> <span data-ttu-id="f9151-105">No se recomiendan instalaciones simultáneas para la instalación de aplicaciones destinadas a publicarse en el público.</span><span class="sxs-lookup"><span data-stu-id="f9151-105">Concurrent installations are not recommended for the installation of applications intended for release to the public.</span></span> <span data-ttu-id="f9151-106">Para obtener más información acerca de las instalaciones simultáneas, consulte [instalaciones simultáneas](concurrent-installations.md).</span><span class="sxs-lookup"><span data-stu-id="f9151-106">For more information about concurrent installations please see [Concurrent Installations](concurrent-installations.md).</span></span>

<span data-ttu-id="f9151-107">Esta acción personalizada instala otro paquete del instalador que está anidado dentro del primer paquete.</span><span class="sxs-lookup"><span data-stu-id="f9151-107">This custom action installs another installer package that is nested inside of the first package.</span></span>

## <a name="source"></a><span data-ttu-id="f9151-108">Source</span><span class="sxs-lookup"><span data-stu-id="f9151-108">Source</span></span>

<span data-ttu-id="f9151-109">La base de datos de la aplicación simultánea se almacena como un subalmacenamiento del paquete y el nombre del subalmacenamiento se designa en el campo origen de la [tabla CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="f9151-109">The database of the concurrent application is stored as a substorage of the package, and the name of the substorage is designated in the Source field of the [CustomAction table](customaction-table.md).</span></span>

## <a name="numeric-type"></a><span data-ttu-id="f9151-110">Tipo numérico</span><span class="sxs-lookup"><span data-stu-id="f9151-110">Numeric Type</span></span>



| <span data-ttu-id="f9151-111">Nombre de tipo</span><span class="sxs-lookup"><span data-stu-id="f9151-111">Type name</span></span>                                                      | <span data-ttu-id="f9151-112">Value</span><span class="sxs-lookup"><span data-stu-id="f9151-112">Value</span></span> |
|----------------------------------------------------------------|-------|
| <span data-ttu-id="f9151-113">msidbCustomActionTypeInstall + msidbCustomActionTypeBinaryData</span><span class="sxs-lookup"><span data-stu-id="f9151-113">msidbCustomActionTypeInstall + msidbCustomActionTypeBinaryData</span></span> | <span data-ttu-id="f9151-114">7</span><span class="sxs-lookup"><span data-stu-id="f9151-114">7</span></span>     |



 

## <a name="target"></a><span data-ttu-id="f9151-115">Destino</span><span class="sxs-lookup"><span data-stu-id="f9151-115">Target</span></span>

<span data-ttu-id="f9151-116">El campo de destino de la [tabla CustomAction](customaction-table.md) contiene los valores de propiedades que se van a pasar a la instalación simultánea.</span><span class="sxs-lookup"><span data-stu-id="f9151-116">The Target field of the [CustomAction table](customaction-table.md) contains property settings to be passed to the concurrent installation.</span></span> <span data-ttu-id="f9151-117">Estos valores de propiedades pueden especificar características.</span><span class="sxs-lookup"><span data-stu-id="f9151-117">These property settings can specify features.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="f9151-118">Opciones de procesamiento de valores devueltos</span><span class="sxs-lookup"><span data-stu-id="f9151-118">Return Processing Options</span></span>

<span data-ttu-id="f9151-119">La sesión de instalación simultánea se ejecuta como un subproceso independiente en el proceso actual.</span><span class="sxs-lookup"><span data-stu-id="f9151-119">The concurrent installation session runs as a separate thread in the current process.</span></span> <span data-ttu-id="f9151-120">Una instalación simultánea no se puede ejecutar de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="f9151-120">A concurrent installation cannot run asynchronously.</span></span>

<span data-ttu-id="f9151-121">Vea [Opciones de procesamiento de devolución de acción personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="f9151-121">See [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="f9151-122">Opciones de programación de ejecución</span><span class="sxs-lookup"><span data-stu-id="f9151-122">Execution Scheduling Options</span></span>

<span data-ttu-id="f9151-123">Las marcas de opciones están disponibles para controlar la posible ejecución múltiple de acciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="f9151-123">Options flags are available to control the potential multiple execution of custom actions.</span></span> <span data-ttu-id="f9151-124">Consulte [Opciones de programación de la ejecución de acciones personalizadas](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="f9151-124">See [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="f9151-125">Opciones de ejecución de In-Script</span><span class="sxs-lookup"><span data-stu-id="f9151-125">In-Script Execution Options</span></span>

<span data-ttu-id="f9151-126">Esta acción personalizada no usa esta opción.</span><span class="sxs-lookup"><span data-stu-id="f9151-126">This custom action does not use this option.</span></span>

## <a name="return-values"></a><span data-ttu-id="f9151-127">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="f9151-127">Return Values</span></span>

<span data-ttu-id="f9151-128">El estado de retorno de usuario Exit, error, Suspend o Success desde una instalación simultánea se procesa de la misma manera que cualquier otra acción.</span><span class="sxs-lookup"><span data-stu-id="f9151-128">The return status of user exit, failure, suspend, or success from a concurrent installation is processed in the same way as any other action.</span></span> <span data-ttu-id="f9151-129">Sin embargo, tenga en cuenta que Windows Installer traduce los valores devueltos de todas las acciones cuando escribe el valor devuelto en el archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="f9151-129">Note however that Windows Installer translates the return values from all actions when it writes the return value into the log file.</span></span> <span data-ttu-id="f9151-130">Por ejemplo, si el valor devuelto de la acción aparece como 1 en el archivo de registro, significa que la acción devolvió un ERROR de \_ éxito.</span><span class="sxs-lookup"><span data-stu-id="f9151-130">For example, if the action return value appears as 1 in the log file, this means that the action returned ERROR\_SUCCESS.</span></span> <span data-ttu-id="f9151-131">Para obtener más información sobre esta traducción, consulte [registro de valores devueltos de acciones](logging-of-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="f9151-131">For more information about this translation see [Logging of Action Return Values](logging-of-action-return-values.md).</span></span>

<span data-ttu-id="f9151-132">Tenga en cuenta que si se ha establecido **msidbCustomActionTypeContinue** en una instalación simultánea, se devuelve un error de \_ instalación de \_ USEREXIT, error de \_ instalación de reinicio, error al reiniciar el proceso de instalación \_ \_ \_ \_ o error de \_ \_ reinicio correcto \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f9151-132">Note that if a concurrent install has **msidbCustomActionTypeContinue** set, then a return of ERROR\_INSTALL\_USEREXIT, ERROR\_INSTALL\_REBOOT, ERROR\_INSTALL\_REBOOT\_NOW, or ERROR\_SUCCESS\_REBOOT\_REQUIRED is treated as ERROR\_SUCCESS.</span></span> <span data-ttu-id="f9151-133">Esto significa que si establece **msidbCustomActionTypeContinue** y la instalación simultánea requiere un reinicio, se omitirá el requisito del reinicio.</span><span class="sxs-lookup"><span data-stu-id="f9151-133">This means that if you set **msidbCustomActionTypeContinue** and your concurrent installation requires a restart, the requirement for the restart will be ignored.</span></span> <span data-ttu-id="f9151-134">Además, se omitirá el código de error de la acción personalizada de instalación simultánea.</span><span class="sxs-lookup"><span data-stu-id="f9151-134">Additionally, the error code from the concurrent installation custom action will be ignored.</span></span>

<span data-ttu-id="f9151-135">Si no se establece **msidbCustomActionTypeContinue** , los siguientes códigos de retorno \_ y error correcto se tratan como correctos y tienen los significados siguientes.</span><span class="sxs-lookup"><span data-stu-id="f9151-135">If **msidbCustomActionTypeContinue** is not set, the following return codes plus ERROR\_SUCCESS are treated as success and have the following meanings.</span></span> <span data-ttu-id="f9151-136">Otros códigos de retorno se tratan como errores.</span><span class="sxs-lookup"><span data-stu-id="f9151-136">Other return codes are treated as failure.</span></span>



| <span data-ttu-id="f9151-137">Mensaje</span><span class="sxs-lookup"><span data-stu-id="f9151-137">Message</span></span>                          | <span data-ttu-id="f9151-138">Significado</span><span class="sxs-lookup"><span data-stu-id="f9151-138">Meaning</span></span>                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9151-139">ERROR de \_ instalación de \_ reinicio</span><span class="sxs-lookup"><span data-stu-id="f9151-139">ERROR\_INSTALL\_REBOOT</span></span>           | <span data-ttu-id="f9151-140">La marca de reinicio se establecerá para reiniciarse al final de la instalación.</span><span class="sxs-lookup"><span data-stu-id="f9151-140">The restart flag will be set to restart at end of the installation.</span></span>                                  |
| <span data-ttu-id="f9151-141">ERROR \_ al \_ reiniciar \_ ahora</span><span class="sxs-lookup"><span data-stu-id="f9151-141">ERROR\_INSTALL\_REBOOT\_NOW</span></span>      | <span data-ttu-id="f9151-142">Se requiere un reinicio antes de completar la instalación.</span><span class="sxs-lookup"><span data-stu-id="f9151-142">A restart is required before completing the installation.</span></span> <span data-ttu-id="f9151-143">El reinicio se procesará inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="f9151-143">The restart will be processed immediately.</span></span> |
| <span data-ttu-id="f9151-144">ERROR \_ de \_ reinicio correcto \_ necesario</span><span class="sxs-lookup"><span data-stu-id="f9151-144">ERROR\_SUCCESS\_REBOOT\_REQUIRED</span></span> | <span data-ttu-id="f9151-145">Se requiere un reinicio, pero se suprime.</span><span class="sxs-lookup"><span data-stu-id="f9151-145">A restart was required, but was suppressed.</span></span>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="f9151-146">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9151-146">Remarks</span></span>

<span data-ttu-id="f9151-147">Se requiere una expresión condicional para habilitar la instalación simultánea en la instalación o desinstalación del componente o característica asociados.</span><span class="sxs-lookup"><span data-stu-id="f9151-147">A conditional expression is required to enable the concurrent installation at either installation or removal of the associated component or feature.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9151-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f9151-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9151-149">Instalaciones simultáneas</span><span class="sxs-lookup"><span data-stu-id="f9151-149">Concurrent Installations</span></span>](concurrent-installations.md)
</dt> <dt>

[<span data-ttu-id="f9151-150">Referencia de acción personalizada</span><span class="sxs-lookup"><span data-stu-id="f9151-150">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="f9151-151">Acerca de las acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="f9151-151">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="f9151-152">Uso de acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="f9151-152">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="f9151-153">Valores devueltos de la acción personalizada</span><span class="sxs-lookup"><span data-stu-id="f9151-153">Custom Action Return Values</span></span>](custom-action-return-values.md)
</dt> </dl>

 

 



