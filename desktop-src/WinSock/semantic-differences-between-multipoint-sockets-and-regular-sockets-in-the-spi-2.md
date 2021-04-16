---
description: Diferencias entre sockets de punto a punto normales y \_ sockets de Multipoint raíz de c en el SPI de Windows Sockets (Winsock).
ms.assetid: 5476933b-70f2-4dcf-a6e9-f9f4a537c29f
title: Diferencias semánticas entre los sockets multipoint y los sockets normales en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd9e4e94583ee653a8ec0bf19c743dddd3e16253
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706104"
---
# <a name="semantic-differences-between-multipoint-sockets-and-regular-sockets-in-the-spi"></a>Diferencias semánticas entre los sockets multipoint y los sockets normales en el SPI

En el plano de control, hay algunas diferencias semánticas significativas entre un \_ socket raíz de c y un socket punto a punto normal:

-   El \_ socket raíz de c se puede usar en [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) para unir una nueva hoja.
-   La colocación de un \_ socket raíz de c en el modo de escucha (llamando a [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))) no impide \_ que el socket raíz de c se use en una llamada a [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) para agregar una hoja nueva o para enviar y recibir datos de multipoint.
-   El cierre de un \_ socket raíz de c hará que todos los sockets de hoja de c asociados \_ obtengan la \_ notificación FD Close.

No hay diferencias semánticas entre un socket de hoja de c \_ y un socket normal en el plano de control, salvo que el \_ socket de hoja de c se puede usar en [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf), y el uso del socket de hoja de c \_ en [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) indica que solo se deben aceptar solicitudes de conexión multipunto.

En el plano de datos, las diferencias semánticas entre el \_ socket raíz d y un socket punto a punto normal son

-   Los datos enviados en el \_ socket raíz d se entregarán a todas las hojas de la misma sesión multipoint.
-   Los datos recibidos en el \_ socket raíz d pueden estar en cualquiera de las hojas.

El \_ socket de hoja d del plano de datos raíz no tiene ninguna diferencia semántica con respecto al socket normal; sin embargo, en el plano de datos no raíz, los datos enviados en el \_ socket de hoja d Irán a todos los demás nodos hoja, y los datos recibidos podrían ser de cualquier otro nodo hoja. Como se mencionó anteriormente, la información sobre si el \_ socket de hoja d está en un plano de datos raíz o no raíz se encuentra en la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondiente para el socket.

 

 
