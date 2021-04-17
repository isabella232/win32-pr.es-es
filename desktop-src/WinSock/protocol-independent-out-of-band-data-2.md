---
description: La abstracción de sockets de secuencia incluye la noción de datos fuera de banda (OOB).
ms.assetid: 1a517885-2688-421f-9389-2d329e5c3d56
title: Protocol-Independent datos fuera de banda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a929f4273d9cc9f268a296b711649406622ca9b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360293"
---
# <a name="protocol-independent-out-of-band-data"></a>Protocol-Independent datos fuera de banda

La abstracción de sockets de secuencia incluye la noción de datos fuera de banda (OOB). Muchos protocolos permiten marcar partes de los datos entrantes como especiales de algún modo, y estos bloques de datos especiales se pueden entregar al usuario fuera de la secuencia normal. Entre los ejemplos se incluyen datos expedidos en X. 25 y otros protocolos OSI, y datos urgentes en el uso de TCP en BSD UNIX. En la siguiente sección se describe el control de datos OOB de manera independiente del protocolo. Una descripción de los datos de OOB implementados mediante datos urgentes de TCP sigue la explicación independiente del protocolo. En cada debate, el uso de [**RECV**](/windows/desktop/api/winsock/nf-winsock-recv) también implica [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)y [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom), y las referencias a [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) también se aplican a [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect).

## <a name="protocol-independent-oob-data"></a>Datos OOB independientes del Protocolo

Los datos OOB son un canal de transmisión independiente lógicamente asociado a cada par de sockets de secuencias conectados. Los datos OOB se pueden entregar al usuario independientemente de los datos normales. La abstracción define que los servicios de datos OOB deben admitir la entrega confiable de al menos un bloque de datos OOB a la vez. Este bloque de datos puede contener al menos un byte de datos, y al menos un bloque de datos OOB puede estar pendiente de entrega al usuario en un momento dado. En el caso de los protocolos de comunicaciones que admiten la señalización en banda (como TCP, donde los datos urgentes se entregan en secuencia con los datos normales), el sistema normalmente extrae los datos OOB del flujo de datos normal y los almacena por separado (quedando un hueco en el flujo de datos normal). Esto permite a los usuarios elegir entre recibir los datos OOB en orden y recibirlos fuera de secuencia sin tener que almacenar en búfer todos los datos que intervienen. Es posible ver los datos fuera de banda (OOB).

Un usuario puede determinar si algún dato OOB está esperando para ser leído mediante la función [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) o [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) con el ioctl **SIOCATMARK** . En el caso de los protocolos en los que el concepto de la posición del bloque de datos OOB dentro del flujo de datos normal es significativo, como TCP, un proveedor de servicios de Windows Sockets mantiene un marcador conceptual que indica la posición del último byte de los datos OOB en el flujo de datos normal. Esto no es necesario para la implementación de las funciones **ioctlsocket** o **WSAIoctl** que admiten **SIOCATMARK**. La presencia o ausencia de datos OOB es obligatoria.

En el caso de los protocolos en los que el concepto de la posición del bloque de datos OOB dentro del flujo de datos normal es significativo, una aplicación podría procesar los datos fuera de banda en línea, como parte del flujo de datos normal. Esto se consigue estableciendo la opción de socket de modo que \_ OOBINLINE [](/windows/desktop/api/winsock/nf-winsock-setsockopt) con la función de la función de la. En el caso de otros protocolos en los que los bloques de datos OOB son verdaderamente independientes del flujo de datos normal, si se intenta establecer el valor de OOBINLINE, se \_ producirá un error. Una aplicación puede usar la función [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) o [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) con el ioctl **SIOCATMARK** para determinar si hay algún dato OOB de no lectura antes de la marca. Por ejemplo, puede usar esta información para volver a sincronizar con su elemento del mismo nivel asegurándose de que todos los datos hasta la marca del flujo de datos se descartan cuando sea necesario.

Con SO \_ OOBINLINE deshabilitado (la configuración predeterminada):

-   Windows Sockets notifica a una aplicación de un \_ evento FD OOB, si la aplicación se registra para recibir notificaciones con [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect), exactamente de la misma manera \_ que se usa FD Read para notificar la presencia de datos normales. Es decir, \_ se publica FD OOB cuando llegan datos OOB sin datos OOB previamente puestos en cola. El FD \_ OOB también se publica cuando se leen los datos mediante la \_ marca de mensaje OOB mientras algunos datos de OOB permanecen en la cola después de que se haya devuelto la operación de lectura. \_Los mensajes de lectura FD no se publican para los datos OOB.
-   Windows Sockets vuelve de [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) con el conjunto de sockets de *exceptfds* adecuado si los datos de OOB se ponen en cola en el socket.
-   La aplicación puede llamar a [**RECV**](/windows/desktop/api/winsock/nf-winsock-recv) con el mensaje \_ OOB para leer el bloque de datos urgentes en cualquier momento. El bloque de datos OOB salta la cola.
-   La aplicación puede llamar a [**RECV**](/windows/desktop/api/winsock/nf-winsock-recv) sin msg \_ OOB para leer el flujo de datos normal. El bloque de datos OOB no aparece en el flujo de datos con datos normales. Si los datos OOB permanecen después de cualquier llamada a **RECV**, Windows Sockets notifica a la aplicación con FD \_ OOB o con *exceptfds* cuando se usa [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select).
-   En el caso de los protocolos en los que los datos OOB tienen una posición dentro del flujo de datos normal, una única operación [**recibida**](/windows/desktop/api/winsock/nf-winsock-recv) no abarca esa posición. Un **RECV** devuelve los datos normales antes de la marca y se requiere una segunda instrucción **RECV** para empezar a leer los datos después de la marca.

