---
description: WSPCloseSocket libera el descriptor de socket para que se anulen las operaciones pendientes en cualquier subproceso del mismo proceso y se producirá un error en cualquier referencia adicional a él.
ms.assetid: 658d0c35-05d4-4b51-a4d3-a3b441a2c735
title: Cierre de sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc35b7ba401e43494d49815e17eca19bd25b0080a385c40813209037c858a456
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051693"
---
# <a name="closing-sockets"></a>Cierre de sockets

[**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) libera el descriptor de socket para que se anulen las operaciones pendientes en cualquier subproceso del mismo proceso y se producirá un error en cualquier referencia adicional a él. Tenga en cuenta que se debe emplear un recuento de referencias para los sockets compartidos y solo si se trata de la última referencia a un socket subyacente, si se descarta la información asociada a este socket, siempre que no se solicite un cierre correcto (es decir, no se establece \_ SO DONTLINGER). En el caso de que se establezca SO DONTLINGER, los datos que se ponen en cola para la transmisión se enviarán, si es posible, antes de que se libera la información \_ asociada al socket. Vea **WSPCloseSocket para** obtener más información.

En el caso de los proveedores de servicios que no sonIFS, se debe invocar [**WPUCloseSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuclosesockethandle) para liberar el identificador de socket de nuevo al archivo DLL Windows Sockets 2.

 

 
