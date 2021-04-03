---
description: Los desarrolladores de paquetes de Windows Installer pueden optar por usar una acción personalizada tipo 23 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: 8219f157-585d-4733-8e10-c05813b398ba
title: Tipo de acción personalizada 23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05576c44ab634dc117501a89e6b86594f5483458
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913870"
---
# <a name="custom-action-type-23"></a><span data-ttu-id="40926-103">Tipo de acción personalizada 23</span><span class="sxs-lookup"><span data-stu-id="40926-103">Custom Action Type 23</span></span>

<span data-ttu-id="40926-104">El tipo de acción personalizada 23 se usa con instalaciones simultáneas.</span><span class="sxs-lookup"><span data-stu-id="40926-104">The Custom Action Type 23 is used with concurrent installations.</span></span> <span data-ttu-id="40926-105">No se recomiendan instalaciones simultáneas para la instalación de aplicaciones destinadas a publicarse en el público.</span><span class="sxs-lookup"><span data-stu-id="40926-105">Concurrent installations are not recommended for the installation of applications intended for release to the public.</span></span> <span data-ttu-id="40926-106">Para obtener información acerca de las instalaciones simultáneas, consulte [instalaciones](concurrent-installations.md)simultáneas.</span><span class="sxs-lookup"><span data-stu-id="40926-106">For information about concurrent installations please see [Concurrent Installations](concurrent-installations.md).</span></span>

<span data-ttu-id="40926-107">Esta acción personalizada instala otro paquete del instalador que reside en el árbol de origen de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="40926-107">This custom action installs another installer package that resides in the application's source tree.</span></span>

## <a name="source"></a><span data-ttu-id="40926-108">Source</span><span class="sxs-lookup"><span data-stu-id="40926-108">Source</span></span>

