---
description: A continuación se proporciona una guía paso a paso para empezar a trabajar con la programación de Windows Sockets.
ms.assetid: 905cd5bc-44af-4d3f-841a-9e9a2700a785
title: Introducción con Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43751663a637fafb2eec453a48c329ff8e4499f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696381"
---
# <a name="getting-started-with-winsock"></a>Introducción con Winsock

A continuación se proporciona una guía paso a paso para empezar a trabajar con la programación de Windows Sockets. Está diseñado para proporcionar una descripción de las funciones básicas de Winsock y las estructuras de datos, y de cómo funcionan en conjunto.

La aplicación de cliente y servidor que se usa para la ilustración es un cliente y un servidor muy básicos. En los ejemplos incluidos en el kit de desarrollo de software (SDK) de Microsoft Windows se incluyen ejemplos de código más avanzados.

Los primeros pasos son los mismos para las aplicaciones de cliente y de servidor.

-   [Acerca de los servidores y clientes](about-clients-and-servers.md)
-   [Crear una aplicación de Winsock básica](creating-a-basic-winsock-application.md)
-   [Inicializando Winsock](initializing-winsock.md)

En las secciones siguientes se describen los pasos restantes para crear una aplicación cliente Winsock.

-   [Crear un socket para el cliente](creating-a-socket-for-the-client.md)
-   [Conexión a un socket](connecting-to-a-socket.md)
-   [Enviar y recibir datos en el cliente](sending-and-receiving-data-on-the-client.md)
-   [Desconectar el cliente](disconnecting-the-client.md)

En las secciones siguientes se describen los pasos restantes para crear una aplicación de servidor Winsock.

-   [Crear un socket para el servidor](creating-a-socket-for-the-server.md)
-   [Enlazar un socket](binding-a-socket.md)
-   [Escuchar en un socket](listening-on-a-socket.md)
-   [Aceptación de una conexión](accepting-a-connection.md)
-   [Recibir y enviar datos en el servidor](receiving-and-sending-data-on-the-server.md)
-   [Desconectar el servidor](disconnecting-the-server.md)

Código fuente completo de estos ejemplos básicos.

-   [Ejecución del ejemplo de código de servidor y cliente Winsock](finished-server-and-client-code.md)
-   [Completar el código de cliente Winsock](complete-client-code.md)
-   [Completar el código del servidor Winsock](complete-server-code.md)

## <a name="advanced-winsock-samples"></a>Ejemplos avanzados de Winsock

En el Windows SDK se incluyen varios ejemplos de servidor y cliente Winsock más avanzados. De forma predeterminada, el código fuente de ejemplo de Winsock se instala en el directorio siguiente mediante el Windows SDK para Windows 7:

*C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ NetDs \\ Winsock*

En versiones anteriores del Windows SDK, el número de versión de la ruta de acceso anterior cambiaría. Por ejemplo, el código fuente del ejemplo Winsock se instala en el directorio predeterminado siguiente mediante el Windows SDK para Windows Vista

*C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ v 6.0 \\ Samples \\ NetDs \\ Winsock*

Los ejemplos más avanzados que se enumeran a continuación en orden de mayor a menor rendimiento se encuentran en los siguientes directorios:

-   IOCP

    Este directorio contiene tres programas de ejemplo que usan puertos de finalización de e/s. Los programas incluyen un servidor Winsock (iocpserver) que usa la función [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) , un servidor Winsock (iocpserverex) que usa la función [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) y un cliente Winsock simple multiproceso (iocpclient) que se usa para probar cualquiera de estos servidores. Los programas de servidor admiten la conexión de varios clientes a través de TCP/IP y el envío de búferes de datos de tamaño arbitrario que el servidor devuelve al cliente. Para mayor comodidad, se desarrolló un sencillo programa cliente, iocpclient, para conectarse y enviar datos continuamente al servidor para recargarlos con varios subprocesos. Los servidores Winsock que usan puertos de finalización de e/s proporcionan la mayor capacidad de rendimiento.

-   superpone

    Este directorio contiene un programa de servidor de ejemplo que usa e/s superpuesta. El programa de ejemplo utiliza la función [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) y la e/s superpuesta para controlar de forma eficaz varias solicitudes de conexión asincrónica de clientes. El servidor utiliza la función **AcceptEx** para multiplexar diferentes conexiones de cliente en una aplicación Win32 de un solo subproceso. El uso de e/s superpuestas permite una mayor escalabilidad.

-   WSAPoll

    Este directorio contiene un programa de ejemplo básico que muestra el uso de la función [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) . El programa de cliente y de servidor combinado no es de bloqueo y usa la función **WSAPoll** para determinar cuándo es posible enviar o recibir sin bloqueos. Este ejemplo es más para la ilustración y no es un servidor de alto rendimiento.

-   simple

    Este directorio contiene tres programas de ejemplo básicos que muestran el uso de varios subprocesos por un servidor. Los programas incluyen un servidor TCP/UDP simple (simple), un servidor solo TCP ( \_ ioctl sencillo) que usa la función [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) en una aplicación de consola Win32 para admitir varias solicitudes de cliente y un programa TCP/UDP de cliente (simplec) para probar los servidores. Los servidores muestran el uso de varios subprocesos para administrar varias solicitudes de cliente. Este método tiene problemas de escalabilidad, ya que se crea un subproceso independiente para cada solicitud de cliente.

-   accept

    Este directorio contiene un programa de cliente y un servidor de ejemplo básico. El servidor muestra el uso de una aceptación sin bloqueo mediante la función [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o la aceptación asincrónica mediante la función [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) . Este ejemplo es más para la ilustración y no es un servidor de alto rendimiento.

 

 
