---
description: Por lo general, la sincronización no es necesaria cuando se tiene un contenedor uniproceso (STA) porque el apartamento proporciona la sincronización automáticamente.
ms.assetid: a05de040-0115-44aa-80e2-55eff2ec894d
title: Conceptos de sincronización de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eaca81050e67c76e3de6ad4845543b9230d2a24
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807808"
---
# <a name="com-synchronization-concepts"></a><span data-ttu-id="02ad3-103">Conceptos de sincronización de COM+</span><span class="sxs-lookup"><span data-stu-id="02ad3-103">COM+ Synchronization Concepts</span></span>

<span data-ttu-id="02ad3-104">Por lo general, la sincronización no es necesaria cuando se tiene un contenedor uniproceso (STA) porque el apartamento proporciona la sincronización automáticamente.</span><span class="sxs-lookup"><span data-stu-id="02ad3-104">Generally, synchronization is not required when you have a single-threaded apartment (STA) because the apartment provides the synchronization for you.</span></span> <span data-ttu-id="02ad3-105">La sincronización es importante cuando tiene un contenedor multiproceso (MTA) y un objeto de subproceso libre.</span><span class="sxs-lookup"><span data-stu-id="02ad3-105">Synchronization becomes important when you have a multithreaded apartment (MTA) and a free-threaded object.</span></span> <span data-ttu-id="02ad3-106">En el pasado, los objetos de subprocesamiento libre tenían que controlar el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="02ad3-106">In the past, free-threaded objects have had to handle locking.</span></span> <span data-ttu-id="02ad3-107">Puede eliminar la necesidad de usar el bloqueo estableciendo el atributo de sincronización de un componente.</span><span class="sxs-lookup"><span data-stu-id="02ad3-107">You can eliminate the need to use locking by setting the synchronization attribute for a component.</span></span>

<span data-ttu-id="02ad3-108">La sincronización tiene las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="02ad3-108">Synchronization has the following properties:</span></span>

-   <span data-ttu-id="02ad3-109">Permite a un llamador entrar en el componente a la vez.</span><span class="sxs-lookup"><span data-stu-id="02ad3-109">Allows one caller to enter the component at a time.</span></span>
-   <span data-ttu-id="02ad3-110">Prohíbe el flujo a través del proceso o entre equipos.</span><span class="sxs-lookup"><span data-stu-id="02ad3-110">Prohibits flow across process or across computer.</span></span>
-   <span data-ttu-id="02ad3-111">Fluye del componente al componente dentro de un proceso.</span><span class="sxs-lookup"><span data-stu-id="02ad3-111">Flows from component to component within a process.</span></span>
-   <span data-ttu-id="02ad3-112">Permite la reentrada del mismo llamador.</span><span class="sxs-lookup"><span data-stu-id="02ad3-112">Allows reentrancy from the same caller.</span></span>

<span data-ttu-id="02ad3-113">A diferencia de apartamentos, las actividades abarcan contextos de varios procesos y hosts.</span><span class="sxs-lookup"><span data-stu-id="02ad3-113">Unlike apartments, activities span contexts from multiple processes and hosts.</span></span> <span data-ttu-id="02ad3-114">La sincronización determina qué actividad contendrá un objeto.</span><span class="sxs-lookup"><span data-stu-id="02ad3-114">Synchronization determines which activity will contain an object.</span></span> <span data-ttu-id="02ad3-115">Los objetos pueden residir en cualquiera de las siguientes actividades:</span><span class="sxs-lookup"><span data-stu-id="02ad3-115">Objects can reside in any of the following activities:</span></span>

-   <span data-ttu-id="02ad3-116">Actividad del creador</span><span class="sxs-lookup"><span data-stu-id="02ad3-116">Creator's activity</span></span>
-   <span data-ttu-id="02ad3-117">Nueva actividad</span><span class="sxs-lookup"><span data-stu-id="02ad3-117">New activity</span></span>
-   <span data-ttu-id="02ad3-118">Sin actividad</span><span class="sxs-lookup"><span data-stu-id="02ad3-118">No activity</span></span>

