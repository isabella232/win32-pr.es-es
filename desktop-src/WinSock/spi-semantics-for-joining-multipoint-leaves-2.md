---
description: En los siguientes casos, un socket Multipoint se caracteriza a menudo por describir su rol en uno de los dos planos (control o datos).
ms.assetid: 35e4a8c9-d943-44b8-be61-605b60a6cf5d
title: Semántica de SPI para combinar hojas de Multipoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa0e77203e5405f6cb820baba5d545de03e3a8ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716291"
---
# <a name="spi-semantics-for-joining-multipoint-leaves"></a>Semántica de SPI para combinar hojas de Multipoint

En los siguientes casos, un socket Multipoint se caracteriza a menudo por describir su rol en uno de los dos planos (control o datos). Debe entenderse que el mismo socket tiene un rol en el otro plano, pero esto no se menciona a fin de mantener las referencias cortas. Por ejemplo, una referencia a un \_ socket raíz de c podría hacer referencia a una \_ raíz raíz/d de c \_ o a un socket de \_ hoja raíz/d \_ de c.

En los esquemas de plano de control con raíz, los nuevos nodos hoja se agregan a una sesión de Multipoint en uno o ambos dos modos diferentes. En el primer método, la raíz usa [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) para iniciar una conexión con un nodo hoja e invitarlo a ser participante. En el nodo hoja, la aplicación del mismo nivel debe haber creado un \_ socket hoja de c y ha usado [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) para establecerlo en el modo de escucha. El nodo hoja recibirá una indicación de aceptación FD cuando se le \_ invite a unirse a la sesión y señalará su voluntad de unirse llamando a [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept). La aplicación raíz recibirá una \_ indicación FD Connect cuando se haya completado la operación de Unión.

En el segundo método, los roles se invierten esencialmente. El cliente raíz crea un \_ socket raíz de c y lo establece en modo de escucha. Un nodo hoja que quiere unirse a la sesión crea un \_ socket hoja de c y usa [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) para iniciar la conexión y solicitar admisión. El cliente raíz recibe el \_ método FD Accept cuando llega una solicitud admisión entrante y admite el nodo hoja llamando a [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept). El nodo hoja recibe FD \_ Connect cuando se ha admitido.

En un plano de control no raíz, donde todos los nodos son \_ hojas de c, la función [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) se usa para iniciar la inclusión de un nodo en una sesión de Multipoint existente. \_Se proporciona una indicación FD Connect cuando se ha completado la combinación y se puede usar el descriptor de socket devuelto en la sesión multipoint. En el caso de la multidifusión IP, esto correspondería a la opción de IP \_ agregar \_ socket de pertenencia.

Por lo tanto, hay tres instancias en las que un cliente usaría [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf):

-   Actuar como una raíz multipunto e invitar a una nueva hoja para unirse a la sesión.
-   Actuar como una hoja que realiza una solicitud admisión a una sesión de multipoint con raíz.
-   Actuar como una hoja que busca admisión en una sesión de Multipoint no raíz (por ejemplo, multidifusión IP).

 

 
