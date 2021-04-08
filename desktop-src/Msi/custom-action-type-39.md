---
description: Los desarrolladores de paquetes de Windows Installer pueden optar por usar un tipo de acción personalizada 39 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: edf96cc6-ef32-4660-b4ee-50c130626e15
title: Tipo de acción personalizada 39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e49667fbad6e71aa8b2197b00ae9dd49f7dfff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910709"
---
# <a name="custom-action-type-39"></a><span data-ttu-id="8fc3d-103">Tipo de acción personalizada 39</span><span class="sxs-lookup"><span data-stu-id="8fc3d-103">Custom Action Type 39</span></span>

<span data-ttu-id="8fc3d-104">El tipo de acción personalizada 39 se usa con instalaciones simultáneas.</span><span class="sxs-lookup"><span data-stu-id="8fc3d-104">The Custom Action Type 39 is used with concurrent installations.</span></span> <span data-ttu-id="8fc3d-105">No se recomiendan instalaciones simultáneas para la instalación de aplicaciones destinadas a publicarse en el público.</span><span class="sxs-lookup"><span data-stu-id="8fc3d-105">Concurrent installations are not recommended for the installation of applications intended for release to the public.</span></span> <span data-ttu-id="8fc3d-106">Para obtener información acerca de las instalaciones simultáneas, consulte [instalaciones](concurrent-installations.md)simultáneas.</span><span class="sxs-lookup"><span data-stu-id="8fc3d-106">For information about concurrent installations please see [Concurrent Installations](concurrent-installations.md).</span></span>

<span data-ttu-id="8fc3d-107">La acción personalizada Type 39 instala una aplicación anunciada o ya instalada.</span><span class="sxs-lookup"><span data-stu-id="8fc3d-107">Type 39 custom action installs an application that is advertised or already installed.</span></span> <span data-ttu-id="8fc3d-108">Este tipo de acción personalizada se puede usar para reinstalar o quitar un producto que el paquete de instalación del producto actual ha instalado como una instalación simultánea.</span><span class="sxs-lookup"><span data-stu-id="8fc3d-108">This custom action type may be used to reinstall or remove a product that has been installed as a concurrent installation by the current product's installation package.</span></span> <span data-ttu-id="8fc3d-109">La acción personalizada Type 39 no se puede usar para reinstalar o quitar ningún producto instalado previamente por otros medios.</span><span class="sxs-lookup"><span data-stu-id="8fc3d-109">The Type 39 custom action cannot be used to reinstall or remove any product previously installed by any other means.</span></span> <span data-ttu-id="8fc3d-110">Por ejemplo, si el producto secundario se instala mediante un tipo 39, el tipo 23 o la acción personalizada tipo 7 durante la instalación del producto principal, se puede usar una acción personalizada tipo 39 para quitar el producto secundario cuando se desinstale el producto principal.</span><span class="sxs-lookup"><span data-stu-id="8fc3d-110">For example, if the secondary product is installed using a Type 39, Type 23, or Type 7 custom action during the installation of the primary product, a Type 39 custom action may be used to remove the secondary product when the primary product is uninstalled.</span></span>

## <a name="source"></a><span data-ttu-id="8fc3d-111">Source</span><span class="sxs-lookup"><span data-stu-id="8fc3d-111">Source</span></span>

<span data-ttu-id="8fc3d-112">El campo de origen de la [tabla CustomAction](customaction-table.md) contiene el código de producto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8fc3d-112">The Source field of the [CustomAction table](customaction-table.md) contains the product code for the application.</span></span>

## <a name="numeric-type"></a><span data-ttu-id="8fc3d-113">Tipo numérico</span><span class="sxs-lookup"><span data-stu-id="8fc3d-113">Numeric Type</span></span>



| <span data-ttu-id="8fc3d-114">Nombre de tipo</span><span class="sxs-lookup"><span data-stu-id="8fc3d-114">Type name</span></span>                                                     | <span data-ttu-id="8fc3d-115">Value</span><span class="sxs-lookup"><span data-stu-id="8fc3d-115">Value</span></span> |
|---------------------------------------------------------------|-------|
| <span data-ttu-id="8fc3d-116">msidbCustomActionTypeInstall + msidbCustomActionTypeDirectory</span><span class="sxs-lookup"><span data-stu-id="8fc3d-116">msidbCustomActionTypeInstall + msidbCustomActionTypeDirectory</span></span> | <span data-ttu-id="8fc3d-117">39</span><span class="sxs-lookup"><span data-stu-id="8fc3d-117">39</span></span>    |



 

