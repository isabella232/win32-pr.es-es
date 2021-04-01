---
description: En esta sección se describen las funciones, estructuras de datos y controles del Protocolo de control de transmisión/Protocolo de Internet (TCP/IP).
ms.assetid: ff92750b-453e-4328-821c-1098de8e6125
title: Anexo TCP/IP de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4fd86a016ed80d9c71ac1647323508cb4dc7b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275791"
---
# <a name="winsock-tcpip-annex"></a><span data-ttu-id="7c30f-103">Anexo TCP/IP de Winsock</span><span class="sxs-lookup"><span data-stu-id="7c30f-103">Winsock TCP/IP Annex</span></span>

<span data-ttu-id="7c30f-104">En esta sección se describen las funciones, estructuras de datos y controles del Protocolo de control de transmisión/Protocolo de Internet (TCP/IP).</span><span class="sxs-lookup"><span data-stu-id="7c30f-104">This section describes Transmission Control Protocol/Internet Protocol (TCP/IP) functions, data structures, and controls.</span></span>



| <span data-ttu-id="7c30f-105">Elemento</span><span class="sxs-lookup"><span data-stu-id="7c30f-105">Element</span></span>          | <span data-ttu-id="7c30f-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c30f-106">Description</span></span>                                                                                                                                 |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c30f-107">Nombre (s) de protocolo</span><span class="sxs-lookup"><span data-stu-id="7c30f-107">Protocol name(s)</span></span> | <span data-ttu-id="7c30f-108">TCP, UDP</span><span class="sxs-lookup"><span data-stu-id="7c30f-108">TCP, UDP</span></span>                                                                                                                                    |
| <span data-ttu-id="7c30f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c30f-109">Description</span></span>      | <span data-ttu-id="7c30f-110">Proporciona servicios de transporte a través del nivel de red IP: UDP para datagramas no confiables, TCP para flujos de bytes orientados a la conexión y confiables.</span><span class="sxs-lookup"><span data-stu-id="7c30f-110">Provides transport services over the IP networking layer: UDP for unreliable datagrams, TCP for reliable, connection-oriented byte streams.</span></span> |
| <span data-ttu-id="7c30f-111">Familia de direcciones</span><span class="sxs-lookup"><span data-stu-id="7c30f-111">Address family</span></span>   | <span data-ttu-id="7c30f-112">**AF \_ INET**, **AF \_ inet6**</span><span class="sxs-lookup"><span data-stu-id="7c30f-112">**AF\_INET**, **AF\_INET6**</span></span>                                                                                                                 |
| <span data-ttu-id="7c30f-113">Archivo de encabezado</span><span class="sxs-lookup"><span data-stu-id="7c30f-113">Header file</span></span>      | <span data-ttu-id="7c30f-114">*Ws2tcpip. h*</span><span class="sxs-lookup"><span data-stu-id="7c30f-114">*Ws2tcpip.h*</span></span>                                                                                                                                |



 

<span data-ttu-id="7c30f-115">Se ofrecen dos tipos básicos de servicios de transporte: datagramas no confiables (UDP) y de conexión confiable orientados a secuencias de bytes (TCP).</span><span class="sxs-lookup"><span data-stu-id="7c30f-115">Two basic types of transport services are offered: unreliable datagrams (UDP), and reliable connection oriented–byte streams (TCP).</span></span> <span data-ttu-id="7c30f-116">Además, se admite opcionalmente un socket sin formato.</span><span class="sxs-lookup"><span data-stu-id="7c30f-116">In addition, a raw socket is optionally supported.</span></span> <span data-ttu-id="7c30f-117">Los sockets sin formato permiten a una aplicación comunicarse a través de protocolos distintos de TCP y UDP, como ICMP.</span><span class="sxs-lookup"><span data-stu-id="7c30f-117">Raw sockets allow an application to communicate through protocols other than TCP and UDP such as ICMP.</span></span> <span data-ttu-id="7c30f-118">Los sockets sin formato se admiten en las familias de direcciones **AF \_ inetd** y **AF \_ inet6** con algunas limitaciones.</span><span class="sxs-lookup"><span data-stu-id="7c30f-118">Raw sockets are supported on the **AF\_INET** and **AF\_INET6** address families with some limitations.</span></span>

<span data-ttu-id="7c30f-119">En esta sección se describen las extensiones de Winsock que son específicas de los protocolos TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="7c30f-119">This section covers extensions to Winsock that are specific to TCP/IP protocols.</span></span> <span data-ttu-id="7c30f-120">También describe aspectos de las funciones base de Winsock que requieren una consideración especial o que pueden presentar un comportamiento único cuando se usa TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="7c30f-120">It also describes aspects of base Winsock functions that require special consideration or that may exhibit unique behavior when using TCP/IP.</span></span>

 

 



