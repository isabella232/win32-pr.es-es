---
description: La acción UnregisterMIMEInfo anula el registro de la información del registro relacionada con MIME del sistema. La acción anula el registro de la información de MIME para los servidores de la tabla MIME para la que está seleccionada actualmente la característica correspondiente para desinstalarla.
ms.assetid: 9a5c12da-e78f-4c99-9b82-d41624593c61
title: Acción UnregisterMIMEInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02c1ca7c0cd12d9ec6236a0c0298ba793713f5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279479"
---
# <a name="unregistermimeinfo-action"></a><span data-ttu-id="cdc85-104">Acción UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="cdc85-104">UnregisterMIMEInfo Action</span></span>

<span data-ttu-id="cdc85-105">La acción UnregisterMIMEInfo anula el registro de la información del registro relacionada con MIME del sistema.</span><span class="sxs-lookup"><span data-stu-id="cdc85-105">The UnregisterMIMEInfo action unregisters MIME-related registry information from the system.</span></span> <span data-ttu-id="cdc85-106">La acción anula el registro de la información de MIME para los servidores de la [tabla MIME](mime-table.md) para la que está seleccionada actualmente la característica correspondiente para desinstalarla.</span><span class="sxs-lookup"><span data-stu-id="cdc85-106">The action unregisters MIME information for servers from the [MIME table](mime-table.md) for which the corresponding feature is currently selected to be uninstalled.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="cdc85-107">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="cdc85-107">Sequence Restrictions</span></span>

<span data-ttu-id="cdc85-108">La acción UnregisterMIMEInfo debe aparecer después de la acción [InstallInitialize](installinitialize-action.md) , la acción [UnregisterClassInfo](unregisterclassinfo-action.md) , la acción [UnregisterExtensionInfo](unregisterextensioninfo-action.md) y antes de la acción [RegisterMIMEInfo](registermimeinfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="cdc85-108">The UnregisterMIMEInfo action must come after the [InstallInitialize](installinitialize-action.md) action, [UnregisterClassInfo](unregisterclassinfo-action.md) action, [UnregisterExtensionInfo](unregisterextensioninfo-action.md) action, and before the [RegisterMIMEInfo](registermimeinfo-action.md) action.</span></span>

<span data-ttu-id="cdc85-109">[RemoveRegistryValues](removeregistryvalues-action.md) debe estar delante de UnregisterMIMEInfo en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="cdc85-109">[RemoveRegistryValues](removeregistryvalues-action.md) must come before UnregisterMIMEInfo in the sequence.</span></span>

<span data-ttu-id="cdc85-110">La secuenciación de las acciones del grupo siguiente está restringida.</span><span class="sxs-lookup"><span data-stu-id="cdc85-110">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="cdc85-111">Si un subconjunto de estas acciones se produce juntos en una tabla de secuencia, deben tener el mismo orden de secuencia relativo que se muestra:</span><span class="sxs-lookup"><span data-stu-id="cdc85-111">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="cdc85-112">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="cdc85-112">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="cdc85-113">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="cdc85-113">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="cdc85-114">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="cdc85-114">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   <span data-ttu-id="cdc85-115">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="cdc85-115">UnregisterMIMEInfo</span></span>
-   [<span data-ttu-id="cdc85-116">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="cdc85-116">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="cdc85-117">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="cdc85-117">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="cdc85-118">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="cdc85-118">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="cdc85-119">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="cdc85-119">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="cdc85-120">Por ejemplo, UnregisterMIMEInfo debe estar antes de [RegisterExtensionInfo](registerextensioninfo-action.md) en la tabla de secuencia.</span><span class="sxs-lookup"><span data-stu-id="cdc85-120">For example, UnregisterMIMEInfo must come before [RegisterExtensionInfo](registerextensioninfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="cdc85-121">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="cdc85-121">ActionData Messages</span></span>



| <span data-ttu-id="cdc85-122">Campo</span><span class="sxs-lookup"><span data-stu-id="cdc85-122">Field</span></span> | <span data-ttu-id="cdc85-123">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="cdc85-123">Description of action data</span></span>                    |
|-------|-----------------------------------------------|
| <span data-ttu-id="cdc85-124">\[1\]</span><span class="sxs-lookup"><span data-stu-id="cdc85-124">\[1\]</span></span> | <span data-ttu-id="cdc85-125">Identificador del tipo de contenido MIME no registrado.</span><span class="sxs-lookup"><span data-stu-id="cdc85-125">Identifier of unregistered MIME content type.</span></span> |
| <span data-ttu-id="cdc85-126">\[2\]</span><span class="sxs-lookup"><span data-stu-id="cdc85-126">\[2\]</span></span> | <span data-ttu-id="cdc85-127">Extensión asociada al tipo de contenido MIME.</span><span class="sxs-lookup"><span data-stu-id="cdc85-127">Extension associated with MIME content type.</span></span>  |



 

 

 



