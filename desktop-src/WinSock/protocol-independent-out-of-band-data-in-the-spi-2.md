---
description: Los datos fuera de banda (OOB) son un canal de transmisión independiente lógicamente asociado a un par de sockets de flujo conectados.
ms.assetid: 30f667cd-5be9-45f2-9d55-bff04834078f
title: Datos de salida de banda independientes del protocolo en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a55e186e34e401e56017097271d5f036f2666bdc51f8bc27c6692be7e12874e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993615"
---
# <a name="protocol-independentout-of-band-data-in-the-spi"></a>Datos de salida de banda independientes del protocolo en el SPI

Los datos fuera de banda (OOB) son un canal de transmisión independiente lógicamente asociado a un par de sockets de flujo conectados. Los datos de OOB se pueden entregar al usuario independientemente de los datos normales. La abstracción define que las instalaciones de datos de OOB deben admitir la entrega confiable de al menos un bloque de datos OOB a la vez. Este bloque de datos puede contener al menos un byte de datos y al menos un bloque de datos OOB puede estar pendiente de entrega al usuario en cualquier momento. En el caso de los protocolos de comunicaciones que admiten la señalización en banda (es decir, TCP, donde los datos urgentes se entregan en secuencia con los datos normales), el sistema normalmente extrae los datos OOB del flujo de datos normal y los almacena por separado (dejando un hueco en el flujo de datos normal). Esto permite a los usuarios elegir entre recibir los datos de OOB en orden y recibirlos fuera de la secuencia sin tener que almacenar en búfer todos los datos intermedios. Es posible ver los datos de OOB.

Un usuario puede determinar si hay algún dato de OOB en espera de lectura mediante la [**función WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) (SIOCATMARK). Para los protocolos en los que el concepto de la posición del bloque de datos OOB dentro del flujo de datos normal es significativo (es decir, TCP), un proveedor de servicios Windows Sockets mantendrá un marcador conceptual que indica la posición del último byte de los datos OOB dentro del flujo de datos normal. Esto no es necesario para la implementación de la funcionalidad **WSPIoctl** (SIOCATMARK): la presencia o ausencia de datos de OOB es todo lo que se requiere.

Para los protocolos en los que el concepto de la posición del bloque de datos OOB dentro del flujo de datos normal es significativo, una aplicación puede preferir procesar datos fuera de banda en línea, como parte del flujo de datos normal. Esto se logra estableciendo la opción de socket SO \_ OOBINLINE (consulte la [**sección WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))). Para otros protocolos en los que los bloques de datos OOB son realmente independientes del flujo de datos normal, si se intenta establecer SO \_ OOBINLINE, se producirá un error. Una aplicación puede usar el comando SIOCATMARK WSPIoctl para determinar si hay datos OOB no leídos antes de la marca. Por ejemplo, podría usarlo para resincronizar con su par asegurándose de que todos los datos hasta la marca del flujo de datos se descartan cuando corresponda.

Con SO \_ OOBINLINE deshabilitado (de forma predeterminada):

-   El proveedor de servicios Winsock notifica a un cliente un evento OOB de FD, si el cliente se registró para la notificación con \_ [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)), exactamente de la misma manera que se usa FD READ para notificar la presencia de datos \_ normales. Es decir, fd OOB se publica cuando llegan los datos de OOB y no había datos de OOB previamente en cola, y también cuando los datos se leen mediante la marca MSG OOB, y algunos datos de OOB permanecen para leerse después de que se haya devuelto la operación de \_ \_ lectura. Los \_ mensajes READ de FD no se publican para los datos de OOB.
-   El proveedor de servicios Winsock devuelve de [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) con el conjunto de *sockets exceptfds* adecuado si los datos de OOB se ponen en cola en el socket.
-   El cliente puede llamar a [**WSPRecv con**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) MSG \_ OOB para leer el bloque de datos urgente en cualquier momento. El bloque de datos OOB salta a la cola.
-   El cliente puede llamar a [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) sin MSG \_ OOB para leer el flujo de datos normal. El bloque de datos OOB no aparecerá en el flujo de datos con datos normales. Si los datos de OOB permanecen después de cualquier llamada a **WSPRecv**, el proveedor de servicios notifica al cliente con FD OOB o a través de \_ *exceptfds* cuando se usa [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)).
-   Para los protocolos en los que los datos de OOB tienen una posición dentro del flujo de datos normal, una sola [**operación WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) no abarcará esa posición. Un **WSPRecv** devolverá los datos normales antes de la marca y se requiere un segundo **WSPRecv** para empezar a leer los datos después de la marca.

Con SO \_ OOBINLINE habilitado:

-   Los mensajes fd OOB no se publican para los datos de OOB: para las funciones \_ [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) y [**WSPAsyncSelect,**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) los datos de OOB se tratan como datos normales y se indican estableciendo el socket en *readfds* o enviando un mensaje FD \_ READ respectivamente.
-   Es posible que el cliente no llame a [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) con la marca MSG OOB establecida para leer el bloque de datos OOB; se devolverá el código de \_ error WSAEINVAL.
-   El cliente puede llamar a [**WSPRecv sin**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) establecer la marca \_ MSG OOB. Los datos de OOB se entregarán en su orden correcto dentro del flujo de datos normal. Los datos de OOB nunca se mezclarán con datos normales; debe haber tres solicitudes de lectura para pasar los datos de OOB. El primero devuelve los datos normales antes del bloque de datos OOB, el segundo devuelve los datos de OOB y el tercero devuelve los datos normales después de los datos de OOB. En otras palabras, se conservan los límites del bloque de datos OOB.

La [**rutina WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) es especialmente adecuada para controlar la notificación de la presencia de datos de OOB cuando SO \_ OOBINLINE está desactivado.

 

 
