---
description: La familia de direcciones IPX define la estructura de direccionamiento para los protocolos que usan el direccionamiento de socket IPX estándar. Para estos transportes, una dirección de punto de conexión consta de un número de red, una dirección de nodo y un número de socket.
ms.assetid: cf749ae7-ab17-4c60-b00c-b34e092c6431
title: AF_IPX familia de direcciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3915eefab8e6fc6c18cf4e2b81835b8c6821d0cdd65f5683f509504d4d2c24bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112808"
---
# <a name="af_ipx-address-family"></a>Familia \_ de direcciones IPX de AF

La familia de direcciones IPX define la estructura de direccionamiento para los protocolos que usan el direccionamiento de socket IPX estándar. Para estos transportes, una dirección de punto de conexión consta de un número de red, una dirección de nodo y un número de socket.

El número de red es un dominio administrativo y normalmente denomina un único segmento Ethernet o anillo de token. El número de nodo es la dirección física de una estación. La combinación de red y nodo forma una dirección de estación única que se supone que es única en el mundo. Los números de nodo y de red se representan en texto ASCII en la notación discontinua o en bloque como: "0101a040,00001b498765" o "01-01-a0-40,00-00-1b-49-87-65". Los ceros iniciales no deben estar presentes.

El número de socket IPX es un número de servicio de red o transporte muy parecido a un número de puerto TCP y no debe confundirse con el descriptor de socket winsock. Los números de socket IPX son globales a la estación final y no se pueden enlazar a direcciones net/node específicas. Por ejemplo, si la estación final tiene dos tarjetas de interfaz de red, un socket enlazado puede enviar y recibir en ambas tarjetas. En concreto, los sockets de datagramas recibirían datagramas de difusión en ambas tarjetas.

> [!Caution]  
> SOCKADDR IPX tiene 14 bytes de longitud y es más corto que la estructura de referencia \_ [**de sockaddr**](sockaddr-2.md) de 16 bytes. Las implementaciones de IPX/SPX pueden aceptar la longitud de 16 bytes, así como la longitud verdadera. Si usa SOCKADDR IPX y una longitud codificada de forma codificada de 16 bytes, la implementación puede suponer que tiene acceso a los 2 bytes que sigue a la \_ estructura.

 



| Campo           | Valor                                    |
|-----------------|------------------------------------------|
| **familia \_ sa**  | Dirección de la familia \_ AF IPX en orden de host.    |
| **Sa \_ netnum**  | Identificador de red IPX en orden de red. |
| **Sa \_ nodenum** | Dirección del nodo de estación, vacía a la derecha.     |
| **Socket \_ sa**  | Número de socket IPX en orden de red.      |



 

 

 