<span data-ttu-id="02ad3-119">COM+ garantiza la simultaneidad mediante una serie de bloqueos para cada actividad.</span><span class="sxs-lookup"><span data-stu-id="02ad3-119">COM+ ensures concurrency by a series of locks for each activity.</span></span> <span data-ttu-id="02ad3-120">Si un llamador intenta entrar en un componente sincronizado de COM+ que ya está siendo utilizado por otro llamador, la llamada se bloquea hasta que se libera el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="02ad3-120">If a caller tries to enter a COM+ synchronized component that is already being used by another caller, the call is blocked until the lock is released.</span></span> <span data-ttu-id="02ad3-121">Este comportamiento de bloqueo no agotará el tiempo de espera y no se puede configurar para que agote el tiempo de espera. Si el bloqueo no está en uso, se adquiere el bloqueo y se procesa la llamada.</span><span class="sxs-lookup"><span data-stu-id="02ad3-121">This blocking behavior will not time out and cannot be configured to time out. If the lock is not in use, the lock is acquired and the call is processed.</span></span> <span data-ttu-id="02ad3-122">Después de completar, se libera el bloqueo para el siguiente autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="02ad3-122">After completing, the lock is released for the next caller.</span></span> <span data-ttu-id="02ad3-123">Para evitar el interbloqueo, COM+ administra el acceso a todos los objetos en todas las actividades mediante una serie anidada de llamadas encadenadas a través de la red.</span><span class="sxs-lookup"><span data-stu-id="02ad3-123">To prevent deadlock, COM+ manages access to all objects across activities by a nested series of calls chained throughout the network.</span></span>

<span data-ttu-id="02ad3-124">COM+ proporciona la siguiente configuración de sincronización:</span><span class="sxs-lookup"><span data-stu-id="02ad3-124">COM+ provides the following synchronization settings:</span></span>

-   <span data-ttu-id="02ad3-125">Disabled</span><span class="sxs-lookup"><span data-stu-id="02ad3-125">Disabled</span></span>
-   <span data-ttu-id="02ad3-126">No compatible</span><span class="sxs-lookup"><span data-stu-id="02ad3-126">Not Supported</span></span>
-   <span data-ttu-id="02ad3-127">Compatible</span><span class="sxs-lookup"><span data-stu-id="02ad3-127">Supported</span></span>
-   <span data-ttu-id="02ad3-128">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="02ad3-128">Required</span></span>
-   <span data-ttu-id="02ad3-129">Se requiere nueva</span><span class="sxs-lookup"><span data-stu-id="02ad3-129">Requires New</span></span>

> [!Note]  
> <span data-ttu-id="02ad3-130">Algunas configuraciones de sincronización funcionan junto con otras configuraciones de componentes de COM+.</span><span class="sxs-lookup"><span data-stu-id="02ad3-130">Some synchronization settings work in conjunction with other COM+ component settings.</span></span> <span data-ttu-id="02ad3-131">Por ejemplo, la sincronización es necesaria si está habilitado el servicio de [activación Just-in-Time (JIT) de com+](com--just-in-time-activation.md) .</span><span class="sxs-lookup"><span data-stu-id="02ad3-131">For example, synchronization is required if the [COM+ just-in-time (JIT) activation](com--just-in-time-activation.md) service is enabled.</span></span> <span data-ttu-id="02ad3-132">JIT es necesario si se habilitan las transacciones; por lo tanto, el [procesamiento de transacciones](com--transactions.md) com+ también requiere sincronización.</span><span class="sxs-lookup"><span data-stu-id="02ad3-132">JIT is required if you enable transactions; therefore, COM+ [transaction processing](com--transactions.md) requires synchronization as well.</span></span> <span data-ttu-id="02ad3-133">Por lo tanto, las clases con la configuración de JIT = true también deben tener el valor de Synchronization = required o Synchronization = RequiresNew.</span><span class="sxs-lookup"><span data-stu-id="02ad3-133">So, classes with the setting of JIT=True must also have the setting of either Synchronization=Required or Synchronization=RequiresNew.</span></span>

 

<span data-ttu-id="02ad3-134">Para obtener instrucciones sobre cómo establecer las opciones de sincronización mediante la herramienta administrativa Servicios de componentes, vea [establecer el atributo de sincronización](setting-the-synchronization-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="02ad3-134">For instructions about setting synchronization options by using the Component Services administrative tool, see [Setting the Synchronization Attribute](setting-the-synchronization-attribute.md).</span></span>

<span data-ttu-id="02ad3-135">Para obtener más información sobre el uso de la biblioteca de administración de COM+ para establecer las opciones de sincronización, vea [automatizar la administración de com+](automating-com--administration.md).</span><span class="sxs-lookup"><span data-stu-id="02ad3-135">To obtain more information on using the COM+ Administration Library to set synchronization options, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="02ad3-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="02ad3-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02ad3-137">Tareas de sincronización de COM+</span><span class="sxs-lookup"><span data-stu-id="02ad3-137">COM+ Synchronization Tasks</span></span>](com--synchronization-tasks.md)
</dt> </dl>

 

 



