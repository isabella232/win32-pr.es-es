---
description: La acción UnregisterExtensionInfo administra la eliminación de la información relacionada con la extensión del registro del sistema.
ms.assetid: 62bb9d17-c221-4bd2-bd7f-9930e28bb946
title: Acción UnregisterExtensionInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85d069a686c5f0e517a0cc9556634895216dd8cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653074"
---
# <a name="unregisterextensioninfo-action"></a><span data-ttu-id="b0b2e-103">Acción UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="b0b2e-103">UnregisterExtensionInfo Action</span></span>

<span data-ttu-id="b0b2e-104">La acción UnregisterExtensionInfo administra la eliminación de la información relacionada con la extensión del registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="b0b2e-104">The UnregisterExtensionInfo action manages the removal of extension-related information from the system registry.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="b0b2e-105">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="b0b2e-105">Sequence Restrictions</span></span>

<span data-ttu-id="b0b2e-106">La acción UnregisterExtensionInfo debe aparecer después de la acción [InstallInitialize](installinitialize-action.md) y antes de la acción [RegisterExtensionInfo](registerextensioninfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="b0b2e-106">The UnregisterExtensionInfo action must come after the [InstallInitialize](installinitialize-action.md) action and before the [RegisterExtensionInfo](registerextensioninfo-action.md) action.</span></span>

<span data-ttu-id="b0b2e-107">[RemoveRegistryValues](removeregistryvalues-action.md) debe estar delante de UnregisterExtensionInfo en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="b0b2e-107">[RemoveRegistryValues](removeregistryvalues-action.md) must come before UnregisterExtensionInfo in the sequence.</span></span>

<span data-ttu-id="b0b2e-108">La secuenciación de las acciones del grupo siguiente está restringida.</span><span class="sxs-lookup"><span data-stu-id="b0b2e-108">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="b0b2e-109">Si un subconjunto de estas acciones se produce juntos en una tabla de secuencia, deben tener el mismo orden de secuencia relativo que se muestra:</span><span class="sxs-lookup"><span data-stu-id="b0b2e-109">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="b0b2e-110">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="b0b2e-110">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   <span data-ttu-id="b0b2e-111">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="b0b2e-111">UnregisterExtensionInfo</span></span>
-   [<span data-ttu-id="b0b2e-112">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="b0b2e-112">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="b0b2e-113">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="b0b2e-113">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="b0b2e-114">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="b0b2e-114">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="b0b2e-115">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="b0b2e-115">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="b0b2e-116">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="b0b2e-116">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="b0b2e-117">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="b0b2e-117">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="b0b2e-118">Por ejemplo, UnregisterExtensionInfo debe estar antes de [UnregisterProgIdInfo](unregisterprogidinfo-action.md) en la tabla de secuencia.</span><span class="sxs-lookup"><span data-stu-id="b0b2e-118">For example, UnregisterExtensionInfo must come before [UnregisterProgIdInfo](unregisterprogidinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="b0b2e-119">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="b0b2e-119">ActionData Messages</span></span>



| <span data-ttu-id="b0b2e-120">Campo</span><span class="sxs-lookup"><span data-stu-id="b0b2e-120">Field</span></span> | <span data-ttu-id="b0b2e-121">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="b0b2e-121">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="b0b2e-122">\[1\]</span><span class="sxs-lookup"><span data-stu-id="b0b2e-122">\[1\]</span></span> | <span data-ttu-id="b0b2e-123">Extensión quitada.</span><span class="sxs-lookup"><span data-stu-id="b0b2e-123">Removed extension.</span></span>         |



 

## <a name="remarks"></a><span data-ttu-id="b0b2e-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b0b2e-124">Remarks</span></span>

<span data-ttu-id="b0b2e-125">Si el sistema no admite la instalación a petición de servidores de extensión, UnregisterExtensionInfo quita todos los servidores de extensión de la [tabla de extensión](extension-table.md) asociados a una característica desinstalada o a una característica instalada como anunciada desde el registro.</span><span class="sxs-lookup"><span data-stu-id="b0b2e-125">If the system does not support the install-on-demand of extension servers, UnregisterExtensionInfo removes all extension servers in the [Extension table](extension-table.md) associated with either an uninstalled feature or a feature installed as advertised from the registry.</span></span> <span data-ttu-id="b0b2e-126">De lo contrario, esta acción quita los servidores de extensión asociados a una característica que está seleccionada para quitarse del registro.</span><span class="sxs-lookup"><span data-stu-id="b0b2e-126">Otherwise, this action removes the extension servers associated with a feature that is selected to be removed from the registry.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0b2e-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b0b2e-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0b2e-128">**Propiedad ShellAdvtSupport**</span><span class="sxs-lookup"><span data-stu-id="b0b2e-128">**ShellAdvtSupport Property**</span></span>](shelladvtsupport.md)
</dt> </dl>

 

 



