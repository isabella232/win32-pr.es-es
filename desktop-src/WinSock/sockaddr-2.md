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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569397"
---
# <a name="sockaddr"></a>sockaddr

La estructura sockaddr varía en función del protocolo seleccionado. Excepto para el parámetro *de \* \_ familia sin,* el contenido de sockaddr se expresa en orden de bytes de red.

Las funciones de Winsock que usan sockaddr no se interpretan estrictamente como punteros a una estructura sockaddr. La estructura se interpreta de forma diferente en el contexto de distintas familias de direcciones. Los únicos requisitos son que la primera **u \_ short** sea la familia de direcciones y que el tamaño total del búfer de memoria en bytes *sea namelen.*

La [**estructura SOCKADDR \_ STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) también almacena información de direcciones de socket y la estructura es lo suficientemente grande como para almacenar información de direcciones IPv4 o IPv6. El uso de la **estructura DE ALMACENAMIENTO DE SOCKADDR \_** promueve la independencia de la familia de protocolos y la versión del protocolo, y simplifica el desarrollo. Se recomienda usar la **estructura SOCKADDR \_ STORAGE** en lugar de la estructura sockaddr. La **estructura SOCKADDR \_ STORAGE** se admite en Windows Server 2003 y versiones posteriores.

La estructura sockaddr y sockaddr en \_ las estructuras siguientes se usan con IPv4. Otros protocolos usan estructuras similares.

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

Las estructuras antiguas sockaddr \_ in6 y sockaddr en 6 se \_ usan con \_ IPv6.

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

En el Kit de desarrollo de software (SDK) de Microsoft Windows publicado para Windows Vista y versiones posteriores, las etiquetas de definición de tipo **SOCKADDR** y **SOCKADDR \_ IN** se definen para sockaddr y sockaddr en estructuras como se muestra a \_ continuación:

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

En el SDK de Windows publicado para Windows Vista y versiones posteriores, la organización de los archivos de encabezado ha cambiado y sockaddr y sockaddr en las estructuras se definen en el archivo de encabezado \_ *Ws2def.h,* no en el archivo de encabezado *Winsock2.h.* El archivo de encabezado *Winsock2.h* incluye automáticamente el archivo de encabezado *Ws2def.h.* La estructura sockaddr in6 se define en el archivo de encabezado \_ *Ws2ipdef.h,* no en el archivo de encabezado *Ws2tcpip.h.* El *archivo de encabezado Ws2tcpip.h* incluye automáticamente el archivo de encabezado *Ws2tcpip.h.* Los *archivos de encabezado Ws2def.h* y *Ws2ipdef.h* nunca deben usarse directamente.

## <a name="example-code"></a>Código de ejemplo

En el ejemplo siguiente se muestra el uso de la **estructura sockaddr.**


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



## <a name="see-also"></a>Consulte también

[**SOCKADDR \_ STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85))


 

 
