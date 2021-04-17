---
description: Administrador de recursos de tarjeta inteligente
ms.assetid: 96434996-88fa-47d3-bb44-3ebb23610b27
title: Administrador de recursos de tarjeta inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3ee8e0bf311539863502d3e789544717e6dff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668257"
---
# <a name="smart-card-resource-manager"></a><span data-ttu-id="e1133-103">Administrador de recursos de tarjeta inteligente</span><span class="sxs-lookup"><span data-stu-id="e1133-103">Smart Card Resource Manager</span></span>

<span data-ttu-id="e1133-104">El [*Administrador de recursos*](../secgloss/r-gly.md) de [*tarjeta inteligente*](../secgloss/s-gly.md) administra el acceso a los [*lectores*](../secgloss/r-gly.md) y a las *tarjetas inteligentes*.</span><span class="sxs-lookup"><span data-stu-id="e1133-104">The [*smart card*](../secgloss/s-gly.md) [*resource manager*](../secgloss/r-gly.md) manages access to [*readers*](../secgloss/r-gly.md) and to *smart cards*.</span></span> <span data-ttu-id="e1133-105">Para administrar estos recursos, realiza las siguientes funciones.</span><span class="sxs-lookup"><span data-stu-id="e1133-105">To manage these resources, it performs the following functions.</span></span>

-   <span data-ttu-id="e1133-106">Identifica y realiza un seguimiento de los recursos.</span><span class="sxs-lookup"><span data-stu-id="e1133-106">Identifies and tracks resources.</span></span>
-   <span data-ttu-id="e1133-107">Asigna lectores y recursos entre varias aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="e1133-107">Allocates readers and resources across multiple applications.</span></span>
-   <span data-ttu-id="e1133-108">Admite primitivas de [*transacción*](../secgloss/t-gly.md) para tener acceso a los servicios disponibles en una tarjeta determinada.</span><span class="sxs-lookup"><span data-stu-id="e1133-108">Supports [*transaction*](../secgloss/t-gly.md) primitives for accessing services available on a given card.</span></span>
    > [!Note]  
    > <span data-ttu-id="e1133-109">Este es un punto importante porque las tarjetas actuales son dispositivos de un solo subproceso, que a menudo requieren la ejecución de varios comandos para completar una sola función.</span><span class="sxs-lookup"><span data-stu-id="e1133-109">This is an important point because current cards are single-threaded devices that often require the execution of multiple commands to complete a single function.</span></span> <span data-ttu-id="e1133-110">[*Las transacciones*](../secgloss/t-gly.md) permiten que se ejecuten varios comandos sin interrupción, lo que garantiza que la información de [*Estado*](../secgloss/s-gly.md) intermedio no esté dañada.</span><span class="sxs-lookup"><span data-stu-id="e1133-110">[*Transactions*](../secgloss/t-gly.md) allow multiple commands to be executed without interruption, ensuring that intermediate [*state*](../secgloss/s-gly.md) information is not corrupted.</span></span>

     

<span data-ttu-id="e1133-111">Se puede acceder directamente al administrador de recursos mediante la API de Resource Manager o indirectamente a través de cualquier [*proveedor de servicios*](../secgloss/s-gly.md)de tarjetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="e1133-111">The resource manager can be accessed directly by way of the resource manager API or indirectly through any smart card [*service provider*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="e1133-112">La API de Resource Manager es un conjunto de funciones de Windows que proporcionan acceso directo a los servicios del administrador de recursos.</span><span class="sxs-lookup"><span data-stu-id="e1133-112">The resource manager API is a set of Windows functions that provide direct access to the resource manager's services.</span></span> <span data-ttu-id="e1133-113">Para obtener información general sobre las funciones de Windows proporcionadas por la API, consulte [API de administrador de recursos de tarjetas inteligentes](smart-card-resource-manager-api.md).</span><span class="sxs-lookup"><span data-stu-id="e1133-113">For an overview of the Windows functions provided by the API, see [Smart Card Resource Manager API](smart-card-resource-manager-api.md).</span></span> <span data-ttu-id="e1133-114">En comparación, los proveedores de servicios de tarjetas inteligentes usan interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="e1133-114">In comparison, smart card service providers use COM interfaces.</span></span>

<span data-ttu-id="e1133-115">Muchas de las funciones de Windows de la API de Resource Manager tienen equivalentes en las propiedades y los métodos de las interfaces COM de los proveedores de servicios de tarjetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="e1133-115">Many of the Windows functions in the resource manager API have equivalents in the properties and methods of the smart card service providers' COM interfaces.</span></span> <span data-ttu-id="e1133-116">Además, aunque la mayoría de los desarrolladores de aplicaciones encontrarán que COM es más fácil de trabajar con, algunas aplicaciones seguirán necesitando usar las funciones de Windows para realizar determinadas tareas.</span><span class="sxs-lookup"><span data-stu-id="e1133-116">And although most application developers will find COM easier to work with, some applications will still need to use the Windows functions to perform certain tasks.</span></span> <span data-ttu-id="e1133-117">Por ejemplo, las aplicaciones que necesitan manipular la lista de lectores o grupos de lectores en la [*base de datos de tarjetas inteligentes*](../secgloss/s-gly.md), y las que necesitan el control directo de un lector, deben usar la API de Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="e1133-117">For example, applications that need to manipulate the list of readers or reader groups in the [*smart card database*](../secgloss/s-gly.md), and those that need direct control of a reader, must use the resource manager API.</span></span> <span data-ttu-id="e1133-118">Los servicios que proporcionan estas funciones solo están disponibles en las funciones de Windows, no en el COM proporcionado por los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="e1133-118">The services that provide these capabilities are available only in the Windows functions, not in the COM provided by the service providers.</span></span>

<span data-ttu-id="e1133-119">Para obtener información sobre cómo se implementa el [*Administrador de recursos*](../secgloss/r-gly.md) en Windows, consulte [Administrador de recursos implementación](resource-manager-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="e1133-119">For information about how the [*resource manager*](../secgloss/r-gly.md) is implemented in Windows, see [Resource Manager Implementation](resource-manager-implementation.md).</span></span>

 

 
