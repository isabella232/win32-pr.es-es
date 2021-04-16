---
description: Los objetos de evento de Windows Sockets son construcciones simples que se pueden crear y cerrar, establecer y borrar, esperar y sondear.
ms.assetid: 65a7627e-150e-4ca3-bc17-d2b380ee02d1
title: Usar objetos de eventos (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26a9b70ff49bf7d46f2907c04fd8911d55dd623
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705588"
---
# <a name="using-event-objects-windows-sockets-2"></a><span data-ttu-id="529fc-103">Usar objetos de eventos (Windows Sockets 2)</span><span class="sxs-lookup"><span data-stu-id="529fc-103">Using Event Objects (Windows Sockets 2)</span></span>

<span data-ttu-id="529fc-104">Los objetos de evento de Windows Sockets son construcciones simples que se pueden crear y cerrar, establecer y borrar, esperar y sondear.</span><span class="sxs-lookup"><span data-stu-id="529fc-104">Windows Sockets event objects are simple constructs that can be created and closed, set and cleared, waited upon and polled.</span></span> <span data-ttu-id="529fc-105">El modelo aceptado es para que los clientes creen un objeto de evento y suministren el identificador como un parámetro (o como un componente de una estructura de parámetros) en funciones como [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) y [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="529fc-105">The accepted model is for clients to create an event object and supply the handle as a parameter (or as a component of a parameter structure) in functions such as [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) and [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span></span> <span data-ttu-id="529fc-106">Cuando se ha producido la condición nombrada, el proveedor de servicios utiliza el identificador para establecer el objeto de evento mediante una llamada a [**WPUSetEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpusetevent).</span><span class="sxs-lookup"><span data-stu-id="529fc-106">When the nominated condition has occurred, the service provider uses the handle to set the event object by calling [**WPUSetEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpusetevent).</span></span> <span data-ttu-id="529fc-107">Mientras tanto, el cliente de Winsock SPI puede bloquear y esperar o sondear hasta que el objeto de evento se establezca (señalado).</span><span class="sxs-lookup"><span data-stu-id="529fc-107">Meanwhile, the Winsock SPI client may either block and wait or poll until the event object becomes set (signaled).</span></span> <span data-ttu-id="529fc-108">Después, el cliente puede borrar o restablecer el objeto de evento y volver a usarlo.</span><span class="sxs-lookup"><span data-stu-id="529fc-108">The client may subsequently clear or reset the event object and use it again.</span></span>

 

 
