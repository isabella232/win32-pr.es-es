---
description: Capacidades de multidifusión y multidifusión independientes del protocolo y de Windows Sockets (Winsock).
ms.assetid: 861f457c-fe7e-4128-a3f3-786424a96ea5
title: Protocol-Independent multidifusión y Multipoint en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bda9e5cab1b790a1e2d2c64c4451063a94dd8bc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156021"
---
# <a name="protocol-independent-multicast-and-multipoint-in-the-spi"></a><span data-ttu-id="7972d-103">Protocol-Independent multidifusión y Multipoint en el SPI</span><span class="sxs-lookup"><span data-stu-id="7972d-103">Protocol-Independent Multicast and Multipoint in the SPI</span></span>

<span data-ttu-id="7972d-104">Del mismo modo que Windows Sockets 2 permite tener acceso a las capacidades básicas de transporte de datos de numerosos protocolos de transporte de forma genérica, también proporciona una manera genérica de usar las capacidades multipoint y multidifusión de los transportes que implementan estas características.</span><span class="sxs-lookup"><span data-stu-id="7972d-104">Just as Windows Sockets 2 allows the basic data transport capabilities of numerous transport protocols to be accessed in a generic manner, it also provides a generic way to use multipoint and multicast capabilities of transports that implement these features.</span></span> <span data-ttu-id="7972d-105">Para simplificar, el término *Multipoint* se usa en adelante para hacer referencia a las comunicaciones multidifusión y multipoint.</span><span class="sxs-lookup"><span data-stu-id="7972d-105">To simplify, the term *multipoint* is used hereafter to refer to both multicast and multipoint communications.</span></span>

<span data-ttu-id="7972d-106">Las implementaciones de Multipoint actuales (por ejemplo, IP multicast, ST-II, T. 120, ATM UNI) varían en gran medida en lo que respecta al modo en que los nodos se unen a una sesión de Multipoint, si un nodo determinado se designa como nodo central o raíz y si los datos se intercambian entre todos los nodos o solo entre un nodo raíz y varios</span><span class="sxs-lookup"><span data-stu-id="7972d-106">Current multipoint implementations (for example, IP multicast, ST-II, T.120, ATM UNI) vary widely with respect to how nodes join a multipoint session, whether a particular node is designated as a central or root node, and whether data is exchanged between all nodes or only between a root node and various leaf nodes.</span></span> <span data-ttu-id="7972d-107">La estructura de [**\_ información WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) de Windows Sockets 2 se usa para declarar los atributos multipunto de un protocolo.</span><span class="sxs-lookup"><span data-stu-id="7972d-107">The Windows Sockets 2 [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure is used to declare the multipoint attributes of a protocol.</span></span> <span data-ttu-id="7972d-108">Mediante el examen de estos atributos, el programador sabrá qué convenciones seguir en el uso de las funciones de Winsock aplicables para configurar, usar y anular las sesiones de multipoint.</span><span class="sxs-lookup"><span data-stu-id="7972d-108">By examining these attributes the programmer will know what conventions to follow in using the applicable Winsock functions to set up, use, and tear down multipoint sessions.</span></span>

<span data-ttu-id="7972d-109">Las características de Windows Sockets 2 que admiten la multidifusión se pueden resumir de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="7972d-109">The features of Windows Sockets 2 that support multicast can be summarized as follows:</span></span>

-   <span data-ttu-id="7972d-110">Tres bits de atributo en la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .</span><span class="sxs-lookup"><span data-stu-id="7972d-110">Three attribute bits in the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure.</span></span>
-   <span data-ttu-id="7972d-111">Cuatro marcas definidas para el parámetro *dwFlags* de [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)</span><span class="sxs-lookup"><span data-stu-id="7972d-111">Four flags defined for the *dwFlags* parameter of [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)</span></span>
-   <span data-ttu-id="7972d-112">Una función, [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf), para agregar nodos hoja en una sesión multipoint.</span><span class="sxs-lookup"><span data-stu-id="7972d-112">One function, [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf), for adding leaf nodes into a multipoint session.</span></span>
-   <span data-ttu-id="7972d-113">Dos códigos de comando [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) para controlar el bucle invertido multipunto y establecer el ámbito para las transmisiones de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="7972d-113">Two [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) command codes for controlling multipoint loopback and establishing the scope for multicast transmissions.</span></span> <span data-ttu-id="7972d-114">(Este último se corresponde con el parámetro TTL o período de vida de multidifusión IP).</span><span class="sxs-lookup"><span data-stu-id="7972d-114">(The latter corresponds to the IP multicast time-to-live or TTL parameter.)</span></span>

> [!Note]  
> <span data-ttu-id="7972d-115">La inclusión de estas características Multipoint en Windows Sockets 2 no impide que un proveedor de servicios admita también una interfaz dependiente del Protocolo existente, como las opciones de socket Deering para multidifusión IP.</span><span class="sxs-lookup"><span data-stu-id="7972d-115">The inclusion of these multipoint features in Windows Sockets 2 does not preclude a service provider from also supporting an existing protocol-dependent interface, such as the Deering socket options for IP multicast.</span></span>

 

 

 