Con SO \_ OOBINLINE habilitado:

-   \_Los mensajes de FD OOB no se publican para los datos OOB. Los datos OOB se tratan como normales para el propósito de las funciones [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) y [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) , y se indican mediante el establecimiento del socket en *readfds* o mediante el envío de un mensaje de \_ lectura FD respectivamente.
-   La aplicación no puede llamar a [**RECV**](/windows/desktop/api/winsock/nf-winsock-recv) con la marca de mensaje \_ OOB establecida para leer el bloque de datos OOB. Se devuelve el código de error WSAEINVAL.
-   La aplicación puede llamar a [**RECV**](/windows/desktop/api/winsock/nf-winsock-recv) sin la \_ marca OOB de MSG establecida. Los datos OOB se entregan en su orden correcto en el flujo de datos normal. Los datos OOB nunca se mezclan con datos normales. Debe haber tres solicitudes de lectura para poder más allá de los datos OOB. El primero devuelve los datos normales antes del bloque de datos OOB, el segundo devuelve los datos OOB, el tercero devuelve los datos normales que siguen a los datos OOB. En otras palabras, los límites del bloque de datos OOB se conservan.

La rutina [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) es especialmente adecuada para controlar la presencia de datos fuera de banda cuando \_ OOBINLINE está desactivada.

## <a name="oob-data-in-tcp"></a>Datos OOB en TCP

> [!IMPORTANT]
> La siguiente explicación de los datos fuera de banda (OOB), implementados mediante datos urgentes de TCP, sigue el modelo usado en la distribución de software Berkeley. Los usuarios e implementadores deben tener en cuenta lo siguiente:

 

-   Existen, en la actualidad, dos interpretaciones conflictivas de [RFC 793](https://www.ietf.org/rfc/rfc793.txt) (donde se introduce el concepto).
-   La implementación de datos OOB en la distribución de software Berkeley (BSD) no cumple los requisitos de host especificados en [RFC 1122](https://www.ietf.org/rfc/rfc1122.txt).

    En concreto, el puntero urgente de TCP en BSD apunta al byte después del byte de datos urgente y un puntero de TCP urgente compatible con RFC apunta al byte de datos urgente. Como resultado, si una aplicación envía datos urgentes desde una implementación compatible con BSD a una implementación compatible con RFC 1122, el receptor lee el byte de datos urgente equivocado (lee el byte que se encuentra después del byte correcto en el flujo de datos como el byte de datos urgente).

    Para minimizar los problemas de interoperabilidad, se recomienda a los escritores de aplicaciones que no usen datos OOB a menos que sea necesario para interoperar con un servicio existente. Se recomienda a los proveedores de Windows Sockets que documenten la semántica de OOB (BSD o RFC 1122) que implementa su producto.

La llegada de un segmento TCP con el conjunto de marcas URG (para urgente) indica la existencia de un solo byte de datos OOB en el flujo de datos TCP. El bloque de datos OOB tiene un tamaño de un byte. El puntero urgente es un desplazamiento positivo desde el número de secuencia actual en el encabezado TCP que indica la ubicación del bloque de datos OOB (de forma ambigua, como se indicó en el anterior). Por lo tanto, podría apuntar a datos que aún no se han recibido.

Si \_ es así, OOBINLINE está deshabilitado (valor predeterminado) cuando llega el segmento TCP que contiene el byte al que apunta el puntero urgente, el bloque de datos OOB (un byte) se quita del flujo de datos y se almacena en búfer. Si un segmento TCP subsiguiente llega con el conjunto de marcas urgentes (y un nuevo puntero urgente), el byte de OOB actualmente en cola se puede perder, ya que se reemplaza por el nuevo bloque de datos OOB (como ocurre en la distribución de software Berkeley). Sin embargo, nunca se reemplaza en el flujo de datos.

Con \_ la OOBINLINE habilitada, los datos urgentes permanecen en el flujo de datos. Como resultado, el bloque de datos OOB nunca se pierde cuando llega un nuevo segmento TCP que contiene datos urgentes. La marca de datos OOB existente se actualiza a la nueva posición.

> [!Note]  
> Cuando \_ se establece la opción de socket for OOBINLINE, el ioctl de SIOCATMARK siempre devuelve **true** y los datos OOB se devuelven al usuario como datos normales.

 

 

 



