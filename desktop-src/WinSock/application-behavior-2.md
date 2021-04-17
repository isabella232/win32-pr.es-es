---
description: Otro aspecto del desarrollo de aplicaciones que se debe tener en cuenta es la diferencia entre el comportamiento entre las operaciones locales o dentro de un equipo, y el comportamiento cuando las operaciones tienen lugar entre dos equipos conectados en red.
ms.assetid: e6f48446-948c-458c-8ecf-04ffb249c8a4
title: Comportamiento de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a9b871a2c0535d9ef4220824651657332a224a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541643"
---
# <a name="application-behavior"></a><span data-ttu-id="5b323-103">Comportamiento de la aplicación</span><span class="sxs-lookup"><span data-stu-id="5b323-103">Application Behavior</span></span>

<span data-ttu-id="5b323-104">Otro aspecto del desarrollo de aplicaciones que se debe tener en cuenta es la diferencia entre el comportamiento entre las operaciones locales o dentro de un equipo, y el comportamiento cuando las operaciones tienen lugar entre dos equipos conectados en red.</span><span class="sxs-lookup"><span data-stu-id="5b323-104">Another aspect of application development to consider is the difference in behavior between local, or intracomputer operations, and behavior when operations take place between two networked computers.</span></span> <span data-ttu-id="5b323-105">Hay comportamientos de aplicación que pueden funcionar bastante bien en un equipo local, pero cuando se ejecutan a través de una red, causan una degradación significativa del rendimiento y el consumo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5b323-105">There are application behaviors that may work acceptably well on a local computer, but when run across a network, cause significant performance degradation and resource consumption.</span></span> <span data-ttu-id="5b323-106">Los siguientes comportamientos de la aplicación deben evitarse al desarrollar aplicaciones de Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="5b323-106">The following application behaviors should be avoided when developing Windows Sockets applications.</span></span>

## <a name="behaviors-to-avoid"></a><span data-ttu-id="5b323-107">Comportamientos que se deben evitar</span><span class="sxs-lookup"><span data-stu-id="5b323-107">Behaviors to Avoid</span></span>

-   <span data-ttu-id="5b323-108">Aplicaciones de chat.</span><span class="sxs-lookup"><span data-stu-id="5b323-108">Chatty Applications.</span></span>

    <span data-ttu-id="5b323-109">Algunas aplicaciones realizan muchas transacciones pequeñas.</span><span class="sxs-lookup"><span data-stu-id="5b323-109">Some applications perform many small transactions.</span></span> <span data-ttu-id="5b323-110">Cuando se combina con la sobrecarga de red asociada a cada una de estas transacciones, se multiplica el efecto.</span><span class="sxs-lookup"><span data-stu-id="5b323-110">When combined with the network overhead associated with each such transaction, the effect is multiplied.</span></span> <span data-ttu-id="5b323-111">En las redes, las transacciones pequeñas pueden consumir tantos recursos como mucho tiempo como transacciones grandes.</span><span class="sxs-lookup"><span data-stu-id="5b323-111">In networking, small transactions can consume as many resources and as much time as large transactions.</span></span> <span data-ttu-id="5b323-112">Un mejor enfoque consiste en combinar muchas transacciones pequeñas en una única transacción grande.</span><span class="sxs-lookup"><span data-stu-id="5b323-112">A better approach is to combine many small transactions into a single large transaction.</span></span>

