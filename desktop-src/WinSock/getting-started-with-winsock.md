---
description: A continuación se muestra una guía paso a paso para empezar a trabajar con la Windows Sockets.
ms.assetid: 905cd5bc-44af-4d3f-841a-9e9a2700a785
title: Tareas iniciales con Winsock
ms.topic: article
ms.date: 09/10/2021
ms.openlocfilehash: c22a4f837506a4ed01de73fe5b9997df7868e127
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063981"
---
# <a name="getting-started-with-winsock"></a>Tareas iniciales con Winsock

A continuación se muestra una guía paso a paso para empezar a trabajar con la Windows Sockets. Está diseñado para proporcionar una comprensión de las funciones básicas de Winsock y las estructuras de datos, y cómo funcionan conjuntamente.

La aplicación cliente y servidor que se usa para la ilustración es un cliente y un servidor muy básicos. En los ejemplos incluidos con el Kit de desarrollo de software (SDK) de Microsoft Windows se incluyen ejemplos de código más avanzados.

Los primeros pasos son los mismos para las aplicaciones cliente y servidor.

- [Acerca de los servidores y clientes](about-clients-and-servers.md)
- [Creación de una aplicación Winsock básica](creating-a-basic-winsock-application.md)
- [Inicialización de Winsock](initializing-winsock.md)

En las secciones siguientes se describen los pasos restantes para crear una aplicación cliente winsock.

- [Crear un socket para el cliente](creating-a-socket-for-the-client.md)
- [Conexión a un socket](connecting-to-a-socket.md)
- [Envío y recepción de datos en el cliente](sending-and-receiving-data-on-the-client.md)
- [Desconectar el cliente](disconnecting-the-client.md)

En las secciones siguientes se describen los pasos restantes para crear una aplicación de servidor Winsock.

- [Crear un socket para el servidor](creating-a-socket-for-the-server.md)
- [Enlazar un socket](binding-a-socket.md)
- [Escuchar en un socket](listening-on-a-socket.md)
- [Aceptación de una conexión](accepting-a-connection.md)
- [Recepción y envío de datos en el servidor](receiving-and-sending-data-on-the-server.md)
- [Desconectar el servidor](disconnecting-the-server.md)

Código fuente completo de estos ejemplos básicos.

- [Ejecución del ejemplo de código de cliente y servidor de Winsock](finished-server-and-client-code.md)
- [Completar el código de cliente de Winsock](complete-client-code.md)
- [Completar el código del servidor Winsock](complete-server-code.md)

## <a name="advanced-winsock-samples"></a>Ejemplos avanzados de Winsock

Hay disponibles varios ejemplos más avanzados de cliente y servidor de Winsock [en GitHub](https://github.com/microsoft/Windows-classic-samples/tree/main/Samples/Win7Samples/netds/winsock). Se enumeran a continuación en orden de mayor a menor rendimiento y se encuentran en los directorios siguientes:

- iocp

    Este directorio contiene tres programas de ejemplo que usan puertos de finalización de E/S. Los programas incluyen un servidor Winsock (iocpserver) que usa la función [**WSAAccept,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) un servidor Winsock (iocpserverex) que usa la función [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) y un cliente Winsock multiproceso simple (iocpclient) que se usa para probar cualquiera de estos servidores. Los programas de servidor admiten varios clientes que se conectan a través de TCP/IP y envían búferes de datos de tamaño arbitrario que el servidor vuelve a hacer eco al cliente. Para mayor comodidad, se desarrolló un programa cliente simple, iocpclient, para conectarse y enviar continuamente datos al servidor para que se estrese mediante varios subprocesos. Los servidores Winsock que usan puertos de finalización de E/S proporcionan la mayor funcionalidad de rendimiento.

- Traslapo

    Este directorio contiene un programa de servidor de ejemplo que usa E/S superpuestas. El programa de ejemplo usa la [**función AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) y la E/S superpuesta para controlar varias solicitudes de conexión asincrónicas de los clientes de forma eficaz. El servidor usa la **función AcceptEx** para multiplexación de conexiones de cliente diferentes en una aplicación Win32 de un solo subproceso. El uso de E/S superpuesta permite una mayor escalabilidad.

- WSAPoll

    Este directorio contiene un programa de ejemplo básico que muestra el uso de la [**función WSAPoll.**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) El programa de cliente y servidor combinado no está bloqueado y usa la función **WSAPoll** para determinar cuándo es posible enviar o recibir sin bloqueo. Este ejemplo es más ilustrativos y no es un servidor de alto rendimiento.

- simple

    Este directorio contiene tres programas de ejemplo básicos que muestran el uso de varios subprocesos por parte de un servidor. Los programas incluyen un servidor TCP/UDP simple (simples), un servidor solo TCP (simple ioctl) que usa la función select en una aplicación de consola Win32 para admitir varias solicitudes de cliente y un programa \_ TCP/UDP [](/windows/desktop/api/Winsock2/nf-winsock2-select) (simplec) de cliente para probar los servidores. Los servidores muestran el uso de varios subprocesos para controlar varias solicitudes de cliente. Este método tiene problemas de escalabilidad, ya que se crea un subproceso independiente para cada solicitud de cliente.

- accept

    Este directorio contiene un servidor de ejemplo básico y un programa cliente. El servidor muestra el uso de la aceptación sin bloqueo mediante la [**función select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o la aceptación asincrónica mediante la [**función WSAAsyncSelect.**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) Este ejemplo es más ilustrativos y no es un servidor de alto rendimiento.
