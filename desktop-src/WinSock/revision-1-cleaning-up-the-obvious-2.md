---
description: En esta versión del programa de ejemplo, se han realizado algunos cambios obvios que tomarán los progresos iniciales al mejorar el rendimiento.
ms.assetid: ef9d594c-31fe-44c0-b707-47c01e2c5bf0
title: 'Revisión 1: limpieza del'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 631bea7395000531cce542b41ace3b3aab9afff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715867"
---
# <a name="revision-one-cleaning-up-the-obvious"></a>Revisión 1: limpieza del

En esta versión del programa de ejemplo, se han realizado algunos cambios obvios que tomarán los progresos iniciales al mejorar el rendimiento. Esta versión del código está lejos del rendimiento, pero es un buen paso incremental que permite examinar los efectos de métodos más incrementales.

> [!WARNING]
> Este ejemplo de la aplicación proporciona un rendimiento insuficiente intencionadamente, con el fin de mostrar las mejoras de rendimiento posibles con los cambios en el código. No use este ejemplo de código en la aplicación; solo es para fines ilustrativos.

 


```C++
#include <windows.h>

BYTE Set(row, col, bAlive)
{
    SOCKET s = socket(...);
    BYTE byRet = 0;
    BYTE tmp[3];
    tmp[0] = (BYTE)row;
    tmp[1] = (BYTE)col;
    tmp[2] = (BYTE)bAlive;
    bind( s, ... );
    connect( s, ... );
    send( s, &tmp, 3 );
    recv( s, &byRet, 1 );
    closesocket( s );
    return byRet;
}
```



## <a name="changes-in-this-version"></a>Cambios en esta versión

Esta versión refleja los cambios siguientes:

-   Se quitó SNDBUF = 0. Se quitan los retrasos de 200 milisegundos debido a los envíos no almacenados en búfer y a las confirmaciones diferidas.
-   Se ha quitado el comportamiento de envío y envío-recepción. Este cambio elimina los retrasos de 200 milisegundos debido a las interacciones de Nagle y de la confirmación diferida.
-   Se quitó la hipótesis Little-Endian. Los bytes están ahora en orden.

## <a name="remaining-problems"></a>Problemas restantes

En esta versión, quedan los siguientes problemas:

-   La aplicación sigue conectándose. Dado que se quitan los retrasos de 600 + milisegundos, la aplicación ahora alcanza la tasa sostenida de 12 conexiones por segundo. Ahora muchas conexiones simultáneas se convierten en un problema.
-   La aplicación sigue siendo FAT; las celdas sin cambios se siguen propagando al servidor.
-   La aplicación todavía exhibe un flujo deficiente; los envíos de 3 bytes siguen siendo pequeños envíos.
-   La aplicación ahora envía 2 bytes/RTT, que es igual a 4 KB/s en la Ethernet conectada directamente. Esto no es demasiado rápido, pero es probable que la espera de tiempo provoque problemas en primer lugar.
-   La sobrecarga está fuera del 99,3%, que sigue sin ser un buen porcentaje de sobrecarga.

## <a name="key-performance-metrics"></a>Métricas de rendimiento clave

Las siguientes métricas clave de rendimiento se expresan en tiempo de ida y vuelta (RTT), Goodput y sobrecarga del protocolo. Consulte el tema [terminología de red](network-terminology-2.md) para obtener una explicación de estos términos.

Esta versión refleja las siguientes métricas de rendimiento:

-   Tiempo de celda: 2 × RTT
-   Goodput: 2 bytes/RTT
-   Sobrecarga de protocolos: 99.3 Percent

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mejora de una aplicación lenta](improving-a-slow-application-2.md)
</dt> <dt>

[Terminología de red](network-terminology-2.md)
</dt> <dt>

[La versión de línea base: una aplicación con un rendimiento muy deficiente](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[Revisión 2: rediseño para menos conexiones](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[Revisión 3: envío de bloque comprimido](revision-3-compressed-block-send-2.md)
</dt> <dt>

[Mejoras futuras](future-improvements-2.md)
</dt> </dl>

 

 



