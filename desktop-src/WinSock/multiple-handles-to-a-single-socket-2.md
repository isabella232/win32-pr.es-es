---
description: Puesto que los elementos duplicados son los descriptores de socket y no los sockets subyacentes, todos los Estados asociados a un socket se mantienen en común en todos los descriptores.
ms.assetid: f3a2cd5a-bc3a-4aeb-8606-7b8aa6afb105
title: Varios identificadores para un solo socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2356f24a69d132f87e0f6543f61509ff12acba5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696372"
---
# <a name="multiple-handles-to-a-single-socket"></a><span data-ttu-id="2b900-103">Varios identificadores para un solo socket</span><span class="sxs-lookup"><span data-stu-id="2b900-103">Multiple Handles to a Single Socket</span></span>

<span data-ttu-id="2b900-104">Puesto que los elementos duplicados son los descriptores de socket y no los sockets subyacentes, todos los Estados asociados a un socket se mantienen en común en todos los descriptores.</span><span class="sxs-lookup"><span data-stu-id="2b900-104">Since what are duplicated are the socket descriptors and not the underlying sockets, all of the states associated with a socket are held in common across all the descriptors.</span></span> <span data-ttu-id="2b900-105">Por ejemplo, una operación de [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) realizada con un descriptor es visible posteriormente mediante un [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) de uno o todos los descriptores.</span><span class="sxs-lookup"><span data-stu-id="2b900-105">For example a [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) operation performed using one descriptor is subsequently visible using a [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) from any or all descriptors.</span></span>

<span data-ttu-id="2b900-106">La notificación en sockets compartidos está sujeta a las restricciones habituales de [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) y [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2b900-106">Notification on shared sockets is subject to the usual constraints of [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) and [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span></span> <span data-ttu-id="2b900-107">La emisión de cualquiera de estas llamadas mediante cualquiera de los descriptores compartidos cancela cualquier registro de eventos anterior para el socket, independientemente del descriptor que se haya utilizado para realizar ese registro.</span><span class="sxs-lookup"><span data-stu-id="2b900-107">Issuing either of these calls using any of the shared descriptors cancels any previous event registration for the socket, regardless of which descriptor was used to make that registration.</span></span> <span data-ttu-id="2b900-108">Por lo tanto, por ejemplo, no sería posible tener el procesamiento de eventos de lectura FD de recepción \_ y eventos de escritura FD de recepción de proceso B \_ .</span><span class="sxs-lookup"><span data-stu-id="2b900-108">Thus, for example, it would not be possible to have process A receive FD\_READ events and process B receive FD\_WRITE events.</span></span> <span data-ttu-id="2b900-109">En situaciones en las que se requiere una coordinación tan estrecha, se recomienda que los desarrolladores consideren el uso de subprocesos en lugar de procesos independientes.</span><span class="sxs-lookup"><span data-stu-id="2b900-109">For situations when such tight coordination is required, it is suggested that developers consider using threads instead of separate processes.</span></span>

 

 
