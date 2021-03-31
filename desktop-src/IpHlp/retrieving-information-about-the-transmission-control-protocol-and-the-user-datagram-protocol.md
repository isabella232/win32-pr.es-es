---
description: La aplicación auxiliar IP permite obtener acceso a información acerca de los protocolos de red que se usan en el equipo local.
ms.assetid: 3ae07fbd-0b69-42d6-81ab-cc239c354bbb
title: Recuperación de información sobre el protocolo de control de transmisión y el protocolo de datagramas de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99a73893bf379dda6a58f86854028967da806863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819483"
---
# <a name="retrieving-information-about-the-transmission-control-protocol-and-the-user-datagram-protocol"></a><span data-ttu-id="44e7e-103">Recuperación de información sobre el protocolo de control de transmisión y el protocolo de datagramas de usuario</span><span class="sxs-lookup"><span data-stu-id="44e7e-103">Retrieving Information About the Transmission Control Protocol and the User Datagram Protocol</span></span>

<span data-ttu-id="44e7e-104">La aplicación auxiliar IP permite obtener acceso a información acerca de los protocolos de red que se usan en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="44e7e-104">IP Helper makes it possible to access information about network protocols that are used on the local computer.</span></span> <span data-ttu-id="44e7e-105">Use las funciones descritas en los párrafos siguientes para recuperar información sobre el protocolo de control de transmisión (TCP) y el protocolo de datagramas de usuario (UDP) en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="44e7e-105">Use the functions described in the following paragraphs to retrieve information about the Transmission Control Protocol (TCP) and User Datagram Protocol (UDP) on the local computer.</span></span>

<span data-ttu-id="44e7e-106">La función [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) recupera las estadísticas actuales para TCP.</span><span class="sxs-lookup"><span data-stu-id="44e7e-106">The [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) function retrieves the current statistics for TCP.</span></span> <span data-ttu-id="44e7e-107">Para obtener ejemplos de código que impliquen a **GetTcpStatistics** , vea [recuperar información mediante GetTcpStatistics](retrieving-information-using-gettcpstatistics.md).</span><span class="sxs-lookup"><span data-stu-id="44e7e-107">For code samples involving **GetTcpStatistics** see [Retrieving Information Using GetTcpStatistics](retrieving-information-using-gettcpstatistics.md).</span></span>

<span data-ttu-id="44e7e-108">La función [**GetUdpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudpstatistics) recupera las estadísticas actuales para UDP.</span><span class="sxs-lookup"><span data-stu-id="44e7e-108">The [**GetUdpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudpstatistics) function retrieves the current statistics for UDP.</span></span>

<span data-ttu-id="44e7e-109">La función [**GetTcpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable) recupera la tabla de conexiones TCP.</span><span class="sxs-lookup"><span data-stu-id="44e7e-109">The [**GetTcpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable) function retrieves the TCP connection table.</span></span> <span data-ttu-id="44e7e-110">[**GetUdpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudptable) recupera la tabla de escucha de UDP.</span><span class="sxs-lookup"><span data-stu-id="44e7e-110">The [**GetUdpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudptable) retrieves the UDP listener table.</span></span>

<span data-ttu-id="44e7e-111">La función [**SetTcpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-settcpentry) permite a un desarrollador establecer el estado de una conexión TCP especificada en MIB \_ TCP \_ \_ Delete \_ TCB.</span><span class="sxs-lookup"><span data-stu-id="44e7e-111">The [**SetTcpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-settcpentry) function enables a developer to set the state of a specified TCP connection to MIB\_TCP\_STATE\_DELETE\_TCB.</span></span>

 

 



