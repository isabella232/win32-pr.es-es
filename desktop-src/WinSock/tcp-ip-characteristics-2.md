---
description: TCP/IP tiene características que permiten que el protocolo funcione a medida que se establecen sus requisitos de implementación normalizados.
ms.assetid: 6e9b3878-85f0-4572-9c00-a2e7647286ff
title: Características de TCP/IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 561ab497d6f37c1c84b0203088b29e216ff0a69f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910578"
---
# <a name="tcpip-characteristics"></a><span data-ttu-id="b317f-103">Características de TCP/IP</span><span class="sxs-lookup"><span data-stu-id="b317f-103">TCP/IP Characteristics</span></span>

<span data-ttu-id="b317f-104">TCP/IP tiene características que permiten que el protocolo funcione a medida que se establecen sus requisitos de implementación normalizados.</span><span class="sxs-lookup"><span data-stu-id="b317f-104">TCP/IP has characteristics that enable the protocol to operate as its standardized implementation requirements dictate.</span></span> <span data-ttu-id="b317f-105">Estas características se pueden combinar con las opciones de desarrollo que dan lugar a un rendimiento deficiente.</span><span class="sxs-lookup"><span data-stu-id="b317f-105">These characteristics can combine with development choices that result in poor performance.</span></span> <span data-ttu-id="b317f-106">El impacto que tienen estas características de TCP/IP en una aplicación depende de si la aplicación es transaccional o de streaming.</span><span class="sxs-lookup"><span data-stu-id="b317f-106">The impact these TCP/IP characteristics have on an application depend on whether the application is transactional or streaming.</span></span>

<span data-ttu-id="b317f-107">Las aplicaciones transaccionales se ven afectadas por la sobrecarga necesaria para el establecimiento y la terminación de la conexión.</span><span class="sxs-lookup"><span data-stu-id="b317f-107">Transactional applications are affected by the overhead required for connection establishment and termination.</span></span> <span data-ttu-id="b317f-108">Por ejemplo, cada vez que se establece una conexión en una red Ethernet, se deben enviar tres paquetes de aproximadamente 60 bytes cada uno y se requiere aproximadamente un RTT para el intercambio.</span><span class="sxs-lookup"><span data-stu-id="b317f-108">For example, each time a connection is established on an Ethernet network, three packets of approximately 60 bytes each must be sent, and approximately one RTT is required for the exchange.</span></span> <span data-ttu-id="b317f-109">Cuando se produce la finalización de una conexión, se intercambian cuatro paquetes.</span><span class="sxs-lookup"><span data-stu-id="b317f-109">When termination of a connection occurs, four packets are exchanged.</span></span> <span data-ttu-id="b317f-110">Esto es para cada conexión; a menudo, una aplicación que abre y cierra conexiones incurre en esta sobrecarga en cada repetición.</span><span class="sxs-lookup"><span data-stu-id="b317f-110">This is for each connection; an application that opens and closes connections often incurs this overhead on each occurrence.</span></span>

<span data-ttu-id="b317f-111">Otro aspecto de TCP/IP es *el inicio lento*, que tiene lugar cada vez que se establece una conexión.</span><span class="sxs-lookup"><span data-stu-id="b317f-111">Another aspect of TCP/IP is *slow-start*, which takes place whenever a connection is established.</span></span> <span data-ttu-id="b317f-112">Slow-Start es un límite artificial del número de segmentos de datos que se pueden enviar antes de que se reciba la confirmación de esos segmentos.</span><span class="sxs-lookup"><span data-stu-id="b317f-112">Slow-start is an artificial limit on the number of data segments that can be sent before acknowledgment of those segments is received.</span></span> <span data-ttu-id="b317f-113">El inicio lento está diseñado para limitar la congestión de la red.</span><span class="sxs-lookup"><span data-stu-id="b317f-113">Slow-start is designed to limit network congestion.</span></span> <span data-ttu-id="b317f-114">Cuando se establece una conexión a través de Ethernet, independientemente del tamaño de la ventana del receptor, una transmisión de 4 KB puede tardar hasta 3-4 RTT debido a un inicio lento.</span><span class="sxs-lookup"><span data-stu-id="b317f-114">When a connection over Ethernet is established, regardless of the receiver's window size, a 4 KB transmission can take up to 3-4 RTT due to slow-start.</span></span>

