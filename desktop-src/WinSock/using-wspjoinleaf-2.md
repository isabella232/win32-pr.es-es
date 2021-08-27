---
description: Como se mencionó anteriormente, WSPJoinLeaf se usa para unir un nodo hoja a una sesión de varios puntos.
ms.assetid: 03325f5e-4d4a-405b-b644-3d8c03435e17
title: Uso de WSPJoinLeaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 057be0e2c1f2c3ffec21d64f3e95f6ad0ee584698e66f57cf4489ff6be887dc5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121015"
---
# <a name="using-wspjoinleaf"></a>Uso de WSPJoinLeaf

Como se mencionó anteriormente, [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) se usa para unir un nodo hoja a una sesión de varios puntos. **WSPJoinLeaf** tiene los mismos parámetros y semántica que [**WSPConnect,**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) salvo que devuelve un descriptor de socket (como en [**WSPAccept)**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)y tiene un parámetro *dwFlags* adicional. El *parámetro dwFlags* se usa para indicar si el socket actuará solo como remitente, solo como receptor o ambos. Solo se pueden usar sockets multipunto para los parámetros *de entrada de* esta función. Si el socket multipunto está en modo de no bloqueo, el descriptor de socket devuelto no se podrá usar hasta después de que se haya recibido una indicación FD \_ CONNECT correspondiente. Una aplicación raíz en una sesión de varios puntos puede llamar a **WSPJoinLeaf** una o varias veces para agregar varios nodos hoja, pero como máximo una solicitud de conexión multipunto puede estar pendiente a la vez.

El descriptor de socket devuelto por [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) es diferente en función de si el descriptor de socket de entrada, *s*, es una raíz c \_ o una hoja \_ c. Cuando se usa con un socket raíz de c, el parámetro name designa un nodo hoja determinado que se va a agregar y el descriptor de socket devuelto es un socket hoja c correspondiente al nodo hoja recién \_  \_ agregado. No está pensado para usarse para el intercambio de datos de varios puntos, sino que se usa para recibir indicaciones de eventos de red (por ejemplo, FD CLOSE) para la conexión que existe con la hoja \_ c \_ concreta. Algunas implementaciones de varios puntos también pueden permitir que este socket se utilice para chats paralelos entre la raíz y un nodo hoja individual. Se debe dar una indicación FD CLOSE para este socket si el nodo hoja correspondiente llama a \_ [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) para salir de la sesión de varios puntos. Simétricamente, al invocar **WSPCloseSocket** en el socket hoja c devuelto desde \_ [**WSPJoinLeaf,**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) el socket del nodo hoja correspondiente recibirá la notificación FD \_ CLOSE.

Cuando se invoca [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) con un socket hoja c, el parámetro name contiene la dirección de la aplicación raíz (para un esquema de control raíz) o una sesión multipunto existente (esquema de control no raíz) y el descriptor de socket devuelto es el mismo que el descriptor de socket de \_ entrada.  En un esquema de control con raíz, el cliente raíz colocaría su socket raíz c en el modo de escucha llamando a \_ [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)). La notificación ESTÁNDAR DE ACEPTACIÓN de FD se entregará cuando el nodo hoja solicite \_ unirse a la sesión multipunto. El cliente raíz usa la función [**WSPAccept habitual**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) para admitir el nuevo nodo hoja. El valor devuelto de **WSPAccept también** es un descriptor de socket hoja c igual que los devueltos \_ de **WSPJoinLeaf**. Para dar cabida a esquemas de varios puntos que permiten combinaciones iniciadas por raíz y iniciadas por hoja, es aceptable que un socket raíz de c que ya está en modo de escucha se utilice como en la entrada de \_ **WSPJoinLeaf**.

Por lo general, un cliente raíz multipunto es responsable de la organización de una sesión multipunto. Esta aplicación puede usar [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) o [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) en un socket raíz de c para hacer que todos los sockets hoja \_ c \_ asociados, incluidos los devueltos desde [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) y sus sockets hoja c correspondientes en los nodos hoja remotos, obtengan la notificación \_ FD \_ CLOSE.

 

 
