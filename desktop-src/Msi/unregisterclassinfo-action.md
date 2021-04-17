---
description: La acción UnregisterClassInfo administra la eliminación de la información de la clase COM del registro del sistema. Usa la tabla AppId.
ms.assetid: 579a69ee-92cd-4d4c-a007-998ec042f9fc
title: Acción UnregisterClassInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ee701925e07e4f74439efb45da00d430d90304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653076"
---
# <a name="unregisterclassinfo-action"></a><span data-ttu-id="d5e4f-104">Acción UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="d5e4f-104">UnregisterClassInfo Action</span></span>

<span data-ttu-id="d5e4f-105">La acción UnregisterClassInfo administra la eliminación de la información de la clase COM del registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="d5e4f-105">The UnregisterClassInfo action manages the removal of COM class information from the system registry.</span></span> <span data-ttu-id="d5e4f-106">Usa la [tabla AppID](appid-table.md).</span><span class="sxs-lookup"><span data-stu-id="d5e4f-106">It uses the [AppId table](appid-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="d5e4f-107">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="d5e4f-107">Sequence Restrictions</span></span>

<span data-ttu-id="d5e4f-108">La acción UnregisterClassInfo debe aparecer después de la acción [InstallInitialize](installinitialize-action.md) y antes de la acción [RegisterClassInfo](registerclassinfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="d5e4f-108">The UnregisterClassInfo action must come after the [InstallInitialize](installinitialize-action.md) action and before the [RegisterClassInfo](registerclassinfo-action.md) action.</span></span>

<span data-ttu-id="d5e4f-109">[RemoveRegistryValues](removeregistryvalues-action.md) debe estar delante de UnregisterClassInfo en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="d5e4f-109">[RemoveRegistryValues](removeregistryvalues-action.md) must come before UnregisterClassInfo in the sequence.</span></span>

<span data-ttu-id="d5e4f-110">La secuenciación de las acciones del grupo siguiente está restringida.</span><span class="sxs-lookup"><span data-stu-id="d5e4f-110">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="d5e4f-111">Si un subconjunto de estas acciones se produce en una tabla de secuencia, debe aparecer en la misma secuencia relativa, tal y como se muestra en la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="d5e4f-111">If any subset of these actions occur together in a sequence table, they must occur in the same relative sequence as shown in the following table:</span></span>

-   <span data-ttu-id="d5e4f-112">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="d5e4f-112">UnregisterClassInfo</span></span>
-   [<span data-ttu-id="d5e4f-113">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="d5e4f-113">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="d5e4f-114">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="d5e4f-114">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="d5e4f-115">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="d5e4f-115">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="d5e4f-116">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="d5e4f-116">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="d5e4f-117">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="d5e4f-117">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="d5e4f-118">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="d5e4f-118">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="d5e4f-119">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="d5e4f-119">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="d5e4f-120">Por ejemplo, [RegisterExtensionInfo](registerextensioninfo-action.md) debe estar antes de UnregisterClassInfo en la tabla de secuencia.</span><span class="sxs-lookup"><span data-stu-id="d5e4f-120">For example, [RegisterExtensionInfo](registerextensioninfo-action.md) must come before UnregisterClassInfo in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="d5e4f-121">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="d5e4f-121">ActionData Messages</span></span>



| <span data-ttu-id="d5e4f-122">Campo</span><span class="sxs-lookup"><span data-stu-id="d5e4f-122">Field</span></span> | <span data-ttu-id="d5e4f-123">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="d5e4f-123">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="d5e4f-124">\[1\]</span><span class="sxs-lookup"><span data-stu-id="d5e4f-124">\[1\]</span></span> | <span data-ttu-id="d5e4f-125">GUID de clase COM no registrada.</span><span class="sxs-lookup"><span data-stu-id="d5e4f-125">GUID of unregistered COM class.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d5e4f-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5e4f-126">Remarks</span></span>

<span data-ttu-id="d5e4f-127">El instalador establece la propiedad [**OLEAdvtSupport**](oleadvtsupport.md) en true cuando el sistema del usuario actual se ha actualizado para que funcione con la instalación a petición a través de com.</span><span class="sxs-lookup"><span data-stu-id="d5e4f-127">The installer sets the [**OLEAdvtSupport**](oleadvtsupport.md) property to true when the current user's system has been upgraded to work with install-on-demand through COM.</span></span> <span data-ttu-id="d5e4f-128">Si el sistema no admite la instalación a petición a través de COM, UnregisterClassInfo quita todas las clases COM enumeradas en la [tabla de clases](class-table.md) asociada a las características o características desinstaladas que se han instalado como se anuncian desde el registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="d5e4f-128">If the system does not support install-on-demand through COM, UnregisterClassInfo removes all COM classes listed in the [Class table](class-table.md) associated with either uninstalled features or features installed as advertised from the system registry.</span></span> <span data-ttu-id="d5e4f-129">De lo contrario, esta acción solo quita las clases COM asociadas a las características seleccionadas que se van a desinstalar del registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="d5e4f-129">Otherwise, this action removes only the COM classes associated with features selected to be uninstalled from the system registry.</span></span>

 

 



