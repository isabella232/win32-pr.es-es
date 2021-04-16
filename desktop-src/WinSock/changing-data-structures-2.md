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
# <a name="changing-data-structures-for-ipv6-winsock-appications"></a>Cambiar las estructuras de datos para IPv6 Winsock Appications

Al agregar compatibilidad con IPv6, debe asegurarse de que la aplicación define las estructuras de datos con el tamaño adecuado. El tamaño de una dirección IPv6 es mucho mayor que una dirección IPv4. Las estructuras que están codificadas de forma rígida para controlar el tamaño de una dirección IPv4 al almacenar una dirección IP provocarán problemas en la aplicación y se deben modificar.

Procedimiento recomendado

El mejor enfoque para asegurarse de que las estructuras tienen el tamaño correcto es usar la estructura de [**\_ almacenamiento de SOCKADDR**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) . La estructura de **\_ almacenamiento de SOCKADDR** es independiente de la versión de la dirección IP. Cuando la estructura de **\_ almacenamiento de SOCKADDR** se usa para almacenar direcciones IP, las direcciones IPv4 e IPv6 se pueden controlar correctamente con una base de código.

En el ejemplo siguiente, que es un extracto tomado del archivo Server. c que se encuentra en el Apéndice B, se identifica un uso adecuado de la estructura de **\_ almacenamiento de SOCKADDR** . Observe que la estructura, cuando se usa correctamente como se muestra en este ejemplo, controla correctamente una dirección IPv4 o IPv6.


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
> La estructura de [**\_ almacenamiento de SOCKADDR**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) es nueva en Windows XP.

 

Código que se debe evitar

Normalmente, muchas aplicaciones usan la estructura [**sockaddr**](sockaddr-2.md) para almacenar direcciones independientes del protocolo o la **sockaddr \_ en** la estructura de las direcciones IP. Ni la estructura sockaddr ni la **sockaddr \_ en** la estructura son lo suficientemente grandes como para contener las direcciones IPv6 y, por tanto, las dos son insuficientes si la aplicación va a ser compatible con IPv6.

Tarea de codificación

**Para modificar la base de código existente de IPv4 a IPv4 e IPv6: interoperabilidad**

1.  Adquiera la utilidad Checkv4.exe. La utilidad se incluye con el kit de desarrollo de software (SDK) de Microsoft Windows, que está disponible a través de su suscripción a MSDN o desde la web como descarga.
2.  Ejecute la utilidad Checkv4.exe en el código. Obtenga información acerca de cómo ejecutar la utilidad Checkv4.exe en los archivos de la sección sobre [el uso de la utilidad Checkv4.exe](using-the-checkv4-exe-utility-2.md).
3.  La utilidad le alerta sobre el uso de **sockaddr** o **sockaddr \_ en** las estructuras y proporciona recomendaciones sobre cómo reemplazar con el [**\_ almacenamiento sockaddr**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85))de la estructura compatible con IPv6.
4.  Reemplace todas las instancias de este tipo, y el código asociado, según corresponda, para utilizar la estructura de **\_ almacenamiento de SOCKADDR** .

Como alternativa, puede buscar en el código base las instancias de **sockaddr** y **sockaddr \_ en** las estructuras y cambiar todo el uso (y otro código asociado, según corresponda) a la estructura de **\_ almacenamiento sockaddr** .

> [!Note]  
> Las estructuras de **\_ almacenamiento** **addrinfo** y SOCKADDR incluyen los miembros de la familia de protocolos y direcciones (familia **AI \_** y **\_ familia SS**), respectivamente. RFC 2553 especifica el miembro de la **\_ familia de AI** de [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) como int, mientras que la **\_ familia SS** se especifica como un valor corto; como tal, una copia directa entre esos miembros produce un error del compilador.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de IPv6 para aplicaciones de Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Sockets de doble pila para aplicaciones Winsock de IPv6](dual-stack-sockets.md)
</dt> <dt>

[Llamadas de función para aplicaciones Winsock de IPv6](function-calls-2.md)
</dt> <dt>

[Uso de direcciones IPv4 codificadas](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Problemas de la interfaz de usuario para las aplicaciones Winsock de IPv6](user-interface-issues-2.md)
</dt> <dt>

[Protocolos subyacentes para aplicaciones Winsock de IPv6](underlying-protocols-2.md)
</dt> </dl>

 

 
