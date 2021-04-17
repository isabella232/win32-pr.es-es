---
description: En esta sección se describe la implementación del Protocolo de multidifusión PGM (multidifusión general pragmática) en Windows, que a menudo se conoce como multidifusión confiable. La multidifusión confiable se implementa a través de Windows Sockets en Windows Server 2003 y versiones posteriores.
ms.assetid: 81c203ed-739f-4a06-99a1-9a99c6164edc
title: Programación de multidifusión confiable (PGM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce57fcce7bf2faf471604bed97d345971801ca1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706195"
---
# <a name="reliable-multicast-programming-pgm"></a><span data-ttu-id="ad3c2-104">Programación de multidifusión confiable (PGM)</span><span class="sxs-lookup"><span data-stu-id="ad3c2-104">Reliable Multicast Programming (PGM)</span></span>

<span data-ttu-id="ad3c2-105">En esta sección se describe la implementación del Protocolo de multidifusión PGM (multidifusión general pragmática) en Windows, que a menudo se conoce como multidifusión confiable.</span><span class="sxs-lookup"><span data-stu-id="ad3c2-105">This section describes the Pragmatic General Multicast (PGM) multicast protocol implementation in Windows, often referred to as reliable multicast.</span></span> <span data-ttu-id="ad3c2-106">La multidifusión confiable se implementa a través de Windows Sockets en Windows Server 2003 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="ad3c2-106">Reliable multicast is implemented through Windows Sockets in Windows Server 2003 and later.</span></span>

<span data-ttu-id="ad3c2-107">**Windows XP:** PGM solo se admite cuando se instala Microsoft Message Queuing (MSMQ) 3,0.</span><span class="sxs-lookup"><span data-stu-id="ad3c2-107">**Windows XP:** PGM is only supported when Microsoft Message Queuing (MSMQ) 3.0 is installed.</span></span>

<span data-ttu-id="ad3c2-108">PGM es un protocolo de multidifusión confiable y escalable que permite a los receptores detectar la pérdida, solicitar la retransmisión de datos perdidos o notificar a una aplicación de una pérdida irrecuperable.</span><span class="sxs-lookup"><span data-stu-id="ad3c2-108">PGM is a reliable and scalable multicast protocol that enables receivers to detect loss, request retransmission of lost data, or notify an application of unrecoverable loss.</span></span> <span data-ttu-id="ad3c2-109">PGM es un protocolo de confianza del receptor, lo que significa que el receptor es responsable de garantizar que se reciban todos los datos, absolving el remitente de la responsabilidad de la recepción.</span><span class="sxs-lookup"><span data-stu-id="ad3c2-109">PGM is a receiver-reliable protocol, which means the receiver is responsible for ensuring all data is received, absolving the sender of reception responsibility.</span></span>

<span data-ttu-id="ad3c2-110">PGM es adecuado para aplicaciones que requieren la entrega de datos de multidifusión sin duplicar desde varios orígenes a varios receptores.</span><span class="sxs-lookup"><span data-stu-id="ad3c2-110">PGM is appropriate for applications that require duplicate-free multicast data delivery from multiple sources to multiple receivers.</span></span> <span data-ttu-id="ad3c2-111">PGM no admite la entrega confirmada, ni garantiza el orden de los paquetes de varios remitentes.</span><span class="sxs-lookup"><span data-stu-id="ad3c2-111">PGM does not support acknowledged delivery, nor does it guarantee ordering of packets from multiple senders.</span></span>

<span data-ttu-id="ad3c2-112">Para obtener más información sobre PGM, consulte RFC 3208 disponible en [www.ietf.org](https://www.ietf.org/).</span><span class="sxs-lookup"><span data-stu-id="ad3c2-112">For more information about PGM, refer to RFC 3208 available at [www.ietf.org](https://www.ietf.org/).</span></span>

<span data-ttu-id="ad3c2-113">En esta sección se describe cómo usar la multidifusión confiable en Windows.</span><span class="sxs-lookup"><span data-stu-id="ad3c2-113">This section describes how to use reliable multicast on Windows.</span></span> <span data-ttu-id="ad3c2-114">En los temas siguientes se explican los diversos aspectos de la creación de una aplicación de multidifusión confiable mediante Windows Sockets:</span><span class="sxs-lookup"><span data-stu-id="ad3c2-114">The following topics explain the various aspects of creating a reliable multicast application using Windows Sockets:</span></span>

-   [<span data-ttu-id="ad3c2-115">Receptores y remitentes de PGM</span><span class="sxs-lookup"><span data-stu-id="ad3c2-115">PGM Senders and Receivers</span></span>](pgm-senders-and-receivers.md)
-   [<span data-ttu-id="ad3c2-116">Opciones del remitente de PGM</span><span class="sxs-lookup"><span data-stu-id="ad3c2-116">PGM Sender Options</span></span>](pgm-sender-options.md)
-   [<span data-ttu-id="ad3c2-117">Envío y recepción de datos PGM</span><span class="sxs-lookup"><span data-stu-id="ad3c2-117">Sending and Receiving PGM Data</span></span>](sending-and-receiving-pgm-data.md)
-   [<span data-ttu-id="ad3c2-118">Host múltiple y PGM</span><span class="sxs-lookup"><span data-stu-id="ad3c2-118">Multihoming and PGM</span></span>](multihoming-and-pgm.md)
-   [<span data-ttu-id="ad3c2-119">Opciones de socket PGM</span><span class="sxs-lookup"><span data-stu-id="ad3c2-119">PGM Socket Options</span></span>](pgm-socket-options.md)

 

 



