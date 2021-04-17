---
description: Versión de línea de base de una aplicación con un rendimiento muy deficiente en Windows Sockets (Winsock).
ms.assetid: 923884c4-f1bd-4f72-983e-6158f368e0dd
title: 'La versión de línea base: una aplicación con un rendimiento muy deficiente'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c094be5fd5cf6e3b9eaeb07c7ff38880e651dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706481"
---
# <a name="the-baseline-version-a-very-poor-performing-application"></a>La versión de línea base: una aplicación con un rendimiento muy deficiente

La siguiente muestra de código de bajo rendimiento que se usa para calcular las actualizaciones es como sigue:

> [!Note]  
> Para simplificar, no hay ningún control de errores en los ejemplos siguientes. Cualquier aplicación de producción siempre comprueba los valores devueltos.

 

> [!WARNING]
> Los primeros ejemplos de la aplicación proporcionan un rendimiento insuficiente intencionadamente, con el fin de mostrar las mejoras de rendimiento posibles con los cambios en el código. No use estos ejemplos de código en la aplicación; solo tienen fines ilustrativos.

 


```C++
#include <windows.h>

BOOL Map[ROWS][COLS];

void LifeUpdate()
{
    ComputeNext( Map );
    for( int i = 0 ; i < ROWS ; ++i )     //serialized
        for( int j = 0 ; j < COLS ; ++j )
            Set( i, j, Map[i][j] );    //chatty
}

BYTE Set(row, col, bAlive)
{
    SOCKET s = socket(...);
    BYTE byRet = 0;
    setsockopt( s, SO_SNDBUF, &Zero, sizeof(int) );
    bind( s, ... );
    connect( s, ... );
    send( s, &row, 1 );
    send( s, &col, 1 );
    send( s, &bAlive, 1 );
    recv( s, &byRet, 1 );
    closesocket( s );
    return byRet;
}
```



En este estado, la aplicación tiene el peor rendimiento posible de la red. Los problemas con esta versión de la aplicación de ejemplo incluyen:

-   La aplicación está conversando. Cada transacción es demasiado pequeña: no es necesario actualizar las celdas una por una.
-   Las transacciones se serializan estrictamente, aunque las celdas se puedan actualizar simultáneamente.
-   El búfer de envío se establece en cero y la aplicación produce un retraso de 200 milisegundos para cada envío (tres veces por celda).
-   La aplicación tiene mucha conexión y se conecta una vez para cada celda. Las aplicaciones están limitadas por el número de conexiones por segundo para un destino determinado debido a un estado de tiempo de espera, pero esto no supone un problema aquí, ya que cada transacción tarda más de 600 milisegundos.
-   La aplicación es FAT; muchas transacciones no tienen ningún efecto en el estado del servidor, ya que muchas celdas no cambian de la actualización a la actualización.
-   La aplicación exhibe un flujo deficiente; los envíos pequeños consumen mucha CPU y RAM.
-   La aplicación asume una representación de Little-Endian para sus envíos. Se trata de una suposición natural para la plataforma actual de Windows, pero puede ser peligrosa para el código de larga duración.

## <a name="key-performance-metrics"></a>Métricas de rendimiento clave

Las siguientes métricas de rendimiento se expresan en tiempo de ida y vuelta (RTT), Goodput y sobrecarga del protocolo. Consulte el tema [terminología de red](network-terminology-2.md) para obtener una explicación de estos términos.

-   Hora de la red, hora de la red para una actualización de una sola celda, requiere 4 \* RTT + 600 milisegundos para las interacciones de Nagle y ACK retrasada.
-   Goodput tiene menos de 6 bytes.
-   La sobrecarga del protocolo es del 99,6%.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mejora de una aplicación lenta](improving-a-slow-application-2.md)
</dt> <dt>

[Terminología de red](network-terminology-2.md)
</dt> <dt>

[Revisión 1: limpieza del manifiesto](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[Revisión 2: rediseño para menos conexiones](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[Revisión 3: envío de bloque comprimido](revision-3-compressed-block-send-2.md)
</dt> <dt>

[Mejoras futuras](future-improvements-2.md)
</dt> </dl>

 

 



