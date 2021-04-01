---
description: La acción UnregisterProgIdInfo administra la anulación del registro de información de identificador de programa OLE con el sistema.
ms.assetid: c9837845-4ffc-4496-8330-11b46d27ec7a
title: Acción UnregisterProgIdInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff880c1d339fc3db3db50bd34d3afb828f65ec07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913654"
---
# <a name="unregisterprogidinfo-action"></a><span data-ttu-id="42744-103">Acción UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="42744-103">UnregisterProgIdInfo Action</span></span>

<span data-ttu-id="42744-104">La acción UnregisterProgIdInfo administra la anulación del registro de información de identificador de programa OLE con el sistema.</span><span class="sxs-lookup"><span data-stu-id="42744-104">The UnregisterProgIdInfo action manages the unregistration of OLE ProgId information with the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="42744-105">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="42744-105">Sequence Restrictions</span></span>

<span data-ttu-id="42744-106">La acción UnregisterProgIdInfo debe aparecer después de la acción [InstallInitialize](installinitialize-action.md) , la acción [UnregisterClassInfo](unregisterclassinfo-action.md) , la acción [UnregisterExtensioninfo](unregisterextensioninfo-action.md) y antes de la acción [RegisterProgIdInfo](registerprogidinfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="42744-106">The UnregisterProgIdInfo action must come after the [InstallInitialize](installinitialize-action.md) action, [UnregisterClassInfo](unregisterclassinfo-action.md) action, [UnregisterExtensioninfo](unregisterextensioninfo-action.md) action, and before the [RegisterProgIdInfo](registerprogidinfo-action.md) action.</span></span>

<span data-ttu-id="42744-107">[RemoveRegistryValues](removeregistryvalues-action.md) debe estar delante de UnregisterProgIdInfo en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="42744-107">[RemoveRegistryValues](removeregistryvalues-action.md) must come before UnregisterProgIdInfo in the sequence.</span></span>

<span data-ttu-id="42744-108">La secuenciación de las acciones del grupo siguiente está restringida.</span><span class="sxs-lookup"><span data-stu-id="42744-108">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="42744-109">Si un subconjunto de estas acciones se produce juntos en una tabla de secuencia, deben tener el mismo orden de secuencia relativo que se muestra:</span><span class="sxs-lookup"><span data-stu-id="42744-109">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="42744-110">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="42744-110">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="42744-111">UnregisterExtensioninfo</span><span class="sxs-lookup"><span data-stu-id="42744-111">UnregisterExtensioninfo</span></span>](unregisterextensioninfo-action.md)
-   <span data-ttu-id="42744-112">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="42744-112">UnregisterProgIdInfo</span></span>
-   [<span data-ttu-id="42744-113">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="42744-113">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="42744-114">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="42744-114">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="42744-115">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="42744-115">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   [<span data-ttu-id="42744-116">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="42744-116">RegisterProgIdInfo</span></span>](registerprogidinfo-action.md)
-   [<span data-ttu-id="42744-117">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="42744-117">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="42744-118">Por ejemplo, UnregisterProgIdInfo debe estar antes de [UnregisterMIMEInfo](unregistermimeinfo-action.md) en la tabla de secuencia.</span><span class="sxs-lookup"><span data-stu-id="42744-118">For example, UnregisterProgIdInfo must come before [UnregisterMIMEInfo](unregistermimeinfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="42744-119">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="42744-119">ActionData Messages</span></span>



| <span data-ttu-id="42744-120">Campo</span><span class="sxs-lookup"><span data-stu-id="42744-120">Field</span></span> | <span data-ttu-id="42744-121">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="42744-121">Description of action data</span></span>                |
|-------|-------------------------------------------|
| <span data-ttu-id="42744-122">\[1\]</span><span class="sxs-lookup"><span data-stu-id="42744-122">\[1\]</span></span> | <span data-ttu-id="42744-123">Identificador de programa del programa registrado.</span><span class="sxs-lookup"><span data-stu-id="42744-123">Program identifier of registered program.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="42744-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="42744-124">Remarks</span></span>

<span data-ttu-id="42744-125">La acción UnregisterProgIdInfo quita la información de ProgId del registro ([tabla ProgID](progid-table.md)) para las características que están conectadas a la información de la extensión ([tabla de extensión](extension-table.md)) o a la información de clase (tabla de[clases](class-table.md)) y están seleccionadas actualmente para desinstalarse.</span><span class="sxs-lookup"><span data-stu-id="42744-125">The UnregisterProgIdInfo action removes ProgId information from the registry ([ProgId Table](progid-table.md)) for features that are connected to the extension information ([Extension table](extension-table.md)) or the Class information ([Class table](class-table.md)) and are currently selected to be uninstalled.</span></span>

 

 



