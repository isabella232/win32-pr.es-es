---
description: Página de navegación de las opciones de socket de Windows Sockets (Winsock).
ms.assetid: e2831f76-4499-45b6-bc60-2908ec3a246c
title: Opciones de socket
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPPROTO_IP
- IPPROTO_IPV6
- IPPROTO_RM
- IPPROTO_TCP
- IPPROTO_UDP
- NSPROTO_IPX
- SOL_APPLETALK
- SOL_IRLMP
- SOL_SOCKET
api_type:
- NA
api_location: ''
ms.openlocfilehash: 805f779965afc808e32952b58815c7b6bc528fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715111"
---
# <a name="socket-options"></a><span data-ttu-id="caab6-103">Opciones de socket</span><span class="sxs-lookup"><span data-stu-id="caab6-103">Socket Options</span></span>

<span data-ttu-id="caab6-104">En esta sección se describen las opciones de socket de Winsock para diversas ediciones de sistemas operativos Windows.</span><span class="sxs-lookup"><span data-stu-id="caab6-104">This section describes Winsock Socket Options for various editions of Windows operating systems.</span></span> <span data-ttu-id="caab6-105">Use [**las funciones**](/windows/desktop/api/winsock/nf-winsock-setsockopt) [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) y el valor de la opción de socket para obtener más opciones de socket.</span><span class="sxs-lookup"><span data-stu-id="caab6-105">Use the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) and [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) functions for more getting and setting socket options.</span></span> <span data-ttu-id="caab6-106">Para enumerar los protocolos y detectar las propiedades compatibles para cada protocolo instalado, utilice la función [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) .</span><span class="sxs-lookup"><span data-stu-id="caab6-106">To enumerate protocols and discover supported properties for each installed protocol, use the [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) function.</span></span>

<span data-ttu-id="caab6-107">Algunas opciones de socket requieren más explicación de lo que pueden transmitir estas tablas; Estas opciones contienen vínculos a páginas adicionales.</span><span class="sxs-lookup"><span data-stu-id="caab6-107">Some socket options require more explanation than these tables can convey; such options contain links to additional pages.</span></span>

<dl> <dt>

