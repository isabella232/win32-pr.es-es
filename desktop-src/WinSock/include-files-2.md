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
# <a name="include-files"></a><span data-ttu-id="e4620-103">Archivos de inclusión</span><span class="sxs-lookup"><span data-stu-id="e4620-103">Include Files</span></span>

<span data-ttu-id="e4620-104">El archivo de inclusión original para su uso con Windows Sockets 1,1 era el archivo de encabezado *Winsock. h* .</span><span class="sxs-lookup"><span data-stu-id="e4620-104">The original include file for use with Windows Sockets 1.1 was the *Winsock.h* header file.</span></span> <span data-ttu-id="e4620-105">Para facilitar la migración del código fuente existente basado en sockets UNIX de Berkeley a Windows Sockets, se recomienda que los kits de desarrollo de Windows Sockets para Winsock 1,1 se proporcionen con varios archivos de inclusión con los mismos nombres que los archivos de inclusión estándar de UNIX (por ejemplo, los archivos de encabezado *Sys/Socket. h* y arpa/inet. h).</span><span class="sxs-lookup"><span data-stu-id="e4620-105">To ease porting existing source code based on Berkeley UNIX sockets to Windows sockets, Windows Sockets development kits for Winsock 1.1 were encouraged to be supplied with several include files with the same names as standard UNIX include files (the *sys/socket.h* and arpa/inet.h header files, for example).</span></span> <span data-ttu-id="e4620-106">Sin embargo, estos archivos de encabezado de nombre similar del mismo nombre solo contenían una directiva para incluir el archivo de encabezado *WinSock2. h* .</span><span class="sxs-lookup"><span data-stu-id="e4620-106">However, these similarly-name Winsock header files merely contained a directive to include the *Winsock2.h* header file.</span></span>

<span data-ttu-id="e4620-107">Cuando se lanzó Windows Sockets 2, se ha cambiado el nombre del archivo de inclusión principal para usarlo con Windows Sockets a *WinSock2. h*.</span><span class="sxs-lookup"><span data-stu-id="e4620-107">When Windows Sockets 2 was released, the primary include file for use with Windows Sockets was renamed to *Winsock2.h*.</span></span> <span data-ttu-id="e4620-108">El archivo de encabezado *Winsock. h* original anterior para Winsock 1,1 también se ha conservado por compatibilidad con aplicaciones anteriores.</span><span class="sxs-lookup"><span data-stu-id="e4620-108">The older original *Winsock.h* header file for Winsock 1.1 was also retained for compatibility with older applications.</span></span> <span data-ttu-id="e4620-109">El desarrollo de aplicaciones compatibles con Winsock 1,1 está en desuso desde que se lanzó Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="e4620-109">The development of Winsock 1.1 compatible applications has been deprecated since Windows 2000 was released.</span></span> <span data-ttu-id="e4620-110">Ahora todas las aplicaciones deben usar la Directiva include *WinSock2. h* en los archivos de origen de la aplicación Winsock.</span><span class="sxs-lookup"><span data-stu-id="e4620-110">All applications should now use use the include *Winsock2.h* directive in Winsock application source files.</span></span>

<span data-ttu-id="e4620-111">El archivo de encabezado *WinSock2. h* contiene la mayoría de las funciones, estructuras y definiciones de Winsock.</span><span class="sxs-lookup"><span data-stu-id="e4620-111">The *Winsock2.h* header file contains most of the Winsock functions, structures, and definitions.</span></span> <span data-ttu-id="e4620-112">El archivo de encabezado *Ws2tcpip. h* contiene las definiciones introducidas en el documento WinSock 2 Protocol-Specific anexo para TCP/IP que incluye las funciones y estructuras más recientes que se usan para recuperar direcciones IP.</span><span class="sxs-lookup"><span data-stu-id="e4620-112">The *Ws2tcpip.h* header file contains definitions introduced in the WinSock 2 Protocol-Specific Annex document for TCP/IP that includes newer functions and structures used to retrieve IP addresses.</span></span> <span data-ttu-id="e4620-113">Entre ellas se incluyen la familia de funciones [**función getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) y [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) que proporcionan la resolución de nombres para direcciones IPv4 o IPv6.</span><span class="sxs-lookup"><span data-stu-id="e4620-113">These include the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) family of functions that provide name resolution for both IPv4 or IPv6 addresses.</span></span> <span data-ttu-id="e4620-114">El archivo de encabezado *Ws2tcpip. h* solo es necesario si la aplicación requiere estas funciones de nomenclatura independientes de IP.</span><span class="sxs-lookup"><span data-stu-id="e4620-114">The *Ws2tcpip.h* header file is only needed if these IP-agnostic naming functions are required by the application.</span></span>