## <a name="target"></a><span data-ttu-id="8fc3d-118">Destino</span><span class="sxs-lookup"><span data-stu-id="8fc3d-118">Target</span></span>

<span data-ttu-id="8fc3d-119">El campo de destino de la [tabla CustomAction](customaction-table.md) contiene valores de propiedades que se van a pasar a la instalación simultánea.</span><span class="sxs-lookup"><span data-stu-id="8fc3d-119">The Target field of the [CustomAction table](customaction-table.md) contains property settings that are to be passed to the concurrent installation.</span></span> <span data-ttu-id="8fc3d-120">Estos valores de propiedades pueden especificar características.</span><span class="sxs-lookup"><span data-stu-id="8fc3d-120">These property settings can specify features.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="8fc3d-121">Opciones de procesamiento de valores devueltos</span><span class="sxs-lookup"><span data-stu-id="8fc3d-121">Return Processing Options</span></span>

<span data-ttu-id="8fc3d-122">Se produce un error en el tipo de acción personalizada 39 si la aplicación no se anuncia ni se instala.</span><span class="sxs-lookup"><span data-stu-id="8fc3d-122">The custom action type 39 fails if the application is not advertised or installed.</span></span> <span data-ttu-id="8fc3d-123">Para evitar este error, debe establecer **msidbCustomActionTypeContinueflag**.</span><span class="sxs-lookup"><span data-stu-id="8fc3d-123">To avoid this failure, you must set the **msidbCustomActionTypeContinueflag**.</span></span>

<span data-ttu-id="8fc3d-124">Una instalación simultánea no se puede ejecutar de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="8fc3d-124">A concurrent install cannot run asynchronously.</span></span>

