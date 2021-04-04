---
description: TCP/IP tiene características que permiten que el protocolo funcione a medida que se establecen sus requisitos de implementación normalizados.
ms.assetid: 6e9b3878-85f0-4572-9c00-a2e7647286ff
title: Características de TCP/IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 561ab497d6f37c1c84b0203088b29e216ff0a69f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910578"
---
# <a name="tcpip-characteristics"></a>Características de TCP/IP

TCP/IP tiene características que permiten que el protocolo funcione a medida que se establecen sus requisitos de implementación normalizados. Estas características se pueden combinar con las opciones de desarrollo que dan lugar a un rendimiento deficiente. El impacto que tienen estas características de TCP/IP en una aplicación depende de si la aplicación es transaccional o de streaming.

Las aplicaciones transaccionales se ven afectadas por la sobrecarga necesaria para el establecimiento y la terminación de la conexión. Por ejemplo, cada vez que se establece una conexión en una red Ethernet, se deben enviar tres paquetes de aproximadamente 60 bytes cada uno y se requiere aproximadamente un RTT para el intercambio. Cuando se produce la finalización de una conexión, se intercambian cuatro paquetes. Esto es para cada conexión; a menudo, una aplicación que abre y cierra conexiones incurre en esta sobrecarga en cada repetición.

Otro aspecto de TCP/IP es *el inicio lento*, que tiene lugar cada vez que se establece una conexión. Slow-Start es un límite artificial del número de segmentos de datos que se pueden enviar antes de que se reciba la confirmación de esos segmentos. El inicio lento está diseñado para limitar la congestión de la red. Cuando se establece una conexión a través de Ethernet, independientemente del tamaño de la ventana del receptor, una transmisión de 4 KB puede tardar hasta 3-4 RTT debido a un inicio lento.

Una optimización de TCP/IP denominada el algoritmo de Nagle también puede limitar la velocidad de transferencia de datos en una conexión. El algoritmo de Nagle está diseñado para reducir la sobrecarga de protocolo para las aplicaciones que envían pequeñas cantidades de datos, como Telnet, que envía un solo carácter cada vez. En lugar de enviar inmediatamente un paquete con gran cantidad de datos de encabezado y poca información, la pila espera más datos de la aplicación o una confirmación antes de continuar.

Las confirmaciones diferidas, que normalmente se denominan *confirmación diferida*, también están diseñadas en TCP/IP para permitir una superpuesta más eficaz de las confirmaciones cuando los datos devueltos se encuentran desde la aplicación de recepción. Desafortunadamente, si estos datos no están disponibles y el lado que realiza el envío está esperando una confirmación, pueden producirse retrasos de aproximadamente 200 milisegundos por envío.

Cuando se cierra una conexión TCP, los recursos de conexión en el nodo que inició el cierre se colocan en un estado de espera, denominado TIME-WAIT, para protegerse frente a daños en los datos si los paquetes duplicados se colocan en la red. Esto garantiza que ambos extremos finalizan con la conexión. Esto puede provocar el agotamiento de los recursos necesarios por conexión, como la RAM y los puertos, cuando las aplicaciones abren y cierran conexiones con frecuencia.

Además de verse afectado por la confirmación diferida y otros esquemas de prevención de congestión, las aplicaciones de streaming también pueden verse afectadas por un tamaño de ventana de recepción predeterminado demasiado pequeño en el extremo receptor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Comportamiento de la aplicación](application-behavior-2.md)
</dt> <dt>

[Aplicaciones de Windows Sockets de alto rendimiento](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Algoritmo de Nagle](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



