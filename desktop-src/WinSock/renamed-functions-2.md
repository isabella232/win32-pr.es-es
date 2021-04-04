---
description: En dos casos, era necesario cambiar el nombre de las funciones que se usan en los sockets de Berkeley para evitar conflictos con otras funciones de la API de Microsoft Windows.
ms.assetid: b53b1622-cba4-47e3-a371-b3186de6d61b
title: Funciones cuyo nombre ha cambiado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a8fd2af33bdeb74dd7a4c83fe535bae2a020530
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908573"
---
# <a name="renamed-functions"></a>Funciones cuyo nombre ha cambiado

En dos casos, era necesario cambiar el nombre de las funciones que se usan en los sockets de Berkeley para evitar conflictos con otras funciones de la API de Microsoft Windows.

## <a name="close-and-closesocket"></a>Close y closesocket

Los descriptores de archivo estándar representan los sockets en sockets de Berkeley, por lo que se puede usar la función **Close** para cerrar sockets, así como archivos normales. Aunque nada en Windows Sockets impide que una implementación use identificadores de archivos normales para identificar sockets, nada lo requiere. En Windows, los sockets deben cerrarse mediante la rutina [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) . EN Windows, el uso de la función **Close** para cerrar un socket es incorrecto y los efectos de hacerlo no están definidos por esta especificación.

## <a name="ioctl-and-ioctlsocketwsaioctl"></a>Ioctl y Ioctlsocket/WSAIoctl

Varios sistemas en tiempo de ejecución de lenguaje C usan el ioctl para fines no relacionados con Windows Sockets. Como consecuencia, la función [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) y la función [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) se definieron para controlar las funciones de socket realizadas por **ioctl** y **fcntl** en la distribución de software Berkeley.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket)
</dt> <dt>

[**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket)
</dt> <dt>

[Trasladar aplicaciones de socket a Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Consideraciones sobre la programación de Winsock](winsock-programming-considerations.md)
</dt> <dt>

[**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)
</dt> </dl>

 

 



