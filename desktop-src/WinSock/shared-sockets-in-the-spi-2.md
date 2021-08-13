---
description: Uso compartido de sockets Windows sockets (Winsock).
ms.assetid: dad31820-6f60-4c3b-9cdf-e301a5ffce48
title: Sockets compartidos en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab0992768a7f3b38f27e4d40c54673e63e855687d0e9b9162e8b9e3cd1d1711d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559706"
---
# <a name="shared-sockets-in-the-spi"></a>Sockets compartidos en el SPI

El uso compartido de sockets entre Windows sockets se implementa como se muestra a continuación. Un proceso de origen llama a [**WSPDuplicateSocket para**](/previous-versions/windows/hardware/network/ff566282(v=vs.85)) obtener una estructura [**info de WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) especial. Usa algún mecanismo de comunicaciones entre procesos (IPC) para pasar el contenido de esta estructura a un proceso de destino. A continuación, el proceso de destino usa la **estructura \_ INFO de WSAPROTOCOL** en una llamada a [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket). El descriptor de socket devuelto por esta función será un descriptor de socket adicional para un socket subyacente que, por tanto, se comparte.

Es responsabilidad del proveedor de servicios realizar las operaciones necesarias en el contexto del proceso de origen y crear una estructura INFO de [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) que se reconocerá cuando aparezca posteriormente como un parámetro de [**WSPSocket en**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) el contexto de los procesos de destino. El **miembro dwProviderReserved** de la estructura **\_ INFO de WSAPROTOCOL** está disponible para el uso del proveedor de servicios y se puede usar para almacenar cualquier información de contexto útil, incluido un identificador duplicado.

Este mecanismo está diseñado para ser adecuado para las versiones multiproceso de un solo subproceso y preferentes de Windows. Sin embargo, tenga en cuenta que los sockets se pueden compartir entre subprocesos de un proceso determinado sin usar la función [**WSPDuplicateSocket,**](/previous-versions/windows/hardware/network/ff566282(v=vs.85)) ya que un descriptor de socket es válido en todos los subprocesos de un proceso.

Como se describe en la sección [Asignación](descriptor-allocation-2.md)de descriptores , cuando se asignan nuevos descriptores de socket, los proveedores IFS deben llamar a [**WPUModifyIFSHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpumodifyifshandle) y los proveedores que no sean IFS deben llamar a [**WPUCreateSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreatesockethandle).

En la tabla siguiente se muestra un escenario posible para establecer y usar un socket compartido en un modo de entrega.

| Proceso de origen                                                                                                                          | IPC    | Proceso de destino                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------|-------------------------------------------------------------------------------|
| 1) [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket), [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))                                                                 |        |                                                                               |
| 2) Solicita el identificador del proceso de destino.                                                                                                  | ==> |                                                                               |
|                                                                                                                                         |        | 3) Recibe la solicitud del identificador de proceso y responde.                          |
| 4) Recibe el identificador del proceso.                                                                                                         | <== |                                                                               |
| 5) Llama a [**WSPDuplicateSocket para**](/previous-versions/windows/hardware/network/ff566282(v=vs.85)) obtener una estructura [**info de WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) especial. |        |                                                                               |
| 6) Envía la **estructura \_ INFO de WSAPROTOCOL** al destino.                                                                                     |        |                                                                               |
|                                                                                                                                         | ==> | 7) Recibe la [**estructura \_ INFO de WSAPROTOCOL.**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)        |
|                                                                                                                                         |        | 8) Llama a [**WSPSocket para**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) crear el descriptor de socket compartido. |
|                                                                                                                                         |        | 9) Usa socket compartido para el intercambio de datos.                                       |
| 10) [ **WSPClosesocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                                          | <== |                                                                               |



 

 

 
