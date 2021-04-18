---
description: En las aplicaciones Winsock, los códigos de error se recuperan mediante la función WSAGetLastError, el sustituto de Windows Sockets para la función GetLastError de Windows.
ms.assetid: cb73fc92-74bd-4c8b-a1c0-6daf4d298aa1
title: 'Códigos de error: errno, h_errno y WSAGetLastError'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31b547e0b580599aaec27a0b77bfad0ffaa8966e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705631"
---
# <a name="error-codes---errno-h_errno-and-wsagetlasterror"></a>Códigos de error: errno, h \_ errno y WSAGetLastError

En las aplicaciones Winsock, los códigos de error se recuperan mediante la función [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) , el sustituto de Windows Sockets para la función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) de Windows. Los códigos de error devueltos por Windows Sockets son similares a las constantes de códigos de error de socket de UNIX, pero todas las constantes tienen el prefijo WSA. Por lo tanto, en las aplicaciones Winsock se devolverá el código de error WSAEWOULDBLOCK, mientras que en las aplicaciones UNIX se devolverá el código de error EWOULDBLOCK.

Los códigos de error establecidos por Windows Sockets no están disponibles a través de la variable *errno* . Además, para la clase **getXbyY** de funciones, los códigos de error no se ponen a disposición a través de la variable *h \_ errno* . La función [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) está diseñada para proporcionar un método confiable para que un subproceso de un proceso multiproceso pueda obtener información de error por subproceso.

Por compatibilidad con Berkeley UNIX (BSD), las primeras versiones de Windows (Windows 95 con la actualización de Windows socket 2 y Windows 98, por ejemplo) constantes de error regulares de Berkeley que se suelen encontrar en *errno. h* en BSD como errores de WSA de Windows Sockets equivalentes. Por ejemplo, ECONNREFUSED se definió como **WSAECONNREFUSED** en el archivo de encabezado *Winsock. h* . En versiones posteriores de Windows (Windows NT 3,1 y versiones posteriores), estas definiciones se comentaron para evitar conflictos con *errno. h* que se usa con Microsoft C/C++ y Visual Studio.

El archivo de encabezado *WinSock2. h* incluido en el kit de desarrollo de software (SDK) de Microsoft Windows, el kit de desarrollo de software (SDK) de la plataforma y Visual Studio todavía contiene un bloque comentado de definiciones dentro de un \# bloque ifdef 0 y \# endif que definen los códigos de error de socket BSD para que sean iguales que las constantes de error WSA. Se pueden usar para proporcionar cierta compatibilidad con la programación de sockets UNIX, BSD y Linux. Por compatibilidad con BSD, una aplicación puede optar por cambiar *WinSock2. h* y quitar la marca de comentario de este bloque. Sin embargo, se desaconseja encarecidamente a los desarrolladores de aplicaciones que quiten los comentarios de este bloque debido a conflictos inevitables con *errno. h* en la mayoría de las aplicaciones. Además, los errores de socket BSD se definen como valores muy diferentes de los que se usan en los programas UNIX, BSD y Linux. Se recomienda encarecidamente a los desarrolladores de aplicaciones el uso de constantes de error WSA en aplicaciones de socket.

Estas definiciones permanecen comentadas en el encabezado *WinSock2. h* dentro de un \# bloque ifdef 0 y \# endif. Si un desarrollador de aplicaciones insiste en usar los códigos de error de BSD para la compatibilidad, una aplicación puede decidir incluir una línea del formulario:


```C++
#include <windows.h>

#define errno WSAGetLastError()
```



Esto permite que el código de red que se escribió para usar el *errno* global funcione correctamente en un entorno de un solo subproceso. Hay algunas desventajas muy graves. Si un archivo de código fuente incluye código que inspecciona *errno* para las funciones de socket y que no son de socket, no se puede usar este mecanismo. Además, no es posible que una aplicación asigne un nuevo valor a *errno*. (En Windows Sockets, la función [**WSASetLastError**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror) se puede usar para este propósito).

Estilo BSD típico


```C++
r = recv(...);
if (r == -1
    && errno == EWOULDBLOCK)
    {...}
```



Estilo preferido


```C++
r = recv(...);
if (r == -1       /* (but see below) */
    && WSAGetLastError() == EWOULDBLOCK)
    {...}
```



Aunque las constantes de error coherentes con los sockets de Berkeley 4,3 se proporcionan con fines de compatibilidad, se recomienda encarecidamente que las aplicaciones usen las definiciones de códigos de error WSA. Esto se debe a que los códigos de error devueltos por determinadas funciones de Windows Sockets se encuentran en el intervalo estándar de códigos de error tal y como se define en la © de Microsoft C. Por lo tanto, una versión mejor del fragmento de código fuente anterior es:


```C++
r = recv(...);
if (r == -1       /* (but see below) */
    && WSAGetLastError() == WSAEWOULDBLOCK)
    {...}
```



La especificación Winsock 1,1 original definida en 1995 recomienda un conjunto de códigos de error y enumera los posibles errores que se pueden devolver como resultado de cada función. Windows Sockets 2 agregó funciones y características con otros códigos de error de Windows Sockets devueltos además de los enumerados en la especificación Winsock original. Se han agregado funciones adicionales con el tiempo para mejorar Winsock para su uso por parte de los desarrolladores. Por ejemplo, se agregaron nuevas funciones de servicio de nombres (por ejemplo,[**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) y [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)) que admiten tanto IPv6 como IPv4 en Windows XP y versiones posteriores. Algunas de las funciones de servicio de nombres solo IPv4 anteriores (por ejemplo, la clase **getXbyY** de funciones) han quedado en desuso.

En la sección sobre [códigos de error de Windows Sockets](windows-sockets-error-codes-2.md)se proporciona una lista completa de los posibles códigos de error devueltos por las funciones de Windows Sockets.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de errores de Winsock](handling-winsock-errors.md)
</dt> <dt>

[Trasladar aplicaciones de socket a Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Códigos de error de Windows Sockets](windows-sockets-error-codes-2.md)
</dt> <dt>

[Consideraciones sobre la programación de Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 
