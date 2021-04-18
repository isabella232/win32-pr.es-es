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
# <a name="error-codes---errno-h_errno-and-wsagetlasterror"></a><span data-ttu-id="4154c-103">Códigos de error: errno, h \_ errno y WSAGetLastError</span><span class="sxs-lookup"><span data-stu-id="4154c-103">Error Codes - errno, h\_errno and WSAGetLastError</span></span>

<span data-ttu-id="4154c-104">En las aplicaciones Winsock, los códigos de error se recuperan mediante la función [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) , el sustituto de Windows Sockets para la función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) de Windows.</span><span class="sxs-lookup"><span data-stu-id="4154c-104">In Winsock applications, error codes are retrieved using the [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) function, the Windows Sockets substitute for the Windows [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span> <span data-ttu-id="4154c-105">Los códigos de error devueltos por Windows Sockets son similares a las constantes de códigos de error de socket de UNIX, pero todas las constantes tienen el prefijo WSA.</span><span class="sxs-lookup"><span data-stu-id="4154c-105">The error codes returned by Windows Sockets are similar to UNIX socket error code constants, but the constants are all prefixed with WSA.</span></span> <span data-ttu-id="4154c-106">Por lo tanto, en las aplicaciones Winsock se devolverá el código de error WSAEWOULDBLOCK, mientras que en las aplicaciones UNIX se devolverá el código de error EWOULDBLOCK.</span><span class="sxs-lookup"><span data-stu-id="4154c-106">So in Winsock applications the WSAEWOULDBLOCK error code would be returned, while in UNIX applications the EWOULDBLOCK error code would be returned.</span></span>

<span data-ttu-id="4154c-107">Los códigos de error establecidos por Windows Sockets no están disponibles a través de la variable *errno* .</span><span class="sxs-lookup"><span data-stu-id="4154c-107">Error codes set by Windows Sockets are not made available through the *errno* variable.</span></span> <span data-ttu-id="4154c-108">Además, para la clase **getXbyY** de funciones, los códigos de error no se ponen a disposición a través de la variable *h \_ errno* .</span><span class="sxs-lookup"><span data-stu-id="4154c-108">Additionally, for the **getXbyY** class of functions, error codes are not made available through the *h\_errno* variable.</span></span> <span data-ttu-id="4154c-109">La función [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) está diseñada para proporcionar un método confiable para que un subproceso de un proceso multiproceso pueda obtener información de error por subproceso.</span><span class="sxs-lookup"><span data-stu-id="4154c-109">The [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) function is intended to provide a reliable way for a thread in a multithreaded process to obtain per-thread error information.</span></span>

<span data-ttu-id="4154c-110">Por compatibilidad con Berkeley UNIX (BSD), las primeras versiones de Windows (Windows 95 con la actualización de Windows socket 2 y Windows 98, por ejemplo) constantes de error regulares de Berkeley que se suelen encontrar en *errno. h* en BSD como errores de WSA de Windows Sockets equivalentes.</span><span class="sxs-lookup"><span data-stu-id="4154c-110">For compatibility with Berkeley UNIX (BSD), early versions of Windows (Windows 95 with the Windows Socket 2 Update and Windows 98, for example) redefined regular Berkeley error constants typically found in *errno.h* on BSD as the equivalent Windows Sockets WSA errors.</span></span> <span data-ttu-id="4154c-111">Por ejemplo, ECONNREFUSED se definió como **WSAECONNREFUSED** en el archivo de encabezado *Winsock. h* .</span><span class="sxs-lookup"><span data-stu-id="4154c-111">So for example, ECONNREFUSED was defined as **WSAECONNREFUSED** in the *Winsock.h* header file.</span></span> <span data-ttu-id="4154c-112">En versiones posteriores de Windows (Windows NT 3,1 y versiones posteriores), estas definiciones se comentaron para evitar conflictos con *errno. h* que se usa con Microsoft C/C++ y Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="4154c-112">In subsequent versions of Windows (Windows NT 3.1 and later) these defines were commented out to avoid conflicts with *errno.h* used with Microsoft C/C++ and Visual Studio.</span></span>

<span data-ttu-id="4154c-113">El archivo de encabezado *WinSock2. h* incluido en el kit de desarrollo de software (SDK) de Microsoft Windows, el kit de desarrollo de software (SDK) de la plataforma y Visual Studio todavía contiene un bloque comentado de definiciones dentro de un \# bloque ifdef 0 y \# endif que definen los códigos de error de socket BSD para que sean iguales que las constantes de error WSA.</span><span class="sxs-lookup"><span data-stu-id="4154c-113">The *Winsock2.h* header file included with the Microsoft Windows Software Development Kit (SDK), Platform Software Development Kit (SDK), and Visual Studio still contains a commented out block of defines within an \#ifdef 0 and \#endif block that define the BSD socket error codes to be the same as the WSA error constants.</span></span> <span data-ttu-id="4154c-114">Se pueden usar para proporcionar cierta compatibilidad con la programación de sockets UNIX, BSD y Linux.</span><span class="sxs-lookup"><span data-stu-id="4154c-114">These can be used to provide some compatibility with UNIX, BSD, and Linux socket programming.</span></span> <span data-ttu-id="4154c-115">Por compatibilidad con BSD, una aplicación puede optar por cambiar *WinSock2. h* y quitar la marca de comentario de este bloque.</span><span class="sxs-lookup"><span data-stu-id="4154c-115">For compatibility with BSD, an application may choose to change the *Winsock2.h* and uncomment this block.</span></span> <span data-ttu-id="4154c-116">Sin embargo, se desaconseja encarecidamente a los desarrolladores de aplicaciones que quiten los comentarios de este bloque debido a conflictos inevitables con *errno. h* en la mayoría de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="4154c-116">However, application developers are strongly discouraged from uncommenting this block because of inevitable conflicts with *errno.h* in most applications.</span></span> <span data-ttu-id="4154c-117">Además, los errores de socket BSD se definen como valores muy diferentes de los que se usan en los programas UNIX, BSD y Linux.</span><span class="sxs-lookup"><span data-stu-id="4154c-117">Also, the BSD socket errors are defined to very different values than are used in UNIX, BSD, and Linux programs.</span></span> <span data-ttu-id="4154c-118">Se recomienda encarecidamente a los desarrolladores de aplicaciones el uso de constantes de error WSA en aplicaciones de socket.</span><span class="sxs-lookup"><span data-stu-id="4154c-118">Application developers are very strongly encouraged to use the WSA error constants in socket applications.</span></span>

<span data-ttu-id="4154c-119">Estas definiciones permanecen comentadas en el encabezado *WinSock2. h* dentro de un \# bloque ifdef 0 y \# endif.</span><span class="sxs-lookup"><span data-stu-id="4154c-119">These defines remain commented out in the *Winsock2.h* header within an \#ifdef 0 and \#endif block.</span></span> <span data-ttu-id="4154c-120">Si un desarrollador de aplicaciones insiste en usar los códigos de error de BSD para la compatibilidad, una aplicación puede decidir incluir una línea del formulario:</span><span class="sxs-lookup"><span data-stu-id="4154c-120">If an application developer insists on using the BSD error codes for compatibility, then an application may choose to include a line of the form:</span></span>


```C++
#include <windows.h>

#define errno WSAGetLastError()
```



<span data-ttu-id="4154c-121">Esto permite que el código de red que se escribió para usar el *errno* global funcione correctamente en un entorno de un solo subproceso.</span><span class="sxs-lookup"><span data-stu-id="4154c-121">This allows networking code which was written to use the global *errno* to work correctly in a single-threaded environment.</span></span> <span data-ttu-id="4154c-122">Hay algunas desventajas muy graves.</span><span class="sxs-lookup"><span data-stu-id="4154c-122">There are some very serious drawbacks.</span></span> <span data-ttu-id="4154c-123">Si un archivo de código fuente incluye código que inspecciona *errno* para las funciones de socket y que no son de socket, no se puede usar este mecanismo.</span><span class="sxs-lookup"><span data-stu-id="4154c-123">If a source file includes code which inspects *errno* for both socket and non-socket functions, this mechanism cannot be used.</span></span> <span data-ttu-id="4154c-124">Además, no es posible que una aplicación asigne un nuevo valor a *errno*.</span><span class="sxs-lookup"><span data-stu-id="4154c-124">Furthermore, it is not possible for an application to assign a new value to *errno*.</span></span> <span data-ttu-id="4154c-125">(En Windows Sockets, la función [**WSASetLastError**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror) se puede usar para este propósito).</span><span class="sxs-lookup"><span data-stu-id="4154c-125">(In Windows Sockets, the function [**WSASetLastError**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror) may be used for this purpose.)</span></span>

<span data-ttu-id="4154c-126">Estilo BSD típico</span><span class="sxs-lookup"><span data-stu-id="4154c-126">Typical BSD Style</span></span>


```C++
r = recv(...);
if (r == -1
    && errno == EWOULDBLOCK)
    {...}
```



<span data-ttu-id="4154c-127">Estilo preferido</span><span class="sxs-lookup"><span data-stu-id="4154c-127">Preferred Style</span></span>


```C++
r = recv(...);
if (r == -1       /* (but see below) */
    && WSAGetLastError() == EWOULDBLOCK)
    {...}
```



<span data-ttu-id="4154c-128">Aunque las constantes de error coherentes con los sockets de Berkeley 4,3 se proporcionan con fines de compatibilidad, se recomienda encarecidamente que las aplicaciones usen las definiciones de códigos de error WSA.</span><span class="sxs-lookup"><span data-stu-id="4154c-128">Although error constants consistent with Berkeley Sockets 4.3 are provided for compatibility purposes, applications are strongly encouraged to use the WSA error code definitions.</span></span> <span data-ttu-id="4154c-129">Esto se debe a que los códigos de error devueltos por determinadas funciones de Windows Sockets se encuentran en el intervalo estándar de códigos de error tal y como se define en la © de Microsoft C.</span><span class="sxs-lookup"><span data-stu-id="4154c-129">This is because error codes returned by certain Windows Sockets functions fall into the standard range of error codes as defined by Microsoft C©.</span></span> <span data-ttu-id="4154c-130">Por lo tanto, una versión mejor del fragmento de código fuente anterior es:</span><span class="sxs-lookup"><span data-stu-id="4154c-130">Thus, a better version of the preceding source code fragment is:</span></span>


```C++
r = recv(...);
if (r == -1       /* (but see below) */
    && WSAGetLastError() == WSAEWOULDBLOCK)
    {...}
```



<span data-ttu-id="4154c-131">La especificación Winsock 1,1 original definida en 1995 recomienda un conjunto de códigos de error y enumera los posibles errores que se pueden devolver como resultado de cada función.</span><span class="sxs-lookup"><span data-stu-id="4154c-131">The original Winsock 1.1 specification defined in 1995 recommended a set of error codes, and listed the possible errors that can be returned as a result of each function.</span></span> <span data-ttu-id="4154c-132">Windows Sockets 2 agregó funciones y características con otros códigos de error de Windows Sockets devueltos además de los enumerados en la especificación Winsock original.</span><span class="sxs-lookup"><span data-stu-id="4154c-132">Windows Sockets 2 added functions and features with other Windows Sockets error codes returned in addition to those listed in the original Winsock specification.</span></span> <span data-ttu-id="4154c-133">Se han agregado funciones adicionales con el tiempo para mejorar Winsock para su uso por parte de los desarrolladores.</span><span class="sxs-lookup"><span data-stu-id="4154c-133">Additional functions have been added over time to enhance Winsock for use by developers.</span></span> <span data-ttu-id="4154c-134">Por ejemplo, se agregaron nuevas funciones de servicio de nombres (por ejemplo,[**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) y [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)) que admiten tanto IPv6 como IPv4 en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4154c-134">For example, new name service functions ([**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo), for example) were added that support both IPv6 and IPv4 on Windows XP and later.</span></span> <span data-ttu-id="4154c-135">Algunas de las funciones de servicio de nombres solo IPv4 anteriores (por ejemplo, la clase **getXbyY** de funciones) han quedado en desuso.</span><span class="sxs-lookup"><span data-stu-id="4154c-135">Some of the older IPv4-only name service functions (the **getXbyY** class of functions, for example) have been deprecated.</span></span>

<span data-ttu-id="4154c-136">En la sección sobre [códigos de error de Windows Sockets](windows-sockets-error-codes-2.md)se proporciona una lista completa de los posibles códigos de error devueltos por las funciones de Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="4154c-136">A complete list of possible error codes returned by Windows Sockets functions is given in the section on [Windows Sockets Error Codes](windows-sockets-error-codes-2.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4154c-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4154c-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4154c-138">Control de errores de Winsock</span><span class="sxs-lookup"><span data-stu-id="4154c-138">Handling Winsock Errors</span></span>](handling-winsock-errors.md)
</dt> <dt>

[<span data-ttu-id="4154c-139">Trasladar aplicaciones de socket a Winsock</span><span class="sxs-lookup"><span data-stu-id="4154c-139">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="4154c-140">Códigos de error de Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="4154c-140">Windows Sockets Error Codes</span></span>](windows-sockets-error-codes-2.md)
</dt> <dt>

[<span data-ttu-id="4154c-141">Consideraciones sobre la programación de Winsock</span><span class="sxs-lookup"><span data-stu-id="4154c-141">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 
