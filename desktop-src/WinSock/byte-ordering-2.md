---
description: Siempre se debe tener cuidado para tener en cuenta las diferencias entre el orden de bytes utilizado para almacenar enteros por la arquitectura de host y el orden de bytes que se usa en la conexión mediante protocolos de transporte individuales.
ms.assetid: 54c84cdb-50a1-4f5e-a18f-0477d90c74d2
title: ordenación de bytes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47af5ea9d22c01e6ae1ad3d78af48b4216f71ecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497470"
---
# <a name="byte-ordering"></a>ordenación de bytes

Siempre se debe tener cuidado para tener en cuenta las diferencias entre el orden de bytes utilizado para almacenar enteros por la arquitectura de host y el orden de bytes que se usa en la conexión mediante protocolos de transporte individuales. Cualquier referencia a una dirección o número de Puerto pasado a o desde una rutina de Windows Sockets debe estar en el orden de la red (Big-endian) para el protocolo que se está usando. En el caso de IP, incluye los parámetros de puerto y dirección IP de una estructura [**sockaddr**](sockaddr-2.md) (pero no el parámetro de la *\_ familia sin* ).

Varios sistemas UNIX operan en CPU que representan enteros en el orden de bytes de la red (Big-endian). Por lo tanto, la necesidad de convertir enteros del orden de bytes del host al orden de bytes de la red se puede omitir sin causar problemas, incluso si no se recomienda para la portabilidad.

En cambio, el orden de los bytes utilizado para representar enteros en la mayoría de las CPU de Intel® es Little-Endian. Por lo tanto, se convierte en obligatorio que los enteros se conviertan del orden de bytes del host al orden de bytes de red antes de usarse en las estructuras y funciones de sockets Winsock.

Considere una aplicación que normalmente se pone en contacto con un servidor en el puerto TCP correspondiente al servicio de hora, pero proporciona un mecanismo para que el usuario especifique un puerto alternativo. El número de Puerto devuelto por [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) ya está en el orden de la red, que es el formato necesario para construir una dirección, de modo que no se requiere ninguna traducción. Sin embargo, si el usuario decide usar un puerto diferente, especificado como un entero, la aplicación debe convertirlo del host al orden de la red TCP/IP (mediante la función [**htons**](/windows/desktop/api/winsock/nf-winsock-htons) o [**WSAHtons**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons) ) antes de usarlo para construir una dirección. Por el contrario, si la aplicación mostrara el número de puerto en una dirección (devuelto por [**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername) por ejemplo), el número de puerto se debe convertir de la red al orden del host (mediante la función [**NTOHS**](/windows/desktop/api/winsock/nf-winsock-ntohs) o [**WSANtohs**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs) ) antes de que se pueda mostrar.

Como los pedidos de bytes de Internet e Intel son diferentes, las conversiones descritas en el anterior son inevitables. Se recomienda a los escritores de aplicaciones que utilicen las funciones de conversión estándar que se proporcionan como parte de Winsock en lugar de escribir su propio código de conversión, ya que es probable que las implementaciones futuras de Winsock se ejecuten en sistemas para los que el orden del host es idéntico al orden de bytes de la red. Solo es posible que las aplicaciones que usan las funciones de conversión estándar entre el host y el orden de bytes de la red sean portátiles.

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

[Trasladar aplicaciones de socket a Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[**sockaddr**](sockaddr-2.md)
</dt> <dt>

[Consideraciones sobre la programación de Winsock](winsock-programming-considerations.md)
</dt> <dt>

[**WSAHtonl**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtonl)
</dt> <dt>

[**WSAHtons**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons)
</dt> <dt>

[**WSANtohl**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohl)
</dt> <dt>

[**WSANtohs**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs)
</dt> </dl>

 

 



