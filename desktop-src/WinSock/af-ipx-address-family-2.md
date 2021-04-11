---
description: La familia de direcciones IPX define la estructura de direccionamiento de los protocolos que usan el direccionamiento estándar de sockets IPX. Para estos transportes, una dirección de punto de conexión consta de un número de red, una dirección de nodo y un número de socket.
ms.assetid: cf749ae7-ab17-4c60-b00c-b34e092c6431
title: Familia de direcciones de AF_IPX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21508b23541b489c11fbdc38a2ff8dcf4ad53e48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154301"
---
# <a name="af_ipx-address-family"></a><span data-ttu-id="a32a8-104">\_Familia de direcciones IPX de AF</span><span class="sxs-lookup"><span data-stu-id="a32a8-104">AF\_IPX Address Family</span></span>

<span data-ttu-id="a32a8-105">La familia de direcciones IPX define la estructura de direccionamiento de los protocolos que usan el direccionamiento estándar de sockets IPX.</span><span class="sxs-lookup"><span data-stu-id="a32a8-105">The IPX address family defines the addressing structure for protocols that use standard IPX socket addressing.</span></span> <span data-ttu-id="a32a8-106">Para estos transportes, una dirección de punto de conexión consta de un número de red, una dirección de nodo y un número de socket.</span><span class="sxs-lookup"><span data-stu-id="a32a8-106">For these transports, an endpoint address consists of a network number, node address, and socket number.</span></span>

<span data-ttu-id="a32a8-107">El número de red es un dominio administrativo y normalmente nombra un único segmento Ethernet o anillo de token.</span><span class="sxs-lookup"><span data-stu-id="a32a8-107">The network number is an administrative domain and typically names a single Ethernet or token ring segment.</span></span> <span data-ttu-id="a32a8-108">El número de nodo es la dirección física de la estación.</span><span class="sxs-lookup"><span data-stu-id="a32a8-108">The node number is a station's physical address.</span></span> <span data-ttu-id="a32a8-109">La combinación de red y de forma de nodo es una dirección de estación única que se supone que es única en el mundo.</span><span class="sxs-lookup"><span data-stu-id="a32a8-109">The combination of net and node form a unique station address that is presumed to be unique in the world.</span></span> <span data-ttu-id="a32a8-110">Los números de red y de nodo se representan en texto ASCII en la notación de bloques o de guiones como: ' 0101a040, 00001b498765 ' o ' 01-01-a0-40, 00-00-1B-49-87-65 '.</span><span class="sxs-lookup"><span data-stu-id="a32a8-110">Net and node numbers are represented in ASCII text in either block or dashed notation as: '0101a040,00001b498765' or '01-01-a0-40,00-00-1b-49-87-65'.</span></span> <span data-ttu-id="a32a8-111">No es necesario que haya ceros a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="a32a8-111">Leading zeros need not be present.</span></span>

<span data-ttu-id="a32a8-112">El número de sockets IPX es un número de servicio de red/transporte muy parecido a un número de puerto TCP y no debe confundirse con el descriptor de socket Winsock.</span><span class="sxs-lookup"><span data-stu-id="a32a8-112">The IPX socket number is a network/transport service number much like a TCP port number and is not to be confused with the Winsock socket descriptor.</span></span> <span data-ttu-id="a32a8-113">Los números de socket IPX son globales para la estación final y no se pueden enlazar a direcciones de red o nodo específicas.</span><span class="sxs-lookup"><span data-stu-id="a32a8-113">IPX socket numbers are global to the end station and cannot be bound to specific net/node addresses.</span></span> <span data-ttu-id="a32a8-114">Por ejemplo, si la estación final tiene dos tarjetas de interfaz de red, un socket enlazado puede enviar y recibir en ambas tarjetas.</span><span class="sxs-lookup"><span data-stu-id="a32a8-114">For instance, if the end station has two network interface cards, a bound socket can send and receive on both cards.</span></span> <span data-ttu-id="a32a8-115">En concreto, los sockets de datagramas recibirían datagramas de difusión en ambas tarjetas.</span><span class="sxs-lookup"><span data-stu-id="a32a8-115">In particular, datagram sockets would receive broadcast datagrams on both cards.</span></span>

> [!Caution]  
> <span data-ttu-id="a32a8-116">SOCKADDR \_ IPX tiene 14 bytes de longitud y es menor que la estructura de referencia [**SOCKADDR**](sockaddr-2.md) de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="a32a8-116">SOCKADDR\_IPX is 14 bytes long and is shorter than the 16-byte [**sockaddr**](sockaddr-2.md) reference structure.</span></span> <span data-ttu-id="a32a8-117">Las implementaciones de IPX/SPX pueden aceptar la longitud de 16 bytes, así como la longitud real.</span><span class="sxs-lookup"><span data-stu-id="a32a8-117">IPX/SPX implementations may accept the 16-byte length as well as the true length.</span></span> <span data-ttu-id="a32a8-118">Si usa SOCKADDR \_ IPX y una longitud codificada de 16 bytes, la implementación puede suponer que tiene acceso a los 2 bytes que siguen a la estructura.</span><span class="sxs-lookup"><span data-stu-id="a32a8-118">If you use SOCKADDR\_IPX and a hard-coded length of 16 bytes, the implementation may assume that it has access to the 2 bytes following your structure.</span></span>

 



| <span data-ttu-id="a32a8-119">Campo</span><span class="sxs-lookup"><span data-stu-id="a32a8-119">Field</span></span>           | <span data-ttu-id="a32a8-120">Value</span><span class="sxs-lookup"><span data-stu-id="a32a8-120">Value</span></span>                                    |
|-----------------|------------------------------------------|
| <span data-ttu-id="a32a8-121">**\_familia SA**</span><span class="sxs-lookup"><span data-stu-id="a32a8-121">**sa\_family**</span></span>  | <span data-ttu-id="a32a8-122">Familia de direcciones \_ de AF IPX en el orden del host.</span><span class="sxs-lookup"><span data-stu-id="a32a8-122">Address family AF\_IPX in host order.</span></span>    |
| <span data-ttu-id="a32a8-123">**SA \_ netnum**</span><span class="sxs-lookup"><span data-stu-id="a32a8-123">**Sa\_netnum**</span></span>  | <span data-ttu-id="a32a8-124">Identificador de red IPX en el orden de la red.</span><span class="sxs-lookup"><span data-stu-id="a32a8-124">IPX network identifier in network order.</span></span> |
| <span data-ttu-id="a32a8-125">**SA \_ nodenum**</span><span class="sxs-lookup"><span data-stu-id="a32a8-125">**Sa\_nodenum**</span></span> | <span data-ttu-id="a32a8-126">Dirección del nodo de la estación, vacía derecha.</span><span class="sxs-lookup"><span data-stu-id="a32a8-126">Station node address, flushed right.</span></span>     |
| <span data-ttu-id="a32a8-127">**\_Socket SA**</span><span class="sxs-lookup"><span data-stu-id="a32a8-127">**Sa\_socket**</span></span>  | <span data-ttu-id="a32a8-128">Número de socket IPX en el orden de la red.</span><span class="sxs-lookup"><span data-stu-id="a32a8-128">IPX socket number in network order.</span></span>      |



 

 

 



