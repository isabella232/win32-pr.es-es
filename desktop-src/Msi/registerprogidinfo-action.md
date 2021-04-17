---
description: La acción RegisterProgIdInfo administra el registro de información de identificador de ensamblado OLE con el sistema.
ms.assetid: f6fd4d0d-d2dc-4953-9402-314c7932746b
title: Acción RegisterProgIdInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c7d53ca4c4125c6ebfc4d089c1c5a0934f9a58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652667"
---
# <a name="registerprogidinfo-action"></a><span data-ttu-id="65949-103">Acción RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="65949-103">RegisterProgIdInfo Action</span></span>

<span data-ttu-id="65949-104">La acción RegisterProgIdInfo administra el registro de información de identificador de ensamblado OLE con el sistema.</span><span class="sxs-lookup"><span data-stu-id="65949-104">The RegisterProgIdInfo action manages the registration of OLE ProgId information with the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="65949-105">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="65949-105">Sequence Restrictions</span></span>

<span data-ttu-id="65949-106">La acción RegisterProgIdInfo debe aparecer después de la acción [InstallFiles](installfiles-action.md) , la acción [UnregisterProgIdInfo](unregisterprogidinfo-action.md) , la acción [RegisterClassInfo](registerclassinfo-action.md) y la acción [RegisterExtensionInfo](registerextensioninfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="65949-106">The RegisterProgIdInfo action must come after the [InstallFiles](installfiles-action.md) action, [UnregisterProgIdInfo](unregisterprogidinfo-action.md) action, [RegisterClassInfo](registerclassinfo-action.md) action, and the [RegisterExtensionInfo](registerextensioninfo-action.md) action.</span></span>

<span data-ttu-id="65949-107">La secuenciación de las acciones del grupo siguiente está restringida.</span><span class="sxs-lookup"><span data-stu-id="65949-107">The sequencing of the actions in the following group is restricted.</span></span> <span data-ttu-id="65949-108">Si un subconjunto de estas acciones se produce juntos en una tabla de secuencia, deben tener el mismo orden de secuencia relativo que se muestra:</span><span class="sxs-lookup"><span data-stu-id="65949-108">If any subset of these actions occur together in a sequence table, they must have the same relative sequence order as shown:</span></span>

-   [<span data-ttu-id="65949-109">UnregisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="65949-109">UnregisterClassInfo</span></span>](unregisterclassinfo-action.md)
-   [<span data-ttu-id="65949-110">UnregisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="65949-110">UnregisterExtensionInfo</span></span>](unregisterextensioninfo-action.md)
-   [<span data-ttu-id="65949-111">UnregisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="65949-111">UnregisterProgIdInfo</span></span>](unregisterprogidinfo-action.md)
-   [<span data-ttu-id="65949-112">UnregisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="65949-112">UnregisterMIMEInfo</span></span>](unregistermimeinfo-action.md)
-   [<span data-ttu-id="65949-113">RegisterClassInfo</span><span class="sxs-lookup"><span data-stu-id="65949-113">RegisterClassInfo</span></span>](registerclassinfo-action.md)
-   [<span data-ttu-id="65949-114">RegisterExtensionInfo</span><span class="sxs-lookup"><span data-stu-id="65949-114">RegisterExtensionInfo</span></span>](registerextensioninfo-action.md)
-   <span data-ttu-id="65949-115">RegisterProgIdInfo</span><span class="sxs-lookup"><span data-stu-id="65949-115">RegisterProgIdInfo</span></span>
-   [<span data-ttu-id="65949-116">RegisterMIMEInfo</span><span class="sxs-lookup"><span data-stu-id="65949-116">RegisterMIMEInfo</span></span>](registermimeinfo-action.md)

<span data-ttu-id="65949-117">Por ejemplo, RegisterProgIdInfo debe aparecer después de [RegisterExtensionInfo](registerextensioninfo-action.md) en la tabla de secuencia.</span><span class="sxs-lookup"><span data-stu-id="65949-117">For example, RegisterProgIdInfo must come after [RegisterExtensionInfo](registerextensioninfo-action.md) in the sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="65949-118">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="65949-118">ActionData Messages</span></span>



| <span data-ttu-id="65949-119">Campo</span><span class="sxs-lookup"><span data-stu-id="65949-119">Field</span></span> | <span data-ttu-id="65949-120">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="65949-120">Description of action data</span></span>                |
|-------|-------------------------------------------|
| <span data-ttu-id="65949-121">\[1\]</span><span class="sxs-lookup"><span data-stu-id="65949-121">\[1\]</span></span> | <span data-ttu-id="65949-122">Identificador de programa del programa registrado.</span><span class="sxs-lookup"><span data-stu-id="65949-122">Program identifier of registered program.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="65949-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65949-123">Remarks</span></span>

<span data-ttu-id="65949-124">La acción RegisterProgIdInfo registra toda la información de ProgId para los servidores que se especifican en la [tabla ProgID](progid-table.md) y para los que se ha seleccionado el servidor de la clase o el servidor de extensiones correspondiente para su instalación.</span><span class="sxs-lookup"><span data-stu-id="65949-124">The RegisterProgIdInfo action registers all ProgId information for servers that are specified in the [ProgId table](progid-table.md) and for which the corresponding class server or extension server has been selected to be installed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="65949-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="65949-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65949-126">Tabla de clases</span><span class="sxs-lookup"><span data-stu-id="65949-126">Class table</span></span>](class-table.md)
</dt> <dt>

[<span data-ttu-id="65949-127">Tabla de extensión</span><span class="sxs-lookup"><span data-stu-id="65949-127">Extension table</span></span>](extension-table.md)
</dt> </dl>

 

 



