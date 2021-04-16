---
description: Puede usar la opción de desinstalación de revisión de acción personalizada para especificar que el instalador ejecute la acción personalizada solo cuando se desinstale una revisión.
ms.assetid: c741aa40-ba4c-459e-936a-19c002620c30
title: Revisión de desinstalación de acciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90cfffbdb37f1f2fab046b794010a790e9a5212
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666463"
---
# <a name="patch-uninstall-custom-actions"></a><span data-ttu-id="69e6e-103">Revisión de desinstalación de acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="69e6e-103">Patch Uninstall Custom Actions</span></span>

<span data-ttu-id="69e6e-104">Puede usar la [opción de desinstalación de revisión de acción personalizada](custom-action-patch-uninstall-option.md) para especificar que el instalador ejecute la acción personalizada solo cuando se desinstale una revisión.</span><span class="sxs-lookup"><span data-stu-id="69e6e-104">You can use the [Custom Action Patch Uninstall option](custom-action-patch-uninstall-option.md) to specify that the installer run the custom action only when a patch is uninstalled.</span></span>

<span data-ttu-id="69e6e-105">**Windows Installer 4,5 y versiones posteriores:** Puede usar la [opción de desinstalación de revisión de acción personalizada](custom-action-patch-uninstall-option.md) para especificar que el instalador solo ejecute la acción personalizada cuando se desinstale una revisión.</span><span class="sxs-lookup"><span data-stu-id="69e6e-105">**Windows Installer 4.5 and later:** You can use the [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md) to specify that the installer only run the custom action when a patch is uninstalled.</span></span>

<span data-ttu-id="69e6e-106">\*\*[Windows Installer 4,0 y versiones anteriores](not-supported-in-windows-installer-4-0.md): \* \*</span><span class="sxs-lookup"><span data-stu-id="69e6e-106">\*\*[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):  \*\*</span></span>

<span data-ttu-id="69e6e-107">La [opción de desinstalación de revisión de acción personalizada](custom-action-patch-uninstall-option.md) no está disponible.</span><span class="sxs-lookup"><span data-stu-id="69e6e-107">The [Custom Action Patch Uninstall option](custom-action-patch-uninstall-option.md) is not available.</span></span> <span data-ttu-id="69e6e-108">No hay ningún método para marcar una [acción personalizada](custom-actions.md) en un paquete de revisión que se ejecute cuando se desinstale la revisión porque el instalador no aplica los paquetes de revisión que se desinstalan.</span><span class="sxs-lookup"><span data-stu-id="69e6e-108">There is no method for marking a [custom action](custom-actions.md) within a patch package to be run when the patch is uninstalled because the installer does not apply the patch packages being uninstalled.</span></span>

<span data-ttu-id="69e6e-109">Para que se ejecute una [acción personalizada](custom-actions.md) cuando se desinstale una revisión determinada, la acción personalizada debe estar presente en la aplicación original o en una revisión para el producto que siempre se aplica.</span><span class="sxs-lookup"><span data-stu-id="69e6e-109">To have a [custom action](custom-actions.md) run when a particular patch is uninstalled, the custom action must either be present in the original application or be in a patch for the product that is always applied.</span></span>

<span data-ttu-id="69e6e-110">Los desarrolladores pueden usar la propiedad [**MsiPatchRemovalList**](msipatchremovallist.md) para crear un paquete de Windows Installer o revisión que realice [acciones personalizadas](custom-actions.md) en la eliminación de una revisión.</span><span class="sxs-lookup"><span data-stu-id="69e6e-110">Developers can use the [**MsiPatchRemovalList**](msipatchremovallist.md) property to author a Windows Installer package or patch that performs [custom actions](custom-actions.md) on the removal of a patch.</span></span> <span data-ttu-id="69e6e-111">La acción personalizada se puede crear en el paquete de instalación original, en una revisión que ya se haya aplicado al paquete o en una revisión que no sea de [instalación](uninstallable-patches.md).</span><span class="sxs-lookup"><span data-stu-id="69e6e-111">The custom action can be authored into the original installation package, a patch that has already been applied to the package, or a patch that is not an [uninstallable patch](uninstallable-patches.md).</span></span> <span data-ttu-id="69e6e-112">La acción personalizada se puede condicionar en la propiedad **MsiPatchRemovalList** de las tablas de secuencia.</span><span class="sxs-lookup"><span data-stu-id="69e6e-112">The custom action can be conditionalized on the **MsiPatchRemovalList** property in the sequence tables.</span></span> <span data-ttu-id="69e6e-113">Vea [usar propiedades en instrucciones condicionales](using-properties-in-conditional-statements.md) para obtener más información sobre las acciones de condicional.</span><span class="sxs-lookup"><span data-stu-id="69e6e-113">See [Using Properties in Conditional Statements](using-properties-in-conditional-statements.md) for more information about conditionalizing actions.</span></span>

