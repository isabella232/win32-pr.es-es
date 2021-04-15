---
description: Elementos de la interfaz de Windows Sockets 2 (Winsock) para multipoint y multidifusión.
ms.assetid: c6f704cf-031b-4714-9f07-2d7715a157a0
title: Elementos de la interfaz de Windows Sockets 2 para multipoint y multidifusión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad86905fe19c5c4c603db488874039b7cc8a0b2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715473"
---
# <a name="windows-sockets-2-interface-elements-for-multipoint-and-multicast"></a><span data-ttu-id="15061-103">Elementos de la interfaz de Windows Sockets 2 para multipoint y multidifusión</span><span class="sxs-lookup"><span data-stu-id="15061-103">Windows Sockets 2 Interface Elements for Multipoint and Multicast</span></span>

<span data-ttu-id="15061-104">Los mecanismos que se han incorporado a Windows Sockets 2 para usar las capacidades de Multipoint se pueden resumir de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="15061-104">The mechanisms that have been incorporated into Windows Sockets 2 for utilizing multipoint capabilities can be summarized as follows:</span></span>

-   <span data-ttu-id="15061-105">Tres bits de atributo en la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .</span><span class="sxs-lookup"><span data-stu-id="15061-105">Three attribute bits in the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure.</span></span>
-   <span data-ttu-id="15061-106">Cuatro marcas definidas para el parámetro *dwFlags* de [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa).</span><span class="sxs-lookup"><span data-stu-id="15061-106">Four flags defined for the *dwFlags* parameter of [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa).</span></span>
-   <span data-ttu-id="15061-107">Una función, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), para agregar nodos hoja en una sesión multipoint.</span><span class="sxs-lookup"><span data-stu-id="15061-107">One function, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), for adding leaf nodes into a multipoint session.</span></span>
-   <span data-ttu-id="15061-108">Dos códigos de comando [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) para controlar el bucle invertido multipoint y el ámbito de las transmisiones de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="15061-108">Two [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) command codes for controlling multipoint loopback and the scope of multicast transmissions.</span></span>

<span data-ttu-id="15061-109">En las secciones siguientes se describen estos elementos de interfaz con más detalle:</span><span class="sxs-lookup"><span data-stu-id="15061-109">The following sections describe these interface elements in more detail:</span></span>

-   [<span data-ttu-id="15061-110">Semántica para combinar hojas de Multipoint</span><span class="sxs-lookup"><span data-stu-id="15061-110">Semantics for Joining Multipoint Leaves</span></span>](semantics-for-joining-multipoint-leaves-2.md)
-   [<span data-ttu-id="15061-111">Cómo los protocolos Multipoint existentes admiten estas extensiones</span><span class="sxs-lookup"><span data-stu-id="15061-111">How Existing Multipoint Protocols Support These Extensions</span></span>](how-existing-multipoint-protocols-support-these-extensions-2.md)

 

 
