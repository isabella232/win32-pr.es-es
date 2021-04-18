---
description: Los problemas de tamaño de los paquetes multimedia descritos en el tema sobre el tamaño de los paquetes multimedia afectan a los distintos protocolos de PF \_ IPX de manera diferente.
ms.assetid: 7f0643b8-6bb2-4dbb-b306-d9b2e0d0e03c
title: Cómo afecta el tamaño de paquete a los protocolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c778ee6c75cd558d19cdf1cbb76052065e03c427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360300"
---
# <a name="how-packet-size-affects-protocols"></a><span data-ttu-id="46120-103">Cómo afecta el tamaño de paquete a los protocolos</span><span class="sxs-lookup"><span data-stu-id="46120-103">How Packet Size Affects Protocols</span></span>

<span data-ttu-id="46120-104">Los problemas de tamaño de los paquetes multimedia descritos en el tema sobre el tamaño de los [paquetes multimedia](about-media-packet-size-2.md)afectan a los distintos protocolos de PF \_ IPX de manera diferente.</span><span class="sxs-lookup"><span data-stu-id="46120-104">Media packet size issues discussed in the topic, [About Media Packet Size](about-media-packet-size-2.md), affect the various PF\_IPX protocols differently.</span></span> <span data-ttu-id="46120-105">Una estrategia común para controlar varias restricciones de tamaño de enrutador y de tamaño de los medios es usar el tamaño total del medio cuando el número de red de la estación remota coincide con la estación local y revertir al tamaño mínimo de los paquetes en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="46120-105">A common strategy for handling various router and media size constraints is to use the full media size when the remote station's network number matches the local station, and fall back to the minimum packet size otherwise.</span></span>

## <a name="parameters"></a><span data-ttu-id="46120-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46120-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46120-107"><span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>NSPROTO \_ IPX</span><span class="sxs-lookup"><span data-stu-id="46120-107"><span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>NSPROTO\_IPX</span></span>
</dt> <dd>

<span data-ttu-id="46120-108">Proporciona un servicio de datagramas; cada datagrama debe residir en el tamaño máximo del paquete.</span><span class="sxs-lookup"><span data-stu-id="46120-108">Provides a datagram service; each datagram must reside within the maximum packet size.</span></span> <span data-ttu-id="46120-109">Winsock establece el tamaño máximo del paquete de datagramas en el tamaño de paquete multimedia local menos el encabezado IPX.</span><span class="sxs-lookup"><span data-stu-id="46120-109">Winsock sets the maximum datagram packet size to the local media packet size minus the IPX header.</span></span> <span data-ttu-id="46120-110">Sin embargo, tenga en cuenta que si se enruta el paquete, puede que se alcancen las restricciones de enrutador en la ruta.</span><span class="sxs-lookup"><span data-stu-id="46120-110">Keep in mind, however, that if the packet is routed, it may hit router restrictions en route.</span></span> <span data-ttu-id="46120-111">Asegúrese de que la aplicación puede revertir a datagramas de 546 bytes.</span><span class="sxs-lookup"><span data-stu-id="46120-111">Make sure your application can fall back to 546-byte datagrams.</span></span>

</dd> <dt>

<span data-ttu-id="46120-112"><span id="NSPROTO_SPX"></span><span id="nsproto_spx"></span>NSPROTO \_ SPX</span><span class="sxs-lookup"><span data-stu-id="46120-112"><span id="NSPROTO_SPX"></span><span id="nsproto_spx"></span>NSPROTO\_SPX</span></span>
</dt> <dd>

<span data-ttu-id="46120-113">Proporciona servicios de secuencia y de paquetes secuenciados.</span><span class="sxs-lookup"><span data-stu-id="46120-113">Provides stream and sequenced-packet services.</span></span> <span data-ttu-id="46120-114">Winsock IPX/SPX permite que los flujos de datos y los mensajes abarquen varios paquetes, por lo que el tamaño de los paquetes no limita la cantidad de datos que se administran mediante el [**envío**](/windows/desktop/api/Winsock2/nf-winsock2-send) y la [**recepción**](/windows/desktop/api/winsock/nf-winsock-recv).</span><span class="sxs-lookup"><span data-stu-id="46120-114">Winsock IPX/SPX lets data streams and messages span multiple packets, so packet size does not limit the amount of data handled by [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) and [**recv**](/windows/desktop/api/winsock/nf-winsock-recv).</span></span> <span data-ttu-id="46120-115">Sin embargo, el tamaño del medio subyacente debe establecerse correctamente o el primer paquete de gran tamaño no se podrá enviar y se restablecerá la conexión.</span><span class="sxs-lookup"><span data-stu-id="46120-115">However, the underlying media size must be set correctly or the first large packet will be undeliverable and the connection will reset.</span></span> <span data-ttu-id="46120-116">Si la estación de destino se encuentra en la red local, Winsock establece el tamaño de paquete en el tamaño de paquete multimedia.</span><span class="sxs-lookup"><span data-stu-id="46120-116">If the target station is on the local network, Winsock sets its packet size to the media packet size.</span></span> <span data-ttu-id="46120-117">De lo contrario, el valor predeterminado es 512 bytes.</span><span class="sxs-lookup"><span data-stu-id="46120-117">Otherwise, it defaults to 512 bytes.</span></span> <span data-ttu-id="46120-118">Este tamaño se puede cambiar inmediatamente después de la [**conexión**](/windows/desktop/api/Winsock2/nf-winsock2-connect) o de [**Aceptar**](/windows/desktop/api/Winsock2/nf-winsock2-accept) [**a la**](/windows/desktop/api/winsock/nf-winsock-setsockopt).</span><span class="sxs-lookup"><span data-stu-id="46120-118">This size can be changed immediately after [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) or [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) through [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt).</span></span>