<span data-ttu-id="69e6e-114">La acción personalizada puede obtener los GUID de las revisiones que se van a quitar del valor de la propiedad [**MsiPatchRemovalList**](msipatchremovallist.md) .</span><span class="sxs-lookup"><span data-stu-id="69e6e-114">The custom action can obtain the GUIDs of patches being removed from the value of the [**MsiPatchRemovalList**](msipatchremovallist.md) property.</span></span> <span data-ttu-id="69e6e-115">La acción personalizada puede determinar si el estado de instalación de la revisión se aplica, está obsoleto o se ha sustituido mediante una llamada a la propiedad [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) o [**PatchProperty**](patch-patchproperty.md) del [objeto patch](patch-object.md).</span><span class="sxs-lookup"><span data-stu-id="69e6e-115">The custom action can determine whether the installation state of the patch is applied, obsolete, or superseded by calling the [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) or the [**PatchProperty**](patch-patchproperty.md) property of the [Patch object](patch-object.md).</span></span>

<span data-ttu-id="69e6e-116">Si la acción personalizada requiere metadatos especiales de la revisión, la revisión debe contener una acción personalizada que escriba los metadatos en un registro o ubicación de archivo cuando se aplique la revisión.</span><span class="sxs-lookup"><span data-stu-id="69e6e-116">If the custom action requires special metadata from the patch, the patch should contain a custom action that writes the metadata to a registry or file location when the patch is applied.</span></span> <span data-ttu-id="69e6e-117">La acción personalizada en la aplicación original o una revisión aplicada siempre puede obtener la información necesaria para quitar los cambios de la revisión.</span><span class="sxs-lookup"><span data-stu-id="69e6e-117">The custom action in the original application or a patch that is always applied can obtain the information needed to remove the patch's changes.</span></span>

<span data-ttu-id="69e6e-118">Las revisiones que realizan cambios difíciles de deshacer correctamente no deben marcarse como revisiones que no se pueden [instalar](uninstallable-patches.md).</span><span class="sxs-lookup"><span data-stu-id="69e6e-118">Patches making changes that are difficult to undo correctly should not be marked as [uninstallable patches](uninstallable-patches.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="69e6e-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="69e6e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69e6e-120">Secuenciación de revisiones</span><span class="sxs-lookup"><span data-stu-id="69e6e-120">Patch Sequencing</span></span>](sequencing-patches.md)
</dt> <dt>

[<span data-ttu-id="69e6e-121">Quitar revisiones</span><span class="sxs-lookup"><span data-stu-id="69e6e-121">Removing Patches</span></span>](removing-patches.md)
</dt> <dt>

[<span data-ttu-id="69e6e-122">Revisiones desinstalables</span><span class="sxs-lookup"><span data-stu-id="69e6e-122">Uninstallable Patches</span></span>](uninstallable-patches.md)
</dt> <dt>

[<span data-ttu-id="69e6e-123">Desinstalación de revisiones</span><span class="sxs-lookup"><span data-stu-id="69e6e-123">Uninstalling Patches</span></span>](uninstalling-patches.md)
</dt> <dt>

[<span data-ttu-id="69e6e-124">**MSIPATCHREMOVE**</span><span class="sxs-lookup"><span data-stu-id="69e6e-124">**MSIPATCHREMOVE**</span></span>](msipatchremove.md)
</dt> <dt>

[<span data-ttu-id="69e6e-125">**MsiEnumapplicationsEx**</span><span class="sxs-lookup"><span data-stu-id="69e6e-125">**MsiEnumapplicationsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[<span data-ttu-id="69e6e-126">**MsiGetPatchInfoEx**</span><span class="sxs-lookup"><span data-stu-id="69e6e-126">**MsiGetPatchInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[<span data-ttu-id="69e6e-127">**MsiRemovePatches**</span><span class="sxs-lookup"><span data-stu-id="69e6e-127">**MsiRemovePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 



