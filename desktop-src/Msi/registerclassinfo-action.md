---
description: La acción RegisterClassInfo administra el registro de información de clase COM con el sistema. Usa la tabla AppId.
ms.assetid: f8b60a75-9c0e-41c5-b6af-6a05a26b2d71
title: Acción RegisterClassInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd916772bc236dfc86df336347514c10d5dfbce7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677762"
---
# <a name="registerclassinfo-action"></a><span data-ttu-id="ca440-104">Acción RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="ca440-104">RegisterClassInfo Action</span></span>

<span data-ttu-id="ca440-105">La acción RegisterClassInfo administra el registro de información de clase COM con el sistema.</span><span class="sxs-lookup"><span data-stu-id="ca440-105">The RegisterClassInfo action manages the registration of COM class information with the system.</span></span> <span data-ttu-id="ca440-106">Usa la [tabla AppID](appid-table.md).</span><span class="sxs-lookup"><span data-stu-id="ca440-106">It uses the [AppId table](appid-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="ca440-107">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="ca440-107">Sequence Restrictions</span></span>

<span data-ttu-id="ca440-108">La acción RegisterClassInfo debe aparecer después de la acción [InstallFiles](installfiles-action.md) y la acción [UnregisterClassInfo](unregisterclassinfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="ca440-108">The RegisterClassInfo action must come after the [InstallFiles](installfiles-action.md) action and the [UnregisterClassInfo](unregisterclassinfo-action.md) action.</span></span>

<span data-ttu-id="ca440-109">La secuenciación de las acciones del grupo siguiente está restringida.</span><span class="sxs-lookup"><span data-stu-id="ca440-109">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="ca440-110">Si un subconjunto de estas acciones se produce juntos en una tabla de secuencia, deben tener el mismo orden de secuencia relativo que se muestra:</span><span class="sxs-lookup"><span data-stu-id="ca440-110">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="ca440-111">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="ca440-111">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="ca440-112">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="ca440-112">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="ca440-113">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="ca440-113">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="ca440-114">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="ca440-114">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   <span data-ttu-id="ca440-115">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="ca440-115">RegisterClassInfo</span></span>
-   [<span data-ttu-id="ca440-116">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="ca440-116">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="ca440-117">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="ca440-117">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="ca440-118">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="ca440-118">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="ca440-119">Por ejemplo, RegisterClassInfo debe aparecer después de [UnregisterMIMEInfo](unregistermimeinfo-action.md) en la tabla de secuencia.</span><span class="sxs-lookup"><span data-stu-id="ca440-119">For example, RegisterClassInfo must come after [UnregisterMIMEInfo](unregistermimeinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="ca440-120">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="ca440-120">ActionData Messages</span></span>



| <span data-ttu-id="ca440-121">Campo</span><span class="sxs-lookup"><span data-stu-id="ca440-121">Field</span></span> | <span data-ttu-id="ca440-122">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="ca440-122">Description of action data</span></span>                          |
|-------|-----------------------------------------------------|
| <span data-ttu-id="ca440-123">\[1\]</span><span class="sxs-lookup"><span data-stu-id="ca440-123">\[1\]</span></span> | <span data-ttu-id="ca440-124">Identificador de clase GUID del servidor COM registrado.</span><span class="sxs-lookup"><span data-stu-id="ca440-124">GUID class identifier of the registered COM server.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ca440-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ca440-125">Remarks</span></span>

<span data-ttu-id="ca440-126">Si el sistema admite la instalación a petición para los servidores OLE, RegisterClassInfo registra todas las clases COM en la [tabla de clases](class-table.md) asociada a una característica seleccionada que se va a instalar o anunciar.</span><span class="sxs-lookup"><span data-stu-id="ca440-126">If the system supports install-on-demand for OLE servers, RegisterClassInfo registers all COM classes in the [Class table](class-table.md) associated with a feature selected to be installed or advertised.</span></span> <span data-ttu-id="ca440-127">De lo contrario, esta acción solo registra las clases COM asociadas a una característica seleccionada para su instalación.</span><span class="sxs-lookup"><span data-stu-id="ca440-127">Otherwise this action only registers the COM classes associated with a feature selected for installation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca440-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ca440-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca440-129">**Propiedad OLEAdvtSupport**</span><span class="sxs-lookup"><span data-stu-id="ca440-129">**OLEAdvtSupport property**</span></span>](oleadvtsupport.md)
</dt> </dl>

 

 



