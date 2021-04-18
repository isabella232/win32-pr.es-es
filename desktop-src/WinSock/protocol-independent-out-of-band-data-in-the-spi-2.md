---
description: Los datos fuera de banda (OOB) son un canal de transmisión independiente lógicamente asociado a un par de sockets de secuencias conectados.
ms.assetid: 30f667cd-5be9-45f2-9d55-bff04834078f
title: Datos de protocolo IndependentOut-of-Band en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b53e5c7c5c8c8ad7a5985ec101dd157370c5f32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541510"
---
# <a name="protocol-independentout-of-band-data-in-the-spi"></a>Datos de protocolo IndependentOut-of-Band en el SPI

Los datos fuera de banda (OOB) son un canal de transmisión independiente lógicamente asociado a un par de sockets de secuencias conectados. Los datos OOB se pueden entregar al usuario independientemente de los datos normales. La abstracción define que los servicios de datos OOB deben admitir la entrega confiable de al menos un bloque de datos OOB a la vez. Este bloque de datos puede contener al menos un byte de datos, y al menos un bloque de datos OOB puede estar pendiente de entrega al usuario en un momento dado. En el caso de los protocolos de comunicaciones que admiten la señalización en banda (es decir, TCP, donde los datos urgentes se entregan en secuencia con los datos normales), el sistema normalmente extrae los datos OOB del flujo de datos normal y los almacena por separado (quedando un hueco en el flujo de datos normal). Esto permite a los usuarios elegir entre recibir los datos OOB en orden y recibirlos fuera de secuencia sin tener que almacenar en búfer todos los datos que intervienen. Es posible inspeccionar los datos OOB.

Un usuario puede determinar si hay algún dato OOB en espera de ser leído mediante la función [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) (SIOCATMARK). En el caso de los protocolos en los que el concepto de la posición del bloque de datos OOB dentro del flujo de datos normal es significativo (es decir, TCP), un proveedor de servicios de Windows Sockets mantendrá un marcador conceptual que indica la posición del último byte de los datos OOB en el flujo de datos normal. Esto no es necesario para la implementación de la funcionalidad de **WSPIoctl** (SIOCATMARK): la presencia o ausencia de datos Oob es todo lo que se necesita.

En el caso de los protocolos en los que el concepto de la posición del bloque de datos OOB en el flujo de datos normal es significativo, es posible que una aplicación prefiera procesar los datos fuera de banda en línea, como parte del flujo de datos normal. Esto se consigue estableciendo la opción de socket de modo que \_ OOBINLINE (vea la sección [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))). En el caso de otros protocolos en los que los bloques de datos OOB son verdaderamente independientes del flujo de datos normal, si se intenta establecer el valor de OOBINLINE, se producirá \_ un error. Una aplicación puede usar el comando SIOCATMARK WSPIoctl para determinar si hay algún dato OOB de no lectura delante de la marca. Por ejemplo, podría utilizar esto para volver a sincronizar con su elemento del mismo nivel asegurándose de que todos los datos hasta la marca del flujo de datos se descartan cuando sea necesario.

Con SO \_ OOBINLINE deshabilitado (de forma predeterminada):

-   El proveedor de servicios Winsock notifica a un cliente de un \_ evento FD OOB, si el cliente se ha registrado para recibir notificaciones con [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)), exactamente de la misma manera \_ que se usa FD Read para notificar la presencia de datos normales. Es decir, \_ se publica FD OOB cuando llegan los datos de OOB y no había datos OOB previamente en cola, y también cuando se leen los datos mediante la marca de mensaje \_ OOB y algunos datos de OOB permanecen para ser leídos después de que se haya devuelto la operación de lectura. \_Los mensajes de lectura FD no se publican para los datos OOB.
-   El proveedor de servicios Winsock vuelve de [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) con el conjunto de sockets *exceptfds* adecuado si los datos OOB se ponen en cola en el socket.
-   El cliente puede llamar a [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) con el mensaje \_ OOB para leer el bloque de datos urgentes en cualquier momento. El bloque de datos OOB salta la cola.
-   El cliente puede llamar a [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) sin msg \_ OOB para leer el flujo de datos normal. El bloque de datos OOB no aparecerá en el flujo de datos con datos normales. Si los datos OOB permanecen después de cualquier llamada a **WSPRecv**, el proveedor de servicios notifica al cliente con FD \_ OOB o a través de *Exceptfds* cuando se usa [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)).
-   En el caso de los protocolos en los que los datos OOB tienen una posición dentro del flujo de datos normal, una sola operación [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) no abarcará esa posición. Una **WSPRecv** devolverá los datos normales antes de la marca y se requiere un segundo **WSPRecv** para empezar a leer los datos después de la marca.

Con SO \_ OOBINLINE habilitado:

-   Los \_ mensajes de FD OOB no se publican para los datos OOB; para el propósito de las funciones [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) y [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) , los datos de OOB se tratan como datos normales y se indican mediante el establecimiento del socket en *readfds* o mediante el envío de un mensaje de lectura FD, \_ respectivamente.
-   El cliente no puede llamar a [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) con la \_ marca de mensaje OOB establecida para leer el bloque de datos OOB; se devolverá el código de error WSAEINVAL.
-   El cliente puede llamar a [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) sin la \_ marca OOB de mensaje establecida. Cualquier dato OOB se entregará en su orden correcto dentro del flujo de datos normal. Los datos OOB nunca se combinarán con los datos normales; debe haber tres solicitudes de lectura para poder más allá de los datos OOB. El primero devuelve los datos normales antes del bloque de datos OOB, el segundo devuelve los datos OOB, el tercero devuelve los datos normales que siguen a los datos OOB. En otras palabras, los límites del bloque de datos OOB se conservan.

La rutina [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) es especialmente adecuada para controlar la presencia de datos OOB cuando \_ OOBINLINE está desactivada.

 

 
