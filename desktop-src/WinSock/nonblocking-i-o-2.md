---
description: Si un socket está en modo de no bloqueo, cualquier operación de e/s debe completarse inmediatamente o devolver el código de error WSAEWOULDBLOCK, lo que indica que la operación no se puede finalizar de inmediato.
ms.assetid: badd279b-ec71-4761-9066-d501aa2485c2
title: Entrada/salida de no bloqueo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df9f6fec896c8daf1998e71a20a23a296b7b5a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541531"
---
# <a name="nonblocking-inputoutput"></a><span data-ttu-id="289fe-103">Entrada/salida de no bloqueo</span><span class="sxs-lookup"><span data-stu-id="289fe-103">Nonblocking Input/Output</span></span>

<span data-ttu-id="289fe-104">Si un socket está en modo de no bloqueo, cualquier operación de e/s debe completarse inmediatamente o devolver el código de error WSAEWOULDBLOCK, lo que indica que la operación no se puede finalizar de inmediato.</span><span class="sxs-lookup"><span data-stu-id="289fe-104">If a socket is in nonblocking mode, any I/O operation must either complete immediately or return the error code WSAEWOULDBLOCK indicating that the operation cannot be finished right away.</span></span> <span data-ttu-id="289fe-105">En el último caso, se necesita un mecanismo para detectar cuándo es adecuado volver a intentar la operación con la expectativa de que la operación se realizará correctamente.</span><span class="sxs-lookup"><span data-stu-id="289fe-105">In the latter case, a mechanism is needed to discover when it is appropriate to try the operation again with the expectation that the operation will succeed.</span></span> <span data-ttu-id="289fe-106">Se ha definido un conjunto de eventos de red para este fin.</span><span class="sxs-lookup"><span data-stu-id="289fe-106">A set of network events has been defined for this purpose.</span></span> <span data-ttu-id="289fe-107">Estos eventos se pueden sondear o esperar mediante [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)), o bien se pueden registrar para la entrega asincrónica llamando a [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) o [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="289fe-107">These events can be polled or waited on by using [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)), or they can be registered for asynchronous delivery by calling [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) or [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span></span> <span data-ttu-id="289fe-108">Consulte [notificación de eventos de red](notification-of-network-events-2.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="289fe-108">See [Notification of Network Events](notification-of-network-events-2.md) for more information.</span></span>

 

 
