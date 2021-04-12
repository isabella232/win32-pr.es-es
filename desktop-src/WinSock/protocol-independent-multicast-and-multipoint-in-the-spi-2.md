---
description: Capacidades de multidifusión y multidifusión independientes del protocolo y de Windows Sockets (Winsock).
ms.assetid: 861f457c-fe7e-4128-a3f3-786424a96ea5
title: Protocol-Independent multidifusión y Multipoint en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bda9e5cab1b790a1e2d2c64c4451063a94dd8bc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156021"
---
# <a name="protocol-independent-multicast-and-multipoint-in-the-spi"></a>Protocol-Independent multidifusión y Multipoint en el SPI

Del mismo modo que Windows Sockets 2 permite tener acceso a las capacidades básicas de transporte de datos de numerosos protocolos de transporte de forma genérica, también proporciona una manera genérica de usar las capacidades multipoint y multidifusión de los transportes que implementan estas características. Para simplificar, el término *Multipoint* se usa en adelante para hacer referencia a las comunicaciones multidifusión y multipoint.

Las implementaciones de Multipoint actuales (por ejemplo, IP multicast, ST-II, T. 120, ATM UNI) varían en gran medida en lo que respecta al modo en que los nodos se unen a una sesión de Multipoint, si un nodo determinado se designa como nodo central o raíz y si los datos se intercambian entre todos los nodos o solo entre un nodo raíz y varios La estructura de [**\_ información WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) de Windows Sockets 2 se usa para declarar los atributos multipunto de un protocolo. Mediante el examen de estos atributos, el programador sabrá qué convenciones seguir en el uso de las funciones de Winsock aplicables para configurar, usar y anular las sesiones de multipoint.

Las características de Windows Sockets 2 que admiten la multidifusión se pueden resumir de la siguiente manera:

-   Tres bits de atributo en la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .
-   Cuatro marcas definidas para el parámetro *dwFlags* de [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)
-   Una función, [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf), para agregar nodos hoja en una sesión multipoint.
-   Dos códigos de comando [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) para controlar el bucle invertido multipunto y establecer el ámbito para las transmisiones de multidifusión. (Este último se corresponde con el parámetro TTL o período de vida de multidifusión IP).

> [!Note]  
> La inclusión de estas características Multipoint en Windows Sockets 2 no impide que un proveedor de servicios admita también una interfaz dependiente del Protocolo existente, como las opciones de socket Deering para multidifusión IP.

 

 

 
