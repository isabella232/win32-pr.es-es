---
description: El parámetro Protocol de socket y WSASocket es un identificador que establece un tipo de red y un método para identificar los distintos protocolos de transporte que se ejecutan en la red.
ms.assetid: cb4d99d5-3ae0-4bfc-b521-122dd9d4f1c2
title: Familia IPX de identificadores de protocolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7fc808a04f1cf10bb099cd7d923bf471e9bd8d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154270"
---
# <a name="ipx-family-of-protocol-identifiers"></a><span data-ttu-id="7c016-103">Familia IPX de identificadores de protocolo</span><span class="sxs-lookup"><span data-stu-id="7c016-103">IPX Family of Protocol Identifiers</span></span>

<span data-ttu-id="7c016-104">El parámetro *Protocol* de [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) y [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) es un identificador que establece un tipo de red y un método para identificar los distintos protocolos de transporte que se ejecutan en la red.</span><span class="sxs-lookup"><span data-stu-id="7c016-104">The *protocol* parameter in [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) and [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) is an identifier that establishes a network type and a method for identifying the various transport protocols that run on the network.</span></span> <span data-ttu-id="7c016-105">A diferencia de IP, IPX no utiliza un único valor de protocolo para seleccionar una pila de transporte.</span><span class="sxs-lookup"><span data-stu-id="7c016-105">Unlike IP, IPX does not use a single protocol value for selecting a transport stack.</span></span> <span data-ttu-id="7c016-106">Puesto que no hay ningún requisito de red para usar un valor específico para cada protocolo de transporte, podemos asignarlos de forma adecuada para las aplicaciones Winsock.</span><span class="sxs-lookup"><span data-stu-id="7c016-106">Since there is no network requirement to use a specific value for each transport protocol, we are free to assign them in a manner convenient for Winsock applications.</span></span> <span data-ttu-id="7c016-107">Se evitan los valores 0 a 255 para evitar colisiones con los valores de \_ Protocolo PF inet correspondientes.</span><span class="sxs-lookup"><span data-stu-id="7c016-107">We avoid values 0–255 in order to avoid collisions with the corresponding PF\_INET protocol values.</span></span>



| <span data-ttu-id="7c016-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="7c016-108">Name</span></span>         | <span data-ttu-id="7c016-109">Value</span><span class="sxs-lookup"><span data-stu-id="7c016-109">Value</span></span>       | <span data-ttu-id="7c016-110">Tipos de socket</span><span class="sxs-lookup"><span data-stu-id="7c016-110">Socket types</span></span>              | <span data-ttu-id="7c016-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c016-111">Description</span></span>                                         |
|--------------|-------------|---------------------------|-----------------------------------------------------|
| <span data-ttu-id="7c016-112">Reservado</span><span class="sxs-lookup"><span data-stu-id="7c016-112">Reserved</span></span>     | <span data-ttu-id="7c016-113">0-255</span><span class="sxs-lookup"><span data-stu-id="7c016-113">0-255</span></span>       |                           | <span data-ttu-id="7c016-114">Reservado para \_ los valores del protocolo PF inet.</span><span class="sxs-lookup"><span data-stu-id="7c016-114">Reserved for PF\_INET protocol values.</span></span>              |
| <span data-ttu-id="7c016-115">NSPROTO \_ IPX</span><span class="sxs-lookup"><span data-stu-id="7c016-115">NSPROTO\_IPX</span></span> | <span data-ttu-id="7c016-116">1000-1255</span><span class="sxs-lookup"><span data-stu-id="7c016-116">1000 - 1255</span></span> | <span data-ttu-id="7c016-117">SOCK \_ DGRAM sock \_ raw</span><span class="sxs-lookup"><span data-stu-id="7c016-117">SOCK\_DGRAM SOCK\_RAW</span></span>     | <span data-ttu-id="7c016-118">Servicio de datagrama para IPX.</span><span class="sxs-lookup"><span data-stu-id="7c016-118">Datagram service for IPX.</span></span>                           |
| <span data-ttu-id="7c016-119">NSPROTO \_ SPX</span><span class="sxs-lookup"><span data-stu-id="7c016-119">NSPROTO\_SPX</span></span> | <span data-ttu-id="7c016-120">1256</span><span class="sxs-lookup"><span data-stu-id="7c016-120">1256</span></span>        | <span data-ttu-id="7c016-121">SOCK \_ Stream sock \_ SEQPKT</span><span class="sxs-lookup"><span data-stu-id="7c016-121">SOCK\_STREAM SOCK\_SEQPKT</span></span> | <span data-ttu-id="7c016-122">Intercambio de paquetes confiable con paquetes de tamaño fijo.</span><span class="sxs-lookup"><span data-stu-id="7c016-122">Reliable packet exchange using fixed-sized packets.</span></span> |



 

> [!Note]  
> <span data-ttu-id="7c016-123">Cuando \_ se especifica NSPROTO SPX, el protocolo SPX II se emplea automáticamente si ambos puntos de conexión son capaces de hacerlo.</span><span class="sxs-lookup"><span data-stu-id="7c016-123">When NSPROTO\_SPX is specified, the SPX II protocol is automatically utilized if both endpoints are capable of doing so.</span></span>

 

 

 



