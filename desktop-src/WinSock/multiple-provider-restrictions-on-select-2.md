---
description: La función select se usa para determinar el estado de uno o varios sockets de un conjunto. Para cada socket, el autor de la llamada puede solicitar información sobre el estado de lectura, escritura o error. Un conjunto de sockets se indica mediante una estructura FD \_ SET.
ms.assetid: 40354d8f-1e8b-48aa-888a-81a421568f23
title: Restricciones de varios proveedores al seleccionar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec5c89c6dd2db809a356f5b53212fd019e32fd9e348c298bcab7f567ee2d0fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569635"
---
# <a name="multiple-provider-restrictions-on-select"></a>Restricciones de varios proveedores al seleccionar

La [**función select**](/windows/desktop/api/Winsock2/nf-winsock2-select) se usa para determinar el estado de uno o varios sockets de un conjunto. Para cada socket, el autor de la llamada puede solicitar información sobre el estado de lectura, escritura o error. Un conjunto de sockets se indica mediante una [**estructura FD \_ SET.**](/windows/desktop/api/winsock/nf-winsock-fd_set)

Windows Sockets 2 permite que una aplicación use más de un proveedor de servicios, pero la función [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) se limita a un conjunto de sockets asociado a un único proveedor de servicios. Esto no impide de ninguna manera que una aplicación tenga varios sockets abiertos a través de varios proveedores.

Hay dos maneras de determinar el estado de un conjunto de sockets que abarca más de un proveedor de servicios:

-   Usar las [**funciones WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) o [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) cuando se emplea la semántica de bloqueo.
-   Usar la [**función WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) cuando se emplean operaciones de no bloqueo y la aplicación ya usa un Windows de mensajes.

Cuando una aplicación necesita usar la semántica de bloqueo en un conjunto de sockets que abarca varios proveedores, se recomienda [**WSAWaitForMultipleEvents.**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) La aplicación también puede usar la función [**WSAEventSelect,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) que permite que los eventos de red XXX de FD \_ (vea [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect)) se asocie a un objeto de evento y se controle desde el paradigma del objeto de evento (descrito en Objetos de evento y [E/S superpuestas).](overlapped-i-o-and-event-objects-2.md)

La [**función WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) no está restringida a un único proveedor porque toma un descriptor de socket único como parámetro de entrada. Sin embargo, tenga en cuenta que la función [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) ofrece un mejor rendimiento y escalabilidad sobre **WSAAsyncSelect** a medida que aumenta la sobrecarga de mantenimiento del bombeo de mensajes con mensajes de evento Winsock a medida que aumenta el número total de sockets que se usan.

 

 



