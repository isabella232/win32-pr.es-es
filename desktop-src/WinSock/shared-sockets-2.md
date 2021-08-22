---
description: La función WSADuplicateSocket se introdujo para habilitar el uso compartido de sockets entre procesos.
ms.assetid: f7cf40e9-f3a6-4b62-8a78-df25464e2365
title: Sockets compartidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98e3f2663aa618b1bacab40b1cb29735c972e1d8b9e9db3528ee5079a336747c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612915"
---
# <a name="shared-sockets"></a>Sockets compartidos

La [**función WSADuplicateSocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa) se introdujo para habilitar el uso compartido de sockets entre procesos. Un proceso de origen llama a **WSADuplicateSocket para** obtener una estructura [**info de WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) especial para un identificador de proceso de destino. Usa algún mecanismo de comunicaciones entre procesos (IPC) para pasar el contenido de esta estructura a un proceso de destino. A continuación, el proceso de destino usa la **estructura \_ INFO de WSAPROTOCOL** en una llamada a [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket). El descriptor de socket devuelto por esta función será un descriptor de socket adicional para un socket subyacente que, por tanto, se comparte. Los sockets se pueden compartir entre subprocesos de un proceso determinado sin usar la función **WSADuplicateSocket** porque un descriptor de socket es válido en todos los subprocesos de un proceso.

Los dos (o más) descriptores que hacen referencia a un socket compartido se pueden usar de forma independiente en lo que respecta a la E/S. Sin embargo, la interfaz Winsock no implementa ningún tipo de control de acceso, por lo que los procesos deben coordinar las operaciones en un socket compartido. Un ejemplo típico de uso compartido de sockets es usar un proceso para crear sockets y establecer conexiones. A continuación, este proceso entrega sockets a otros procesos responsables del intercambio de información.

La [**función WSADuplicateSocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa) crea descriptores de socket y no el socket subyacente. Como resultado, todos los estados asociados a un socket se mantienen en común en todos los descriptores. Por ejemplo, una [**operación setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) realizada con un descriptor se puede ver posteriormente mediante [**un getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) de cualquiera o de todos los descriptores. Un proceso puede llamar [**a closesocket en**](/windows/desktop/api/winsock/nf-winsock-closesocket) un socket duplicado y el descriptor se desasignará. Sin embargo, el socket subyacente permanece abierto hasta que se llama **a closesocket** con el último descriptor restante.

La notificación en sockets compartidos está sujeta a las restricciones habituales de las funciones [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) y [**WSAEventSelect.**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) La emisión de cualquiera de estas llamadas mediante cualquiera de los descriptores compartidos cancela cualquier registro de eventos anterior para el socket, independientemente del descriptor que se usó para realizar ese registro. Por lo tanto, por ejemplo, no sería posible que el proceso A reciba eventos DE LECTURA de FD y que \_ el proceso B reciba eventos FD \_ WRITE. En situaciones en las que se requiere una coordinación tan estrecha, se recomienda que los desarrolladores usen subprocesos en lugar de procesos independientes.

 

 
