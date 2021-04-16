---
title: Bluetooth y aceptar
description: Bluetooth usa la función Accept para habilitar los intentos de conexión entrantes en un socket.
ms.assetid: 79708118-2f70-4759-b5d6-cf5cfc33c27e
keywords:
- accept
- Bluetooth
- Bluetooth
- Bluetooth y aceptar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28dff84ec05429411614e64a08ab159a5ee134b6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105656386"
---
# <a name="bluetooth-and-accept"></a>Bluetooth y aceptar

Bluetooth usa la función [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) para habilitar los intentos de conexión entrantes en un socket. La \_ Dirección BTH de la aplicación cliente se obtiene al leer la sección específica del transporte Bluetooth de la estructura [**sockaddr**](/windows/desktop/WinSock/sockaddr-2) devuelta. El uso de la función **Accept** con Bluetooth tiene el siguiente formato:

-   El parámetro *addr* de la función [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) es un puntero opcional a un búfer que recibe la dirección de la entidad de conexión, como se conoce en el nivel de comunicaciones. Se devuelve un puntero a una estructura de [**\_ BTH de SOCKADDR**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) con la dirección del dispositivo Bluetooth remoto.
-   El parámetro *addrlen* de la función [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) es un puntero opcional a un entero que contiene la longitud, en bytes, de addr. El entero debe ser mayor o igual que el valor de **sizeof** ([**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**acept**](/windows/desktop/api/winsock2/nf-winsock2-accept)
</dt> </dl>

 

 