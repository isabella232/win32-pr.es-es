---
description: La aplicación auxiliar de IP proporciona funciones de recuperación de información que son útiles para la administración de red del equipo local.
ms.assetid: b50b3927-6c74-4282-b79b-c86d72d93ae3
title: Recuperación de información sobre el protocolo de Internet y el protocolo de mensajes de control de Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b2768ff591b53db79bbbfb38fc2c6c2596ca9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000895"
---
# <a name="retrieving-information-on-the-internet-protocol-and-the-internet-control-message-protocol"></a><span data-ttu-id="286cb-103">Recuperación de información sobre el protocolo de Internet y el protocolo de mensajes de control de Internet</span><span class="sxs-lookup"><span data-stu-id="286cb-103">Retrieving Information on the Internet Protocol and the Internet Control Message Protocol</span></span>

<span data-ttu-id="286cb-104">La aplicación auxiliar de IP proporciona funciones de recuperación de información que son útiles para la administración de red del equipo local.</span><span class="sxs-lookup"><span data-stu-id="286cb-104">IP Helper provides information retrieval capabilities that are useful for the network administration of the local computer.</span></span> <span data-ttu-id="286cb-105">Las siguientes funciones recuperan estadísticas del Protocolo de Internet (IP) y del Protocolo de mensajes de control de Internet (ICMP).</span><span class="sxs-lookup"><span data-stu-id="286cb-105">The following functions retrieve statistics for the Internet Protocol (IP) and the Internet Control Message Protocol (ICMP).</span></span> <span data-ttu-id="286cb-106">También puede usar estas funciones para establecer determinados parámetros de configuración de IP.</span><span class="sxs-lookup"><span data-stu-id="286cb-106">You can also use these functions to set certain configuration parameters for IP.</span></span>

<span data-ttu-id="286cb-107">La función [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) recupera las estadísticas de IP actuales para el equipo local.</span><span class="sxs-lookup"><span data-stu-id="286cb-107">The [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) function retrieves the current IP statistics for the local computer.</span></span> <span data-ttu-id="286cb-108">Para obtener ejemplos de código que impliquen a **GetIpStatistics** , vea [recuperar información mediante GetIpStatistics](retrieving-information-using-getipstatistics.md).</span><span class="sxs-lookup"><span data-stu-id="286cb-108">For code samples involving **GetIpStatistics** see [Retrieving Information Using GetIpStatistics](retrieving-information-using-getipstatistics.md).</span></span>

<span data-ttu-id="286cb-109">La función [**GetIcmpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-geticmpstatistics) recupera las estadísticas de ICMP actuales.</span><span class="sxs-lookup"><span data-stu-id="286cb-109">The [**GetIcmpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-geticmpstatistics) function retrieves the current ICMP statistics.</span></span>

<span data-ttu-id="286cb-110">Use la función [**SetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipstatistics) para habilitar o deshabilitar el reenvío IP.</span><span class="sxs-lookup"><span data-stu-id="286cb-110">Use the [**SetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipstatistics) function to enable or disable IP forwarding.</span></span> <span data-ttu-id="286cb-111">Esta función también permite establecer el período de vida (TTL) predeterminado para los datagramas IP.</span><span class="sxs-lookup"><span data-stu-id="286cb-111">This function also makes it possible for you to set the default time-to-live (TTL) for IP datagrams.</span></span> <span data-ttu-id="286cb-112">Como alternativa, puede establecer el TTL mediante la función [**SetIpTTL**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipttl) .</span><span class="sxs-lookup"><span data-stu-id="286cb-112">Alternatively, you can set the TTL by using the [**SetIpTTL**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipttl) function.</span></span>

 

 



