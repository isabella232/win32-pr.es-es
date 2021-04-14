---
description: El archivo de inclusión original para su uso con Windows Sockets 1,1 era el archivo de encabezado Winsock. h.
ms.assetid: 0536abcc-4277-4bd8-927c-3bf429bc65bb
title: Archivos de inclusión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf7a4edcd70e6a6280b26f7b6ab9f0f1dab674e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360299"
---
# <a name="include-files"></a>Archivos de inclusión

El archivo de inclusión original para su uso con Windows Sockets 1,1 era el archivo de encabezado *Winsock. h* . Para facilitar la migración del código fuente existente basado en sockets UNIX de Berkeley a Windows Sockets, se recomienda que los kits de desarrollo de Windows Sockets para Winsock 1,1 se proporcionen con varios archivos de inclusión con los mismos nombres que los archivos de inclusión estándar de UNIX (por ejemplo, los archivos de encabezado *Sys/Socket. h* y arpa/inet. h). Sin embargo, estos archivos de encabezado de nombre similar del mismo nombre solo contenían una directiva para incluir el archivo de encabezado *WinSock2. h* .

Cuando se lanzó Windows Sockets 2, se ha cambiado el nombre del archivo de inclusión principal para usarlo con Windows Sockets a *WinSock2. h*. El archivo de encabezado *Winsock. h* original anterior para Winsock 1,1 también se ha conservado por compatibilidad con aplicaciones anteriores. El desarrollo de aplicaciones compatibles con Winsock 1,1 está en desuso desde que se lanzó Windows 2000. Ahora todas las aplicaciones deben usar la Directiva include *WinSock2. h* en los archivos de origen de la aplicación Winsock.

El archivo de encabezado *WinSock2. h* contiene la mayoría de las funciones, estructuras y definiciones de Winsock. El archivo de encabezado *Ws2tcpip. h* contiene las definiciones introducidas en el documento WinSock 2 Protocol-Specific anexo para TCP/IP que incluye las funciones y estructuras más recientes que se usan para recuperar direcciones IP. Entre ellas se incluyen la familia de funciones [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) y [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) que proporcionan la resolución de nombres para direcciones IPv4 o IPv6. El archivo de encabezado *Ws2tcpip. h* solo es necesario si la aplicación requiere estas funciones de nomenclatura independientes de IP.

El archivo de encabezado *mswsock. h* contiene definiciones de extensiones específicas de Microsoft para Windows Sockets 2 ([**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)y [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), por ejemplo). El archivo de encabezado *mswsock. h* no suele ser necesario a menos que la aplicación use estas extensiones específicas de Microsoft.

El archivo de encabezado *WinSock2. h* incluye internamente los elementos básicos del archivo de encabezado *Windows. h* , por lo que no suele haber una \# línea de inclusión para el archivo de encabezado *Windows. h* en aplicaciones Winsock. Si \# se necesita una línea de inclusión para el archivo de encabezado de *Windows. h* , debe ir precedida de la \# macro definir Win32 \_ lean \_ y \_ Mean. Por motivos históricos, el encabezado *Windows. h* tiene como valor predeterminado el archivo de encabezado *Winsock. h* para Windows Sockets 1,1. Las declaraciones del archivo de encabezado *Winsock. h* entrarán en conflicto con las declaraciones del archivo de encabezado *WinSock2. h* requerido por Windows Sockets 2. La \_ macro lean \_ y \_ Mean de Win32 evita que se incluya *Winsock. h* en el encabezado de *Windows. h* . A continuación se muestra un ejemplo que ilustra esto.


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

[Crear una aplicación de Winsock básica](creating-a-basic-winsock-application.md)
</dt> <dt>

[Introducción con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Trasladar aplicaciones de socket a Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Consideraciones sobre la programación de Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 
