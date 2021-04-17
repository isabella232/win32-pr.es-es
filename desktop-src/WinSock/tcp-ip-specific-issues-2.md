---
description: Algunas técnicas de programación experimentan problemas de rendimiento que están vinculados a la implementación de TCP/IP.
ms.assetid: 2a63e85e-06fd-4b6f-8351-9866099b9d54
title: Problemas específicos de TCP/IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9a7334471d3e419830eb054399ff1dcb721cd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716219"
---
# <a name="tcpip-specific-issues"></a><span data-ttu-id="744d8-103">Problemas específicos de TCP/IP</span><span class="sxs-lookup"><span data-stu-id="744d8-103">TCP/IP-specific Issues</span></span>

<span data-ttu-id="744d8-104">Algunas técnicas de programación experimentan problemas de rendimiento que están vinculados a la implementación de TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="744d8-104">Certain programming techniques run into performance issues that are linked to the implementation of TCP/IP.</span></span> <span data-ttu-id="744d8-105">Estos problemas de rendimiento no sugieren que TCP/IP sea ineficaz o un cuello de botella de rendimiento. en su lugar, estos problemas se ven cuando no se comprenden las operaciones de TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="744d8-105">Such performance issues do not suggest that TCP/IP is inefficient or a performance bottleneck; rather, these issues are seen when TCP/IP operations are not understood.</span></span>

<span data-ttu-id="744d8-106">Los siguientes problemas identifican escenarios comunes en los que la combinación de las opciones de desarrollo de aplicaciones de red y operaciones de TCP/IP da lugar a un rendimiento deficiente.</span><span class="sxs-lookup"><span data-stu-id="744d8-106">The following issues identify common scenarios in which the combination of TCP/IP operation and network application development choices result in poor performance.</span></span>

-   <span data-ttu-id="744d8-107">Aplicaciones de conexión intensivas.</span><span class="sxs-lookup"><span data-stu-id="744d8-107">Connect-heavy Applications.</span></span>

    <span data-ttu-id="744d8-108">Algunas aplicaciones crean una nueva conexión TCP para cada transacción.</span><span class="sxs-lookup"><span data-stu-id="744d8-108">Some applications instantiate a new TCP connection for each transaction.</span></span> <span data-ttu-id="744d8-109">El establecimiento de la conexión TCP lleva tiempo, aporta RTTs adicionales y está sujeto a un inicio lento.</span><span class="sxs-lookup"><span data-stu-id="744d8-109">TCP connection establishment takes time, contributes extra RTTs, and is subject to slow-start.</span></span> <span data-ttu-id="744d8-110">Además, las conexiones cerradas están sujetas a TIME-WAIT, que consume recursos del sistema.</span><span class="sxs-lookup"><span data-stu-id="744d8-110">In addition, the closed connections are subject to TIME-WAIT, which consumes system resources.</span></span>

    <span data-ttu-id="744d8-111">Las aplicaciones con una gran cantidad de conexiones son muy comunes, ya que son fáciles de crear; las pruebas y el control de errores son muy sencillos.</span><span class="sxs-lookup"><span data-stu-id="744d8-111">Connect-heavy applications are common largely because they are easy to create; testing and error handling is very simple.</span></span> <span data-ttu-id="744d8-112">La detección de errores en una conexión persistente puede llevar a cabo un código y un esfuerzo considerables, por lo que a veces no se completa.</span><span class="sxs-lookup"><span data-stu-id="744d8-112">Detecting faults on a persistent connection can take considerable code and effort, and therefore is sometimes not completed.</span></span>

    <span data-ttu-id="744d8-113">Remedy esta situación reutilizando la conexión TCP.</span><span class="sxs-lookup"><span data-stu-id="744d8-113">Remedy this situation by reusing the TCP connection.</span></span> <span data-ttu-id="744d8-114">Esto puede provocar la serialización a través de la conexión TCP a menos que las transacciones se multiplexan en varias conexiones.</span><span class="sxs-lookup"><span data-stu-id="744d8-114">This may cause serialization over the TCP connection unless the transactions are multiplexed over multiple connections.</span></span> <span data-ttu-id="744d8-115">Si se toma este enfoque, el número de conexiones se debe limitar a dos, y las tramas de capa de aplicación y el control de errores avanzado son obligatorios.</span><span class="sxs-lookup"><span data-stu-id="744d8-115">If this approach is taken, the number of connections should be limited to two, and application-layer framing and advanced error handling are required.</span></span>

