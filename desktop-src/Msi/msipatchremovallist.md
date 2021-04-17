---
description: El instalador establece el valor de la propiedad MsiPatchRemovalList en una lista de revisiones que se están quitando durante la instalación.
ms.assetid: 6e0b391a-d840-4f01-af12-4708ce6c9ce8
title: Propiedad MsiPatchRemovalList
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2af522d9570297f2ff911b501bc543cf4b5971c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670644"
---
# <a name="msipatchremovallist-property"></a><span data-ttu-id="e9764-103">Propiedad MsiPatchRemovalList</span><span class="sxs-lookup"><span data-stu-id="e9764-103">MsiPatchRemovalList property</span></span>

<span data-ttu-id="e9764-104">El instalador establece el valor de la propiedad **MsiPatchRemovalList** en una lista de revisiones que se están quitando durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="e9764-104">The installer sets the value of the **MsiPatchRemovalList** property to a list of patches that are being removed during the installation.</span></span> <span data-ttu-id="e9764-105">Las revisiones se representan en la lista mediante sus GUID de código de revisión separados por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="e9764-105">The patches are represented in the list by their patch code GUIDs separated by semicolons.</span></span>

<span data-ttu-id="e9764-106">Los desarrolladores pueden usar la propiedad **MsiPatchRemovalList** para crear un paquete de Windows Installer o revisión que realice [acciones personalizadas](custom-actions.md) en la eliminación de una revisión.</span><span class="sxs-lookup"><span data-stu-id="e9764-106">Developers can use the **MsiPatchRemovalList** property to author a Windows Installer package or patch that performs [custom actions](custom-actions.md) on the removal of a patch.</span></span> <span data-ttu-id="e9764-107">La acción personalizada se puede crear en el paquete de instalación original, en una revisión que ya se haya aplicado al paquete o en una revisión que no sea de [instalación](uninstallable-patches.md).</span><span class="sxs-lookup"><span data-stu-id="e9764-107">The custom action can be authored into the original installation package, a patch that has already been applied to the package, or a patch that is not an [uninstallable patch](uninstallable-patches.md).</span></span> <span data-ttu-id="e9764-108">La acción personalizada se puede condicionar en la propiedad **MsiPatchRemovalList** de las tablas de secuencia.</span><span class="sxs-lookup"><span data-stu-id="e9764-108">The custom action can be conditionalized on the **MsiPatchRemovalList** property in the sequence tables.</span></span> <span data-ttu-id="e9764-109">Vea [usar propiedades en instrucciones condicionales](using-properties-in-conditional-statements.md) para obtener más información sobre las acciones de condicional.</span><span class="sxs-lookup"><span data-stu-id="e9764-109">See [Using Properties in Conditional Statements](using-properties-in-conditional-statements.md) for more information about conditionalizing actions.</span></span>

<span data-ttu-id="e9764-110">La acción personalizada puede obtener los GUID de las revisiones que se van a quitar del valor de la propiedad **MsiPatchRemovalList** .</span><span class="sxs-lookup"><span data-stu-id="e9764-110">The custom action can obtain the GUIDs of patches being removed from the value of the **MsiPatchRemovalList** property.</span></span> <span data-ttu-id="e9764-111">La acción personalizada puede determinar si el estado de instalación de la revisión se aplica, está obsoleto o se ha sustituido mediante una llamada a la función [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) o la propiedad [**PatchProperty**](patch-patchproperty.md) del [objeto patch](patch-object.md).</span><span class="sxs-lookup"><span data-stu-id="e9764-111">The custom action can determine whether the installation state of the patch is applied, obsolete, or superseded by calling the [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) function or the [**PatchProperty**](patch-patchproperty.md) property of the [Patch object](patch-object.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e9764-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e9764-112">Remarks</span></span>

<span data-ttu-id="e9764-113">Para obtener más información acerca de cómo quitar revisiones, consulte [quitar revisiones](removing-patches.md).</span><span class="sxs-lookup"><span data-stu-id="e9764-113">For more information about removing patches, see [Removing Patches](removing-patches.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e9764-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9764-114">Requirements</span></span>



| <span data-ttu-id="e9764-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9764-115">Requirement</span></span> | <span data-ttu-id="e9764-116">Value</span><span class="sxs-lookup"><span data-stu-id="e9764-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9764-117">Versión</span><span class="sxs-lookup"><span data-stu-id="e9764-117">Version</span></span><br/> | <span data-ttu-id="e9764-118">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e9764-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e9764-119">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e9764-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e9764-120">Windows Installer 3,0 o posterior en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e9764-120">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="e9764-121">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="e9764-121">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e9764-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e9764-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9764-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e9764-123">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="e9764-124">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="e9764-124">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




