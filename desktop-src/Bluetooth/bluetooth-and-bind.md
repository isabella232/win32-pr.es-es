---
title: Bluetooth y enlazar
description: Bluetooth utiliza la función bind para enlazar a un socket.
ms.assetid: 308d2680-de51-49e6-a0da-7aba494d9572
keywords:
- bind
- Bluetooth
- Bluetooth
- Bluetooth y enlazar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12ccbd088ab61edcfa3dfc511ea591593d0cf781
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974627"
---
# <a name="bluetooth-and-bind"></a>Bluetooth y enlazar

Bluetooth utiliza la [**función bind**](/windows/desktop/api/winsock/nf-winsock-bind) para enlazar a un socket. Para enlazar un Bluetooth socket, llame a la **función bind** mediante la [**estructura SOCKADDR \_ BTH.**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) Use la **estructura SOCKADDR \_ BTH** con la siguiente configuración:

``` syntax
name.addressFamily = AF_BTH;
name.btAddr = 0;
name.serviceClassId = GUID_NULL;
name.port = number of service channel, 0 or BT_PORT_ANY;
```

En las aplicaciones cliente, el miembro de puerto debe ser cero para permitir que se asigne un punto de conexión local adecuado. En las aplicaciones de servidor, el miembro de puerto debe ser un número de puerto válido o BT PORT ANY; los puertos asignados automáticamente mediante BT PORT ANY se pueden consultar posteriormente con una llamada a la función \_ \_ \_ \_ [**getsockname.**](bluetooth-and-getsockname.md) El intervalo válido para solicitar un puerto RFCOMM específico es de 1 a 30. Los canales de servidor son recursos globales y solo 30 canales de servidor están disponibles para RFCOMM en cualquier dispositivo Bluetooth, que deben compartir todos los sockets de Windows que pertenecen a la familia de direcciones Bluetooth. Si no hay ningún canal de servidor disponible o si el canal de servidor especificado ya está reservado, se produce un error en la [**llamada de**](/windows/desktop/api/winsock/nf-winsock-bind) enlace.

Tras la devolución correcta del enlace, el canal del servidor se reserva hasta que se cierra el socket. Use la [**función getsockname**](bluetooth-and-getsockname.md) para recuperar el número de canal para el registro de SDP.

Las aplicaciones deben usar la asignación automática para el canal del servidor.

La [**función bind**](/windows/desktop/api/winsock/nf-winsock-bind) no anuncia automáticamente la aplicación de servidor mediante el Bluetooth SDP; Las aplicaciones deben llamar a [**la función WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) para que la puedan encontrar las aplicaciones Bluetooth remotas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**Atar**](/windows/desktop/api/winsock/nf-winsock-bind)
</dt> </dl>

 

 