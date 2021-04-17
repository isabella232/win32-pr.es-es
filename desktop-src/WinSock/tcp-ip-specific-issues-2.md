---
description: Algunas técnicas de programación experimentan problemas de rendimiento que están vinculados a la implementación de TCP/IP.
ms.assetid: 2a63e85e-06fd-4b6f-8351-9866099b9d54
title: Problemas específicos de TCP/IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9a7334471d3e419830eb054399ff1dcb721cd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716219"
---
# <a name="tcpip-specific-issues"></a>Problemas específicos de TCP/IP

Algunas técnicas de programación experimentan problemas de rendimiento que están vinculados a la implementación de TCP/IP. Estos problemas de rendimiento no sugieren que TCP/IP sea ineficaz o un cuello de botella de rendimiento. en su lugar, estos problemas se ven cuando no se comprenden las operaciones de TCP/IP.

Los siguientes problemas identifican escenarios comunes en los que la combinación de las opciones de desarrollo de aplicaciones de red y operaciones de TCP/IP da lugar a un rendimiento deficiente.

-   Aplicaciones de conexión intensivas.

    Algunas aplicaciones crean una nueva conexión TCP para cada transacción. El establecimiento de la conexión TCP lleva tiempo, aporta RTTs adicionales y está sujeto a un inicio lento. Además, las conexiones cerradas están sujetas a TIME-WAIT, que consume recursos del sistema.

    Las aplicaciones con una gran cantidad de conexiones son muy comunes, ya que son fáciles de crear; las pruebas y el control de errores son muy sencillos. La detección de errores en una conexión persistente puede llevar a cabo un código y un esfuerzo considerables, por lo que a veces no se completa.

    Remedy esta situación reutilizando la conexión TCP. Esto puede provocar la serialización a través de la conexión TCP a menos que las transacciones se multiplexan en varias conexiones. Si se toma este enfoque, el número de conexiones se debe limitar a dos, y las tramas de capa de aplicación y el control de errores avanzado son obligatorios.

-   Búferes de envío de longitud cero y envíos de bloqueo.

    La desactivación del almacenamiento en búfer mediante [**la función de**](/windows/desktop/api/winsock/nf-winsock-setsockopt) SNDBUF para establecer el búfer de envío (de modo que \_ ) en cero es similar a desactivar el almacenamiento en caché de disco. Al establecer el búfer de envío en cero y emitir envíos de bloqueo, una aplicación tiene un 50 por ciento de probabilidad de que se produzca una confirmación retrasada de 200 segundos.

    No desactive el almacenamiento en búfer de envío a menos que tenga en cuenta el impacto en todos los entornos de red. Una excepción: la transmisión de datos mediante e/s superpuestas debe establecer el búfer de envío en cero.

-   Modelo de programación de envío-envío-recepción.

    La estructuración de una aplicación para realizar Send-SEND-RECEIVE aumenta las posibilidades de encontrar el algoritmo de Nagle, lo que produce un retraso de RTT + 200 ms. Es posible que se encuentre el algoritmo de Nagle si el último envío es menor que el tamaño de segmento máximo de TCP (MSS, el número máximo de datos en un solo datagrama). MSS puede ser un valor muy grande (64 KB en IPv4 e incluso mayor en IPv6), por lo que no se debe contar con un MSS pequeño. Una opción mejor es combinar los dos envíos en un solo envío mediante la función [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) o **memcpy** .

-   Gran número de conexiones simultáneas.

    Las conexiones simultáneas no deben superar dos, excepto en las aplicaciones de uso especial. Si se superan dos conexiones simultáneas, se producen recursos desperdiciados. Una buena regla es tener hasta cuatro conexiones de corta duración, o dos conexiones persistentes por destino.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Comportamiento de la aplicación](application-behavior-2.md)
</dt> <dt>

[Aplicaciones de Windows Sockets de alto rendimiento](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Algoritmo de Nagle](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



