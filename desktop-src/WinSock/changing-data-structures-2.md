---
description: Al agregar compatibilidad con IPv6, debe asegurarse de que la aplicación define las estructuras de datos con el tamaño adecuado.
ms.assetid: 2bf353e2-38d5-462c-9e6c-65886b617215
title: Cambiar las estructuras de datos para IPv6 Winsock Appications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2c91e19ed733d111bd4e12d824da6ee1a988e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705647"
---
# <a name="changing-data-structures-for-ipv6-winsock-appications"></a><span data-ttu-id="690d9-103">Cambiar las estructuras de datos para IPv6 Winsock Appications</span><span class="sxs-lookup"><span data-stu-id="690d9-103">Changing Data Structures for IPv6 Winsock Appications</span></span>

<span data-ttu-id="690d9-104">Al agregar compatibilidad con IPv6, debe asegurarse de que la aplicación define las estructuras de datos con el tamaño adecuado.</span><span class="sxs-lookup"><span data-stu-id="690d9-104">When adding support for IPv6, you must ensure that your application defines properly sized data structures.</span></span> <span data-ttu-id="690d9-105">El tamaño de una dirección IPv6 es mucho mayor que una dirección IPv4.</span><span class="sxs-lookup"><span data-stu-id="690d9-105">The size of an IPv6 address is much larger than an IPv4 address.</span></span> <span data-ttu-id="690d9-106">Las estructuras que están codificadas de forma rígida para controlar el tamaño de una dirección IPv4 al almacenar una dirección IP provocarán problemas en la aplicación y se deben modificar.</span><span class="sxs-lookup"><span data-stu-id="690d9-106">Structures that are hard-coded to handle the size of an IPv4 address when storing an IP address will cause problems in your application, and must be modified.</span></span>

<span data-ttu-id="690d9-107">Procedimiento recomendado</span><span class="sxs-lookup"><span data-stu-id="690d9-107">Best Practice</span></span>

