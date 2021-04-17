---
description: Otro aspecto del desarrollo de aplicaciones que se debe tener en cuenta es la diferencia entre el comportamiento entre las operaciones locales o dentro de un equipo, y el comportamiento cuando las operaciones tienen lugar entre dos equipos conectados en red.
ms.assetid: e6f48446-948c-458c-8ecf-04ffb249c8a4
title: Comportamiento de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a9b871a2c0535d9ef4220824651657332a224a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541643"
---
# <a name="application-behavior"></a>Comportamiento de la aplicación

Otro aspecto del desarrollo de aplicaciones que se debe tener en cuenta es la diferencia entre el comportamiento entre las operaciones locales o dentro de un equipo, y el comportamiento cuando las operaciones tienen lugar entre dos equipos conectados en red. Hay comportamientos de aplicación que pueden funcionar bastante bien en un equipo local, pero cuando se ejecutan a través de una red, causan una degradación significativa del rendimiento y el consumo de recursos. Los siguientes comportamientos de la aplicación deben evitarse al desarrollar aplicaciones de Windows Sockets.

## <a name="behaviors-to-avoid"></a>Comportamientos que se deben evitar

-   Aplicaciones de chat.

    Algunas aplicaciones realizan muchas transacciones pequeñas. Cuando se combina con la sobrecarga de red asociada a cada una de estas transacciones, se multiplica el efecto. En las redes, las transacciones pequeñas pueden consumir tantos recursos como mucho tiempo como transacciones grandes. Un mejor enfoque consiste en combinar muchas transacciones pequeñas en una única transacción grande.

-   Transacciones serializadas.

    Una serialización innecesaria de transacciones puede dar lugar a un rendimiento deficiente y afectar a la escalabilidad. Por ejemplo, 1000 las transacciones serializadas tardan al menos 1000 \* RTT en completarse. Un mejor enfoque consiste en ejecutar transacciones no relacionadas en paralelo. Cuando las aplicaciones serializadas se combinan con aplicaciones de chat, la capacidad de respuesta puede verse seriamente obstaculizada.

    > [!Note]  
    > La deserialización correcta de una aplicación puede ser difícil. Si el cambio de serializado a paralelo resulta demasiado difícil, considere la posibilidad de combinar varias transacciones en menos transacciones de gran tamaño.

     

-   Transacciones FAT.

    Las aplicaciones que envían bytes innecesarios en la red se consideran aplicaciones FAT. Las aplicaciones que envían bytes innecesarios en la red aumentan la sobrecarga de la red y se obstaculiza el rendimiento. Esta situación suele proceder de estructuras de datos ineficaces o de un flujo de datos ineficaz. Para solucionarlo, optimice las estructuras de datos o considere la posibilidad de usar la compresión.

En las secciones siguientes se tratan aspectos del desarrollo de aplicaciones que se deben tener en cuenta.

-   [Problemas específicos de TCP/IP](tcp-ip-specific-issues-2.md)
-   [Reconocer aplicaciones lentas](recognizing-slow-applications-2.md)
-   [Calcular la sobrecarga con netstat](calculating-overhead-with-netstat-2.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de Windows Sockets de alto rendimiento](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



