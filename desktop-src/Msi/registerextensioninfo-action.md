---
description: La acción RegisterExtensionInfo administra el registro de información relacionada con la extensión con el sistema.
ms.assetid: 3c243ca3-9fa7-41ec-968e-7954d7d45432
title: Acción RegisterExtensionInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0310344b6579ef65faac41238bb607ce98411b52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652669"
---
# <a name="registerextensioninfo-action"></a><span data-ttu-id="191f3-103">Acción RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="191f3-103">RegisterExtensionInfo Action</span></span>

<span data-ttu-id="191f3-104">La acción RegisterExtensionInfo administra el registro de información relacionada con la extensión con el sistema.</span><span class="sxs-lookup"><span data-stu-id="191f3-104">The RegisterExtensionInfo action manages the registration of extension related information with the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="191f3-105">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="191f3-105">Sequence Restrictions</span></span>

<span data-ttu-id="191f3-106">La acción RegisterExtensionInfo debe aparecer después de la acción [InstallFiles](installfiles-action.md) y la acción [UnregisterExtensionInfo](unregisterextensioninfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="191f3-106">The RegisterExtensionInfo action must come after the [InstallFiles](installfiles-action.md) action and the [UnregisterExtensionInfo](unregisterextensioninfo-action.md) action.</span></span>

<span data-ttu-id="191f3-107">La secuenciación de las acciones del grupo siguiente está restringida.</span><span class="sxs-lookup"><span data-stu-id="191f3-107">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="191f3-108">Si un subconjunto de estas acciones se produce juntos en una tabla de secuencia, deben tener el mismo orden de secuencia relativo que se muestra:</span><span class="sxs-lookup"><span data-stu-id="191f3-108">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="191f3-109">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="191f3-109">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="191f3-110">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="191f3-110">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="191f3-111">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="191f3-111">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="191f3-112">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="191f3-112">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="191f3-113">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="191f3-113">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   <span data-ttu-id="191f3-114">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="191f3-114">RegisterExtensionInfo</span></span>
-   [<span data-ttu-id="191f3-115">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="191f3-115">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="191f3-116">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="191f3-116">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="191f3-117">Por ejemplo, RegisterExtensionInfo debe aparecer después de [UnregisterMIMEInfo](unregistermimeinfo-action.md) en la tabla de secuencia.</span><span class="sxs-lookup"><span data-stu-id="191f3-117">For example, RegisterExtensionInfo must come after [UnregisterMIMEInfo](unregistermimeinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="191f3-118">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="191f3-118">ActionData Messages</span></span>



| <span data-ttu-id="191f3-119">Campo</span><span class="sxs-lookup"><span data-stu-id="191f3-119">Field</span></span> | <span data-ttu-id="191f3-120">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="191f3-120">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="191f3-121">\[1\]</span><span class="sxs-lookup"><span data-stu-id="191f3-121">\[1\]</span></span> | <span data-ttu-id="191f3-122">Extensión registrada.</span><span class="sxs-lookup"><span data-stu-id="191f3-122">Registered extension.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="191f3-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="191f3-123">Remarks</span></span>

<span data-ttu-id="191f3-124">Si el sistema admite la instalación a petición para los servidores de extensión, RegisterExtensionInfo registra todos los servidores de extensión en la [tabla de extensión](extension-table.md) asociada a las características establecidas para la instalación o el anuncio.</span><span class="sxs-lookup"><span data-stu-id="191f3-124">If the system supports installation-on-demand for extension servers, RegisterExtensionInfo registers all extension servers in the [Extension table](extension-table.md) associated with features set for installation or advertisement.</span></span> <span data-ttu-id="191f3-125">De lo contrario, esta acción solo registra los servidores de extensión asociados a las características establecidas en instalación.</span><span class="sxs-lookup"><span data-stu-id="191f3-125">Otherwise this action only registers extension servers associated with features set to installation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="191f3-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="191f3-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="191f3-127">**Propiedad ShellAdvtSupport**</span><span class="sxs-lookup"><span data-stu-id="191f3-127">**ShellAdvtSupport property**</span></span>](shelladvtsupport.md)
</dt> </dl>

 

 



