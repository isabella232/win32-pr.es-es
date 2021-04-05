---
description: El destino predeterminado se puede cambiar simplemente llamando a WSPConnect, incluso si el socket ya está conectado. Los datagramas en cola para la recepción se descartan si la nueva dirección es diferente de la especificada en un WSPConnect anterior.
ms.assetid: b5f5ab97-03bd-4f5c-8808-d14ad5a56a5a
title: Volver a conectar y desconectar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7babefe03be44f942ee60a840aa210ee3c0e25da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908687"
---
# <a name="reconnecting-and-disconnecting"></a><span data-ttu-id="e5061-104">Volver a conectar y desconectar</span><span class="sxs-lookup"><span data-stu-id="e5061-104">Reconnecting and Disconnecting</span></span>

<span data-ttu-id="e5061-105">El destino predeterminado se puede cambiar simplemente llamando a [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) , incluso si el socket ya está conectado.</span><span class="sxs-lookup"><span data-stu-id="e5061-105">The default destination may be changed by simply calling [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) again, even if the socket is already connected.</span></span> <span data-ttu-id="e5061-106">Los datagramas en cola para la recepción se descartan si la nueva dirección es diferente de la especificada en un **WSPConnect** anterior.</span><span class="sxs-lookup"><span data-stu-id="e5061-106">Any datagrams queued for receipt are discarded if the new address is different from the address specified in a previous **WSPConnect**.</span></span>

<span data-ttu-id="e5061-107">Si la dirección proporcionada para el socket es cero, el socket se desconectará; la dirección remota predeterminada será indeterminada, por lo que las llamadas a [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) y [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) devolverán el código de error WSAENOTCONN, aunque es posible que se sigan usando [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) y [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e5061-107">If the address supplied for the socket is all zeros, the socket will be disconnected — the default remote address will be indeterminate, so [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) and [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) calls will return the error code WSAENOTCONN, although [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) and [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) may still be used.</span></span>

 

 
