---
description: Otro aspecto del desarrollo de aplicaciones que se debe tener en cuenta es la diferencia de comportamiento entre las operaciones locales o dentro del equipo, y el comportamiento cuando se llevan a cabo operaciones entre dos equipos en red.
ms.assetid: e6f48446-948c-458c-8ecf-04ffb249c8a4
title: Comportamiento de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abb09441eda4f0d909652ac38a9ca0596a1b4bce456f58c0e1eae1a7af7dc53b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121465"
---
# <a name="application-behavior"></a>Comportamiento de la aplicación

Otro aspecto del desarrollo de aplicaciones que se debe tener en cuenta es la diferencia de comportamiento entre las operaciones locales o dentro del equipo, y el comportamiento cuando se llevan a cabo operaciones entre dos equipos en red. Hay comportamientos de aplicación que pueden funcionar correctamente en un equipo local, pero cuando se ejecutan a través de una red, provocan una degradación significativa del rendimiento y el consumo de recursos. Se deben evitar los siguientes comportamientos de aplicación al desarrollar Windows sockets.

## <a name="behaviors-to-avoid"></a>Comportamientos que se deben evitar

-   Aplicaciones chatty.

    Algunas aplicaciones realizan muchas transacciones pequeñas. Cuando se combina con la sobrecarga de red asociada a cada transacción de este tipo, el efecto se multiplica. En redes, las transacciones pequeñas pueden consumir tantos recursos como transacciones de gran tamaño. Un enfoque mejor es combinar muchas transacciones pequeñas en una única transacción grande.

-   Transacciones serializadas.

    La serialización innecesaria de transacciones puede dar lugar a un rendimiento deficiente y afectar a la escalabilidad. Por ejemplo, 1000 transacciones serializadas toman al menos 1000 \* RTT para completarse. Un enfoque mejor es ejecutar transacciones no relacionadas en paralelo. Cuando las aplicaciones serializadas se combinan con aplicaciones con chat, la capacidad de respuesta se puede ver gravemente dificultada.

    > [!Note]  
    > Deserializar correctamente una aplicación puede ser difícil. Si el cambio de serializado a paralelo resulta demasiado difícil, considere la posibilidad de combinar varias transacciones en menos transacciones de gran tamaño.

     

-   Transacciones fat.

    Las aplicaciones que envían bytes innecesarios en la red se consideran aplicaciones fat. Las aplicaciones que envían bytes innecesarios en la red aumentan la sobrecarga de red y el rendimiento se ve dificultado. Esta situación suele ser de estructuras de datos ineficaces o de un streaming de datos ineficaz. Para solucionar este problema, optimice las estructuras de datos o considere la posibilidad de usar la compresión.

En las secciones siguientes se abordan aspectos del desarrollo de aplicaciones que se deben tener en cuenta.

-   [Problemas específicos de TCP/IP](tcp-ip-specific-issues-2.md)
-   [Reconocimiento de aplicaciones lentas](recognizing-slow-applications-2.md)
-   [Cálculo de la sobrecarga con Netstat](calculating-overhead-with-netstat-2.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de sockets Windows alto rendimiento](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



