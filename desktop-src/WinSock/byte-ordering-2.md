---
description: Siempre debe tenerse en cuenta las diferencias entre la ordenación de bytes utilizada para almacenar enteros por la arquitectura de host y la ordenación de bytes utilizada en la conexión por protocolos de transporte individuales.
ms.assetid: 54c84cdb-50a1-4f5e-a18f-0477d90c74d2
title: ordenación de bytes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 554b9f00b67fcd602daee0ed33443e228e4e3976f334506d949e3af79fef7e8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118560185"
---
# <a name="byte-ordering"></a>ordenación de bytes

Siempre debe tenerse en cuenta las diferencias entre la ordenación de bytes utilizada para almacenar enteros por la arquitectura de host y la ordenación de bytes utilizada en la conexión por protocolos de transporte individuales. Cualquier referencia a una dirección o número de puerto pasado a o desde una rutina de sockets de Windows debe estar en el orden de red (big-endian) para el protocolo que se utiliza. En el caso de IP, esto incluye la dirección IP y los parámetros de puerto de una estructura [**sockaddr**](sockaddr-2.md) (pero no el *parámetro de \_ familia sin).*

Varios de los sistemas de UNIX funcionan en CPU que representan enteros en orden de bytes de red (big-endian). Por lo tanto, la necesidad de convertir enteros del orden de bytes del host al orden de bytes de red se puede omitir sin causar problemas aunque no se recomienda para la portabilidad.

Por el contrario, la ordenación de bytes usada para representar enteros por la mayoría de las CPU ® Intel es little-endian. Por lo tanto, es obligatorio que los enteros se conviertan del orden de bytes del host al orden de bytes de red antes de usarse en las funciones y estructuras de Winsock Sockets.

Considere una aplicación que normalmente se pone en contacto con un servidor en el puerto TCP correspondiente al servicio de hora, pero proporciona un mecanismo para que el usuario especifique un puerto alternativo. El número de puerto devuelto por [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) ya está en orden de red, que es el formato necesario para construir una dirección para que no se requiera ninguna traducción. Sin embargo, si el usuario elige usar un puerto diferente, especificado como un entero, la aplicación debe convertir esto del host al orden de red TCP/IP (mediante la función [**htons**](/windows/desktop/api/winsock/nf-winsock-htons) o [**WSAHtons)**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons) antes de usarlo para construir una dirección. Por el contrario, si la aplicación mostrara el número del puerto dentro de una dirección (devuelta por [**getpeername,**](/windows/desktop/api/winsock/nf-winsock-getpeername) por ejemplo), el número de puerto debe convertirse de la red al orden de host (mediante la función [**ntlejos o**](/windows/desktop/api/winsock/nf-winsock-ntohs) [**WSANt adheres)**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs) antes de que se pueda mostrar.

Dado que los pedidos de bytes de Intel e Internet son diferentes, las conversiones descritas en el anterior son inevitables. Se advierte a los escritores de aplicaciones que deben usar las funciones de conversión estándar proporcionadas como parte de Winsock en lugar de escribir su propio código de conversión, ya que es probable que las implementaciones futuras de Winsock se ejecuten en sistemas para los que el orden de host es idéntico al orden de bytes de red. Es probable que solo las aplicaciones que usan las funciones de conversión estándar entre el host y el orden de bytes de red sean portátiles.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername)
</dt> <dt>

[**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname)
</dt> <dt>

[**htonl**](/windows/desktop/api/winsock/nf-winsock-htonl)
</dt> <dt>

[**htons**](/windows/desktop/api/winsock/nf-winsock-htons)
</dt> <dt>

[**ntohl**](/windows/desktop/api/winsock/nf-winsock-ntohl)
</dt> <dt>

[**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs)
</dt> <dt>

[Porting Socket Applications to Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[**sockaddr**](sockaddr-2.md)
</dt> <dt>

[Consideraciones de programación de Winsock](winsock-programming-considerations.md)
</dt> <dt>

[**WSAHtonl**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtonl)
</dt> <dt>

[**WSAHtons**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons)
</dt> <dt>

[**WSANtohl**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohl)
</dt> <dt>

[**WSANt adheres**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs)
</dt> </dl>

 

 