<span data-ttu-id="b317f-115">Una optimización de TCP/IP denominada el algoritmo de Nagle también puede limitar la velocidad de transferencia de datos en una conexión.</span><span class="sxs-lookup"><span data-stu-id="b317f-115">A TCP/IP optimization called the Nagle Algorithm can also limit data transfer speed on a connection.</span></span> <span data-ttu-id="b317f-116">El algoritmo de Nagle está diseñado para reducir la sobrecarga de protocolo para las aplicaciones que envían pequeñas cantidades de datos, como Telnet, que envía un solo carácter cada vez.</span><span class="sxs-lookup"><span data-stu-id="b317f-116">The Nagle Algorithm is designed to reduce protocol overhead for applications that send small amounts of data, such as Telnet, which sends a single character at a time.</span></span> <span data-ttu-id="b317f-117">En lugar de enviar inmediatamente un paquete con gran cantidad de datos de encabezado y poca información, la pila espera más datos de la aplicación o una confirmación antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="b317f-117">Rather than immediately send a packet with lots of header and little data, the stack waits for more data from the application, or an acknowledgment, before proceeding.</span></span>

<span data-ttu-id="b317f-118">Las confirmaciones diferidas, que normalmente se denominan *confirmación diferida*, también están diseñadas en TCP/IP para permitir una superpuesta más eficaz de las confirmaciones cuando los datos devueltos se encuentran desde la aplicación de recepción.</span><span class="sxs-lookup"><span data-stu-id="b317f-118">Delayed acknowledgments, commonly referred to as *delayed ACK*, are also designed into TCP/IP to enable more efficient piggybacking of acknowledgments when return data is forthcoming from the receiving side application.</span></span> <span data-ttu-id="b317f-119">Desafortunadamente, si estos datos no están disponibles y el lado que realiza el envío está esperando una confirmación, pueden producirse retrasos de aproximadamente 200 milisegundos por envío.</span><span class="sxs-lookup"><span data-stu-id="b317f-119">Unfortunately, if this data is not forthcoming and the sending side is waiting for an acknowledgment, delays of approximately 200 milliseconds per send can occur.</span></span>

<span data-ttu-id="b317f-120">Cuando se cierra una conexión TCP, los recursos de conexión en el nodo que inició el cierre se colocan en un estado de espera, denominado TIME-WAIT, para protegerse frente a daños en los datos si los paquetes duplicados se colocan en la red.</span><span class="sxs-lookup"><span data-stu-id="b317f-120">When a TCP connection is closed, connection resources at the node that initiated the close are put into a wait state, called TIME-WAIT, to guard against data corruption if duplicate packets linger in the network.</span></span> <span data-ttu-id="b317f-121">Esto garantiza que ambos extremos finalizan con la conexión.</span><span class="sxs-lookup"><span data-stu-id="b317f-121">This ensures both ends are finished with the connection.</span></span> <span data-ttu-id="b317f-122">Esto puede provocar el agotamiento de los recursos necesarios por conexión, como la RAM y los puertos, cuando las aplicaciones abren y cierran conexiones con frecuencia.</span><span class="sxs-lookup"><span data-stu-id="b317f-122">This can cause depletion of resources required per-connection, such as RAM and ports, when applications open and close connections frequently.</span></span>

<span data-ttu-id="b317f-123">Además de verse afectado por la confirmación diferida y otros esquemas de prevención de congestión, las aplicaciones de streaming también pueden verse afectadas por un tamaño de ventana de recepción predeterminado demasiado pequeño en el extremo receptor.</span><span class="sxs-lookup"><span data-stu-id="b317f-123">Besides being affected by delayed ACK and other congestion avoidance schemes, streaming applications can also be affected by a too-small default receive window size on the receiving end.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b317f-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b317f-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b317f-125">Comportamiento de la aplicación</span><span class="sxs-lookup"><span data-stu-id="b317f-125">Application Behavior</span></span>](application-behavior-2.md)
</dt> <dt>

[<span data-ttu-id="b317f-126">Aplicaciones de Windows Sockets de alto rendimiento</span><span class="sxs-lookup"><span data-stu-id="b317f-126">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="b317f-127">Algoritmo de Nagle</span><span class="sxs-lookup"><span data-stu-id="b317f-127">Nagle Algorithm</span></span>](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



