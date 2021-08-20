---
description: En esta guía se identifica una aplicación lenta como una aplicación de Microsoft Windows con un rendimiento deficiente.
ms.assetid: cacf55d8-ab64-47a4-a55b-59a3c4e3877b
title: Reconocimiento de aplicaciones lentas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 775239b76cfd287a446596f9a4a0eda6298caab35c31f70fade378ec0d44d586
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118111819"
---
# <a name="recognizing-slow-applications"></a>Reconocimiento de aplicaciones lentas

En esta guía se identifica una *aplicación* lenta como una aplicación de Microsoft Windows con un rendimiento deficiente. Una aplicación lenta presenta uno o varios de los síntomas siguientes:

-   El uso de CPU y red es bajo.

    Parece que el equipo está esperando algo. A menudo, la aplicación está esperando en la red.

-   La desactivación del algoritmo de Nagle mediante la opción de socket NODELAY de TCP \_ aumenta el rendimiento.

    Esto indica otros problemas y no debe considerarse una solución. Al desactivar el algoritmo de Nagle, aumenta la sobrecarga del protocolo. No use este método como corrección para las aplicaciones rotas, solo como indicación de que la aplicación necesita otro trabajo para solucionar problemas de rendimiento.

-   La aplicación presenta una sobrecarga alta.

    Para calcular la sobrecarga de las aplicaciones, determine la cantidad de datos que se pretende transferir en cada dirección. A continuación, use Netstat y agregue (para Ethernet) 60 bytes para cada paquete y 500 bytes para cada conexión. La mejor sobrecarga que se puede esperar para el streaming a través de Ethernet es aproximadamente del 6 %. Para una conexión de módem, la mejor sobrecarga es aproximadamente del 2 %, debido al hecho de que un vínculo PPP usa la compresión de encabezado. Consulte [Calcular la sobrecarga con Netstat](calculating-overhead-with-netstat-2.md) para obtener más información.

-   La respuesta de la aplicación se ralentiza cuando la conexión tiene un RTT grande.

    Suponiendo que la aplicación no se aproxima al ancho de banda del vínculo, un RTT grande debería tener poco o ningún efecto. Una ralentización drástica con un RTT grande es un claro signo de procesamiento serializado y muchas transacciones pequeñas.

Todas las aplicaciones deben probarse en un entorno con un RTT grande. Esto revela la mayoría de las aplicaciones que sufren de opciones de desarrollo deficientes. Estas pruebas se pueden realizar en varios entornos, como una red LAN inalámbrica, un simulador de retraso de vínculo o una red satélite.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Comportamiento de la aplicación](application-behavior-2.md)
</dt> <dt>

[Aplicaciones de sockets Windows alto rendimiento](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Algoritmo de Nagle](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



