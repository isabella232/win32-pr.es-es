---
title: Modelo para sistemas distribuidos
description: Tradicionalmente, tener un sistema monolítico ejecutado en varios equipos significaba dividir el sistema en componentes de cliente y servidor independientes.
ms.assetid: 6055bcef-e34c-4f2d-92b9-9aec75cf3cec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 859b2a0a83e7f12bd7caf372e60acf2736a114a0cdf46893830032a47a548019
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924182"
---
# <a name="the-model-for-distributed-systems"></a>Modelo para sistemas distribuidos

Tradicionalmente, tener un sistema monolítico ejecutado en varios equipos significaba dividir el sistema en componentes de cliente y servidor independientes. En estos sistemas, el componente cliente controló la interfaz de usuario y el servidor proporcionó procesamiento de back-end, como el acceso a la base de datos, la impresión, y así sucesivamente. A medida que los equipos proliferaban, reducban el costo y se conectaban mediante redes de ancho de banda cada vez mayores, la división de sistemas de software en varios componentes se hacía más cómoda, con cada componente ejecutándose en un equipo diferente y realizando una función especializada. Este enfoque simplifica el desarrollo, la administración, la administración y, a menudo, mejora el rendimiento y la solidez, ya que el error en un equipo no deshabilite necesariamente todo el sistema.

En muchos casos, el sistema aparece al cliente como una nube opaca que realiza las operaciones necesarias, aunque el sistema distribuido se compone de nodos individuales, como se muestra en la ilustración siguiente.

![los clientes acceden a servicios en un sistema de servidores rpc que aparece como una nube opaca para clientes externos](images/indy-nodes.png)

La opacidad de la nube se mantiene porque las operaciones informáticas se invocan en nombre del cliente. Por lo tanto, los clientes pueden localizar un equipo (un *nodo*) dentro de la nube y solicitar una operación determinada; al realizar la operación, ese equipo puede invocar la funcionalidad en otros equipos dentro de la nube sin exponer los pasos adicionales, o el equipo en el que se realizaron, al cliente.

Con este paradigma, la mecánica de un sistema distribuido, parecido a la nube, se puede dividir en muchos intercambios de paquetes individuales o conversaciones entre nodos individuales.

Los sistemas cliente-servidor tradicionales tienen dos nodos con roles fijos y responsabilidades. Los sistemas distribuidos modernamente pueden tener más de dos nodos y sus roles suelen ser dinámicos. En una conversación, un nodo puede ser un cliente, mientras que en otra conversación el nodo puede ser el servidor. En muchos casos, el consumidor final de la funcionalidad expuesta es un cliente con un usuario sentado en un teclado que observa la salida. En otros casos, las funciones del sistema distribuido desatendidas, realizando operaciones en segundo plano.

Es posible que el sistema distribuido no tenga clientes y servidores dedicados para cada intercambio de paquetes determinado, pero es importante recordar que hay un autor de llamada (o iniciador, cualquiera de los cuales a menudo se conoce como cliente). También está el destinatario de la llamada (a menudo denominado servidor). No es necesario tener intercambios de paquetes de dos maneras en el formato de solicitud-respuesta de un sistema distribuido; a menudo, los mensajes se envían solo de una manera.

 

 




