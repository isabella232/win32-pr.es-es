---
description: Diferencias entre sockets de punto a punto normales y \_ sockets de Multipoint raíz de c en el SPI de Windows Sockets (Winsock).
ms.assetid: 5476933b-70f2-4dcf-a6e9-f9f4a537c29f
title: Diferencias semánticas entre los sockets multipoint y los sockets normales en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd9e4e94583ee653a8ec0bf19c743dddd3e16253
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706104"
---
# <a name="semantic-differences-between-multipoint-sockets-and-regular-sockets-in-the-spi"></a><span data-ttu-id="4b5fd-103">Diferencias semánticas entre los sockets multipoint y los sockets normales en el SPI</span><span class="sxs-lookup"><span data-stu-id="4b5fd-103">Semantic Differences Between Multipoint Sockets and Regular Sockets in the SPI</span></span>

<span data-ttu-id="4b5fd-104">En el plano de control, hay algunas diferencias semánticas significativas entre un \_ socket raíz de c y un socket punto a punto normal:</span><span class="sxs-lookup"><span data-stu-id="4b5fd-104">In the control plane, there are some significant semantic differences between a c\_root socket and a regular point-to-point socket:</span></span>

-   <span data-ttu-id="4b5fd-105">El \_ socket raíz de c se puede usar en [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) para unir una nueva hoja.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-105">The c\_root socket can be used in [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) to join a new leaf.</span></span>
-   <span data-ttu-id="4b5fd-106">La colocación de un \_ socket raíz de c en el modo de escucha (llamando a [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))) no impide \_ que el socket raíz de c se use en una llamada a [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) para agregar una hoja nueva o para enviar y recibir datos de multipoint.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-106">Placing a c\_root socket into the listening mode (by calling [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))) does not preclude the c\_root socket from being used in a call to [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) to add a new leaf, or for sending and receiving multipoint data.</span></span>
-   <span data-ttu-id="4b5fd-107">El cierre de un \_ socket raíz de c hará que todos los sockets de hoja de c asociados \_ obtengan la \_ notificación FD Close.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-107">The closing of a c\_root socket will cause all the associated c\_leaf sockets to get FD\_CLOSE notification.</span></span>

<span data-ttu-id="4b5fd-108">No hay diferencias semánticas entre un socket de hoja de c \_ y un socket normal en el plano de control, salvo que el \_ socket de hoja de c se puede usar en [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf), y el uso del socket de hoja de c \_ en [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) indica que solo se deben aceptar solicitudes de conexión multipunto.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-108">There are no semantic differences between a c\_leaf socket and a regular socket in the control plane, except that the c\_leaf socket can be used in [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf), and the use of c\_leaf socket in [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) indicates that only multipoint connection requests should be accepted.</span></span>

<span data-ttu-id="4b5fd-109">En el plano de datos, las diferencias semánticas entre el \_ socket raíz d y un socket punto a punto normal son</span><span class="sxs-lookup"><span data-stu-id="4b5fd-109">In the data plane, the semantic differences between the d\_root socket and a regular point-to-point socket are</span></span>

-   <span data-ttu-id="4b5fd-110">Los datos enviados en el \_ socket raíz d se entregarán a todas las hojas de la misma sesión multipoint.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-110">The data sent on the d\_root socket will be delivered to all the leaves in the same multipoint session.</span></span>
-   <span data-ttu-id="4b5fd-111">Los datos recibidos en el \_ socket raíz d pueden estar en cualquiera de las hojas.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-111">The data received on the d\_root socket may be from any of the leaves.</span></span>

<span data-ttu-id="4b5fd-112">El \_ socket de hoja d del plano de datos raíz no tiene ninguna diferencia semántica con respecto al socket normal; sin embargo, en el plano de datos no raíz, los datos enviados en el \_ socket de hoja d Irán a todos los demás nodos hoja, y los datos recibidos podrían ser de cualquier otro nodo hoja.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-112">The d\_leaf socket in the rooted data plane has no semantic difference from the regular socket, however, in the nonrooted data plane, the data sent on the d\_leaf socket will go to all of the other leaf nodes, and the data received could be from any of the other leaf nodes.</span></span> <span data-ttu-id="4b5fd-113">Como se mencionó anteriormente, la información sobre si el \_ socket de hoja d está en un plano de datos raíz o no raíz se encuentra en la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondiente para el socket.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-113">As mentioned earlier, the information about whether the d\_leaf socket is in a rooted or nonrooted data plane is contained in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the socket.</span></span>

 

 