-   <span data-ttu-id="5b323-113">Transacciones serializadas.</span><span class="sxs-lookup"><span data-stu-id="5b323-113">Serialized Transactions.</span></span>

    <span data-ttu-id="5b323-114">Una serialización innecesaria de transacciones puede dar lugar a un rendimiento deficiente y afectar a la escalabilidad.</span><span class="sxs-lookup"><span data-stu-id="5b323-114">Unnecessary serialization of transactions can result in poor performance, and affect scalability.</span></span> <span data-ttu-id="5b323-115">Por ejemplo, 1000 las transacciones serializadas tardan al menos 1000 \* RTT en completarse.</span><span class="sxs-lookup"><span data-stu-id="5b323-115">For example, 1000 serialized transactions take at least 1000 \* RTT to complete.</span></span> <span data-ttu-id="5b323-116">Un mejor enfoque consiste en ejecutar transacciones no relacionadas en paralelo.</span><span class="sxs-lookup"><span data-stu-id="5b323-116">A better approach is to run unrelated transactions in parallel.</span></span> <span data-ttu-id="5b323-117">Cuando las aplicaciones serializadas se combinan con aplicaciones de chat, la capacidad de respuesta puede verse seriamente obstaculizada.</span><span class="sxs-lookup"><span data-stu-id="5b323-117">When serialized applications are combined with chatty applications, responsiveness can be seriously hampered.</span></span>

    > [!Note]  
    > <span data-ttu-id="5b323-118">La deserialización correcta de una aplicación puede ser difícil.</span><span class="sxs-lookup"><span data-stu-id="5b323-118">Properly deserializing an application can be difficult.</span></span> <span data-ttu-id="5b323-119">Si el cambio de serializado a paralelo resulta demasiado difícil, considere la posibilidad de combinar varias transacciones en menos transacciones de gran tamaño.</span><span class="sxs-lookup"><span data-stu-id="5b323-119">If changing from serialized to parallel proves too difficult, consider combining multiple transactions into fewer large transactions.</span></span>

     

-   <span data-ttu-id="5b323-120">Transacciones FAT.</span><span class="sxs-lookup"><span data-stu-id="5b323-120">Fat Transactions.</span></span>

    <span data-ttu-id="5b323-121">Las aplicaciones que envían bytes innecesarios en la red se consideran aplicaciones FAT.</span><span class="sxs-lookup"><span data-stu-id="5b323-121">Applications that send unnecessary bytes on the network are considered fat applications.</span></span> <span data-ttu-id="5b323-122">Las aplicaciones que envían bytes innecesarios en la red aumentan la sobrecarga de la red y se obstaculiza el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="5b323-122">Applications that send unnecessary bytes on the network increase network overhead, and performance is hampered.</span></span> <span data-ttu-id="5b323-123">Esta situación suele proceder de estructuras de datos ineficaces o de un flujo de datos ineficaz.</span><span class="sxs-lookup"><span data-stu-id="5b323-123">This situation often comes from inefficient data structures or inefficient data streaming.</span></span> <span data-ttu-id="5b323-124">Para solucionarlo, optimice las estructuras de datos o considere la posibilidad de usar la compresión.</span><span class="sxs-lookup"><span data-stu-id="5b323-124">To remedy this, optimize data structures, or consider using compression.</span></span>

<span data-ttu-id="5b323-125">En las secciones siguientes se tratan aspectos del desarrollo de aplicaciones que se deben tener en cuenta.</span><span class="sxs-lookup"><span data-stu-id="5b323-125">The following sections address aspects of application development to consider.</span></span>

-   [<span data-ttu-id="5b323-126">Problemas específicos de TCP/IP</span><span class="sxs-lookup"><span data-stu-id="5b323-126">TCP/IP-specific Issues</span></span>](tcp-ip-specific-issues-2.md)
-   [<span data-ttu-id="5b323-127">Reconocer aplicaciones lentas</span><span class="sxs-lookup"><span data-stu-id="5b323-127">Recognizing Slow Applications</span></span>](recognizing-slow-applications-2.md)
-   [<span data-ttu-id="5b323-128">Calcular la sobrecarga con netstat</span><span class="sxs-lookup"><span data-stu-id="5b323-128">Calculating Overhead with Netstat</span></span>](calculating-overhead-with-netstat-2.md)

## <a name="related-topics"></a><span data-ttu-id="5b323-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5b323-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b323-130">Aplicaciones de Windows Sockets de alto rendimiento</span><span class="sxs-lookup"><span data-stu-id="5b323-130">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



