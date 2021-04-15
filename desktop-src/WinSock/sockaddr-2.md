---
description: La estructura sockaddr varía en función del protocolo seleccionado.
ms.assetid: d1392e1c-2b20-425a-8adf-38e665fb6275
title: sockaddr
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- sockaddr
api_type:
- NA
api_location: ''
ms.openlocfilehash: ccd4b98efc987630ab625e5c9788f0be16018e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715863"
---
# <a name="sockaddr"></a><span data-ttu-id="33d65-103">sockaddr</span><span class="sxs-lookup"><span data-stu-id="33d65-103">sockaddr</span></span>

<span data-ttu-id="33d65-104">La estructura sockaddr varía en función del protocolo seleccionado.</span><span class="sxs-lookup"><span data-stu-id="33d65-104">The sockaddr structure varies depending on the protocol selected.</span></span> <span data-ttu-id="33d65-105">Excepto en el caso del parámetro de la *\* \_ familia sin* , el contenido de sockaddr se expresa en el orden de bytes de la red.</span><span class="sxs-lookup"><span data-stu-id="33d65-105">Except for the *sin\*\_family* parameter, sockaddr contents are expressed in network byte order.</span></span>

<span data-ttu-id="33d65-106">Las funciones Winsock que usan sockaddr no se interpretan de forma estricta como punteros a una estructura sockaddr.</span><span class="sxs-lookup"><span data-stu-id="33d65-106">Winsock functions using sockaddr are not strictly interpreted to be pointers to a sockaddr structure.</span></span> <span data-ttu-id="33d65-107">La estructura se interpreta de manera diferente en el contexto de distintas familias de direcciones.</span><span class="sxs-lookup"><span data-stu-id="33d65-107">The structure is interpreted differently in the context of different address families.</span></span> <span data-ttu-id="33d65-108">Los únicos requisitos son que el primer **u \_ corto** es la familia de direcciones y el tamaño total del búfer de memoria en bytes es *namelen*.</span><span class="sxs-lookup"><span data-stu-id="33d65-108">The only requirements are that the first **u\_short** is the address family and the total size of the memory buffer in bytes is *namelen*.</span></span>

<span data-ttu-id="33d65-109">La estructura de [**\_ almacenamiento de SOCKADDR**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) también almacena información de la dirección del socket y la estructura es lo suficientemente grande como para almacenar la información de la dirección IPv4 o IPv6.</span><span class="sxs-lookup"><span data-stu-id="33d65-109">The [**SOCKADDR\_STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) structure also stores socket address information and the structure is sufficiently large to store IPv4 or IPv6 address information.</span></span> <span data-ttu-id="33d65-110">El uso de la estructura de **\_ almacenamiento de SOCKADDR** promueve la independencia de la familia de protocolos y de la versión del Protocolo, y simplifica el desarrollo.</span><span class="sxs-lookup"><span data-stu-id="33d65-110">The use of the **SOCKADDR\_STORAGE** structure promotes protocol-family and protocol-version independence, and simplifies development.</span></span> <span data-ttu-id="33d65-111">Se recomienda usar la estructura **de \_ almacenamiento SOCKADDR** en lugar de la estructura SOCKADDR.</span><span class="sxs-lookup"><span data-stu-id="33d65-111">It is recommended that the **SOCKADDR\_STORAGE** structure be used in place of the sockaddr structure.</span></span> <span data-ttu-id="33d65-112">La estructura de **\_ almacenamiento de SOCKADDR** se admite en Windows Server 2003 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="33d65-112">The **SOCKADDR\_STORAGE** structure is supported on Windows Server 2003 and later.</span></span>

<span data-ttu-id="33d65-113">La estructura sockaddr y sockaddr \_ en las estructuras siguientes se usan con IPv4.</span><span class="sxs-lookup"><span data-stu-id="33d65-113">The sockaddr structure and sockaddr\_in structures below are used with IPv4.</span></span> <span data-ttu-id="33d65-114">Otros protocolos usan estructuras similares.</span><span class="sxs-lookup"><span data-stu-id="33d65-114">Other protocols use similar structures.</span></span>

``` syntax
struct sockaddr {
        ushort  sa_family;
        char    sa_data[14];
};

struct sockaddr_in {
        short   sin_family;
        u_short sin_port;
        struct  in_addr sin_addr;
        char    sin_zero[8];
};
```

<span data-ttu-id="33d65-115">Las \_ siguientes estructuras sockaddr IN6 y sockaddr \_ IN6 \_ anteriores se utilizan con IPv6.</span><span class="sxs-lookup"><span data-stu-id="33d65-115">The sockaddr\_in6 and sockaddr\_in6\_old structures below are used with IPv6.</span></span>