</dd> <dt>

<span data-ttu-id="46120-119"><span id="NSPROTO_SPXII"></span><span id="nsproto_spxii"></span>NSPROTO \_ SPXII</span><span class="sxs-lookup"><span data-stu-id="46120-119"><span id="NSPROTO_SPXII"></span><span id="nsproto_spxii"></span>NSPROTO\_SPXII</span></span>
</dt> <dd>

<span data-ttu-id="46120-120">SPXII incluye una gran negociación de paquetes de Internet para mantener un tamaño mejor para los paquetes y no requiere la intervención del programador.</span><span class="sxs-lookup"><span data-stu-id="46120-120">SPXII features large Internet packet negotiation to maintain a best-fit size for packets and does not require programmer intervention.</span></span> <span data-ttu-id="46120-121">Sin embargo, si la estación remota no es compatible con SPXII y se negocia a la SPX estándar, las \_ reglas de NSPROTO SPX estarán en vigor.</span><span class="sxs-lookup"><span data-stu-id="46120-121">However, if the remote station does not support SPXII and negotiates down to standard SPX, the NSPROTO\_SPX rules are in effect.</span></span>



| <span data-ttu-id="46120-122">Protocolo</span><span class="sxs-lookup"><span data-stu-id="46120-122">Protocol</span></span>     | <span data-ttu-id="46120-123">Medios</span><span class="sxs-lookup"><span data-stu-id="46120-123">Media</span></span>      | <span data-ttu-id="46120-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="46120-124">Type</span></span>        | <span data-ttu-id="46120-125">Tamaño de paquete de datos</span><span class="sxs-lookup"><span data-stu-id="46120-125">Data packet size</span></span> |
|--------------|------------|-------------|------------------|
| <span data-ttu-id="46120-126">NSPROTO \_ IPX</span><span class="sxs-lookup"><span data-stu-id="46120-126">NSPROTO\_IPX</span></span> | <span data-ttu-id="46120-127">Ethernet</span><span class="sxs-lookup"><span data-stu-id="46120-127">Ethernet</span></span>   | <span data-ttu-id="46120-128">Ethernet II</span><span class="sxs-lookup"><span data-stu-id="46120-128">Ethernet II</span></span> |                  |
|              |            | <span data-ttu-id="46120-129">802.3</span><span class="sxs-lookup"><span data-stu-id="46120-129">802.3</span></span>       |                  |
|              |            | <span data-ttu-id="46120-130">802.2</span><span class="sxs-lookup"><span data-stu-id="46120-130">802.2</span></span>       | <span data-ttu-id="46120-131">1466</span><span class="sxs-lookup"><span data-stu-id="46120-131">1466</span></span>             |
|              |            | <span data-ttu-id="46120-132">COMPLEMENTO</span><span class="sxs-lookup"><span data-stu-id="46120-132">SNAP</span></span>        |                  |
|              | <span data-ttu-id="46120-133">Token Ring</span><span class="sxs-lookup"><span data-stu-id="46120-133">Token Ring</span></span> | <span data-ttu-id="46120-134">4 megabits</span><span class="sxs-lookup"><span data-stu-id="46120-134">4 megabit</span></span>   |                  |
|              |            | <span data-ttu-id="46120-135">16 megabits</span><span class="sxs-lookup"><span data-stu-id="46120-135">16 megabit</span></span>  |                  |
| <span data-ttu-id="46120-136">NSPROTO \_ SPX</span><span class="sxs-lookup"><span data-stu-id="46120-136">NSPROTO\_SPX</span></span> | <span data-ttu-id="46120-137">Ethernet</span><span class="sxs-lookup"><span data-stu-id="46120-137">Ethernet</span></span>   | <span data-ttu-id="46120-138">Ethernet II</span><span class="sxs-lookup"><span data-stu-id="46120-138">Ethernet II</span></span> |                  |
|              |            | <span data-ttu-id="46120-139">802.3</span><span class="sxs-lookup"><span data-stu-id="46120-139">802.3</span></span>       |                  |
|              |            | <span data-ttu-id="46120-140">802.2</span><span class="sxs-lookup"><span data-stu-id="46120-140">802.2</span></span>       | <span data-ttu-id="46120-141">1454</span><span class="sxs-lookup"><span data-stu-id="46120-141">1454</span></span>             |
|              |            | <span data-ttu-id="46120-142">COMPLEMENTO</span><span class="sxs-lookup"><span data-stu-id="46120-142">SNAP</span></span>        |                  |
|              | <span data-ttu-id="46120-143">Token Ring</span><span class="sxs-lookup"><span data-stu-id="46120-143">Token Ring</span></span> | <span data-ttu-id="46120-144">4 megabits</span><span class="sxs-lookup"><span data-stu-id="46120-144">4 megabit</span></span>   |                  |
|              |            | <span data-ttu-id="46120-145">16 megabits</span><span class="sxs-lookup"><span data-stu-id="46120-145">16 megabit</span></span>  |                  |



 

</dd> </dl>

 

 