-   <span data-ttu-id="744d8-116">Búferes de envío de longitud cero y envíos de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="744d8-116">Zero-length Send Buffers and Blocking Sends.</span></span>

    <span data-ttu-id="744d8-117">La desactivación del almacenamiento en búfer mediante [**la función de**](/windows/desktop/api/winsock/nf-winsock-setsockopt) SNDBUF para establecer el búfer de envío (de modo que \_ ) en cero es similar a desactivar el almacenamiento en caché de disco.</span><span class="sxs-lookup"><span data-stu-id="744d8-117">Turning off buffering by using the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function to set the send buffer (SO\_SNDBUF) to zero is similar to turning off disk caching.</span></span> <span data-ttu-id="744d8-118">Al establecer el búfer de envío en cero y emitir envíos de bloqueo, una aplicación tiene un 50 por ciento de probabilidad de que se produzca una confirmación retrasada de 200 segundos.</span><span class="sxs-lookup"><span data-stu-id="744d8-118">When setting the send buffer to zero and issuing blocking sends, an application has a fifty percent chance of hitting a 200-millisecond delayed acknowledgment.</span></span>

    <span data-ttu-id="744d8-119">No desactive el almacenamiento en búfer de envío a menos que tenga en cuenta el impacto en todos los entornos de red.</span><span class="sxs-lookup"><span data-stu-id="744d8-119">Do not turn off send buffering unless you have considered the impact in all network environments.</span></span> <span data-ttu-id="744d8-120">Una excepción: la transmisión de datos mediante e/s superpuestas debe establecer el búfer de envío en cero.</span><span class="sxs-lookup"><span data-stu-id="744d8-120">One exception: streaming data using overlapped I/O should set the send buffer to zero.</span></span>

-   <span data-ttu-id="744d8-121">Modelo de programación de envío-envío-recepción.</span><span class="sxs-lookup"><span data-stu-id="744d8-121">Send-Send-Receive programming model.</span></span>

    <span data-ttu-id="744d8-122">La estructuración de una aplicación para realizar Send-SEND-RECEIVE aumenta las posibilidades de encontrar el algoritmo de Nagle, lo que produce un retraso de RTT + 200 ms.</span><span class="sxs-lookup"><span data-stu-id="744d8-122">Structuring an application to perform send-send-receives increases your chances of encountering the Nagle Algorithm, which causes a delay of RTT+200 ms.</span></span> <span data-ttu-id="744d8-123">Es posible que se encuentre el algoritmo de Nagle si el último envío es menor que el tamaño de segmento máximo de TCP (MSS, el número máximo de datos en un solo datagrama).</span><span class="sxs-lookup"><span data-stu-id="744d8-123">The Nagle Algorithm may be encountered if the last send is less than the TCP Maximum Segment Size (MSS, the maximum data in a single datagram).</span></span> <span data-ttu-id="744d8-124">MSS puede ser un valor muy grande (64 KB en IPv4 e incluso mayor en IPv6), por lo que no se debe contar con un MSS pequeño.</span><span class="sxs-lookup"><span data-stu-id="744d8-124">MSS can be a very large value (64K in IPv4, and even larger in IPv6), so do not count on a typically small MSS.</span></span> <span data-ttu-id="744d8-125">Una opción mejor es combinar los dos envíos en un solo envío mediante la función [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) o **memcpy** .</span><span class="sxs-lookup"><span data-stu-id="744d8-125">A better option is to combine the two sends into a single send using the [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) or **memcpy** function.</span></span>

-   <span data-ttu-id="744d8-126">Gran número de conexiones simultáneas.</span><span class="sxs-lookup"><span data-stu-id="744d8-126">Large Number of Simultaneous Connections.</span></span>

    <span data-ttu-id="744d8-127">Las conexiones simultáneas no deben superar dos, excepto en las aplicaciones de uso especial.</span><span class="sxs-lookup"><span data-stu-id="744d8-127">Concurrent connections should not exceed two, except in special purpose applications.</span></span> <span data-ttu-id="744d8-128">Si se superan dos conexiones simultáneas, se producen recursos desperdiciados.</span><span class="sxs-lookup"><span data-stu-id="744d8-128">Exceeding two concurrent connections results in wasted resources.</span></span> <span data-ttu-id="744d8-129">Una buena regla es tener hasta cuatro conexiones de corta duración, o dos conexiones persistentes por destino.</span><span class="sxs-lookup"><span data-stu-id="744d8-129">A good rule is to have up to four short lived connections, or two persistent connections per destination.</span></span>

## <a name="related-topics"></a><span data-ttu-id="744d8-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="744d8-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="744d8-131">Comportamiento de la aplicación</span><span class="sxs-lookup"><span data-stu-id="744d8-131">Application Behavior</span></span>](application-behavior-2.md)
</dt> <dt>

[<span data-ttu-id="744d8-132">Aplicaciones de Windows Sockets de alto rendimiento</span><span class="sxs-lookup"><span data-stu-id="744d8-132">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="744d8-133">Algoritmo de Nagle</span><span class="sxs-lookup"><span data-stu-id="744d8-133">Nagle Algorithm</span></span>](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