``` syntax
struct sockaddr_in6 {
        short   sin6_family;
        u_short sin6_port;
        u_long  sin6_flowinfo;
        struct  in6_addr sin6_addr;
        u_long  sin6_scope_id;
};

typedef struct sockaddr_in6 SOCKADDR_IN6;
typedef struct sockaddr_in6 *PSOCKADDR_IN6;
typedef struct sockaddr_in6 FAR *LPSOCKADDR_IN6;


struct sockaddr_in6_old {
        short   sin6_family;        
        u_short sin6_port;          
        u_long  sin6_flowinfo;      
        struct  in6_addr sin6_addr;  
};
```

<span data-ttu-id="33d65-116">En el kit de desarrollo de software (SDK) de Microsoft Windows publicado para Windows Vista y versiones posteriores, **SOCKADDR** y **SOCKADDR \_ en** las etiquetas typedef se definen para SOCKADDR y SOCKADDR \_ en estructuras como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="33d65-116">On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, **SOCKADDR** and **SOCKADDR\_IN** typedef tags are defined for sockaddr and sockaddr\_in structures as follows:</span></span>

``` syntax
typedef struct sockaddr {
#if (_WIN32_WINNT < 0x0600)
    u_short sa_family;
#else 
    ADDRESS_FAMILY sa_family;
#endif //(_WIN32_WINNT < 0x0600)
    CHAR sa_data[14];
} SOCKADDR, *PSOCKADDR, FAR *LPSOCKADDR;


typedef struct sockaddr_in {
#if(_WIN32_WINNT < 0x0600)
    short   sin_family;    
#else //(_WIN32_WINNT < 0x0600)
    ADDRESS_FAMILY sin_family;
#endif //(_WIN32_WINNT < 0x0600)
    USHORT sin_port;
    IN_ADDR sin_addr;
    CHAR sin_zero[8];
} SOCKADDR_IN, *PSOCKADDR_IN;
```

<span data-ttu-id="33d65-117">En la Windows SDK publicada para Windows Vista y versiones posteriores, la organización de los archivos de encabezado ha cambiado y las estructuras sockaddr y sockaddr \_ de las estructuras se definen en el archivo de encabezado *Ws2def. h* , no en el archivo de encabezado *WinSock2. h* .</span><span class="sxs-lookup"><span data-stu-id="33d65-117">On the Windows SDK released for Windows Vista and later, the organization of header files has changed and the sockaddr and sockaddr\_in structures are defined in the *Ws2def.h* header file, not the *Winsock2.h* header file.</span></span> <span data-ttu-id="33d65-118">El archivo de encabezado *Ws2def. h* se incluye automáticamente en el archivo de encabezado *WinSock2. h* .</span><span class="sxs-lookup"><span data-stu-id="33d65-118">The *Ws2def.h* header file is automatically included by the *Winsock2.h* header file.</span></span> <span data-ttu-id="33d65-119">La \_ estructura sockaddr IN6 se define en el archivo de encabezado *Ws2ipdef. h* , no en el archivo de encabezado *Ws2tcpip. h* .</span><span class="sxs-lookup"><span data-stu-id="33d65-119">The sockaddr\_in6 structure is defined in the *Ws2ipdef.h* header file, not the *Ws2tcpip.h* header file.</span></span> <span data-ttu-id="33d65-120">El archivo de encabezado *Ws2ipdef. h* se incluye automáticamente en el archivo de encabezado *Ws2tcpip. h* .</span><span class="sxs-lookup"><span data-stu-id="33d65-120">The *Ws2ipdef.h* header file is automatically included by the *Ws2tcpip.h* header file.</span></span> <span data-ttu-id="33d65-121">Los archivos de encabezado *Ws2def. h* y *Ws2ipdef. h* nunca deben usarse directamente.</span><span class="sxs-lookup"><span data-stu-id="33d65-121">The *Ws2def.h* and *Ws2ipdef.h* header files should never be used directly.</span></span>

## <a name="example-code"></a><span data-ttu-id="33d65-122">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="33d65-122">Example Code</span></span>

<span data-ttu-id="33d65-123">En el siguiente ejemplo se muestra el uso de la estructura **sockaddr** .</span><span class="sxs-lookup"><span data-stu-id="33d65-123">The following example demonstrates the use of the **sockaddr** structure.</span></span>


```C++

// Declare variables
SOCKET ListenSocket;
struct sockaddr_in saServer;
hostent* localHost;
char* localIP;

// Create a listening socket
ListenSocket = socket(AF_INET, SOCK_STREAM, IPPROTO_TCP);

// Get the local host information
localHost = gethostbyname("");
localIP = inet_ntoa (*(struct in_addr *)*localHost->h_addr_list);

// Set up the sockaddr structure
saServer.sin_family = AF_INET;
saServer.sin_addr.s_addr = inet_addr(localIP);
saServer.sin_port = htons(5150);

// Bind the listening socket using the
// information in the sockaddr structure
bind( ListenSocket,(SOCKADDR*) &saServer, sizeof(saServer) );


```



## <a name="see-also"></a><span data-ttu-id="33d65-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="33d65-124">See Also</span></span>

<span data-ttu-id="33d65-125">[**almacenamiento de SOCKADDR \_**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="33d65-125">[**SOCKADDR\_STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85))</span></span>


 

 