<span data-ttu-id="8fc3d-125">Vea [Opciones de procesamiento de devolución de acción personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="8fc3d-125">See [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="8fc3d-126">Opciones de programación de ejecución</span><span class="sxs-lookup"><span data-stu-id="8fc3d-126">Execution Scheduling Options</span></span>

<span data-ttu-id="8fc3d-127">Las marcas de opciones están disponibles para controlar la posible ejecución múltiple de acciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="8fc3d-127">Options flags are available to control the potential multiple execution of custom actions.</span></span> <span data-ttu-id="8fc3d-128">Consulte [Opciones de programación de la ejecución de acciones personalizadas](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="8fc3d-128">See [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="8fc3d-129">Opciones de ejecución de In-Script</span><span class="sxs-lookup"><span data-stu-id="8fc3d-129">In-Script Execution Options</span></span>

<span data-ttu-id="8fc3d-130">La acción personalizada no usa esta opción.</span><span class="sxs-lookup"><span data-stu-id="8fc3d-130">The custom action does not use this option.</span></span>

## <a name="return-values"></a><span data-ttu-id="8fc3d-131">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="8fc3d-131">Return Values</span></span>

<span data-ttu-id="8fc3d-132">El estado de retorno de usuario Exit, error, Suspend o Success desde una instalación simultánea se procesa de la misma manera que cualquier otra acción.</span><span class="sxs-lookup"><span data-stu-id="8fc3d-132">The return status of user exit, failure, suspend, or success from a concurrent installation is processed in the same way as any other action.</span></span> <span data-ttu-id="8fc3d-133">Sin embargo, tenga en cuenta que Windows Installer traduce los valores devueltos de todas las acciones cuando escribe el valor devuelto en el archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="8fc3d-133">Note however that Windows Installer translates the return values from all actions when it writes the return value into the log file.</span></span> <span data-ttu-id="8fc3d-134">Por ejemplo, si el valor devuelto de la acción aparece como 1 en el archivo de registro, significa que la acción devolvió un ERROR de \_ éxito.</span><span class="sxs-lookup"><span data-stu-id="8fc3d-134">For example, if the action return value appears as 1 in the log file, this means that the action returned ERROR\_SUCCESS.</span></span> <span data-ttu-id="8fc3d-135">Para obtener más información, vea [registro de valores devueltos de acción](logging-of-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="8fc3d-135">For more information, see [Logging of Action Return Values](logging-of-action-return-values.md).</span></span>

<span data-ttu-id="8fc3d-136">Tenga en cuenta que si se establece **msidbCustomActionTypeContinue** en una instalación simultánea, se reiniciará un error de instalación de \_ \_ USEREXIT, error de \_ instalación de \_ reinicio, error al reiniciar el proceso de \_ instalación \_ \_ , o \_ \_ se requiere un reinicio correcto \_ \_ para el error.</span><span class="sxs-lookup"><span data-stu-id="8fc3d-136">Note that if a concurrent installation has **msidbCustomActionTypeContinue** set, then a return of ERROR\_INSTALL\_USEREXIT, ERROR\_INSTALL\_REBOOT, ERROR\_INSTALL\_REBOOT\_NOW, or ERROR\_SUCCESS\_REBOOT\_REQUIRED is treated as ERROR\_SUCCESS.</span></span> <span data-ttu-id="8fc3d-137">Esto significa que si establece **msidbCustomActionTypeContinue** y la instalación simultánea requiere un reinicio, se omitirá el requisito del reinicio.</span><span class="sxs-lookup"><span data-stu-id="8fc3d-137">This means that if you set **msidbCustomActionTypeContinue** and your concurrent installation requires a restart, the requirement for the restart will be ignored.</span></span> <span data-ttu-id="8fc3d-138">Además, se omitirá el código de error de la acción personalizada de instalación simultánea.</span><span class="sxs-lookup"><span data-stu-id="8fc3d-138">Additionally, the error code from the concurrent installation custom action will be ignored.</span></span>

<span data-ttu-id="8fc3d-139">Si no se establece **msidbCustomActionTypeContinue** , los siguientes códigos de retorno \_ y error correcto se tratan como correctos y tienen los significados siguientes.</span><span class="sxs-lookup"><span data-stu-id="8fc3d-139">If **msidbCustomActionTypeContinue** is not set, the following return codes plus ERROR\_SUCCESS are treated as success and have the following meanings.</span></span> <span data-ttu-id="8fc3d-140">Otros códigos de retorno se tratan como errores.</span><span class="sxs-lookup"><span data-stu-id="8fc3d-140">Other return codes are treated as failure.</span></span>



| <span data-ttu-id="8fc3d-141">Mensaje</span><span class="sxs-lookup"><span data-stu-id="8fc3d-141">Message</span></span>                          | <span data-ttu-id="8fc3d-142">Significado</span><span class="sxs-lookup"><span data-stu-id="8fc3d-142">Meaning</span></span>                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fc3d-143">ERROR de \_ instalación de \_ reinicio</span><span class="sxs-lookup"><span data-stu-id="8fc3d-143">ERROR\_INSTALL\_REBOOT</span></span>           | <span data-ttu-id="8fc3d-144">La marca de reinicio se establecerá para reiniciarse al final de la instalación.</span><span class="sxs-lookup"><span data-stu-id="8fc3d-144">The restart flag will be set to restart at end of the installation.</span></span>                                  |
| <span data-ttu-id="8fc3d-145">ERROR \_ al \_ reiniciar \_ ahora</span><span class="sxs-lookup"><span data-stu-id="8fc3d-145">ERROR\_INSTALL\_REBOOT\_NOW</span></span>      | <span data-ttu-id="8fc3d-146">Se requiere un reinicio antes de completar la instalación.</span><span class="sxs-lookup"><span data-stu-id="8fc3d-146">A restart is required before completing the installation.</span></span> <span data-ttu-id="8fc3d-147">El reinicio se procesará inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="8fc3d-147">The restart will be processed immediately.</span></span> |
| <span data-ttu-id="8fc3d-148">ERROR \_ de \_ reinicio correcto \_ necesario</span><span class="sxs-lookup"><span data-stu-id="8fc3d-148">ERROR\_SUCCESS\_REBOOT\_REQUIRED</span></span> | <span data-ttu-id="8fc3d-149">Se requiere un reinicio, pero se suprime.</span><span class="sxs-lookup"><span data-stu-id="8fc3d-149">A restart was required, but was suppressed.</span></span>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="8fc3d-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8fc3d-150">Remarks</span></span>

<span data-ttu-id="8fc3d-151">Se requiere una expresión condicional para habilitar la instalación simultánea en la instalación o desinstalación del componente o característica asociados.</span><span class="sxs-lookup"><span data-stu-id="8fc3d-151">A conditional expression is required to enable the concurrent installation at either installation or removal of the associated component or feature.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8fc3d-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8fc3d-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fc3d-153">Instalaciones simultáneas</span><span class="sxs-lookup"><span data-stu-id="8fc3d-153">Concurrent Installations</span></span>](concurrent-installations.md)
</dt> <dt>

[<span data-ttu-id="8fc3d-154">Referencia de acción personalizada</span><span class="sxs-lookup"><span data-stu-id="8fc3d-154">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="8fc3d-155">Acerca de las acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="8fc3d-155">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="8fc3d-156">Uso de acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="8fc3d-156">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> </dl>

 

 



