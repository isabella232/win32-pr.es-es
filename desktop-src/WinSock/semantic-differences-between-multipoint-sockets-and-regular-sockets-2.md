---
title: Diferencias semánticas entre Multipoint sockets y Sockets normales
description: Diferencias entre los \_ sockets de Multipoint raíz de c y los sockets de punto a punto normales.
ms.assetid: fbadfde8-44dc-41ac-bd93-1a22c76ca321
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04d95b2637a4f805cea5ee6f138cc6992080a238
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706184"
---
# <a name="semantic-differences-between-multipoint-sockets-and-regular-sockets"></a><span data-ttu-id="8132d-103">Diferencias semánticas entre Multipoint sockets y Sockets normales</span><span class="sxs-lookup"><span data-stu-id="8132d-103">Semantic differences between multipoint sockets and regular sockets</span></span>

<span data-ttu-id="8132d-104">En el plano de control, hay algunas diferencias semánticas significativas entre un \_ socket raíz de c y un socket punto a punto normal:</span><span class="sxs-lookup"><span data-stu-id="8132d-104">In the control plane, there are some significant semantic differences between a c\_root socket and a regular point-to-point socket:</span></span>

-   <span data-ttu-id="8132d-105">El \_ socket raíz de c se puede usar en [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) para combinar una nueva hoja.</span><span class="sxs-lookup"><span data-stu-id="8132d-105">The c\_root socket can be used in [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) to join a new a leaf.</span></span>
-   <span data-ttu-id="8132d-106">La colocación de un \_ socket raíz de c en el modo de escucha (mediante una llamada a [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen)) no impide \_ que el socket raíz de c se use en una llamada a [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) para agregar una hoja nueva o para enviar y recibir datos de multipoint.</span><span class="sxs-lookup"><span data-stu-id="8132d-106">Placing a c\_root socket into listening mode (by calling [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen)) does not preclude the c\_root socket from being used in a call to [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) to add a new leaf, or for sending and receiving multipoint data.</span></span>
-   <span data-ttu-id="8132d-107">El cierre de un \_ socket raíz de c hace que todos los sockets de hoja de c asociados \_ obtengan una notificación de proximidad de FD \_ .</span><span class="sxs-lookup"><span data-stu-id="8132d-107">The closing of a c\_root socket causes all of the associated c\_leaf sockets to get FD\_CLOSE notification.</span></span>

<span data-ttu-id="8132d-108">No hay diferencias semánticas entre un socket de hoja de c \_ y un socket normal en el plano de control, salvo que el \_ socket de hoja de c se puede usar en [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)y el uso de \_ sockets de hoja de c en la [**escucha**](/windows/desktop/api/Winsock2/nf-winsock2-listen) indica que solo se deben aceptar solicitudes de conexión multipunto.</span><span class="sxs-lookup"><span data-stu-id="8132d-108">There are no semantic differences between a c\_leaf socket and a regular socket in the control plane, except that the c\_leaf socket can be used in [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), and the use of c\_leaf socket in [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) indicates that only multipoint connection requests should be accepted.</span></span>

<span data-ttu-id="8132d-109">En el plano de datos, las diferencias semánticas entre el \_ socket raíz d y un socket punto a punto normal son:</span><span class="sxs-lookup"><span data-stu-id="8132d-109">In the data plane, the semantic differences between the d\_root socket and a regular point-to-point socket are:</span></span>

-   <span data-ttu-id="8132d-110">Los datos enviados en el \_ socket raíz d se entregan a todas las hojas de la misma sesión multipoint.</span><span class="sxs-lookup"><span data-stu-id="8132d-110">The data sent on the d\_root socket is delivered to all the leaves in the same multipoint session.</span></span>
-   <span data-ttu-id="8132d-111">Los datos recibidos en el \_ socket raíz d pueden estar en cualquiera de las hojas.</span><span class="sxs-lookup"><span data-stu-id="8132d-111">The data received on the d\_root socket may be from any of the leaves.</span></span>

<span data-ttu-id="8132d-112">El \_ socket de hoja d del plano de datos raíz no tiene ninguna diferencia semántica con respecto al socket normal; sin embargo, en el plano de datos no raíz, los datos enviados en el \_ socket hoja d van a todos los demás nodos hoja, y los datos recibidos podrían ser de cualquier otro nodo hoja.</span><span class="sxs-lookup"><span data-stu-id="8132d-112">The d\_leaf socket in the rooted data plane has no semantic difference from the regular socket, however, in the nonrooted data plane, the data sent on the d\_leaf socket goes to all the other leaf nodes, and the data received could be from any other leaf nodes.</span></span> <span data-ttu-id="8132d-113">Como se mencionó anteriormente, la información sobre si el \_ socket de hoja d está en un plano de datos raíz o no raíz se encuentra en la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondiente para el socket.</span><span class="sxs-lookup"><span data-stu-id="8132d-113">As mentioned earlier, the information about whether the d\_leaf socket is in a rooted or nonrooted data plane is contained in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the socket.</span></span>

 

 
