---
description: El servicio de componentes en cola COM+ es totalmente compatible con el concepto de particiones. Es decir, cuando se ejecuta un componente en cola dentro de una partición, el mensaje se pone en cola y el componente se ejecuta finalmente dentro de la partición de componentes.
ms.assetid: 08b0f7b5-6c45-4471-9634-1f42fbbf500c
title: Particiones y componentes en cola de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 589d7cb7c3e61be8ef53a248f990cde65447cf9d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538614"
---
# <a name="com-queued-components-and-partitions"></a><span data-ttu-id="78f7d-104">Particiones y componentes en cola de COM+</span><span class="sxs-lookup"><span data-stu-id="78f7d-104">COM+ Queued Components and Partitions</span></span>

<span data-ttu-id="78f7d-105">El servicio de componentes en cola COM+ es totalmente compatible con el concepto de particiones.</span><span class="sxs-lookup"><span data-stu-id="78f7d-105">The COM+ queued components service fully supports the concept of partitions.</span></span> <span data-ttu-id="78f7d-106">Es decir, cuando se ejecuta un componente en cola dentro de una partición, el mensaje se pone en cola y el componente se ejecuta finalmente dentro de la partición del componente.</span><span class="sxs-lookup"><span data-stu-id="78f7d-106">That is, when a queued component within a partition is executed, the message is queued and the component is eventually executed within the component's partition.</span></span>

## <a name="queue-names-for-partitioned-components"></a><span data-ttu-id="78f7d-107">Nombres de cola para componentes con particiones</span><span class="sxs-lookup"><span data-stu-id="78f7d-107">Queue Names for Partitioned Components</span></span>

<span data-ttu-id="78f7d-108">Tradicionalmente, el servicio de componentes en cola utiliza el nombre de la aplicación como el nombre de la cola.</span><span class="sxs-lookup"><span data-stu-id="78f7d-108">Traditionally, the queued components service uses the application name as the queue name.</span></span> <span data-ttu-id="78f7d-109">Esto significa que en un escenario sin particiones, donde solo existe una instancia de un nombre de aplicación en un equipo, cada nombre de aplicación tiene su propia cola de mensajes.</span><span class="sxs-lookup"><span data-stu-id="78f7d-109">This means that in a non-partitions scenario, where only one instance of an application name exists on a computer, each application name has its own message queue.</span></span>

<span data-ttu-id="78f7d-110">Sin embargo, en el caso de las particiones, donde pueden existir varias instancias del mismo nombre de aplicación en un equipo, el servicio de componentes en cola utiliza la misma cola para todos los componentes en cola que comparten el mismo nombre de aplicación.</span><span class="sxs-lookup"><span data-stu-id="78f7d-110">In the case of partitions, however, where multiple instances of the same application name can exist on a computer, the queued components service uses the same queue for any queued components that share the same application name.</span></span>

## <a name="activating-queued-components"></a><span data-ttu-id="78f7d-111">Activar componentes en cola</span><span class="sxs-lookup"><span data-stu-id="78f7d-111">Activating Queued Components</span></span>

<span data-ttu-id="78f7d-112">Las mismas reglas sobre cómo se usa el identificador de partición para activar un componente que no está en cola se aplican a un componente en cola, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="78f7d-112">The same rules for how the partition ID is used to activate a non-queued component applies to a queued component, as follows:</span></span>

-   <span data-ttu-id="78f7d-113">Si se usa un moniker para activar el componente en cola y se incluye un identificador de partición, se utiliza este ID. de partición para ubicar la partición.</span><span class="sxs-lookup"><span data-stu-id="78f7d-113">If a moniker is used to activate the queued component and a partition ID is included, this partition ID is used to locate the partition.</span></span> <span data-ttu-id="78f7d-114">Este identificador de partición tiene prioridad sobre cualquier ID. de partición que pueda existir en el contexto del componente que se está activando.</span><span class="sxs-lookup"><span data-stu-id="78f7d-114">This partition ID takes precedence over any partition ID that might exist in the context for the component being activated.</span></span>
-   <span data-ttu-id="78f7d-115">Si no se usa ningún moniker para activar el componente, se usa el ID. de partición que se encuentra en el contexto del objeto.</span><span class="sxs-lookup"><span data-stu-id="78f7d-115">If no moniker is being used to activate the component, the partition ID that is in the object's context is used.</span></span>
-   <span data-ttu-id="78f7d-116">Si no existe ningún ID. de partición en el contexto del objeto, se usa la asignación de usuario a partición predeterminada dentro de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="78f7d-116">If no partition ID exists in the object's context, the default user-to-partition mapping within Active Directory is used.</span></span>

> [!Note]  
> <span data-ttu-id="78f7d-117">Si un equipo servidor está desconectado de la red y se cambia la asignación de usuario a partición del conjunto mientras el servidor está desconectado, es posible que la memoria caché de particiones contenga una asignación de conjunto de usuario a partición no actualizada.</span><span class="sxs-lookup"><span data-stu-id="78f7d-117">If a server computer is disconnected from the network and if the user-to-partition set mapping is changed while the server is disconnected, the partition cache might contain outdated user-to-partition set mapping.</span></span> <span data-ttu-id="78f7d-118">Esto podría dar lugar a un error de activación si la asignación de un usuario a un conjunto de particiones es el mecanismo usado para activar un componente.</span><span class="sxs-lookup"><span data-stu-id="78f7d-118">This could result in an activation error if user-to-partition set mapping is the mechanism used to activate a component.</span></span>

 

<span data-ttu-id="78f7d-119">Los eventos COM+ están totalmente integrados en las particiones.</span><span class="sxs-lookup"><span data-stu-id="78f7d-119">COM+ events are fully integrated into partitions.</span></span> <span data-ttu-id="78f7d-120">Esto significa que un suscriptor puede suscribirse a un publicador cuya aplicación reside en una partición.</span><span class="sxs-lookup"><span data-stu-id="78f7d-120">This means that a subscriber can subscribe to a publisher whose application resides within a partition.</span></span> <span data-ttu-id="78f7d-121">Para permitir esta suscripción, la colección de clases de suscriptores incluye dos propiedades relacionadas con la partición: un identificador de partición de clase de evento y un identificador de aplicación de clase de evento.</span><span class="sxs-lookup"><span data-stu-id="78f7d-121">To allow this subscription, the subscriber class collection includes two partition-related properties—an event class partition ID and an event class application ID.</span></span>

## <a name="related-topics"></a><span data-ttu-id="78f7d-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="78f7d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78f7d-123">Restricciones de diseño de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="78f7d-123">Application Design Restrictions</span></span>](application-design-restrictions.md)
</dt> <dt>

[<span data-ttu-id="78f7d-124">Implementación de particiones</span><span class="sxs-lookup"><span data-stu-id="78f7d-124">Partition Implementation</span></span>](partition-implementation.md)
</dt> <dt>

[<span data-ttu-id="78f7d-125">Registro y activación de componentes en particiones</span><span class="sxs-lookup"><span data-stu-id="78f7d-125">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[<span data-ttu-id="78f7d-126">¿Qué son las particiones COM+?</span><span class="sxs-lookup"><span data-stu-id="78f7d-126">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
</dt> </dl>

 

 



