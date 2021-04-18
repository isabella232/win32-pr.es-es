---
description: En esta guía se identifica una aplicación lenta como aplicación de Microsoft Windows con un rendimiento desemparejado.
ms.assetid: cacf55d8-ab64-47a4-a55b-59a3c4e3877b
title: Reconocer aplicaciones lentas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07be9484a3b08951b8b64989757459531ff72906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706981"
---
# <a name="recognizing-slow-applications"></a><span data-ttu-id="8b018-103">Reconocer aplicaciones lentas</span><span class="sxs-lookup"><span data-stu-id="8b018-103">Recognizing Slow Applications</span></span>

<span data-ttu-id="8b018-104">En esta guía se identifica una aplicación *lenta* como aplicación de Microsoft Windows con un rendimiento desemparejado.</span><span class="sxs-lookup"><span data-stu-id="8b018-104">This guide identifies a *slow* application as a Microsoft Windows application with impaired performance.</span></span> <span data-ttu-id="8b018-105">Una aplicación lenta exhibe uno o varios de los síntomas siguientes:</span><span class="sxs-lookup"><span data-stu-id="8b018-105">A slow application exhibits one or more of the following symptoms:</span></span>

-   <span data-ttu-id="8b018-106">La utilización de la CPU y la red son bajas.</span><span class="sxs-lookup"><span data-stu-id="8b018-106">CPU and network utilization are low.</span></span>

    <span data-ttu-id="8b018-107">Parece que el equipo está esperando.</span><span class="sxs-lookup"><span data-stu-id="8b018-107">The computer appears to be waiting on something.</span></span> <span data-ttu-id="8b018-108">A menudo, la aplicación espera en la red.</span><span class="sxs-lookup"><span data-stu-id="8b018-108">Often, the application is waiting on the network.</span></span>

-   <span data-ttu-id="8b018-109">La desactivación del algoritmo de Nagle mediante la opción de socket de TCP \_ Nodelay aumenta el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="8b018-109">Turning off the Nagle Algorithm through the TCP\_NODELAY socket option increases performance.</span></span>

    <span data-ttu-id="8b018-110">Esto indica otros problemas y no debe considerarse una solución.</span><span class="sxs-lookup"><span data-stu-id="8b018-110">This indicates other problems, and should not be considered a solution.</span></span> <span data-ttu-id="8b018-111">La desactivación del algoritmo de Nagle aumenta la sobrecarga del protocolo.</span><span class="sxs-lookup"><span data-stu-id="8b018-111">Turning off the Nagle algorithm increases the protocol overhead.</span></span> <span data-ttu-id="8b018-112">No utilice este método como una corrección para las aplicaciones interrumpidas, solo como una indicación de que la aplicación necesita otro trabajo para solucionar problemas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="8b018-112">Do not use this method as a fix for the broken applications—only as an indication the application needs other work to fix performance issues.</span></span>

-   <span data-ttu-id="8b018-113">La aplicación exhibe una sobrecarga elevada.</span><span class="sxs-lookup"><span data-stu-id="8b018-113">The application exhibits high overhead.</span></span>

    <span data-ttu-id="8b018-114">Para calcular la sobrecarga de las aplicaciones, determine la cantidad de datos que desea transferir en cada dirección.</span><span class="sxs-lookup"><span data-stu-id="8b018-114">To calculate your applications overhead, determine how much data you intended to transfer in each direction.</span></span> <span data-ttu-id="8b018-115">A continuación, use netstat y agregue (para Ethernet) 60 bytes para cada paquete y 500 bytes para cada conexión.</span><span class="sxs-lookup"><span data-stu-id="8b018-115">Then use Netstat and add (for Ethernet) 60 bytes for each packet and 500 bytes for each connection.</span></span> <span data-ttu-id="8b018-116">La mejor sobrecarga que se puede esperar para la transmisión por secuencias sobre Ethernet es aproximadamente del 6%.</span><span class="sxs-lookup"><span data-stu-id="8b018-116">The best overhead that can be expected for streaming over Ethernet is approximately 6%.</span></span> <span data-ttu-id="8b018-117">En el caso de una conexión de módem, la mejor sobrecarga es aproximadamente del 2%, debido al hecho de que un vínculo PPP usa la compresión de encabezado.</span><span class="sxs-lookup"><span data-stu-id="8b018-117">For a modem connection, the best overhead is approximately 2%, due to the fact that a PPP link uses header compression.</span></span> <span data-ttu-id="8b018-118">Consulte [calcular la sobrecarga con netstat](calculating-overhead-with-netstat-2.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="8b018-118">See [Calculating Overhead with Netstat](calculating-overhead-with-netstat-2.md) for more information.</span></span>

-   <span data-ttu-id="8b018-119">La respuesta de la aplicación se ralentiza cuando la conexión tiene un RTT grande.</span><span class="sxs-lookup"><span data-stu-id="8b018-119">Application response slows when the connection has a large RTT.</span></span>

    <span data-ttu-id="8b018-120">Suponiendo que la aplicación no se aproxima al ancho de banda del vínculo, un RTT grande debería tener poco o ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="8b018-120">Assuming the application is not approaching the link's bandwidth, a large RTT should have little or no effect.</span></span> <span data-ttu-id="8b018-121">Una ralentización dramática con un RTT grande es un claro signo de procesamiento serializado y muchas transacciones pequeñas.</span><span class="sxs-lookup"><span data-stu-id="8b018-121">A dramatic slowdown with a large RTT is a clear sign of serialized processing and many small transactions.</span></span>

<span data-ttu-id="8b018-122">Todas las aplicaciones deben probarse en un entorno con un RTT grande.</span><span class="sxs-lookup"><span data-stu-id="8b018-122">Every application should be tested in an environment with a large RTT.</span></span> <span data-ttu-id="8b018-123">Al hacerlo, se revela la mayoría de las aplicaciones que sufren opciones de desarrollo deficientes.</span><span class="sxs-lookup"><span data-stu-id="8b018-123">Doing so reveals most applications that suffer from poor development choices.</span></span> <span data-ttu-id="8b018-124">Esta prueba puede realizarse en varios entornos, como una red LAN inalámbrica, un simulador de retraso de vínculos o una red satélite.</span><span class="sxs-lookup"><span data-stu-id="8b018-124">This testing can be performed in several environments, including a wireless LAN network, a link-delay simulator, or a satellite network.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b018-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8b018-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b018-126">Comportamiento de la aplicación</span><span class="sxs-lookup"><span data-stu-id="8b018-126">Application Behavior</span></span>](application-behavior-2.md)
</dt> <dt>

[<span data-ttu-id="8b018-127">Aplicaciones de Windows Sockets de alto rendimiento</span><span class="sxs-lookup"><span data-stu-id="8b018-127">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="8b018-128">Algoritmo de Nagle</span><span class="sxs-lookup"><span data-stu-id="8b018-128">Nagle Algorithm</span></span>](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



