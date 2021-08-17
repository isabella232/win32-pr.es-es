---
description: Diferencias entre los sockets de punto a punto normales y los sockets multipunto raíz c en \_ el SPI Windows Sockets (Winsock).
ms.assetid: 5476933b-70f2-4dcf-a6e9-f9f4a537c29f
title: Diferencias semánticas entre sockets multipunto y sockets normales en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e585c335d7503d884d58e25b6fc0ad6dd0c0c3356064ebb1504898770d4b7b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740613"
---
# <a name="semantic-differences-between-multipoint-sockets-and-regular-sockets-in-the-spi"></a>Diferencias semánticas entre sockets multipunto y sockets normales en el SPI

En el plano de control, hay algunas diferencias semánticas significativas entre un socket raíz c y un socket de \_ punto a punto normal:

-   El socket raíz de c \_ se puede usar en [**WSPJoinLeaf para**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) unir una hoja nueva.
-   La colocación de un socket raíz de c en el modo de escucha (mediante una llamada a WSPListen) no impide que el socket raíz de c se utilice en una llamada \_ [](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) \_ a [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) para agregar una hoja nueva o para enviar y recibir datos de varios puntos.
-   El cierre de un socket raíz de c hará que todos \_ los sockets hoja de c \_ asociados obtengan una notificación FD \_ CLOSE.

No hay diferencias semánticas entre un socket hoja de c y un socket normal en el plano de control, salvo que el socket hoja c se puede usar en \_ \_ [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)y el uso de socket hoja c en \_ [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) indica que solo se deben aceptar solicitudes de conexión multipunto.

En el plano de datos, las diferencias semánticas entre el socket raíz d y un socket de punto \_ a punto normal son

-   Los datos enviados en el socket raíz d se entregarán a \_ todas las hojas de la misma sesión multipunto.
-   Los datos recibidos en el socket raíz d \_ pueden ser de cualquiera de las hojas.

El socket hoja d del plano de datos raíz no tiene ninguna diferencia semántica con respecto al socket normal; sin embargo, en el plano de datos no raíz, los datos enviados en el socket hoja d irán a todos los demás nodos hoja y los datos recibidos podrían ser de cualquiera de los demás nodos \_ \_ hoja. Como se mencionó anteriormente, la información sobre si el socket hoja d está en un plano de datos raíz o no raíz se encuentra en la estructura INFO de \_ [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondiente para el socket.

 

 
