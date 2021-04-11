---
description: La familia de direcciones IPX define la estructura de direccionamiento de los protocolos que usan el direccionamiento estándar de sockets IPX. Para estos transportes, una dirección de punto de conexión consta de un número de red, una dirección de nodo y un número de socket.
ms.assetid: cf749ae7-ab17-4c60-b00c-b34e092c6431
title: Familia de direcciones de AF_IPX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21508b23541b489c11fbdc38a2ff8dcf4ad53e48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154301"
---
# <a name="af_ipx-address-family"></a>\_Familia de direcciones IPX de AF

La familia de direcciones IPX define la estructura de direccionamiento de los protocolos que usan el direccionamiento estándar de sockets IPX. Para estos transportes, una dirección de punto de conexión consta de un número de red, una dirección de nodo y un número de socket.

El número de red es un dominio administrativo y normalmente nombra un único segmento Ethernet o anillo de token. El número de nodo es la dirección física de la estación. La combinación de red y de forma de nodo es una dirección de estación única que se supone que es única en el mundo. Los números de red y de nodo se representan en texto ASCII en la notación de bloques o de guiones como: ' 0101a040, 00001b498765 ' o ' 01-01-a0-40, 00-00-1B-49-87-65 '. No es necesario que haya ceros a la izquierda.

El número de sockets IPX es un número de servicio de red/transporte muy parecido a un número de puerto TCP y no debe confundirse con el descriptor de socket Winsock. Los números de socket IPX son globales para la estación final y no se pueden enlazar a direcciones de red o nodo específicas. Por ejemplo, si la estación final tiene dos tarjetas de interfaz de red, un socket enlazado puede enviar y recibir en ambas tarjetas. En concreto, los sockets de datagramas recibirían datagramas de difusión en ambas tarjetas.

> [!Caution]  
> SOCKADDR \_ IPX tiene 14 bytes de longitud y es menor que la estructura de referencia [**SOCKADDR**](sockaddr-2.md) de 16 bytes. Las implementaciones de IPX/SPX pueden aceptar la longitud de 16 bytes, así como la longitud real. Si usa SOCKADDR \_ IPX y una longitud codificada de 16 bytes, la implementación puede suponer que tiene acceso a los 2 bytes que siguen a la estructura.

 



| Campo           | Value                                    |
|-----------------|------------------------------------------|
| **\_familia SA**  | Familia de direcciones \_ de AF IPX en el orden del host.    |
| **SA \_ netnum**  | Identificador de red IPX en el orden de la red. |
| **SA \_ nodenum** | Dirección del nodo de la estación, vacía derecha.     |
| **\_Socket SA**  | Número de socket IPX en el orden de la red.      |



 

 

 



