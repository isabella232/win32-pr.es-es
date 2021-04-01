---
description: La acción RegisterMIMEInfo registra información del registro relacionada con MIME con el sistema.
ms.assetid: 2ba88b5f-bd8a-4572-af82-9c0b91b9b6d9
title: Acción RegisterMIMEInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41130d9e595cc2d95557470f79c217f3c3235d75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813646"
---
# <a name="registermimeinfo-action"></a><span data-ttu-id="8a0ec-103">Acción RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="8a0ec-103">RegisterMIMEInfo Action</span></span>

<span data-ttu-id="8a0ec-104">La acción RegisterMIMEInfo registra información del registro relacionada con MIME con el sistema.</span><span class="sxs-lookup"><span data-stu-id="8a0ec-104">The RegisterMIMEInfo action registers MIME-related registry information with the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="8a0ec-105">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="8a0ec-105">Sequence Restrictions</span></span>

<span data-ttu-id="8a0ec-106">La acción RegisterMIMEInfo debe aparecer después de la acción [InstallFiles](installfiles-action.md) , la acción [UnregisterMIMEInfo](unregistermimeinfo-action.md) , la acción [RegisterClassInfo](registerclassinfo-action.md) y la acción [RegisterExtensionInfo](registerextensioninfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="8a0ec-106">The RegisterMIMEInfo action must come after the [InstallFiles](installfiles-action.md) action, [UnregisterMIMEInfo](unregistermimeinfo-action.md) action, [RegisterClassInfo](registerclassinfo-action.md) action, and the [RegisterExtensionInfo](registerextensioninfo-action.md) action.</span></span>

<span data-ttu-id="8a0ec-107">La secuenciación de las acciones del grupo siguiente está restringida.</span><span class="sxs-lookup"><span data-stu-id="8a0ec-107">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="8a0ec-108">Si un subconjunto de estas acciones se produce juntos en una tabla de secuencia, deben tener el mismo orden de secuencia relativo que se muestra:</span><span class="sxs-lookup"><span data-stu-id="8a0ec-108">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="8a0ec-109">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="8a0ec-109">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="8a0ec-110">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="8a0ec-110">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="8a0ec-111">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="8a0ec-111">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="8a0ec-112">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="8a0ec-112">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="8a0ec-113">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="8a0ec-113">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="8a0ec-114">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="8a0ec-114">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="8a0ec-115">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="8a0ec-115">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   <span data-ttu-id="8a0ec-116">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="8a0ec-116">RegisterMIMEInfo</span></span>

<span data-ttu-id="8a0ec-117">Por ejemplo, RegisterMIMEInfo debe aparecer después de [UnregisterMIMEInfo](unregistermimeinfo-action.md) en la tabla de secuencia.</span><span class="sxs-lookup"><span data-stu-id="8a0ec-117">For example, RegisterMIMEInfo must come after [UnregisterMIMEInfo](unregistermimeinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="8a0ec-118">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="8a0ec-118">ActionData Messages</span></span>



| <span data-ttu-id="8a0ec-119">Campo</span><span class="sxs-lookup"><span data-stu-id="8a0ec-119">Field</span></span> | <span data-ttu-id="8a0ec-120">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="8a0ec-120">Description of action data</span></span>                   |
|-------|----------------------------------------------|
| <span data-ttu-id="8a0ec-121">\[1\]</span><span class="sxs-lookup"><span data-stu-id="8a0ec-121">\[1\]</span></span> | <span data-ttu-id="8a0ec-122">Identificador del tipo de contenido MIME registrado.</span><span class="sxs-lookup"><span data-stu-id="8a0ec-122">Identifier of registered MIME content type.</span></span>  |
| <span data-ttu-id="8a0ec-123">\[2\]</span><span class="sxs-lookup"><span data-stu-id="8a0ec-123">\[2\]</span></span> | <span data-ttu-id="8a0ec-124">Extensión asociada al tipo de contenido MIME.</span><span class="sxs-lookup"><span data-stu-id="8a0ec-124">Extension associated with MIME content type.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8a0ec-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8a0ec-125">Remarks</span></span>

<span data-ttu-id="8a0ec-126">La acción RegisterMIMEInfo registra toda la información de MIME para los servidores de la [tabla MIME](mime-table.md) para la que se ha seleccionado el servidor de clase o el servidor de extensiones correspondiente para su instalación.</span><span class="sxs-lookup"><span data-stu-id="8a0ec-126">The RegisterMIMEInfo action registers all MIME information for servers from the [MIME table](mime-table.md) for which the corresponding class server or extension server has been selected to be installed.</span></span>

 

 