<span data-ttu-id="caab6-108"><span id="IPPROTO_IP"></span><span id="ipproto_ip"></span>**\_IP IPPROTO**</span><span class="sxs-lookup"><span data-stu-id="caab6-108"><span id="IPPROTO_IP"></span><span id="ipproto_ip"></span>**IPPROTO\_IP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="caab6-109">Opciones de socket aplicables en el nivel IPv4.</span><span class="sxs-lookup"><span data-stu-id="caab6-109">Socket options applicable at the IPv4 level.</span></span> <span data-ttu-id="caab6-110">Para obtener más información, consulte [**las \_ Opciones de socket IP IPPROTO**](ipproto-ip-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="caab6-110">For more information, see the [**IPPROTO\_IP Socket Options**](ipproto-ip-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="caab6-111"><span id="IPPROTO_IPV6"></span><span id="ipproto_ipv6"></span>**\_IPv6 IPPROTO**</span><span class="sxs-lookup"><span data-stu-id="caab6-111"><span id="IPPROTO_IPV6"></span><span id="ipproto_ipv6"></span>**IPPROTO\_IPV6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="caab6-112">Opciones de socket aplicables en el nivel IPv6.</span><span class="sxs-lookup"><span data-stu-id="caab6-112">Socket options applicable at the IPv6 level.</span></span> <span data-ttu-id="caab6-113">Para obtener más información, consulte [**IPPROTO \_ IPv6 socket Options**](ipproto-ipv6-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="caab6-113">For more information, see the [**IPPROTO\_IPV6 Socket Options**](ipproto-ipv6-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="caab6-114"><span id="IPPROTO_RM"></span><span id="ipproto_rm"></span>**IPPROTO \_ RM**</span><span class="sxs-lookup"><span data-stu-id="caab6-114"><span id="IPPROTO_RM"></span><span id="ipproto_rm"></span>**IPPROTO\_RM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="caab6-115">Opciones de socket aplicables en el nivel de multidifusión confiable.</span><span class="sxs-lookup"><span data-stu-id="caab6-115">Socket options applicable at the reliable multicast level.</span></span> <span data-ttu-id="caab6-116">Para obtener más información, consulte [**las \_ Opciones de socket de RM de IPPROTO**](ipproto-rm-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="caab6-116">For more information, see the [**IPPROTO\_RM Socket Options**](ipproto-rm-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="caab6-117"><span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span>**\_TCP IPPROTO**</span><span class="sxs-lookup"><span data-stu-id="caab6-117"><span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span>**IPPROTO\_TCP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="caab6-118">Opciones de socket aplicables en el nivel de TCP.</span><span class="sxs-lookup"><span data-stu-id="caab6-118">Socket options applicable at the TCP level.</span></span> <span data-ttu-id="caab6-119">Para obtener más información, consulte [**las \_ Opciones de socket TCP de IPPROTO**](ipproto-tcp-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="caab6-119">For more information, see the [**IPPROTO\_TCP Socket Options**](ipproto-tcp-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="caab6-120"><span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span>**IPPROTO \_ UDP**</span><span class="sxs-lookup"><span data-stu-id="caab6-120"><span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span>**IPPROTO\_UDP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="caab6-121">Opciones de socket aplicables en el nivel de UDP.</span><span class="sxs-lookup"><span data-stu-id="caab6-121">Socket options applicable at the UDP level.</span></span> <span data-ttu-id="caab6-122">Para obtener más información, consulte [**las \_ Opciones de socket UDP de IPPROTO**](ipproto-udp-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="caab6-122">For more information, see the [**IPPROTO\_UDP Socket Options**](ipproto-udp-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="caab6-123"><span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>**NSPROTO \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="caab6-123"><span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>**NSPROTO\_IPX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="caab6-124">Opciones de socket aplicables en el nivel de IPX.</span><span class="sxs-lookup"><span data-stu-id="caab6-124">Socket options applicable at the IPX level.</span></span> <span data-ttu-id="caab6-125">Para obtener más información, consulte [**las \_ Opciones de socket IPX NSPROTO**](nsproto-ipx-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="caab6-125">For more information, see the [**NSPROTO\_IPX Socket Options**](nsproto-ipx-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="caab6-126"><span id="SOL_APPLETALK"></span><span id="sol_appletalk"></span>**de SOL con \_ APPLETALK**</span><span class="sxs-lookup"><span data-stu-id="caab6-126"><span id="SOL_APPLETALK"></span><span id="sol_appletalk"></span>**SOL\_APPLETALK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="caab6-127">Opciones de socket aplicables en el nivel de AppleTalk.</span><span class="sxs-lookup"><span data-stu-id="caab6-127">Socket options applicable at the AppleTalk level.</span></span> <span data-ttu-id="caab6-128">Para obtener más información, consulte [**las \_ Opciones de socket de APPLETALK de Apple**](sol-appletalk-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="caab6-128">For more information, see the [**SOL\_APPLETALK Socket Options**](sol-appletalk-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="caab6-129"><span id="SOL_IRLMP"></span><span id="sol_irlmp"></span>**SOL \_ IRLMP**</span><span class="sxs-lookup"><span data-stu-id="caab6-129"><span id="SOL_IRLMP"></span><span id="sol_irlmp"></span>**SOL\_IRLMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="caab6-130">Opciones de socket aplicables en el nivel de protocolo de administración de vínculos de infrarrojos.</span><span class="sxs-lookup"><span data-stu-id="caab6-130">Socket options applicable at the InfraRed Link Management Protocol level.</span></span> <span data-ttu-id="caab6-131">Para obtener más información, consulte [**las \_ Opciones de socket IRLMP de sol**](sol-irlmp-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="caab6-131">For more information, see the [**SOL\_IRLMP Socket Options**](sol-irlmp-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="caab6-132"><span id="SOL_SOCKET"></span><span id="sol_socket"></span>**\_socket sol**</span><span class="sxs-lookup"><span data-stu-id="caab6-132"><span id="SOL_SOCKET"></span><span id="sol_socket"></span>**SOL\_SOCKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="caab6-133">Opciones de socket aplicables en el nivel de socket.</span><span class="sxs-lookup"><span data-stu-id="caab6-133">Socket options applicable at the socket level.</span></span> <span data-ttu-id="caab6-134">Para obtener más información, consulte [**las \_ Opciones de socket de socket sol**](sol-socket-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="caab6-134">For more information, see the [**SOL\_SOCKET Socket Options**](sol-socket-socket-options.md).</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="caab6-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="caab6-135">Remarks</span></span>

<span data-ttu-id="caab6-136">Todas \_ \* las opciones de socket se aplican por igual a IPv4 e IPv6 (excepto por el caso de la \_ difusión, ya que la difusión no se implementa en IPv6).</span><span class="sxs-lookup"><span data-stu-id="caab6-136">All SO\_\* socket options apply equally to IPv4 and IPv6 (except SO\_BROADCAST, since broadcast is not implemented in IPv6).</span></span>

 

 



