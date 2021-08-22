---
description: El archivo de incluir original para su uso Windows Sockets 1.1 era el archivo de encabezado Winsock.h.
ms.assetid: 0536abcc-4277-4bd8-927c-3bf429bc65bb
title: Archivos de inclusión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 740bde9fae96aa3088a4317c66479bcc75176ee3b9ca9f5e390365c5ef481109
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051533"
---
# <a name="include-files"></a>Archivos de inclusión

El archivo de incluir original para su uso con Windows Sockets 1.1 era el *archivo de encabezado Winsock.h.* Para facilitar la porción del código fuente existente basado en sockets de UNIX de Berkeley a sockets de Windows, se ha animado a los kits de desarrollo de sockets de Windows para Winsock 1.1 a que se les proporcionaran varios archivos de incluyención con los mismos nombres que los archivos de incluir estándar de UNIX (los archivos de encabezado *sys/socket.h* y arpa/inet.h, por ejemplo). Sin embargo, estos archivos de encabezado Winsock de nombre similar simplemente contenían una directiva para incluir el archivo de *encabezado Winsock2.h.*

Cuando Windows Sockets 2, el archivo de incluir principal para su uso con Windows Sockets se cambió a *Winsock2.h.* El archivo de encabezado *Winsock.h* original anterior para Winsock 1.1 también se conservaba por compatibilidad con aplicaciones anteriores. El desarrollo de aplicaciones compatibles con Winsock 1.1 ha quedado en desuso desde Windows 2000. Todas las aplicaciones deben usar ahora la directiva *include Winsock2.h* en los archivos de origen de la aplicación Winsock.

El *archivo de encabezado Winsock2.h* contiene la mayoría de las funciones, estructuras y definiciones de Winsock. El archivo de encabezado *Ws2tcpip.h* contiene definiciones introducidas en el documento Protocol-Specific Anexo de WinSock 2 para TCP/IP que incluye funciones y estructuras más recientes que se usan para recuperar direcciones IP. Estos incluyen la [**familia de funciones getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) y [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) que proporcionan resolución de nombres para direcciones IPv4 o IPv6. El *archivo de encabezado Ws2tcpip.h* solo es necesario si la aplicación requiere estas funciones de nomenclatura independientes de IP.

El archivo *de encabezado Mswsock.h* contiene definiciones de extensiones específicas de Microsoft para Windows Sockets 2 [**(TransmitFile,**](/windows/win32/api/mswsock/nf-mswsock-transmitfile) [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)y [**ConnectEx,**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex)por ejemplo). Normalmente, el archivo de encabezado *Mswsock.h* no es necesario a menos que la aplicación utilice estas extensiones específicas de Microsoft.

El archivo de encabezado *Winsock2.h* incluye internamente elementos principales del archivo de encabezado *Windows.h,* por lo que no suele haber una línea de include para el archivo de encabezado Windows.h en las aplicaciones \# Winsock.  Si se necesita una línea de include para el archivo de encabezado Windows.h, debe ir precedida de la \# macro DEFINE  \# WIN32 LEAN AND \_ \_ \_ MEAN. Por motivos históricos, el *encabezado Windows.h* incluye de forma predeterminada el archivo de encabezado *Winsock.h* para Windows Sockets 1.1. Las declaraciones del archivo de encabezado *Winsock.h* entra en conflicto con las declaraciones del archivo de encabezado *Winsock2.h* que requiere Windows Sockets 2. La macro WIN32 LEAN AND MEAN impide que winsock.h se incluya en \_ \_ el encabezado \_ *Windows.h.*  A continuación se muestra un ejemplo que ilustra esto.


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de una aplicación Winsock básica](creating-a-basic-winsock-application.md)
</dt> <dt>

[Tareas iniciales con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Porting Socket Applications to Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Consideraciones de programación de Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 