<span data-ttu-id="40926-109">La ubicación del paquete de instalación simultánea se especifica en relación con la raíz de la ubicación de origen que se muestra en el campo origen de la [tabla CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="40926-109">The location of the concurrent installation package is specified relative to the root of the source location shown in the Source field of the [CustomAction table](customaction-table.md).</span></span>

## <a name="numeric-type"></a><span data-ttu-id="40926-110">Tipo numérico</span><span class="sxs-lookup"><span data-stu-id="40926-110">Numeric Type</span></span>



| <span data-ttu-id="40926-111">Nombre de tipo</span><span class="sxs-lookup"><span data-stu-id="40926-111">Type name</span></span>                                                      | <span data-ttu-id="40926-112">Value</span><span class="sxs-lookup"><span data-stu-id="40926-112">Value</span></span> |
|----------------------------------------------------------------|-------|
| <span data-ttu-id="40926-113">msidbCustomActionTypeInstall + msidbCustomActionTypeSourceFile</span><span class="sxs-lookup"><span data-stu-id="40926-113">msidbCustomActionTypeInstall + msidbCustomActionTypeSourceFile</span></span> | <span data-ttu-id="40926-114">23</span><span class="sxs-lookup"><span data-stu-id="40926-114">23</span></span>    |



 

## <a name="target"></a><span data-ttu-id="40926-115">Destino</span><span class="sxs-lookup"><span data-stu-id="40926-115">Target</span></span>

<span data-ttu-id="40926-116">El campo de destino de la [tabla CustomAction](customaction-table.md) contiene valores de propiedades que se van a pasar a la instalación simultánea.</span><span class="sxs-lookup"><span data-stu-id="40926-116">The Target field of the [CustomAction table](customaction-table.md) contains property settings that are to be passed to the concurrent installation.</span></span> <span data-ttu-id="40926-117">Estos valores de propiedades pueden especificar características.</span><span class="sxs-lookup"><span data-stu-id="40926-117">These property settings can specify features.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="40926-118">Opciones de procesamiento de valores devueltos</span><span class="sxs-lookup"><span data-stu-id="40926-118">Return Processing Options</span></span>

<span data-ttu-id="40926-119">La sesión de instalación simultánea se ejecuta como un subproceso independiente en el proceso actual.</span><span class="sxs-lookup"><span data-stu-id="40926-119">The concurrent installation session runs as a separate thread in the current process.</span></span> <span data-ttu-id="40926-120">Una instalación simultánea no se puede ejecutar de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="40926-120">A concurrent installation cannot run asynchronously.</span></span>

<span data-ttu-id="40926-121">Para obtener más información, vea [Opciones de procesamiento de devoluciones de acciones personalizadas](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="40926-121">For more information, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="40926-122">Opciones de programación de ejecución</span><span class="sxs-lookup"><span data-stu-id="40926-122">Execution Scheduling Options</span></span>

<span data-ttu-id="40926-123">Las marcas de opciones están disponibles para controlar la posible ejecución múltiple de acciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="40926-123">Options flags are available to control the potential multiple execution of custom actions.</span></span> <span data-ttu-id="40926-124">Para obtener más información, consulte Opciones de programación de la [ejecución de acciones personalizadas](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="40926-124">For more information, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="40926-125">Opciones de ejecución de In-Script</span><span class="sxs-lookup"><span data-stu-id="40926-125">In-Script Execution Options</span></span>

<span data-ttu-id="40926-126">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="40926-126">Not used.</span></span>

## <a name="return-values"></a><span data-ttu-id="40926-127">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="40926-127">Return Values</span></span>

<span data-ttu-id="40926-128">El estado de retorno de usuario Exit, error, Suspend o Success desde una instalación simultánea se procesa de la misma manera que cualquier otra acción.</span><span class="sxs-lookup"><span data-stu-id="40926-128">The return status of user exit, failure, suspend, or success from a concurrent installation is processed in the same way as any other action.</span></span> <span data-ttu-id="40926-129">Sin embargo, tenga en cuenta que Windows Installer traduce los valores devueltos de todas las acciones cuando escribe el valor devuelto en el archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="40926-129">Note however, that Windows Installer translates the return values from all actions when it writes the return value into the log file.</span></span> <span data-ttu-id="40926-130">Por ejemplo, si el valor devuelto de la acción aparece como 1 en el archivo de registro, significa que la acción devolvió un ERROR de \_ éxito.</span><span class="sxs-lookup"><span data-stu-id="40926-130">For example, if the action return value appears as 1 in the log file, this means that the action returned ERROR\_SUCCESS.</span></span> <span data-ttu-id="40926-131">Para obtener más información, vea [registro de valores devueltos de acción](logging-of-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="40926-131">For more information, see [Logging of Action Return Values](logging-of-action-return-values.md).</span></span>

<span data-ttu-id="40926-132">Tenga en cuenta que si se establece **msidbCustomActionTypeContinue** en una instalación simultánea, se reiniciará un error de instalación de \_ \_ USEREXIT, error de \_ instalación de \_ reinicio, error al reiniciar el proceso de \_ instalación \_ \_ , o \_ \_ se requiere un reinicio correcto \_ \_ para el error.</span><span class="sxs-lookup"><span data-stu-id="40926-132">Note that if a concurrent installation has **msidbCustomActionTypeContinue** set, then a return of ERROR\_INSTALL\_USEREXIT, ERROR\_INSTALL\_REBOOT, ERROR\_INSTALL\_REBOOT\_NOW, or ERROR\_SUCCESS\_REBOOT\_REQUIRED is treated as ERROR\_SUCCESS.</span></span> <span data-ttu-id="40926-133">Esto significa que si establece **msidbCustomActionTypeContinue** y la instalación simultánea requiere un reinicio, se omitirá el requisito del reinicio.</span><span class="sxs-lookup"><span data-stu-id="40926-133">This means that if you set **msidbCustomActionTypeContinue** and your concurrent installation requires a restart, the requirement for the restart will be ignored.</span></span> <span data-ttu-id="40926-134">Además, se omitirá el código de error de la acción personalizada de instalación simultánea.</span><span class="sxs-lookup"><span data-stu-id="40926-134">Additionally, the error code from the concurrent installation custom action will be ignored.</span></span>

<span data-ttu-id="40926-135">Si no se establece **msidbCustomActionTypeContinue** , los siguientes códigos de retorno \_ y error correcto se tratan como correctos y tienen los significados siguientes.</span><span class="sxs-lookup"><span data-stu-id="40926-135">If **msidbCustomActionTypeContinue** is not set, the following return codes plus ERROR\_SUCCESS are treated as success and have the following meanings.</span></span> <span data-ttu-id="40926-136">Otros códigos de retorno se tratan como errores.</span><span class="sxs-lookup"><span data-stu-id="40926-136">Other return codes are treated as failure.</span></span>



| <span data-ttu-id="40926-137">Mensaje</span><span class="sxs-lookup"><span data-stu-id="40926-137">Message</span></span>                          | <span data-ttu-id="40926-138">Significado</span><span class="sxs-lookup"><span data-stu-id="40926-138">Meaning</span></span>                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40926-139">ERROR de \_ instalación de \_ reinicio</span><span class="sxs-lookup"><span data-stu-id="40926-139">ERROR\_INSTALL\_REBOOT</span></span>           | <span data-ttu-id="40926-140">La marca de reinicio se establecerá para reiniciarse al final de la instalación.</span><span class="sxs-lookup"><span data-stu-id="40926-140">The restart flag will be set to restart at end of the installation.</span></span>                                  |
| <span data-ttu-id="40926-141">ERROR \_ al \_ reiniciar \_ ahora</span><span class="sxs-lookup"><span data-stu-id="40926-141">ERROR\_INSTALL\_REBOOT\_NOW</span></span>      | <span data-ttu-id="40926-142">Se requiere un reinicio antes de completar la instalación.</span><span class="sxs-lookup"><span data-stu-id="40926-142">A restart is required before completing the installation.</span></span> <span data-ttu-id="40926-143">El reinicio se procesará inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="40926-143">The restart will be processed immediately.</span></span> |
| <span data-ttu-id="40926-144">ERROR \_ de \_ reinicio correcto \_ necesario</span><span class="sxs-lookup"><span data-stu-id="40926-144">ERROR\_SUCCESS\_REBOOT\_REQUIRED</span></span> | <span data-ttu-id="40926-145">Se requiere un reinicio, pero se suprime.</span><span class="sxs-lookup"><span data-stu-id="40926-145">A restart was required, but was suppressed.</span></span>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="40926-146">Observaciones</span><span class="sxs-lookup"><span data-stu-id="40926-146">Remarks</span></span>

<span data-ttu-id="40926-147">Se requiere una expresión condicional para habilitar la instalación simultánea en la instalación o desinstalación del componente o característica asociados.</span><span class="sxs-lookup"><span data-stu-id="40926-147">A conditional expression is required to enable the concurrent installation at either installation or removal of the associated component or feature.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40926-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="40926-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40926-149">Instalaciones simultáneas</span><span class="sxs-lookup"><span data-stu-id="40926-149">Concurrent Installations</span></span>](concurrent-installations.md)
</dt> <dt>

[<span data-ttu-id="40926-150">Referencia de acción personalizada</span><span class="sxs-lookup"><span data-stu-id="40926-150">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="40926-151">Acerca de las acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="40926-151">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="40926-152">Uso de acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="40926-152">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="40926-153">Valores devueltos de la acción personalizada</span><span class="sxs-lookup"><span data-stu-id="40926-153">Custom Action Return Values</span></span>](custom-action-return-values.md)
</dt> </dl>

 

 



