---
title: Bluetooth y aceptar
description: Bluetooth utiliza la función accept para habilitar los intentos de conexión entrantes en un socket.
ms.assetid: 79708118-2f70-4759-b5d6-cf5cfc33c27e
keywords:
- accept
- Bluetooth
- Bluetooth
- Bluetooth y aceptar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28dff84ec05429411614e64a08ab159a5ee134b6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974628"
---
# <a name="bluetooth-and-accept"></a>Bluetooth y aceptar

Bluetooth utiliza la [**función accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) para habilitar los intentos de conexión entrantes en un socket. El BTH ADDR de la aplicación cliente se obtiene al leer la Bluetooth específica del transporte de la \_ estructura [**sockaddr devuelta.**](/windows/desktop/WinSock/sockaddr-2) El uso de **la función accept** con Bluetooth tiene el formato siguiente:

-   El *parámetro addr* de la [**función accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) es un puntero opcional a un búfer que recibe la dirección de la entidad de conexión, como se conoce a la capa de comunicaciones. Puntero a una [**estructura SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) con la dirección Bluetooth dispositivo remoto.
-   El *parámetro addrlen* de la [**función accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) es un puntero opcional a un entero que contiene la longitud, en bytes, de addr. El entero debe ser mayor o igual que el valor de **sizeof** ([**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**Aceptar**](/windows/desktop/api/winsock2/nf-winsock2-accept)
</dt> </dl>

 

 