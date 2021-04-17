---
title: Diferencias semánticas entre Multipoint sockets y Sockets normales
description: Diferencias entre los \_ sockets de Multipoint raíz de c y los sockets de punto a punto normales.
ms.assetid: fbadfde8-44dc-41ac-bd93-1a22c76ca321
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04d95b2637a4f805cea5ee6f138cc6992080a238
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706184"
---
# <a name="semantic-differences-between-multipoint-sockets-and-regular-sockets"></a>Diferencias semánticas entre Multipoint sockets y Sockets normales

En el plano de control, hay algunas diferencias semánticas significativas entre un \_ socket raíz de c y un socket punto a punto normal:

-   El \_ socket raíz de c se puede usar en [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) para combinar una nueva hoja.
-   La colocación de un \_ socket raíz de c en el modo de escucha (mediante una llamada a [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen)) no impide \_ que el socket raíz de c se use en una llamada a [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) para agregar una hoja nueva o para enviar y recibir datos de multipoint.
-   El cierre de un \_ socket raíz de c hace que todos los sockets de hoja de c asociados \_ obtengan una notificación de proximidad de FD \_ .

No hay diferencias semánticas entre un socket de hoja de c \_ y un socket normal en el plano de control, salvo que el \_ socket de hoja de c se puede usar en [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)y el uso de \_ sockets de hoja de c en la [**escucha**](/windows/desktop/api/Winsock2/nf-winsock2-listen) indica que solo se deben aceptar solicitudes de conexión multipunto.

En el plano de datos, las diferencias semánticas entre el \_ socket raíz d y un socket punto a punto normal son:

-   Los datos enviados en el \_ socket raíz d se entregan a todas las hojas de la misma sesión multipoint.
-   Los datos recibidos en el \_ socket raíz d pueden estar en cualquiera de las hojas.

El \_ socket de hoja d del plano de datos raíz no tiene ninguna diferencia semántica con respecto al socket normal; sin embargo, en el plano de datos no raíz, los datos enviados en el \_ socket hoja d van a todos los demás nodos hoja, y los datos recibidos podrían ser de cualquier otro nodo hoja. Como se mencionó anteriormente, la información sobre si el \_ socket de hoja d está en un plano de datos raíz o no raíz se encuentra en la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondiente para el socket.

 

 
