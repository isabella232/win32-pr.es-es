---
title: El modelo para sistemas distribuidos
description: Tradicionalmente, tener un sistema monolítico en varios equipos significaba dividir el sistema en componentes independientes de cliente y servidor.
ms.assetid: 6055bcef-e34c-4f2d-92b9-9aec75cf3cec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82cd1ea3301d68e77562a63c542bc075692e5192
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994056"
---
# <a name="the-model-for-distributed-systems"></a>El modelo para sistemas distribuidos

Tradicionalmente, tener un sistema monolítico en varios equipos significaba dividir el sistema en componentes independientes de cliente y servidor. En estos sistemas, el componente de cliente administraba la interfaz de usuario y el servidor proporcionaba el procesamiento de back-end, como el acceso a la base de datos, la impresión, etc. A medida que los equipos proliferan, descartaban el costo y se conectaban a través de redes de ancho de banda cada vez mayores, la división de los sistemas de software en varios componentes resultaba más cómoda, con cada componente que se ejecutaba en un equipo diferente y realizaba una función especializada. Este enfoque simplifica el desarrollo, la administración, la administración y, a menudo, el rendimiento y la solidez mejorados, ya que los errores en un equipo no deshabilitaron necesariamente todo el sistema.

En muchos casos, el sistema aparece en el cliente como una nube opaca que realiza las operaciones necesarias, aunque el sistema distribuido se compone de nodos individuales, tal y como se muestra en la ilustración siguiente.

![los clientes obtienen acceso a los servicios de un sistema de servidores RPC que aparece como una nube opaca para clientes externos](images/indy-nodes.png)

La opacidad de la nube se mantiene porque las operaciones de cálculo se invocan en nombre del cliente. Como tal, los clientes pueden localizar un equipo (un *nodo*) dentro de la nube y solicitar una operación determinada; al realizar la operación, ese equipo puede invocar la funcionalidad en otros equipos dentro de la nube sin exponer los pasos adicionales, o el equipo en el que se realizaron, al cliente.

Con este paradigma, la mecánica de un sistema distribuido, similar a la nube, se puede dividir en muchos intercambios de paquetes individuales o en conversaciones entre nodos individuales.

Los sistemas cliente-servidor tradicionales tienen dos nodos con roles y responsabilidades fijos. Los sistemas distribuidos modernos pueden tener más de dos nodos y sus roles suelen ser dinámicos. En una conversación, un nodo puede ser un cliente, mientras que en otra conversación el nodo puede ser el servidor. En muchos casos, el consumidor más avanzado de la funcionalidad expuesta es un cliente con un usuario que se encuentra en un teclado y ve la salida. En otros casos, las funciones del sistema distribuido están desatendidas y realizan operaciones en segundo plano.

Es posible que el sistema distribuido no tenga clientes y servidores dedicados para cada intercambio de paquetes determinado, pero es importante recordar que hay un llamador (o iniciador, cualquiera de los cuales a menudo se conoce como cliente). También hay el destinatario de la llamada (a menudo denominado servidor). No es necesario tener intercambios de paquetes bidireccionales en el formato de solicitud-respuesta de un sistema distribuido; a menudo, los mensajes solo se envían de una manera.

 

 




