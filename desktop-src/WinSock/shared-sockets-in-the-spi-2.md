---
description: Uso compartido de sockets en Windows Sockets (Winsock).
ms.assetid: dad31820-6f60-4c3b-9cdf-e301a5ffce48
title: Sockets compartidos en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21ff0d8f73d2bd9de942d17de7f9564158d1810c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908685"
---
# <a name="shared-sockets-in-the-spi"></a>Sockets compartidos en el SPI

El uso compartido de sockets entre procesos en Windows Sockets se implementa de la siguiente manera. Un proceso de origen llama a [**WSPDuplicateSocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85)) para obtener una estructura especial de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) . Utiliza algún mecanismo de comunicaciones entre procesos (IPC) para pasar el contenido de esta estructura a un proceso de destino. A continuación, el proceso de destino utiliza la estructura de **\_ información de WSAPROTOCOL** en una llamada a [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket). El descriptor de socket devuelto por esta función será un descriptor de socket adicional a un socket subyacente que, por tanto, se va a compartir.

Es responsabilidad del proveedor de servicios realizar todas las operaciones necesarias en el contexto del proceso de origen y crear una estructura [**de \_ información WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) que se reconocerá cuando aparezca posteriormente como un parámetro de [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) en el contexto de los procesos de destino. El miembro **dwProviderReserved** de la estructura de **\_ información de WSAPROTOCOL** está disponible para el uso del proveedor de servicios y se puede usar para almacenar información de contexto útil, incluido un identificador duplicado.

Este mecanismo está diseñado para ser adecuado para las versiones de Windows de un solo subproceso y preferente. Sin embargo, tenga en cuenta que los sockets se pueden compartir entre subprocesos en un proceso determinado sin usar la función [**WSPDuplicateSocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85)) , ya que un descriptor de socket es válido en todos los subprocesos del proceso.

Como se describe en la sección [asignación de descriptores](descriptor-allocation-2.md), cuando se asignan los nuevos descriptores de socket, los proveedores de IFS deben llamar a [**WPUModifyIFSHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpumodifyifshandle) y los proveedores que no son IFS deben llamar a [**WPUCreateSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreatesockethandle).

En la tabla siguiente se muestra un posible escenario para establecer y usar un socket compartido en un modo de entrega.

| Proceso de origen                                                                                                                          | IPC    | Proceso de destino                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------|-------------------------------------------------------------------------------|
| 1) [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket), [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))                                                                 |        |                                                                               |
| 2) solicita el identificador del proceso de destino.                                                                                                  | ==> |                                                                               |
|                                                                                                                                         |        | 3) recibe la solicitud de identificador de proceso y responde.                          |
| 4) recibe el identificador del proceso.                                                                                                         | <== |                                                                               |
| 5) llama a [**WSPDuplicateSocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85)) para obtener una estructura especial de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) . |        |                                                                               |
| 6) envía la estructura de **\_ información de WSAPROTOCOL** al destino.                                                                                     |        |                                                                               |
|                                                                                                                                         | ==> | 7) recibe la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .        |
|                                                                                                                                         |        | 8) llama a [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) para crear un descriptor de socket compartido. |
|                                                                                                                                         |        | 9) utiliza Sockets compartidos para el intercambio de datos.                                       |
| 10) [ **WSPClosesocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                                          | <== |                                                                               |



 

 

 
