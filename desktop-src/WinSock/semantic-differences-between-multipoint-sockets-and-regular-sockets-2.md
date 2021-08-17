---
title: Diferencias semánticas entre sockets multipunto y sockets normales
description: Diferencias entre los \_ sockets multipunto raíz de c y los sockets de punto a punto normales.
ms.assetid: fbadfde8-44dc-41ac-bd93-1a22c76ca321
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06b30ff05c72fc43bf3f4e731242d9f22a2236e9f6fd275c382b57fb05d094cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740815"
---
# <a name="semantic-differences-between-multipoint-sockets-and-regular-sockets"></a>Diferencias semánticas entre sockets multipunto y sockets normales

En el plano de control, hay algunas diferencias semánticas significativas entre un socket raíz c y un socket punto \_ a punto normal:

-   El socket \_ raíz c se puede usar en [**WSAJoinLeaf para**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) unir una nueva hoja.
-   La colocación de un socket raíz de c en modo de escucha (mediante una llamada a listen) no impide que el socket raíz c se utilice en una llamada \_ [](/windows/desktop/api/Winsock2/nf-winsock2-listen) \_ a [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) para agregar una hoja nueva o para enviar y recibir datos de varios puntos.
-   El cierre de un socket raíz de c hace que todos \_ los sockets hoja c \_ asociados obtengan la notificación FD \_ CLOSE.

No hay diferencias semánticas entre un socket hoja de c y un socket normal en el plano de control, salvo que el socket hoja c se puede usar en \_ \_ [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)y el uso de c leaf socket en listen indica que solo se deben aceptar solicitudes de conexión \_ multipunto. [](/windows/desktop/api/Winsock2/nf-winsock2-listen)

En el plano de datos, las diferencias semánticas entre el socket raíz d y un socket de punto \_ a punto normal son:

-   Los datos enviados en el socket raíz d se entregan a \_ todas las hojas de la misma sesión multipunto.
-   Los datos recibidos en el socket raíz d \_ pueden ser de cualquiera de las hojas.

El socket hoja d del plano de datos raíz no tiene ninguna diferencia semántica con respecto al socket normal; sin embargo, en el plano de datos no raíz, los datos enviados en el socket hoja d van a todos los demás nodos hoja y los datos recibidos podrían ser de cualquier otro nodo \_ \_ hoja. Como se mencionó anteriormente, la información sobre si el socket hoja d está en un plano de datos raíz o no raíz se encuentra en la estructura info de \_ [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) correspondiente para el socket.

 

 
