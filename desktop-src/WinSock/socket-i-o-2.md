---
description: Mediante la e/s de bloqueo, la e/s de no bloqueo con notificación asincrónica de eventos de red y la e/s superpuestas con indicación de finalización en Windows Sockets 2 (Winsock).
ms.assetid: 07f34177-72bc-4b2a-b655-57e53d1742b0
title: E/s de socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9efcd325a0a379671dd39709f37e2c6d2133ca27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154246"
---
# <a name="socket-io"></a><span data-ttu-id="8325f-103">E/s de socket</span><span class="sxs-lookup"><span data-stu-id="8325f-103">Socket I/O</span></span>

<span data-ttu-id="8325f-104">Existen tres formas principales de realizar operaciones de e/s en Windows Sockets 2:</span><span class="sxs-lookup"><span data-stu-id="8325f-104">There are three primary ways of doing I/O in Windows Sockets 2:</span></span>

-   <span data-ttu-id="8325f-105">E/s de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="8325f-105">Blocking I/O.</span></span>
-   <span data-ttu-id="8325f-106">E/s de no bloqueo junto con notificación asincrónica de eventos de red.</span><span class="sxs-lookup"><span data-stu-id="8325f-106">Nonblocking I/O along with asynchronous notification of network events.</span></span>
-   <span data-ttu-id="8325f-107">E/s superpuestas con indicación de finalización.</span><span class="sxs-lookup"><span data-stu-id="8325f-107">Overlapped I/O with completion indication.</span></span>

<span data-ttu-id="8325f-108">En las secciones siguientes se describe cada método.</span><span class="sxs-lookup"><span data-stu-id="8325f-108">We describe each method in the following sections.</span></span> <span data-ttu-id="8325f-109">El bloqueo de e/s es el comportamiento predeterminado, el modo de no bloqueo se puede usar en cualquier socket que se encuentre en modo de no bloqueo, y la e/s superpuesta solo puede producirse en sockets creados con el atributo superpuesto.</span><span class="sxs-lookup"><span data-stu-id="8325f-109">Blocking I/O is the default behavior, nonblocking mode can be used on any socket that is placed into nonblocking mode, and overlapped I/O can only occur on sockets that are created with the overlapped attribute.</span></span> <span data-ttu-id="8325f-110">También es interesante tener en cuenta que las dos llamadas para enviar: [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) y [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) y las dos llamadas para recibir: [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) y [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) implementan los tres métodos de e/s.</span><span class="sxs-lookup"><span data-stu-id="8325f-110">It is also interesting to note that the two calls for sending: [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) and [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) and the two calls for receiving: [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) and [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) each implement all three methods of I/O.</span></span> <span data-ttu-id="8325f-111">Los proveedores de servicios determinan cómo realizar la operación de e/s en función de los modos de socket, atributos y valores de parámetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="8325f-111">Service providers determine how to perform the I/O operation based on socket modes, attributes, and the input parameter values.</span></span>

 

 
