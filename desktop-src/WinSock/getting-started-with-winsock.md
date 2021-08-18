---
description: A continuación se muestra una guía paso a paso para empezar a trabajar con la programación Windows Sockets.
ms.assetid: 905cd5bc-44af-4d3f-841a-9e9a2700a785
title: Tareas iniciales con Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcce956d7dcb142e4a51ac3a461868dfa055acc9a2d1624b6a6dff5132f86ea7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132158"
---
# <a name="getting-started-with-winsock"></a>Tareas iniciales con Winsock

A continuación se muestra una guía paso a paso para empezar a trabajar con la programación Windows Sockets. Está diseñado para proporcionar una comprensión de las funciones y estructuras de datos básicas de Winsock, y cómo funcionan conjuntamente.

La aplicación cliente y servidor que se usa para ilustrar es un cliente y un servidor muy básicos. Se incluyen ejemplos de código más avanzados en los ejemplos incluidos con el Kit de desarrollo de software (SDK) de Microsoft Windows.

Los primeros pasos son los mismos para las aplicaciones cliente y servidor.

-   [Acerca de servidores y clientes](about-clients-and-servers.md)
-   [Creación de una aplicación Winsock básica](creating-a-basic-winsock-application.md)
-   [Inicialización de Winsock](initializing-winsock.md)

En las secciones siguientes se describen los pasos restantes para crear una aplicación cliente de Winsock.

-   [Crear un socket para el cliente](creating-a-socket-for-the-client.md)
-   [Conexión a un socket](connecting-to-a-socket.md)
-   [Envío y recepción de datos en el cliente](sending-and-receiving-data-on-the-client.md)
-   [Desconectar el cliente](disconnecting-the-client.md)

En las secciones siguientes se describen los pasos restantes para crear una aplicación de servidor Winsock.

-   [Crear un socket para el servidor](creating-a-socket-for-the-server.md)
-   [Enlazar un socket](binding-a-socket.md)
-   [Escuchar en un socket](listening-on-a-socket.md)
-   [Aceptación de una conexión](accepting-a-connection.md)
-   [Recepción y envío de datos en el servidor](receiving-and-sending-data-on-the-server.md)
-   [Desconectar el servidor](disconnecting-the-server.md)

El código fuente completo de estos ejemplos básicos.

-   [Ejecución del ejemplo de código de cliente y servidor de Winsock](finished-server-and-client-code.md)
-   [Completar el código de cliente de Winsock](complete-client-code.md)
-   [Completar el código del servidor Winsock](complete-server-code.md)

## <a name="advanced-winsock-samples"></a>Ejemplos avanzados de Winsock

Se incluyen varios ejemplos de cliente y servidor de Winsock más avanzados con Windows SDK. De forma predeterminada, el SDK de Windows para Windows 7 instala el código fuente de ejemplo de Winsock en el directorio siguiente:

*C: \\ Archivos de programa Sdk de Microsoft Windows \\ \\ \\ v7.0 \\ Samples \\ NetDs \\ winsock*

En versiones anteriores del SDK Windows, el número de versión de la ruta de acceso anterior cambiaría. Por ejemplo, el SDK de Windows para Windows Vista instala el código fuente de ejemplo de Winsock en el siguiente directorio predeterminado.

*C: \\ Archivos de programa sdk de Microsoft Windows \\ \\ \\ v6.0 \\ Samples \\ NetDs \\ winsock*

Los ejemplos más avanzados que se enumeran a continuación en orden de mayor a menor rendimiento se encuentran en los directorios siguientes:

-   iocp

    Este directorio contiene tres programas de ejemplo que usan puertos de finalización de E/S. Los programas incluyen un servidor Winsock (iocpserver) que usa la función [**WSAAccept,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) un servidor Winsock (iocpserverex) que usa la función [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) y un cliente Winsock multiproceso simple (iocpclient) que se usa para probar cualquiera de estos servidores. Los programas de servidor admiten varios clientes que se conectan a través de TCP/IP y envían búferes de datos de tamaño arbitrario que el servidor vuelve a devolver al cliente. Para mayor comodidad, se desarrolló un programa cliente simple, iocpclient, para conectarse y enviar continuamente datos al servidor para hacer que se estrese mediante varios subprocesos. Los servidores Winsock que usan puertos de finalización de E/S proporcionan la mayor funcionalidad de rendimiento.

-   Traslapo

    Este directorio contiene un programa de servidor de ejemplo que usa E/S superpuesta. El programa de ejemplo usa la [**función AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) y la E/S superpuesta para controlar varias solicitudes de conexión asincrónicas de los clientes de forma eficaz. El servidor usa la **función AcceptEx** para multiplexación de conexiones de cliente diferentes en una aplicación Win32 de un solo subproceso. El uso de E/S superpuesta permite una mayor escalabilidad.

-   WSAPoll

    Este directorio contiene un programa de ejemplo básico que muestra el uso de la [**función WSAPoll.**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) El programa combinado de cliente y servidor no bloquea y usa la función **WSAPoll** para determinar cuándo es posible enviar o recibir sin bloqueo. Este ejemplo es más ilustrativos y no es un servidor de alto rendimiento.

-   simple

    Este directorio contiene tres programas de ejemplo básicos que muestran el uso de varios subprocesos por parte de un servidor. Los programas incluyen un servidor TCP/UDP simple (simples), un servidor solo TCP (simple ioctl) que usa la función select en una aplicación de consola Win32 para admitir varias solicitudes de cliente y un programa \_ CLIENTE TCP/UDP [](/windows/desktop/api/Winsock2/nf-winsock2-select) (simplec) para probar los servidores. Los servidores muestran el uso de varios subprocesos para controlar varias solicitudes de cliente. Este método tiene problemas de escalabilidad, ya que se crea un subproceso independiente para cada solicitud de cliente.

-   accept

    Este directorio contiene un servidor de ejemplo básico y un programa cliente. El servidor muestra el uso de la aceptación sin bloqueo mediante la función [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o la aceptación asincrónica mediante la [**función WSAAsyncSelect.**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) Este ejemplo es más ilustrativos y no es un servidor de alto rendimiento.

 

 
