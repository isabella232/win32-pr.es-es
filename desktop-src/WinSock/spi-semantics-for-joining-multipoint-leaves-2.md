---
description: A continuación, un socket multipunto se caracteriza con frecuencia por describir su rol en uno de los dos planos (control o datos).
ms.assetid: 35e4a8c9-d943-44b8-be61-605b60a6cf5d
title: Semántica de SPI para unir hojas de varios puntos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 693333f4ddbf53410992589349dd246485b32d24770101a5bf1cbd32dd03c1c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993335"
---
# <a name="spi-semantics-for-joining-multipoint-leaves"></a>Semántica de SPI para unir hojas de varios puntos

A continuación, un socket multipunto se caracteriza con frecuencia por describir su rol en uno de los dos planos (control o datos). Debe entenderse que este mismo socket tiene un rol en el otro plano, pero esto no se menciona para mantener las referencias cortas. Por ejemplo, una referencia a un socket raíz de c podría hacer referencia a una raíz \_ c \_ root/d \_ o a un socket \_ raíz/d \_ de c.

En los esquemas de plano de control raíz, los nuevos nodos hoja se agregan a una sesión de varios puntos de una o ambas maneras diferentes. En el primer método, la raíz usa [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) para iniciar una conexión con un nodo hoja e invitarla a convertirse en participante. En el nodo hoja, la aplicación del mismo nivel debe haber creado un socket hoja c y usado \_ [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) para establecerlo en modo de escucha. El nodo hoja recibirá una indicación FD ACCEPT cuando se le invite a unirse a la sesión y señala su disposición a unirse mediante una llamada \_ a [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept). La aplicación raíz recibirá una indicación de FD CONNECT cuando se haya completado \_ la operación de combinación.

En el segundo método, los roles se invierten básicamente. El cliente raíz crea un socket raíz de c \_ y lo establece en modo de escucha. Un nodo hoja que desea unirse a la sesión crea un socket hoja c y usa \_ [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) para iniciar la conexión y solicitar la admisión. El cliente raíz recibe FD ACCEPT cuando llega una solicitud de admisión entrante y admite el nodo hoja mediante una \_ llamada a [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept). El nodo hoja recibe FD \_ CONNECT cuando se ha admitido.

En un plano de control no raíz, donde todos los nodos son hojas C, la función \_ [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) se usa para iniciar la inclusión de un nodo en una sesión multipunto existente. Se proporciona una indicación de FD CONNECT cuando se ha completado la combinación y el descriptor de socket devuelto \_ se puede utiliza en la sesión multipunto. En el caso de la multidifusión IP, esto correspondería a la opción \_ de socket ADD MEMBERSHIP de \_ IP.

Por lo tanto, hay tres instancias en las que un cliente usaría [**WSPJoinLeaf:**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)

-   Actuar como raíz multipunto e invitar a una hoja nueva para unirse a la sesión.
-   Actuar como hoja realizando una solicitud de admisión a una sesión multipunto raíz.
-   Actuar como una hoja que busca la admisión a una sesión multipunto no raíz (por ejemplo, multidifusión IP).

 

 
