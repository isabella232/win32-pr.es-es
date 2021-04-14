---
description: WSPCloseSocket libera el descriptor de socket para que se anulen todas las operaciones pendientes en los subprocesos del mismo proceso y se producirá un error en cualquier otra referencia a ella.
ms.assetid: 658d0c35-05d4-4b51-a4d3-a3b441a2c735
title: Cerrar Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d0c877767925f67e07427a77dc8ec8445f30c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541611"
---
# <a name="closing-sockets"></a><span data-ttu-id="5b0cc-103">Cerrar Sockets</span><span class="sxs-lookup"><span data-stu-id="5b0cc-103">Closing Sockets</span></span>

<span data-ttu-id="5b0cc-104">[**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) libera el descriptor de socket para que se anulen todas las operaciones pendientes en los subprocesos del mismo proceso y se producirá un error en cualquier otra referencia a ella.</span><span class="sxs-lookup"><span data-stu-id="5b0cc-104">[**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) releases the socket descriptor so that any pending operations in any threads of the same process will be aborted, and any further reference to it will fail.</span></span> <span data-ttu-id="5b0cc-105">Tenga en cuenta que se debe emplear un recuento de referencias para los sockets compartidos, y solo si se trata de la última referencia a un socket subyacente, en caso de que se descarte la información asociada a este socket, siempre que no se solicite el cierre correcto (es decir, \_ no se establece DONTLINGER).</span><span class="sxs-lookup"><span data-stu-id="5b0cc-105">Note that a reference count should be employed for shared sockets, and only if this is the last reference to an underlying socket, should the information associated with this socket be discarded, provided graceful close is not requested (that is, SO\_DONTLINGER is not set).</span></span> <span data-ttu-id="5b0cc-106">En el caso de que \_ se establezca DONTLINGER, se enviarán todos los datos en cola para la transmisión, si es posible, antes de que se libere la información asociada al socket.</span><span class="sxs-lookup"><span data-stu-id="5b0cc-106">In the case of SO\_DONTLINGER being set, any data queued for transmission will be sent, if possible, before information associated with the socket is released.</span></span> <span data-ttu-id="5b0cc-107">Vea **WSPCloseSocket** para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="5b0cc-107">See **WSPCloseSocket** for more information.</span></span>

<span data-ttu-id="5b0cc-108">En el caso de los proveedores de servicios de nonIFS, se debe invocar a [**WPUCloseSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuclosesockethandle) para liberar el identificador de socket de nuevo en el archivo dll de Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="5b0cc-108">For nonIFS service providers, [**WPUCloseSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuclosesockethandle) must be invoked to release the socket handle back to the Windows Sockets 2 DLL.</span></span>

 

 
