---
description: Utilice la siguiente marca de opción para especificar que el instalador ejecute la acción personalizada solo cuando se desinstale una revisión. Para establecer la opción, agregue el valor de esta tabla al valor del campo ExtendedType de la tabla CustomAction.
ms.assetid: aa4d9e21-5316-42b5-a22e-c7a5becd3cae
title: Opción de desinstalación de revisión de acción personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108365876393733f7cc520ae565bb2c5ea7ff3df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653063"
---
# <a name="custom-action-patch-uninstall-option"></a><span data-ttu-id="acea3-104">Opción de desinstalación de revisión de acción personalizada</span><span class="sxs-lookup"><span data-stu-id="acea3-104">Custom Action Patch Uninstall Option</span></span>

<span data-ttu-id="acea3-105">Utilice la siguiente marca de opción para especificar que el instalador ejecute la acción personalizada solo cuando se desinstale una revisión.</span><span class="sxs-lookup"><span data-stu-id="acea3-105">Use the following option flag to specify that the installer run the custom action only when a patch is being uninstalled.</span></span> <span data-ttu-id="acea3-106">Para establecer la opción, agregue el valor de esta tabla al valor del campo ExtendedType de la [tabla CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="acea3-106">To set the option, add the value in this table to the value in the ExtendedType field of the [CustomAction table](customaction-table.md).</span></span>

<span data-ttu-id="acea3-107">**[Windows Installer 4,0 y versiones anteriores](not-supported-in-windows-installer-4-0.md):** No compatible.</span><span class="sxs-lookup"><span data-stu-id="acea3-107">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="acea3-108">Esta opción está disponible a partir de Windows Installer 4,5.</span><span class="sxs-lookup"><span data-stu-id="acea3-108">This option is available beginning with Windows Installer 4.5.</span></span>



| <span data-ttu-id="acea3-109">Constante</span><span class="sxs-lookup"><span data-stu-id="acea3-109">Constant</span></span>                                | <span data-ttu-id="acea3-110">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="acea3-110">Hexadecimal</span></span> | <span data-ttu-id="acea3-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="acea3-111">Decimal</span></span> | <span data-ttu-id="acea3-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="acea3-112">Description</span></span>                                                    |
|-----------------------------------------|-------------|---------|----------------------------------------------------------------|
| <span data-ttu-id="acea3-113">**msidbCustomActionTypePatchUninstall**</span><span class="sxs-lookup"><span data-stu-id="acea3-113">**msidbCustomActionTypePatchUninstall**</span></span> | <span data-ttu-id="acea3-114">0x8000</span><span class="sxs-lookup"><span data-stu-id="acea3-114">0x8000</span></span>      | <span data-ttu-id="acea3-115">32 768</span><span class="sxs-lookup"><span data-stu-id="acea3-115">32768</span></span>   | <span data-ttu-id="acea3-116">La acción personalizada solo se ejecuta cuando se está desinstalando una revisión.</span><span class="sxs-lookup"><span data-stu-id="acea3-116">The custom action runs only when a patch is being uninstalled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="acea3-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="acea3-117">Remarks</span></span>

<span data-ttu-id="acea3-118">Este atributo se puede Agregar a una acción personalizada mediante su creación en el paquete de Windows Installer (archivo. msi).</span><span class="sxs-lookup"><span data-stu-id="acea3-118">This attribute can be added to a custom action by authoring it in the Windows Installer package (.msi file).</span></span> <span data-ttu-id="acea3-119">Una revisión puede Agregar una nueva acción personalizada con este atributo.</span><span class="sxs-lookup"><span data-stu-id="acea3-119">A new custom action with this attribute can be added by a patch.</span></span> <span data-ttu-id="acea3-120">Una acción personalizada que tiene este atributo se puede actualizar mediante una revisión.</span><span class="sxs-lookup"><span data-stu-id="acea3-120">A custom action having this attribute can be updated by a patch.</span></span> <span data-ttu-id="acea3-121">Este atributo no se puede agregar ni quitar en una revisión para una acción personalizada existente.</span><span class="sxs-lookup"><span data-stu-id="acea3-121">This attribute cannot be added or removed by a patch to an existing custom action.</span></span>

<span data-ttu-id="acea3-122">Si una revisión agrega o actualiza una acción personalizada con este atributo, Windows Installer ejecutará la acción personalizada nueva o actualizada cuando se desinstale la revisión.</span><span class="sxs-lookup"><span data-stu-id="acea3-122">If a patch adds or updates a custom action with this attribute, Windows Installer runs the new or updated custom action when the patch is uninstalled.</span></span> <span data-ttu-id="acea3-123">Windows Installer hace que las actualizaciones de la revisión se desinstalen disponibles para la acción personalizada desinstalar revisión.</span><span class="sxs-lookup"><span data-stu-id="acea3-123">Windows Installer makes the updates within the patch being uninstalled available to the patch uninstall custom action.</span></span> <span data-ttu-id="acea3-124">La revisión debe incluir una [tabla *<PatchGUID>* MsiTransformView](msitransformview.md) para proporcionar esta información a Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="acea3-124">The patch must include a [MsiTransformView *<PatchGUID>*](msitransformview.md) table to provide this information to Windows Installer.</span></span>

<span data-ttu-id="acea3-125">Cuando un paquete que contiene una acción personalizada con el atributo **msidbCustomActionTypePatchUninstall** se instala con una versión de instalador anterior a Windows Installer 4,0, el instalador no llama a la acción personalizada cuando se desinstala la revisión.</span><span class="sxs-lookup"><span data-stu-id="acea3-125">When a package that contains a custom action with the **msidbCustomActionTypePatchUninstall** attribute is installed using an installer version earlier than Windows Installer 4.0, the installer does not call the custom action when the patch is uninstalled.</span></span> <span data-ttu-id="acea3-126">La instalación puede ejecutar la acción personalizada durante la instalación, reparación o actualización del paquete.</span><span class="sxs-lookup"><span data-stu-id="acea3-126">The install can run the custom action during the installation, repair, or update of the package.</span></span>

<span data-ttu-id="acea3-127">Las acciones personalizadas con el atributo **msidbCustomActionTypePatchUninstall** deben estar condicionadas mediante la propiedad [**MSIPATCHREMOVE**](msipatchremove.md) para evitar que la acción personalizada se ejecute al instalar, reparar o actualizar mediante un sistema con Windows Installer 4,0 o una versión anterior.</span><span class="sxs-lookup"><span data-stu-id="acea3-127">Custom actions with the **msidbCustomActionTypePatchUninstall** attribute should be conditioned using the [**MSIPATCHREMOVE**](msipatchremove.md) property to prevent the custom action from running when installing, repairing, or updating using a system with Windows Installer 4.0 or earlier.</span></span> <span data-ttu-id="acea3-128">Cuando se instala Windows Installer 4,5 y versiones posteriores, todas las revisiones del sistema que tienen acciones personalizadas marcadas con el atributo **msidbCustomActionTypePatchUninstall** ejecutan la acción personalizada durante la desinstalación de la revisión.</span><span class="sxs-lookup"><span data-stu-id="acea3-128">When Windows Installer 4.5 and later is installed, all the patches on the system having custom actions marked with the **msidbCustomActionTypePatchUninstall** attribute run the custom action during patch uninstallation.</span></span> <span data-ttu-id="acea3-129">Si se quita Windows Installer 4,5 o posterior del sistema, las revisiones pierden la funcionalidad de desinstalación de la revisión de acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="acea3-129">If Windows Installer 4.5 or later is removed from the system, patches lose the custom action patch uninstall functionality.</span></span>

<span data-ttu-id="acea3-130">Para obtener información sobre la ejecución de una acción personalizada durante la desinstalación de una revisión con una versión anterior a Windows Installer 4,5, vea [revisión de desinstalación de acciones personalizadas](patch-uninstall-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="acea3-130">For information about running a custom action during the uninstallation of a patch using a version earlier than Windows Installer 4.5, see [Patch Uninstall Custom Actions](patch-uninstall-custom-actions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="acea3-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="acea3-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acea3-132">Opciones de ejecución de la acción personalizada In-Script</span><span class="sxs-lookup"><span data-stu-id="acea3-132">Custom Action In-Script Execution Options</span></span>](custom-action-in-script-execution-options.md)
</dt> <dt>

[<span data-ttu-id="acea3-133">Referencia de acción personalizada</span><span class="sxs-lookup"><span data-stu-id="acea3-133">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="acea3-134">Acerca de las acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="acea3-134">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="acea3-135">Uso de acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="acea3-135">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="acea3-136">MsiTransformView *<PatchGUID>*</span><span class="sxs-lookup"><span data-stu-id="acea3-136">MsiTransformView *<PatchGUID>*</span></span>](msitransformview.md)
</dt> </dl>

 

 



