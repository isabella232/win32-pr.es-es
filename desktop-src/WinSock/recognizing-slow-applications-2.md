---
description: En esta guía se identifica una aplicación lenta como aplicación de Microsoft Windows con un rendimiento desemparejado.
ms.assetid: cacf55d8-ab64-47a4-a55b-59a3c4e3877b
title: Reconocer aplicaciones lentas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07be9484a3b08951b8b64989757459531ff72906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706981"
---
# <a name="recognizing-slow-applications"></a>Reconocer aplicaciones lentas

En esta guía se identifica una aplicación *lenta* como aplicación de Microsoft Windows con un rendimiento desemparejado. Una aplicación lenta exhibe uno o varios de los síntomas siguientes:

-   La utilización de la CPU y la red son bajas.

    Parece que el equipo está esperando. A menudo, la aplicación espera en la red.

-   La desactivación del algoritmo de Nagle mediante la opción de socket de TCP \_ Nodelay aumenta el rendimiento.

    Esto indica otros problemas y no debe considerarse una solución. La desactivación del algoritmo de Nagle aumenta la sobrecarga del protocolo. No utilice este método como una corrección para las aplicaciones interrumpidas, solo como una indicación de que la aplicación necesita otro trabajo para solucionar problemas de rendimiento.

-   La aplicación exhibe una sobrecarga elevada.

    Para calcular la sobrecarga de las aplicaciones, determine la cantidad de datos que desea transferir en cada dirección. A continuación, use netstat y agregue (para Ethernet) 60 bytes para cada paquete y 500 bytes para cada conexión. La mejor sobrecarga que se puede esperar para la transmisión por secuencias sobre Ethernet es aproximadamente del 6%. En el caso de una conexión de módem, la mejor sobrecarga es aproximadamente del 2%, debido al hecho de que un vínculo PPP usa la compresión de encabezado. Consulte [calcular la sobrecarga con netstat](calculating-overhead-with-netstat-2.md) para obtener más información.

-   La respuesta de la aplicación se ralentiza cuando la conexión tiene un RTT grande.

    Suponiendo que la aplicación no se aproxima al ancho de banda del vínculo, un RTT grande debería tener poco o ningún efecto. Una ralentización dramática con un RTT grande es un claro signo de procesamiento serializado y muchas transacciones pequeñas.

Todas las aplicaciones deben probarse en un entorno con un RTT grande. Al hacerlo, se revela la mayoría de las aplicaciones que sufren opciones de desarrollo deficientes. Esta prueba puede realizarse en varios entornos, como una red LAN inalámbrica, un simulador de retraso de vínculos o una red satélite.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Comportamiento de la aplicación](application-behavior-2.md)
</dt> <dt>

[Aplicaciones de Windows Sockets de alto rendimiento](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Algoritmo de Nagle](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



