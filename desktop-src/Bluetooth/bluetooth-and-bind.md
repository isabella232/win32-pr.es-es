---
title: Bluetooth y BIND
description: Bluetooth utiliza la función de enlace para enlazar con un socket.
ms.assetid: 308d2680-de51-49e6-a0da-7aba494d9572
keywords:
- bind
- Bluetooth
- Bluetooth
- Bluetooth y BIND
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12ccbd088ab61edcfa3dfc511ea591593d0cf781
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904798"
---
# <a name="bluetooth-and-bind"></a>Bluetooth y BIND

Bluetooth utiliza la función de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) para enlazar con un socket. Para enlazar un Socket Bluetooth, llame a la función **BIND** mediante la estructura [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) . Use la estructura **SOCKADDR \_ BTH** con la siguiente configuración:

``` syntax
name.addressFamily = AF_BTH;
name.btAddr = 0;
name.serviceClassId = GUID_NULL;
name.port = number of service channel, 0 or BT_PORT_ANY;
```

En las aplicaciones cliente, el miembro del puerto debe ser cero para permitir que se asigne un punto de conexión local adecuado. En las aplicaciones de servidor, el miembro del puerto debe ser un número de puerto o un puerto BT válido \_ \_ ; los puertos asignados automáticamente mediante \_ el puerto BT \_ Any se pueden consultar posteriormente con una llamada a la función [**getsockname**](bluetooth-and-getsockname.md) . El intervalo válido para solicitar un puerto RFCOMM específico es de 1 a 30. Los canales de servidor son recursos globales y solo hay 30 canales de servidor disponibles para RFCOMM en cualquier dispositivo Bluetooth, que deben ser compartidos por todos los Windows Sockets que pertenecen a la familia de direcciones de Bluetooth. Si no hay ningún canal de servidor disponible, o si el canal de servidor especificado ya está reservado, se produce un error en la llamada de [**enlace**](/windows/desktop/api/winsock/nf-winsock-bind) .

Cuando se devuelve correctamente de BIND, el canal de servidor se reserva hasta que se cierra el socket. Use la función [**getsockname**](bluetooth-and-getsockname.md) para recuperar el número de canal para el registro de SDP.

Las aplicaciones deben usar la asignación automática para el canal del servidor.

La función [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) no anuncia automáticamente la aplicación de servidor mediante el SDP de Bluetooth; las aplicaciones deben llamar a la función [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) para que las aplicaciones Bluetooth remotas las encuentren.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**volver**](/windows/desktop/api/winsock/nf-winsock-bind)
</dt> </dl>

 

 