<span data-ttu-id="e4620-115">El archivo de encabezado *mswsock. h* contiene definiciones de extensiones específicas de Microsoft para Windows Sockets 2 ([**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)y [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), por ejemplo).</span><span class="sxs-lookup"><span data-stu-id="e4620-115">The *Mswsock.h* header file contains definitions for Microsoft-specific extensions to the Windows Sockets 2 ([**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), and [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), for example).</span></span> <span data-ttu-id="e4620-116">El archivo de encabezado *mswsock. h* no suele ser necesario a menos que la aplicación use estas extensiones específicas de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e4620-116">The *Mswsock.h* header file is not normally needed unless these Microsoft-specific extensions are used by the application.</span></span>

<span data-ttu-id="e4620-117">El archivo de encabezado *WinSock2. h* incluye internamente los elementos básicos del archivo de encabezado *Windows. h* , por lo que no suele haber una \# línea de inclusión para el archivo de encabezado *Windows. h* en aplicaciones Winsock.</span><span class="sxs-lookup"><span data-stu-id="e4620-117">The *Winsock2.h* header file internally includes core elements from the *Windows.h* header file, so there is not usually an \#include line for the *Windows.h* header file in Winsock applications.</span></span> <span data-ttu-id="e4620-118">Si \# se necesita una línea de inclusión para el archivo de encabezado de *Windows. h* , debe ir precedida de la \# macro definir Win32 \_ lean \_ y \_ Mean.</span><span class="sxs-lookup"><span data-stu-id="e4620-118">If an \#include line is needed for the *Windows.h* header file, this should be preceded with the \#define WIN32\_LEAN\_AND\_MEAN macro.</span></span> <span data-ttu-id="e4620-119">Por motivos históricos, el encabezado *Windows. h* tiene como valor predeterminado el archivo de encabezado *Winsock. h* para Windows Sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="e4620-119">For historical reasons, the *Windows.h* header defaults to including the *Winsock.h* header file for Windows Sockets 1.1.</span></span> <span data-ttu-id="e4620-120">Las declaraciones del archivo de encabezado *Winsock. h* entrarán en conflicto con las declaraciones del archivo de encabezado *WinSock2. h* requerido por Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="e4620-120">The declarations in the *Winsock.h* header file will conflict with the declarations in the *Winsock2.h* header file required by Windows Sockets 2.</span></span> <span data-ttu-id="e4620-121">La \_ macro lean \_ y \_ Mean de Win32 evita que se incluya *Winsock. h* en el encabezado de *Windows. h* .</span><span class="sxs-lookup"><span data-stu-id="e4620-121">The WIN32\_LEAN\_AND\_MEAN macro prevents the *Winsock.h* from being included by the *Windows.h* header.</span></span> <span data-ttu-id="e4620-122">A continuación se muestra un ejemplo que ilustra esto.</span><span class="sxs-lookup"><span data-stu-id="e4620-122">An example illustrating this is shown below.</span></span>


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



## <a name="related-topics"></a><span data-ttu-id="e4620-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e4620-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4620-124">Crear una aplicación de Winsock básica</span><span class="sxs-lookup"><span data-stu-id="e4620-124">Creating a Basic Winsock Application</span></span>](creating-a-basic-winsock-application.md)
</dt> <dt>

[<span data-ttu-id="e4620-125">Introducción con Winsock</span><span class="sxs-lookup"><span data-stu-id="e4620-125">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="e4620-126">Trasladar aplicaciones de socket a Winsock</span><span class="sxs-lookup"><span data-stu-id="e4620-126">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="e4620-127">Consideraciones sobre la programación de Winsock</span><span class="sxs-lookup"><span data-stu-id="e4620-127">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 
