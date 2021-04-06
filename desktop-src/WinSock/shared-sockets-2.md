---
description: La función WSADuplicateSocket se introduce para permitir el uso compartido de sockets entre los procesos.
ms.assetid: f7cf40e9-f3a6-4b62-8a78-df25464e2365
title: Sockets compartidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb6753b01f6389254756254d2ebe196af8e2a8a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001547"
---
# <a name="shared-sockets"></a>Sockets compartidos

La función [**WSADuplicateSocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa) se introduce para permitir el uso compartido de sockets entre los procesos. Un proceso de origen llama a **WSADuplicateSocket** para obtener una estructura especial de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para un identificador de proceso de destino. Utiliza algún mecanismo de comunicaciones entre procesos (IPC) para pasar el contenido de esta estructura a un proceso de destino. A continuación, el proceso de destino utiliza la estructura de **\_ información de WSAPROTOCOL** en una llamada a [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket). El descriptor de socket devuelto por esta función será un descriptor de socket adicional a un socket subyacente que, por tanto, se va a compartir. Los sockets se pueden compartir entre subprocesos en un proceso determinado sin usar la función **WSADuplicateSocket** porque un descriptor de socket es válido en todos los subprocesos de un proceso.

Los dos (o más) descriptores que hacen referencia a un socket compartido se pueden usar de forma independiente en lo que respecta a la e/s. Sin embargo, la interfaz Winsock no implementa ningún tipo de control de acceso, por lo que los procesos deben coordinar las operaciones en un socket compartido. Un ejemplo típico de uso compartido de sockets es usar un proceso para crear sockets y establecer conexiones. Este proceso, a continuación, entrega los sockets a otros procesos responsables del intercambio de información.

La función [**WSADuplicateSocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa) crea descriptores de socket y no el socket subyacente. Como resultado, todos los Estados asociados a un socket se mantienen en común en todos los descriptores. Por ejemplo, una [**operación de**](/windows/desktop/api/winsock/nf-winsock-setsockopt) r realizada con un descriptor es visible posteriormente mediante un [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) de uno o todos los descriptores. Un proceso puede llamar a [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) en un socket duplicado y el descriptor se desasignará. Sin embargo, el socket subyacente permanece abierto hasta que se llama a **closesocket** con el último descriptor restante.

La notificación en sockets compartidos está sujeta a las restricciones habituales de las funciones [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) y [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) . La emisión de cualquiera de estas llamadas mediante cualquiera de los descriptores compartidos cancela cualquier registro de eventos anterior para el socket, independientemente del descriptor que se haya utilizado para realizar ese registro. Por lo tanto, por ejemplo, no sería posible tener el procesamiento de eventos de lectura FD de recepción \_ y eventos de escritura FD de recepción de proceso B \_ . En situaciones en las que se requiere una coordinación tan estrecha, se recomienda que los desarrolladores utilicen subprocesos en lugar de procesos independientes.

 

 
