---
description: Windows Sockets (Winsock) y funcionalidades multipunto y multidifusión independientes del protocolo de transportes.
ms.assetid: 861f457c-fe7e-4128-a3f3-786424a96ea5
title: Protocol-Independent multidifusión y multipunto en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f6e7176d9b64ac8c7ef339ee82b8252e2a0d466dd8709fa008363ec3ef954e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993625"
---
# <a name="protocol-independent-multicast-and-multipoint-in-the-spi"></a>Protocol-Independent multidifusión y multipunto en el SPI

Al igual que Windows Sockets 2 permite el acceso genérico a las funcionalidades básicas de transporte de datos de numerosos protocolos de transporte, también proporciona una manera genérica de usar funcionalidades multipunto y multidifusión de transportes que implementan estas características. Para simplificar, el término *multipunto* se usa más adelante para hacer referencia a las comunicaciones multipunto y multipunto.

Las implementaciones actuales de varios puntos (por ejemplo, multidifusión IP, ST-II, T.120, ATM UNI) varían ampliamente con respecto a cómo los nodos se unen a una sesión de varios puntos, si un nodo determinado se designa como nodo central o raíz, y si los datos se intercambian entre todos los nodos o solo entre un nodo raíz y varios nodos hoja. La Windows info de [**WSAPROTOCOL \_ de Sockets**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 2 se usa para declarar los atributos multipunto de un protocolo. Mediante el examen de estos atributos, el programador sabrá qué convenciones seguir en el uso de las funciones de Winsock aplicables para configurar, usar y desmontar sesiones de varios puntos.

Las características de Windows Sockets 2 que admiten multidifusión se pueden resumir de la siguiente manera:

-   Tres bits de atributo en la [**estructura INFO de WSAPROTOCOL. \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)
-   Cuatro marcas definidas para el *parámetro dwFlags* [**de WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)
-   Una función, [**WSPJoinLeaf,**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)para agregar nodos hoja a una sesión de varios puntos.
-   Dos [**códigos de comando WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) para controlar el bucle de bucles multipunto y establecer el ámbito de las transmisiones de multidifusión. (Este último corresponde al parámetro TTL o período de vida de multidifusión IP).

> [!Note]  
> La inclusión de estas características multipunto en Windows Sockets 2 no impide que un proveedor de servicios admita también una interfaz dependiente del protocolo existente, como las opciones de socket de deering para multidifusión IP.

 

 

 
