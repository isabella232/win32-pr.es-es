---
description: Windows Sockets 2 proporciona un método genérico para usar las capacidades multipoint y multidifusión de los transportes.
ms.assetid: 75cd8f21-a391-4626-b909-0760d12db995
title: Multidifusión y Multipoint Protocol-Independent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e409c18752b32af7cf65b4a55862ec75cec7a3e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696811"
---
# <a name="protocol-independent-multicast-and-multipoint"></a><span data-ttu-id="9d473-103">Multidifusión y Multipoint Protocol-Independent</span><span class="sxs-lookup"><span data-stu-id="9d473-103">Protocol-Independent Multicast and Multipoint</span></span>

<span data-ttu-id="9d473-104">Windows Sockets 2 proporciona un método genérico para usar las capacidades multipoint y multidifusión de los transportes.</span><span class="sxs-lookup"><span data-stu-id="9d473-104">Windows Sockets 2 provides a generic method for utilizing the multipoint and multicast capabilities of transports.</span></span> <span data-ttu-id="9d473-105">Este método genérico implementa estas características de la misma forma que permite el acceso a las capacidades básicas de transporte de datos de numerosos protocolos de transporte.</span><span class="sxs-lookup"><span data-stu-id="9d473-105">This generic method implements these features just as it allows the basic data transport capabilities of numerous transport protocols to be accessed.</span></span> <span data-ttu-id="9d473-106">El término, Multipoint, se usa en adelante para hacer referencia a las comunicaciones multidifusión y multipoint.</span><span class="sxs-lookup"><span data-stu-id="9d473-106">The term, multipoint, is used hereafter to refer to both multicast and multipoint communications.</span></span>

<span data-ttu-id="9d473-107">Las implementaciones de Multipoint actuales (por ejemplo, multidifusión IP, ST-II, T. 120 y ATM UNI) varían considerablemente.</span><span class="sxs-lookup"><span data-stu-id="9d473-107">Current multipoint implementations (for example, IP multicast, ST-II, T.120, and ATM UNI) vary widely.</span></span> <span data-ttu-id="9d473-108">Cómo se unen los nodos a una sesión de Multipoint, si un nodo determinado se designa como nodo central o raíz, y si los datos se intercambian entre todos los nodos o solo entre un nodo raíz y los distintos nodos hoja difieren entre las implementaciones.</span><span class="sxs-lookup"><span data-stu-id="9d473-108">How nodes join a multipoint session, whether a particular node is designated as a central or root node, and whether data is exchanged between all nodes or only between a root node and the various leaf nodes differ among implementations.</span></span> <span data-ttu-id="9d473-109">La estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para Windows Sockets 2 se usa para declarar los distintos atributos multipunto de un protocolo.</span><span class="sxs-lookup"><span data-stu-id="9d473-109">The [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for Windows Sockets 2 is used to declare the various multipoint attributes of a protocol.</span></span> <span data-ttu-id="9d473-110">Mediante el examen de estos atributos, el programador sabe qué convenciones seguir con las funciones de Windows Sockets 2 aplicables para configurar, emplear y anular sesiones multipoint.</span><span class="sxs-lookup"><span data-stu-id="9d473-110">By examining these attributes, the programmer knows what conventions to follow with the applicable Windows Sockets 2 functions to set up, utilize, and tear down multipoint sessions.</span></span>

<span data-ttu-id="9d473-111">A continuación se resumen las características de Winsock que admiten Multipoint:</span><span class="sxs-lookup"><span data-stu-id="9d473-111">The following summarizes Winsock features that support multipoint:</span></span>

-   <span data-ttu-id="9d473-112">Bits de dos atributos en la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .</span><span class="sxs-lookup"><span data-stu-id="9d473-112">Two-attribute bits in the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure.</span></span>
-   <span data-ttu-id="9d473-113">Cuatro marcas definidas para el parámetro *dwFlags* de la función [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) .</span><span class="sxs-lookup"><span data-stu-id="9d473-113">Four flags defined for the *dwFlags* parameter of the [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) function.</span></span>
-   <span data-ttu-id="9d473-114">Una función, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), para agregar nodos hoja en una sesión de Multipoint</span><span class="sxs-lookup"><span data-stu-id="9d473-114">One function, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), for adding leaf nodes into a multipoint session</span></span>
-   <span data-ttu-id="9d473-115">Dos códigos de comando [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) para controlar el bucle invertido multipunto y establecer el ámbito para las transmisiones de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="9d473-115">Two [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) command codes for controlling multipoint loopback and establishing the scope for multicast transmissions.</span></span> <span data-ttu-id="9d473-116">(Este último se corresponde con el parámetro TTL o período de vida de multidifusión IP).</span><span class="sxs-lookup"><span data-stu-id="9d473-116">(The latter corresponds to the IP multicast time-to-live or TTL parameter.)</span></span>

> [!Note]  
> <span data-ttu-id="9d473-117">La inclusión de estas características Multipoint en Windows Sockets 2 no impide que una aplicación use una interfaz dependiente del Protocolo existente, como las opciones de socket Deering para multidifusión IP.</span><span class="sxs-lookup"><span data-stu-id="9d473-117">The inclusion of these multipoint features in Windows Sockets 2 does not preclude an application from using an existing protocol-dependent interface, such as the Deering socket options for IP multicast.</span></span>

 

<span data-ttu-id="9d473-118">Consulte [semántica de multidifusión y multidifusión](multipoint-and-multicast-semantics-2.md) para obtener información detallada sobre cómo se caracterizan los distintos esquemas de multipoint y cómo se usan las características aplicables de Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="9d473-118">See [Multipoint and Multicast Semantics](multipoint-and-multicast-semantics-2.md) for detailed information on how the various multipoint schemes are characterized and how the applicable features of Windows Sockets 2 are utilized.</span></span>

 

 
