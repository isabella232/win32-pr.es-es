---
description: TCP/IP tiene características que permiten que el protocolo funcione según lo que dictan sus requisitos de implementación estandarizados.
ms.assetid: 6e9b3878-85f0-4572-9c00-a2e7647286ff
title: Características de TCP/IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 561ab497d6f37c1c84b0203088b29e216ff0a69f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570041"
---
# <a name="tcpip-characteristics"></a>Características de TCP/IP

TCP/IP tiene características que permiten que el protocolo funcione según lo que dictan sus requisitos de implementación estandarizados. Estas características se pueden combinar con opciones de desarrollo que tienen como resultado un rendimiento deficiente. El impacto que estas características de TCP/IP tienen en una aplicación depende de si la aplicación es transaccional o de streaming.

Las aplicaciones transaccionales se ven afectadas por la sobrecarga necesaria para el establecimiento y la terminación de la conexión. Por ejemplo, cada vez que se establece una conexión en una red Ethernet, se deben enviar tres paquetes de aproximadamente 60 bytes cada uno y se requiere aproximadamente un RTT para el intercambio. Cuando se produce la terminación de una conexión, se intercambian cuatro paquetes. Esto es para cada conexión; Una aplicación que abre y cierra las conexiones a menudo incurre en esta sobrecarga en cada repetición.

Otro aspecto de TCP/IP es *el inicio lento,* que tiene lugar cada vez que se establece una conexión. El inicio lento es un límite artificial en el número de segmentos de datos que se pueden enviar antes de recibir la confirmación de esos segmentos. El inicio lento está diseñado para limitar la congestión de la red. Cuando se establece una conexión a través de Ethernet, independientemente del tamaño de la ventana del receptor, una transmisión de 4 KB puede tardar hasta 3-4 RTT debido a un inicio lento.

Una optimización tcp/IP denominada algoritmo de Nagle también puede limitar la velocidad de transferencia de datos en una conexión. El algoritmo de Nagle está diseñado para reducir la sobrecarga del protocolo para las aplicaciones que envían pequeñas cantidades de datos, como Telnet, que envía un solo carácter a la vez. En lugar de enviar inmediatamente un paquete con muchos encabezados y pocos datos, la pila espera más datos de la aplicación, o una confirmación, antes de continuar.

Las confirmaciones retrasadas, conocidas normalmente como *confirmación* retrasada, también están diseñadas en TCP/IP para permitir una depuración más eficaz de las confirmaciones cuando se devuelven datos de la aplicación del lado receptor. Desafortunadamente, si estos datos no están disponibles y el lado emisor está esperando una confirmación, pueden producirse retrasos de aproximadamente 200 milisegundos por envío.

Cuando se cierra una conexión TCP, los recursos de conexión del nodo que inició el cierre se ponen en estado de espera, denominado TIME-WAIT, para protegerse contra daños en los datos si los paquetes duplicados persisten en la red. Esto garantiza que ambos extremos finalicen con la conexión. Esto puede provocar el agotamiento de los recursos necesarios por conexión, como la RAM y los puertos, cuando las aplicaciones abren y cierran conexiones con frecuencia.

Además de verse afectadas por el retraso de ACK y otros esquemas de prevención de congestión, las aplicaciones de streaming también pueden verse afectadas por un tamaño de ventana de recepción predeterminado demasiado pequeño en el extremo receptor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Comportamiento de la aplicación](application-behavior-2.md)
</dt> <dt>

[Aplicaciones de sockets Windows alto rendimiento](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Algoritmo de Nagle](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