<span data-ttu-id="690d9-108">El mejor enfoque para asegurarse de que las estructuras tienen el tamaño correcto es usar la estructura de [**\_ almacenamiento de SOCKADDR**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="690d9-108">The best approach to ensuring that your structures are properly sized is to use the [**SOCKADDR\_STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) structure.</span></span> <span data-ttu-id="690d9-109">La estructura de **\_ almacenamiento de SOCKADDR** es independiente de la versión de la dirección IP.</span><span class="sxs-lookup"><span data-stu-id="690d9-109">The **SOCKADDR\_STORAGE** structure is agnostic to IP address version.</span></span> <span data-ttu-id="690d9-110">Cuando la estructura de **\_ almacenamiento de SOCKADDR** se usa para almacenar direcciones IP, las direcciones IPv4 e IPv6 se pueden controlar correctamente con una base de código.</span><span class="sxs-lookup"><span data-stu-id="690d9-110">When the **SOCKADDR\_STORAGE** structure is used to store IP addresses, IPv4 and IPv6 addresses can be properly handled with one code base.</span></span>

<span data-ttu-id="690d9-111">En el ejemplo siguiente, que es un extracto tomado del archivo Server. c que se encuentra en el Apéndice B, se identifica un uso adecuado de la estructura de **\_ almacenamiento de SOCKADDR** .</span><span class="sxs-lookup"><span data-stu-id="690d9-111">The following example, which is an excerpt taken from the Server.c file found in Appendix B, identifies an appropriate use of the **SOCKADDR\_STORAGE** structure.</span></span> <span data-ttu-id="690d9-112">Observe que la estructura, cuando se usa correctamente como se muestra en este ejemplo, controla correctamente una dirección IPv4 o IPv6.</span><span class="sxs-lookup"><span data-stu-id="690d9-112">Notice that the structure, when used properly as this example shows, gracefully handles either an IPv4 or IPv6 address.</span></span>


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

#define BUFFER_SIZE 512
#define DEFAULT_PORT "27015"

int main(int argc, char **argv)
{
    char Buffer[BUFFER_SIZE] = {0};
    char *Hostname;
    int Family = AF_UNSPEC;
    int SocketType = SOCK_STREAM;
    char *Port = DEFAULT_PORT;
    char *Address = NULL;
    int i = 0;
    DWORD dwRetval = 0;
    int iResult = 0;
    int FromLen = 0;
    int AmountRead = 0;

    SOCKADDR_STORAGE From;

    WSADATA wsaData;

    ADDRINFO *AddrInfo = NULL;
    ADDRINFO *AI = NULL;

    // Parse arguments
    if (argc >= 1) {
        Hostname = argv[1];
    }    

   // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }

    From.ss_family = (ADDRESS_FAMILY) Family;
    
    //...
        
        return 0;
}
```



> [!Note]  
> <span data-ttu-id="690d9-113">La estructura de [**\_ almacenamiento de SOCKADDR**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) es nueva en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="690d9-113">The [**SOCKADDR\_STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) structure is new for Windows XP.</span></span>

 

<span data-ttu-id="690d9-114">Código que se debe evitar</span><span class="sxs-lookup"><span data-stu-id="690d9-114">Code To Avoid</span></span>

<span data-ttu-id="690d9-115">Normalmente, muchas aplicaciones usan la estructura [**sockaddr**](sockaddr-2.md) para almacenar direcciones independientes del protocolo o la **sockaddr \_ en** la estructura de las direcciones IP.</span><span class="sxs-lookup"><span data-stu-id="690d9-115">Typically, many applications used the [**sockaddr**](sockaddr-2.md) structure to store protocol-independent addresses, or the **sockaddr\_in** structure for IP addresses.</span></span> <span data-ttu-id="690d9-116">Ni la estructura sockaddr ni la **sockaddr \_ en** la estructura son lo suficientemente grandes como para contener las direcciones IPv6 y, por tanto, las dos son insuficientes si la aplicación va a ser compatible con IPv6.</span><span class="sxs-lookup"><span data-stu-id="690d9-116">Neither the sockaddr structure nor the **sockaddr\_in** structure is large enough to hold IPv6 addresses, and therefore both are insufficient if your application is to be IPv6 compatible.</span></span>

<span data-ttu-id="690d9-117">Tarea de codificación</span><span class="sxs-lookup"><span data-stu-id="690d9-117">Coding Task</span></span>

<span data-ttu-id="690d9-118">**Para modificar la base de código existente de IPv4 a IPv4 e IPv6: interoperabilidad**</span><span class="sxs-lookup"><span data-stu-id="690d9-118">**To modify your existing code base from IPv4 to IPv4- and IPv6-interoperability**</span></span>

1.  <span data-ttu-id="690d9-119">Adquiera la utilidad Checkv4.exe.</span><span class="sxs-lookup"><span data-stu-id="690d9-119">Acquire the Checkv4.exe utility.</span></span> <span data-ttu-id="690d9-120">La utilidad se incluye con el kit de desarrollo de software (SDK) de Microsoft Windows, que está disponible a través de su suscripción a MSDN o desde la web como descarga.</span><span class="sxs-lookup"><span data-stu-id="690d9-120">The utility is included with the Microsoft Windows Software Development Kit (SDK) which is made available through your MSDN subscription, or from the web as a download.</span></span>
2.  <span data-ttu-id="690d9-121">Ejecute la utilidad Checkv4.exe en el código.</span><span class="sxs-lookup"><span data-stu-id="690d9-121">Run the Checkv4.exe utility against your code.</span></span> <span data-ttu-id="690d9-122">Obtenga información acerca de cómo ejecutar la utilidad Checkv4.exe en los archivos de la sección sobre [el uso de la utilidad Checkv4.exe](using-the-checkv4-exe-utility-2.md).</span><span class="sxs-lookup"><span data-stu-id="690d9-122">Learn about how to run the Checkv4.exe utility against your files in the section on [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md).</span></span>
3.  <span data-ttu-id="690d9-123">La utilidad le alerta sobre el uso de **sockaddr** o **sockaddr \_ en** las estructuras y proporciona recomendaciones sobre cómo reemplazar con el [**\_ almacenamiento sockaddr**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85))de la estructura compatible con IPv6.</span><span class="sxs-lookup"><span data-stu-id="690d9-123">The utility alerts you to usage of **sockaddr** or **sockaddr\_in** structures, and provides recommendations on how to replace either with the IPv6 compatible structure [**SOCKADDR\_STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)).</span></span>
4.  <span data-ttu-id="690d9-124">Reemplace todas las instancias de este tipo, y el código asociado, según corresponda, para utilizar la estructura de **\_ almacenamiento de SOCKADDR** .</span><span class="sxs-lookup"><span data-stu-id="690d9-124">Replace any such instances, and associated code as appropriate, to use the **SOCKADDR\_STORAGE** structure.</span></span>

<span data-ttu-id="690d9-125">Como alternativa, puede buscar en el código base las instancias de **sockaddr** y **sockaddr \_ en** las estructuras y cambiar todo el uso (y otro código asociado, según corresponda) a la estructura de **\_ almacenamiento sockaddr** .</span><span class="sxs-lookup"><span data-stu-id="690d9-125">Alternatively, you can search your code base for instances of the **sockaddr** and **sockaddr\_in** structures, and change all such usage (and other associated code, as appropriate) to the **SOCKADDR\_STORAGE** structure.</span></span>

> [!Note]  
> <span data-ttu-id="690d9-126">Las estructuras de **\_ almacenamiento** **addrinfo** y SOCKADDR incluyen los miembros de la familia de protocolos y direcciones (familia **AI \_** y **\_ familia SS**), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="690d9-126">The **addrinfo** and **SOCKADDR\_STORAGE** structures include protocol and address family members (**ai\_family** and **ss\_family**), respectively.</span></span> <span data-ttu-id="690d9-127">RFC 2553 especifica el miembro de la **\_ familia de AI** de [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) como int, mientras que la **\_ familia SS** se especifica como un valor corto; como tal, una copia directa entre esos miembros produce un error del compilador.</span><span class="sxs-lookup"><span data-stu-id="690d9-127">RFC 2553 specifies the **ai\_family** member of [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) as an int, while **ss\_family** is specified as a short; as such, a direct copy between those members results in a compiler error.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="690d9-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="690d9-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="690d9-129">Guía de IPv6 para aplicaciones de Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="690d9-129">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="690d9-130">Sockets de doble pila para aplicaciones Winsock de IPv6</span><span class="sxs-lookup"><span data-stu-id="690d9-130">Dual-Stack Sockets for IPv6 Winsock Applications</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="690d9-131">Llamadas de función para aplicaciones Winsock de IPv6</span><span class="sxs-lookup"><span data-stu-id="690d9-131">Function Calls for IPv6 Winsock Applications</span></span>](function-calls-2.md)
</dt> <dt>

[<span data-ttu-id="690d9-132">Uso de direcciones IPv4 codificadas</span><span class="sxs-lookup"><span data-stu-id="690d9-132">Use of Hardcoded IPv4 Addresses</span></span>](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="690d9-133">Problemas de la interfaz de usuario para las aplicaciones Winsock de IPv6</span><span class="sxs-lookup"><span data-stu-id="690d9-133">User Interface Issues for IPv6 Winsock Applications</span></span>](user-interface-issues-2.md)
</dt> <dt>

[<span data-ttu-id="690d9-134">Protocolos subyacentes para aplicaciones Winsock de IPv6</span><span class="sxs-lookup"><span data-stu-id="690d9-134">Underlying Protocols for IPv6 Winsock Applications</span></span>](underlying-protocols-2.md)
</dt> </dl>

 

 
