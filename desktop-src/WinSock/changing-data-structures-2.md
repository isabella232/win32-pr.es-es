---
description: Al agregar compatibilidad con IPv6, debe asegurarse de que la aplicación define estructuras de datos con el tamaño correcto.
ms.assetid: 2bf353e2-38d5-462c-9e6c-65886b617215
title: Cambio de estructuras de datos para aplicaciones Winsock de IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2999c0d0c5a335c1367165c227fc1aad805579db5a790a19d316a1624e922947
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741555"
---
# <a name="changing-data-structures-for-ipv6-winsock-appications"></a>Cambio de estructuras de datos para aplicaciones Winsock de IPv6

Al agregar compatibilidad con IPv6, debe asegurarse de que la aplicación define estructuras de datos con el tamaño correcto. El tamaño de una dirección IPv6 es mucho mayor que una dirección IPv4. Las estructuras codificadas de forma segura para controlar el tamaño de una dirección IPv4 al almacenar una dirección IP provocarán problemas en la aplicación y se deben modificar.

Procedimiento recomendado

El mejor enfoque para asegurarse de que las estructuras tienen el tamaño correcto es usar la estructura [**DE ALMACENAMIENTO \_ SOCKADDR.**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) La **estructura SOCKADDR \_ STORAGE** es independiente de la versión de la dirección IP. Cuando se usa la estructura **SOCKADDR \_ STORAGE** para almacenar direcciones IP, las direcciones IPv4 e IPv6 se pueden controlar correctamente con una base de código.

En el ejemplo siguiente, que es un extracto tomado del archivo Server.c que se encuentra en el Apéndice B, se identifica un uso adecuado de la estructura DE ALMACENAMIENTO **DE SOCKADDR. \_** Observe que la estructura, cuando se usa correctamente como se muestra en este ejemplo, controla correctamente una dirección IPv4 o IPv6.


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
> La [**estructura SOCKADDR \_ STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) es nueva para Windows XP.

 

Código que se debe evitar

Normalmente, muchas aplicaciones usaban la estructura [**sockaddr**](sockaddr-2.md) para almacenar direcciones independientes del protocolo o **el sockaddr \_** en la estructura de las direcciones IP. Ni la estructura sockaddr ni la estructura **sockaddr \_** en la estructura son lo suficientemente grandes como para contener direcciones IPv6 y, por tanto, ambas son insuficientes si la aplicación va a ser compatible con IPv6.

Tarea De codificación

**Para modificar la base de código existente de IPv4 a interoperabilidad IPv4 e IPv6**

1.  Adquiera la utilidad Checkv4.exe. La utilidad se incluye con el Kit de desarrollo de software (SDK) de Microsoft Windows, que está disponible a través de su suscripción a MSDN o desde la web como descarga.
2.  Ejecute la utilidad Checkv4.exe en el código. Obtenga información sobre cómo ejecutar la utilidad Checkv4.exe en los archivos en la sección Uso de [la utilidad Checkv4.exe .](using-the-checkv4-exe-utility-2.md)
3.  La utilidad le avisa del uso de **sockaddr** o **sockaddr \_** en estructuras y proporciona recomendaciones sobre cómo reemplazar por la estructura compatible con IPv6 [**SOCKADDR \_ STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)).
4.  Reemplace estas instancias y el código asociado según corresponda para usar la estructura **SOCKADDR \_ STORAGE.**

Como alternativa, puede buscar en la base de código instancias de **sockaddr** y **sockaddr \_** en estructuras, y cambiar todo ese uso (y otro código asociado, según corresponda) a la estructura **SOCKADDR \_ STORAGE.**

> [!Note]  
> Las **estructuras addrinfo** y **SOCKADDR \_ STORAGE** incluyen los miembros de la familia de protocolos y direcciones **(familia ai \_** y **ss \_**), respectivamente. RFC 2553 especifica el miembro de la familia **\_ ai** de [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) como int, mientras que la familia **\_ ss** se especifica como una corta; por lo tanto, una copia directa entre esos miembros produce un error del compilador.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de IPv6 para Windows sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Sockets de pila doble para aplicaciones Winsock IPv6](dual-stack-sockets.md)
</dt> <dt>

[Llamadas de función para aplicaciones IPv6 Winsock](function-calls-2.md)
</dt> <dt>

[Uso de direcciones IPv4 codificadas de forma rígida](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Interfaz de usuario problemas de aplicaciones IPv6 Winsock](user-interface-issues-2.md)
</dt> <dt>

[Protocolos subyacentes para aplicaciones IPv6 Winsock](underlying-protocols-2.md)
</dt> </dl>

 

 
