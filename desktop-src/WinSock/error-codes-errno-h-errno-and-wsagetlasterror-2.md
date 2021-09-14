---
description: En las aplicaciones winsock, los códigos de error se recuperan mediante la función WSAGetLastError, el sustituto de Windows Sockets para Windows función GetLastError.
ms.assetid: cb73fc92-74bd-4c8b-a1c0-6daf4d298aa1
title: 'Códigos de error: errno, h_errno y WSAGetLastError'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31b547e0b580599aaec27a0b77bfad0ffaa8966e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068283"
---
# <a name="error-codes---errno-h_errno-and-wsagetlasterror"></a>Códigos de error: errno, h \_ errno y WSAGetLastError

En las aplicaciones winsock, los códigos de error se recuperan mediante la función [**WSAGetLastError,**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) el sustituto de Windows Sockets para la Windows [**función GetLastError.**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) Los códigos de error devueltos por Windows Sockets son similares UNIX constantes de código de error de socket, pero todas las constantes tienen el prefijo WSA. Por lo tanto, en las aplicaciones winsock, se devolvería el código de error WSAEYEOULDBLOCK, mientras que en UNIX las aplicaciones se devolvería el código de error QRDBLOCK.

Los códigos de error establecidos por Windows sockets no están disponibles a través de la variable *errno.* Además, para la **clase getXbyY** de funciones, los códigos de error no están disponibles a través de la variable *h \_ errno.* La [**función WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) está diseñada para proporcionar una manera confiable para que un subproceso de un proceso multiproceso obtenga información de error por subproceso.

Por compatibilidad con Berkeley UNIX (BSD), las primeras versiones de Windows (Windows 95 con la actualización de socket 2 de Windows y Windows 98, por ejemplo) redefinen las constantes de error regulares de Berkeley que normalmente se encuentran en *errno.h* en BSD como errores equivalentes de WSA de sockets de Windows. Por ejemplo, ECONNREFUSED se definió como **WSAECONNREFUSED** en el archivo de encabezado *Winsock.h.* En versiones posteriores de Windows (Windows NT 3.1 y versiones posteriores), estas define se comentaron para evitar conflictos con *errno.h* usados con Microsoft C/C++ y Visual Studio.

El archivo de encabezado *Winsock2.h* incluido con el Kit de desarrollo de software (SDK) de Microsoft Windows, el Kit de desarrollo de software de plataforma (SDK) y Visual Studio todavía contiene un bloque comentado de define dentro de un bloque ifdef 0 y endif que definen los códigos de error de socket de BSD para que sean iguales que las constantes de error de \# \# WSA. Se pueden usar para proporcionar cierta compatibilidad con la programación de sockets UNIX, BSD y Linux. Por compatibilidad con BSD, una aplicación puede optar por cambiar *Winsock2.h* y descomprimir este bloque. Sin embargo, se desaconseja encarecidamente que los desarrolladores de aplicaciones desaconsejen este bloque debido a conflictos inevitables con *errno.h* en la mayoría de las aplicaciones. Además, los errores de socket de BSD se definen en valores muy diferentes de los que se usan en los programas UNIX, BSD y Linux. Se recomienda encarecidamente a los desarrolladores de aplicaciones que usen las constantes de error de WSA en las aplicaciones de socket.

Estas definiciones permanecen comentadas en el *encabezado Winsock2.h* dentro de \# un bloque ifdef 0 \# y endif. Si un desarrollador de aplicaciones decide usar los códigos de error de BSD para la compatibilidad, una aplicación puede optar por incluir una línea del formulario:


```C++
#include <windows.h>

#define errno WSAGetLastError()
```



Esto permite que el código de red que se escribió para usar el *errno* global funcione correctamente en un entorno de un solo subproceso. Hay algunas desventajas muy graves. Si un archivo de código fuente incluye código que inspecciona *errno* para las funciones de socket y no socket, no se puede usar este mecanismo. Además, no es posible que una aplicación asigne un nuevo valor a *errno*. (En Windows sockets, la función [**WSASetLastError**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror) se puede usar para este propósito).

Estilo típico de BSD


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



Aunque las constantes de error coherentes con Sockets de Berkeley 4.3 se proporcionan con fines de compatibilidad, se recomienda encarecidamente a las aplicaciones que usen las definiciones de código de error de WSA. Esto se debe a que los códigos de error devueltos por ciertas funciones Windows Sockets se encuentra en el intervalo estándar de códigos de error definido por Microsoft C©. Por lo tanto, una versión mejor del fragmento de código fuente anterior es:


```C++
r = recv(...);
if (r == -1       /* (but see below) */
    && WSAGetLastError() == WSAEWOULDBLOCK)
    {...}
```



La especificación winsock 1.1 original definida en 1995 recomienda un conjunto de códigos de error y enumera los posibles errores que se pueden devolver como resultado de cada función. Windows Sockets 2 agregó funciones y características con otros códigos de error Windows Sockets devueltos además de los enumerados en la especificación original de Winsock. Se han agregado funciones adicionales con el tiempo para mejorar Winsock para que los desarrolladores las usen. Por ejemplo, se agregaron nuevas funciones de servicio de nombres [**(getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) y [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo), por ejemplo) que admiten IPv6 e IPv4 en Windows XP y versiones posteriores. Algunas de las funciones anteriores del servicio de nombres solo IPv4 (la clase **getXbyY** de funciones, por ejemplo) han quedado en desuso.

En la sección sobre códigos de error de sockets de Windows se proporciona una lista completa de los posibles códigos [de error devueltos por Windows sockets](windows-sockets-error-codes-2.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de errores de Winsock](handling-winsock-errors.md)
</dt> <dt>

[Porte de aplicaciones de socket a Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Windows Códigos de error de sockets](windows-sockets-error-codes-2.md)
</dt> <dt>

[Consideraciones de programación de Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 
