---
description: La función Select se usa para determinar el estado de uno o varios sockets de un conjunto. Para cada socket, el autor de la llamada puede solicitar información sobre el estado de lectura, escritura o error. Un conjunto de sockets se indica mediante una \_ estructura de conjunto FD.
ms.assetid: 40354d8f-1e8b-48aa-888a-81a421568f23
title: Varias restricciones de proveedor en Select
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2556d98aea60e6fa822f9e3df57cc142c33491d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154265"
---
# <a name="multiple-provider-restrictions-on-select"></a>Varias restricciones de proveedor en Select

La función [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) se usa para determinar el estado de uno o varios sockets de un conjunto. Para cada socket, el autor de la llamada puede solicitar información sobre el estado de lectura, escritura o error. Un conjunto de sockets se indica mediante una estructura de [**\_ conjunto FD**](/windows/desktop/api/winsock/nf-winsock-fd_set) .

Windows Sockets 2 permite que una aplicación use más de un proveedor de servicios, pero la función [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) está limitada a un conjunto de sockets asociados a un único proveedor de servicios. Esto no impide de ningún modo que una aplicación tenga varios Sockets abiertos a través de varios proveedores.

Hay dos maneras de determinar el estado de un conjunto de sockets que abarca más de un proveedor de servicios:

-   El uso de las funciones [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) o [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) cuando se emplea la semántica de bloqueo.
-   Usar la función [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) cuando se emplean operaciones de no bloqueo y la aplicación ya está utilizando un bombeo de mensajes de Windows.

Cuando una aplicación necesita usar la semántica de bloqueo en un conjunto de sockets que abarca varios proveedores, se recomienda [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) . La aplicación también puede usar la función [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) , que permite que los \_ eventos de red FD xxx (vea [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect)) se asocien a un objeto de evento y se controlen desde dentro del paradigma del objeto de evento (descrito en [e/s superpuestas y objetos de evento](overlapped-i-o-and-event-objects-2.md)).

La función [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) no está restringida a un único proveedor porque toma un único descriptor de socket como parámetro de entrada. Sin embargo, tenga en cuenta que la función [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) ofrece un mejor rendimiento y escalabilidad en **WSAAsyncSelect** a medida que la sobrecarga que supone mantener el bombeo de mensajes con mensajes de eventos Winsock aumenta a medida que aumenta el número total de sockets que se usan.

 

 



