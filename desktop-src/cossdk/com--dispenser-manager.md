---
description: El administrador dispensador proporciona la agrupación de recursos para los dispensadores de recursos y garantiza que un recurso proporcionado por un dispensador de recursos esté correctamente dado de alta en la transacción de objetos de la aplicación.
ms.assetid: c8986943-56a1-4668-9e80-7ab2a42333a8
title: Administrador del dispensador de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2422b7debb8ee12ed97444f3b16f31e663e1e71
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538836"
---
# <a name="com-dispenser-manager"></a><span data-ttu-id="84793-103">Administrador del dispensador de COM+</span><span class="sxs-lookup"><span data-stu-id="84793-103">COM+ Dispenser Manager</span></span>

<span data-ttu-id="84793-104">El gestor del dispensador proporciona la agrupación de recursos para los dispensadores de recursos y garantiza que un recurso proporcionado por un dispensador de recursos está correctamente dado de alta en la transacción del objeto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="84793-104">The dispenser manager provides resource pooling for the resource dispensers and ensures that a resource supplied by a resource dispenser is correctly enlisted in the application object's transaction.</span></span> <span data-ttu-id="84793-105">El administrador del dispensador reclama automáticamente los recursos que aún se reservan al final de la duración de un objeto, lo que elimina la posibilidad de que se produzcan pérdidas de recursos.</span><span class="sxs-lookup"><span data-stu-id="84793-105">The dispenser manager automatically reclaims resources that are still reserved at the end of an object's lifetime, eliminating the possibility of resource "leaks."</span></span> <span data-ttu-id="84793-106">El gestor dispensador puede pedir a un dispensador de recursos que cree un nuevo recurso o destruya los recursos inactivos cuando sea necesario para ajustar los niveles de inventario, en lugar de usar valores estáticos.</span><span class="sxs-lookup"><span data-stu-id="84793-106">The dispenser manager can ask a resource dispenser to create a new resource or to destroy idle resources when necessary to adjust inventory levels, rather than using static settings.</span></span>

> [!Note]  
> <span data-ttu-id="84793-107">Dado que las interfaces dispensadoras de recursos expuestas a la aplicación no deben ser interfaces COM, el administrador dispensador se puede usar en un proceso sin inicializar COM, por ejemplo, para admitir el dispensador de recursos ODBC.</span><span class="sxs-lookup"><span data-stu-id="84793-107">Because resource dispenser interfaces exposed to the application are not required to be COM interfaces, the dispenser manager can be used in a process without initializing COM, for example, to support the ODBC resource dispenser.</span></span>

 

<span data-ttu-id="84793-108">Tras la creación de recursos, el dispensador de recursos puede especificar cuánto tiempo se permite que un recurso inactivo permanezca en el grupo antes de que se destruya.</span><span class="sxs-lookup"><span data-stu-id="84793-108">Upon resource creation, the resource dispenser may specify how long an idle resource is allowed to remain in the pool before it's destroyed.</span></span> <span data-ttu-id="84793-109">Un subproceso que se ejecuta en el administrador dispensador siempre busca estos recursos inactivos.</span><span class="sxs-lookup"><span data-stu-id="84793-109">A thread that runs in the dispenser manager is always looking for these idle resources.</span></span>

## <a name="the-inventory-statistics-manager"></a><span data-ttu-id="84793-110">Administrador de estadísticas de inventario</span><span class="sxs-lookup"><span data-stu-id="84793-110">The Inventory Statistics Manager</span></span>

<span data-ttu-id="84793-111">El gestor del dispensador utiliza el *Administrador de estadísticas de inventario* para administrar los niveles de inventario de recursos del grupo.</span><span class="sxs-lookup"><span data-stu-id="84793-111">The dispenser manager uses the *inventory statistics manager* to manage pool resource inventory levels.</span></span> <span data-ttu-id="84793-112">El administrador de estadísticas de inventario mantiene un registro de Cuándo se usó cada recurso y quita los recursos del inventario cuando no se han usado durante *x* segundos, donde el valor de *x* se establece por recurso cuando se crea el recurso.</span><span class="sxs-lookup"><span data-stu-id="84793-112">The inventory statistics manager maintains a record of when each resource was used and removes resources from inventory when they have not been used for *x* seconds, where the value of *x* is set per resource when the resource is created.</span></span>

## <a name="the-holder-component"></a><span data-ttu-id="84793-113">Componente de titular</span><span class="sxs-lookup"><span data-stu-id="84793-113">The Holder Component</span></span>

<span data-ttu-id="84793-114">El administrador del dispensador sondea cada *titular*, un componente creado por el administrador del dispensador que muestra el inventario de recursos de cada dispensador de recursos, cada 10 segundos, para que pueda reajustar su inventario de recursos.</span><span class="sxs-lookup"><span data-stu-id="84793-114">The dispenser manager polls each *holder*, a component created by the dispenser manager that lists the resource inventory for each resource dispenser, every 10 seconds to allow it to readjust its resource inventory.</span></span> <span data-ttu-id="84793-115">Cada titular llama a Inventory Statistics Manager para sugerir niveles de inventario para cada tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="84793-115">Each holder calls the inventory statistics manager to suggest inventory levels for each type of resource.</span></span> <span data-ttu-id="84793-116">Como resultado, el titular puede pedir al dispensador de recursos que cree o destruya algún inventario.</span><span class="sxs-lookup"><span data-stu-id="84793-116">As a result, the holder may ask the resource dispenser to either create or destroy some inventory.</span></span>

<span data-ttu-id="84793-117">El titular y el dispensador de recursos se comunican con los recursos de solicitud de un tipo determinado.</span><span class="sxs-lookup"><span data-stu-id="84793-117">The holder and resource dispenser communicate to request resources of a particular type.</span></span> <span data-ttu-id="84793-118">Las siguientes relaciones existen entre el titular y el dispensador de recursos:</span><span class="sxs-lookup"><span data-stu-id="84793-118">The following relationships exist between the holder and resource dispenser:</span></span>

-   <span data-ttu-id="84793-119">El titular puede solicitar un recurso desde el dispensador de recursos.</span><span class="sxs-lookup"><span data-stu-id="84793-119">The holder can request a resource from the resource dispenser.</span></span> <span data-ttu-id="84793-120">El dispensador de recursos devuelve un recurso disponible o crea uno nuevo.</span><span class="sxs-lookup"><span data-stu-id="84793-120">The resource dispenser either returns an available resource or creates a new one.</span></span>
-   <span data-ttu-id="84793-121">El titular puede notificar al dispensador de recursos que una aplicación ya no necesita un recurso y, a continuación, devolverlo al grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="84793-121">The holder can notify the resource dispenser that an application no longer needs a resource and then return it to the resource pool.</span></span>
-   <span data-ttu-id="84793-122">El titular y el dispensador de recursos trabajan juntos para mantener el tamaño del grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="84793-122">The holder and the resource dispenser work together to maintain the size of the resource pool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="84793-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="84793-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84793-124">Conceptos del dispensador de recursos COM+</span><span class="sxs-lookup"><span data-stu-id="84793-124">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



