---
title: Grupos de funciones de administración de red
description: Las funciones de administración de red se pueden dividir en los siguientes grupos.
ms.assetid: 4b5d3554-f81a-4ecf-bf31-ee4753509f38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bce5c0fb3dd70facb0ebbbb2479b968d428c49e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077922"
---
# <a name="network-management-function-groups"></a><span data-ttu-id="700ac-103">Grupos de funciones de administración de red</span><span class="sxs-lookup"><span data-stu-id="700ac-103">Network Management Function Groups</span></span>

<span data-ttu-id="700ac-104">Las funciones de administración de red se pueden dividir en los siguientes grupos:</span><span class="sxs-lookup"><span data-stu-id="700ac-104">The network management functions can be divided into the following groups:</span></span>

-   [<span data-ttu-id="700ac-105">Funciones de alerta</span><span class="sxs-lookup"><span data-stu-id="700ac-105">Alert functions</span></span>](alert-functions.md)
-   [<span data-ttu-id="700ac-106">Funciones de ApiBuffer</span><span class="sxs-lookup"><span data-stu-id="700ac-106">ApiBuffer functions</span></span>](apibuffer-functions.md)
-   [<span data-ttu-id="700ac-107">Funciones del servicio de directorio</span><span class="sxs-lookup"><span data-stu-id="700ac-107">Directory Service functions</span></span>](directory-service-functions.md)
-   [<span data-ttu-id="700ac-108">Funciones de Sistema de archivos distribuido (DFS)</span><span class="sxs-lookup"><span data-stu-id="700ac-108">Distributed File System (Dfs) functions</span></span>](/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions)
-   [<span data-ttu-id="700ac-109">Funciones Get</span><span class="sxs-lookup"><span data-stu-id="700ac-109">Get functions</span></span>](get-functions.md)
-   [<span data-ttu-id="700ac-110">Funciones de grupo</span><span class="sxs-lookup"><span data-stu-id="700ac-110">Group functions</span></span>](group-functions.md)
-   [<span data-ttu-id="700ac-111">Funciones de grupo local</span><span class="sxs-lookup"><span data-stu-id="700ac-111">Local group functions</span></span>](local-group-functions.md)
-   [<span data-ttu-id="700ac-112">Funciones de mensaje</span><span class="sxs-lookup"><span data-stu-id="700ac-112">Message functions</span></span>](message-functions.md)
-   [<span data-ttu-id="700ac-113">Funciones de NetFile</span><span class="sxs-lookup"><span data-stu-id="700ac-113">NetFile functions</span></span>](netfile-functions.md)
-   [<span data-ttu-id="700ac-114">Funciones de utilidad remota</span><span class="sxs-lookup"><span data-stu-id="700ac-114">Remote Utility functions</span></span>](remote-utility-functions.md)
-   [<span data-ttu-id="700ac-115">Funciones de programación</span><span class="sxs-lookup"><span data-stu-id="700ac-115">Schedule functions</span></span>](schedule-functions.md)
-   [<span data-ttu-id="700ac-116">Funciones de servidor</span><span class="sxs-lookup"><span data-stu-id="700ac-116">Server functions</span></span>](server-functions.md)
-   [<span data-ttu-id="700ac-117">Funciones de transporte de servidor y estación de trabajo</span><span class="sxs-lookup"><span data-stu-id="700ac-117">Server and workstation transport functions</span></span>](server-and-workstation-transport-functions.md)
-   [<span data-ttu-id="700ac-118">Funciones de sesión</span><span class="sxs-lookup"><span data-stu-id="700ac-118">Session functions</span></span>](session-functions.md)
-   [<span data-ttu-id="700ac-119">Funciones de uso compartido</span><span class="sxs-lookup"><span data-stu-id="700ac-119">Share functions</span></span>](share-functions.md)
-   [<span data-ttu-id="700ac-120">Funciones de estadísticas</span><span class="sxs-lookup"><span data-stu-id="700ac-120">Statistics functions</span></span>](/windows/desktop/NetShare/statistics-functions)
-   [<span data-ttu-id="700ac-121">Uso de las funciones</span><span class="sxs-lookup"><span data-stu-id="700ac-121">Use functions</span></span>](use-functions.md)
-   [<span data-ttu-id="700ac-122">Funciones de usuario</span><span class="sxs-lookup"><span data-stu-id="700ac-122">User functions</span></span>](user-functions.md)
-   [<span data-ttu-id="700ac-123">Funciones modales de usuario</span><span class="sxs-lookup"><span data-stu-id="700ac-123">User modal functions</span></span>](user-modal-functions.md)
-   [<span data-ttu-id="700ac-124">Funciones de usuario de estación de trabajo y estación de trabajo</span><span class="sxs-lookup"><span data-stu-id="700ac-124">Workstation and workstation user functions</span></span>](workstation-and-workstation-user-functions.md)

<span data-ttu-id="700ac-125">Si programa para Active Directory, es posible que pueda llamar a determinados métodos de la interfaz ADSI para lograr la misma funcionalidad que puede lograr mediante una llamada a determinadas funciones de administración de red.</span><span class="sxs-lookup"><span data-stu-id="700ac-125">If you are programming for Active Directory, you may be able to call certain ADSI interface methods to achieve the same functionality you can achieve by calling certain network management functions.</span></span> <span data-ttu-id="700ac-126">Para obtener más información, consulte [asignación de interfaces ADSI a las funciones de administración de redes](mapping-adsi-interfaces-to-the-network-management-functions.md).</span><span class="sxs-lookup"><span data-stu-id="700ac-126">For more information, see [Mapping ADSI Interfaces to the Network Management Functions](mapping-adsi-interfaces-to-the-network-management-functions.md).</span></span>

<span data-ttu-id="700ac-127">El sistema también proporciona un conjunto independiente de la red de funciones de red ([funciones de WNet](/windows/desktop/WNet/wnet-functions)) que permiten a las funciones de red trabajar en productos de distintos proveedores de red.</span><span class="sxs-lookup"><span data-stu-id="700ac-127">The system also provides a network-independent set of network functions ([WNet functions](/windows/desktop/WNet/wnet-functions)) that allow network functions to work across different network vendors' products.</span></span> <span data-ttu-id="700ac-128">Si la aplicación se puede convertir para usar una función de WNet, debe realizar la conversión.</span><span class="sxs-lookup"><span data-stu-id="700ac-128">If your application could be converted to use a WNet function, you should perform the conversion.</span></span> <span data-ttu-id="700ac-129">Hay motivos para hacer el cambio:</span><span class="sxs-lookup"><span data-stu-id="700ac-129">There are reasons to make the change:</span></span>

-   <span data-ttu-id="700ac-130">Las funciones de WNet son independientes de la red, mientras que las funciones de administración de red solo funcionan en redes de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="700ac-130">The WNet functions are network independent, while the network management functions work only on Microsoft networks.</span></span>
-   <span data-ttu-id="700ac-131">Es posible que algunas de las funciones no se admitan en futuras versiones de los sistemas operativos de Microsoft si se han sustituido.</span><span class="sxs-lookup"><span data-stu-id="700ac-131">Some of the functions may not be supported in future releases of Microsoft operating systems if they have been superseded.</span></span> <span data-ttu-id="700ac-132">Microsoft no planea quitar funciones específicas a menos que esté disponible una funcionalidad equivalente o mejor.</span><span class="sxs-lookup"><span data-stu-id="700ac-132">Microsoft does not plan to remove specific functions unless equivalent or better functionality is available.</span></span>

 

 