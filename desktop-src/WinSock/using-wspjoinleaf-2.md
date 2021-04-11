---
description: Como se mencionó anteriormente, se usa WSPJoinLeaf para unir un nodo hoja a una sesión multipoint.
ms.assetid: 03325f5e-4d4a-405b-b644-3d8c03435e17
title: Usar WSPJoinLeaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4426c0d22657b26dcc2217d856865d9ebe98db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275389"
---
# <a name="using-wspjoinleaf"></a>Usar WSPJoinLeaf

Como se mencionó anteriormente, se usa [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) para unir un nodo hoja a una sesión multipoint. **WSPJoinLeaf** tiene los mismos parámetros y semántica que [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) , salvo que devuelve un descriptor de socket (como en [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)) y tiene un parámetro *dwFlags* adicional. El parámetro *dwFlags* se usa para indicar si el socket actuará solo como remitente, solo como receptor o ambos. Solo se pueden usar Multipoint Sockets para los *parámetros de* entrada de esta función. Si el socket Multipoint está en el modo de no bloqueo, el descriptor de socket devuelto no se podrá usar hasta que se haya \_ recibido la indicación FD Connect correspondiente. Una aplicación raíz en una sesión Multipoint puede llamar a **WSPJoinLeaf** una o más veces para agregar un número de nodos hoja; sin embargo, puede que al menos una solicitud de conexión multipunto esté pendiente a la vez.

El descriptor de socket devuelto por [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) es diferente dependiendo de si el descriptor de *socket de entrada* es una raíz de c \_ o una hoja de c \_ . Cuando se usa con un \_ socket raíz de c, el parámetro de *nombre* designa un nodo de hoja determinado que se va a agregar y el descriptor de socket devuelto es un \_ socket hoja de c que corresponde al nodo hoja recién agregado. No está diseñado para su uso en el intercambio de datos multipunto, sino que se usa para recibir indicaciones de eventos de red (por ejemplo, \_ el cierre de FD) para la conexión que existe en la hoja de c determinada \_ . Algunas implementaciones de Multipoint también pueden permitir el uso de este socket para chats laterales entre la raíz y un nodo hoja individual. \_Se debe proporcionar una indicación de cierre FD para este socket si el nodo hoja correspondiente llama a [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) para quitarlo de la sesión de multipoint. Simétricamente, la invocación de **WSPCloseSocket** en el \_ socket hoja de c devuelto desde [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) hará que el socket del nodo hoja correspondiente obtenga la \_ notificación FD Close.

Cuando [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) se invoca con un socket de \_ hoja de c, el parámetro *Name* contiene la dirección de la aplicación raíz (para un esquema de control con raíz) o una sesión de Multipoint existente (esquema de control sin raíz) y el descriptor de sockets devuelto es el mismo que el descriptor de socket de entrada. En un esquema de control con raíz, el cliente raíz pondría su \_ socket raíz de c en el modo de escucha mediante una llamada a [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)). La notificación de aceptación de FD estándar \_ se entregará cuando el nodo hoja solicite unirse a la sesión de multipoint. El cliente raíz utiliza la función [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) habitual para admitir el nuevo nodo hoja. El valor devuelto de **WSPAccept** también es un \_ descriptor de socket de hoja de c como el devuelto por **WSPJoinLeaf**. Para dar cabida a esquemas Multipoint que permitan combinaciones iniciadas por raíz y iniciadas por hojas, es aceptable que un \_ socket raíz de c que ya esté en modo de escucha se use como entrada en **WSPJoinLeaf**.

Un cliente raíz MultiPoint es generalmente responsable del desmontaje ordenado de una sesión multipoint. Este tipo de aplicación puede usar [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) o [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) en un \_ socket raíz de c para producir todos los sockets de hoja de c asociados \_ , incluidos los devueltos desde [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) y sus correspondientes \_ sockets de hoja de c en los nodos de hoja remotos, para obtener la notificación de tipo FD \_ .

 

 
